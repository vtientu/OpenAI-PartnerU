# 01 — Where AI Systems Run

> **Course:** OpenAI Foundational Knowledge  
> **Course group:** Core AI Concepts & Solution Patterns  
> **Sub-course:** AI Infrastructure & Implementation  
> **Section:** Where AI systems run
>
> **Source note:** Đây là study guide tổng hợp theo tên section PartnerU. Chưa có transcript/slides nội bộ, vì vậy nội dung tập trung vào concepts bền vững của AI infrastructure và implementation.

---

# 1. Section objective

Sau section này, bạn cần:

- hiểu AI system có thể chạy ở những layer/location nào;
- phân biệt **model hosting**, **application hosting** và **enterprise systems**;
- hiểu cloud, on-prem, edge và hybrid deployment ở mức concept;
- hiểu hosted API khác self-hosting như thế nào;
- biết tại sao “model chạy ở đâu?” ảnh hưởng cost, latency, data và security.

---

# 2. Big picture

Một AI solution không “chạy ở một chỗ duy nhất”.

Nó thường có nhiều layer:

```text
User device
   ↓
Application frontend
   ↓
Backend / orchestration
   ↓
AI model endpoint
   ↓
Data / retrieval / tools
   ↓
Enterprise systems
```

Mỗi layer có thể ở:

- cloud;
- customer data center;
- managed SaaS;
- edge/device;
- hybrid environment.

---

# 3. Model hosting vs application hosting

Đây là distinction đầu tiên cần nhớ.

## Model hosting

Nơi model được phục vụ để nhận input và tạo output.

Ví dụ:

```text
App
→ model API
→ inference
→ response
```

## Application hosting

Nơi code của solution chạy:

- backend;
- orchestration;
- business logic;
- auth;
- logging;
- tool integrations.

Hai thứ có thể ở cùng cloud hoặc khác nơi.

---

# 4. Data layer

AI solution còn cần:

- databases;
- vector stores;
- document repositories;
- APIs;
- CRM;
- ERP;
- knowledge systems.

Do đó architecture thực tế thường là:

```text
Frontend
↓
Backend
├─ AI model
├─ Retrieval store
├─ Business DB
├─ Internal API
└─ Monitoring
```

Không nên nhìn model như toàn bộ infrastructure.

---

# 5. Cloud-hosted AI

Cloud-hosted model/API là pattern rất phổ biến.

Flow:

```text
Customer app
→ secure network/API request
→ cloud AI service
→ inference
→ response
```

Benefits:

- no need to manage model servers;
- easier scaling;
- managed updates;
- lower operational complexity.

Trade-offs:

- network dependency;
- service limits;
- external service integration;
- data/control requirements.

---

# 6. Managed AI service

A managed AI service means provider handles much of:

- model hosting;
- serving infrastructure;
- scaling;
- availability;
- model deployment lifecycle.

Customer/partner focuses on:

- application;
- integration;
- prompts/context;
- tools;
- evals;
- business workflow.

This is often the default mental model for OpenAI API-based solutions.

---

# 7. Self-hosted model

Self-hosting means organization operates model serving itself.

Potential motivations:

- specialized infrastructure requirements;
- offline/isolated environments;
- hardware ownership;
- specific control requirements;
- use of open-weight models.

But self-hosting also adds responsibility for:

- GPUs/accelerators;
- model serving;
- capacity;
- scaling;
- upgrades;
- monitoring;
- security;
- cost optimization.

Partner should not assume self-hosting is automatically cheaper or more secure.

---

# 8. On-premises

**On-premises / on-prem** means infrastructure runs in customer-controlled physical environment/data center.

Reasons may include:

- legacy integration;
- regulatory requirements;
- data residency constraints;
- isolated networks.

But on-prem introduces:

- hardware procurement;
- maintenance;
- slower scaling;
- capacity planning.

---

# 9. Edge / device AI

Some AI workloads can run near the user/device.

Examples:

- phone;
- laptop;
- factory device;
- vehicle;
- local gateway.

Advantages:

- lower network dependence;
- lower latency for some tasks;
- offline capability;
- local data processing.

Constraints:

- limited compute/memory;
- smaller models;
- update complexity;
- device fragmentation.

---

# 10. Hybrid architecture

Hybrid means different components run in different environments.

Example:

```text
Frontend
→ customer backend/on-prem
→ approved data retrieval
→ cloud model API
→ response
```

Or:

```text
Edge preprocessing
→ cloud reasoning
→ local action
```

Hybrid is common in enterprise systems.

---

# 11. Region and data residency

Infrastructure location can matter because of:

- regulatory requirements;
- customer policy;
- latency;
- data residency;
- disaster recovery.

Partner should verify product-specific regional availability and controls from current official documentation rather than assume.

---

# 12. Compute infrastructure

AI models require compute.

Common accelerator terms:

- GPU;
- TPU;
- specialized AI accelerators.

For partner-level understanding:

> Larger/more complex inference usually requires more compute.

More compute can influence:

- cost;
- latency;
- capacity;
- availability.

You don't need to design GPU clusters for every PartnerU conversation, but you should understand why compute matters.

---

# 13. CPU vs GPU intuition

## CPU

General-purpose processor.

Good for:

- business logic;
- databases;
- application servers;
- many deterministic tasks.

## GPU

Highly parallel processor.

Well suited to large matrix operations common in neural networks.

Simplified:

```text
Application logic → CPU/server
Model inference → often accelerator/GPU
```

Architecture can mix both.

---

# 14. AI serving layer

Model serving is infrastructure that exposes trained model for inference.

Responsibilities include:

- receive request;
- load model;
- allocate compute;
- execute inference;
- return output;
- manage batching/capacity.

Hosted AI providers abstract most of this away.

---

# 15. Client-server mental model

As a frontend developer:

```text
Browser
→ backend API
→ database
```

AI version:

```text
Browser
→ your backend
→ AI API/model endpoint
→ optional tools/data
→ response
```

Why backend is often useful:

- hide credentials;
- apply auth;
- add business rules;
- orchestrate tools;
- log/evaluate;
- control data flow.

---

# 16. Should frontend call model directly?

For enterprise apps, direct frontend-to-model calls can create issues around:

- credentials;
- permissions;
- business logic;
- audit;
- abuse control.

A backend/orchestration layer is often valuable.

Conceptual pattern:

```text
Frontend
→ application backend
→ AI service
```

---

# 17. Data proximity

Where data lives affects architecture.

If documents are in:

- SharePoint;
- internal DB;
- SaaS CRM;
- data warehouse;

the system must connect securely.

Data movement affects:

- latency;
- security;
- integration effort.

Sometimes moving model to data is better.

Sometimes moving selected data/context to model is better.

Depends on constraints.

---

# 18. Network is part of AI infrastructure

AI API requests travel over network.

Therefore network factors matter:

- round-trip latency;
- reliability;
- bandwidth;
- region;
- retries;
- timeouts.

For realtime voice or interactive agent, network design matters more than for batch jobs.

---

# 19. Storage types in AI applications

AI solution may use:

## Operational database
User/app state.

## Object storage
Documents/files.

## Vector index
Semantic retrieval.

## Logs/telemetry
Monitoring/evals.

## Cache
Reduce repeated cost/latency.

Each has different role.

---

# 20. Control plane vs data plane — intuition

You may hear these terms.

## Control plane
Manages configuration/resources.

## Data plane
Handles actual workload/request data.

Not always necessary in customer conversation, but useful infrastructure vocabulary.

---

# 21. Availability and redundancy

Production systems need:

- uptime;
- retries;
- failover;
- rate-limit handling;
- queueing.

Model endpoint availability alone is not enough.

Your entire chain must work:

```text
App
+ auth
+ model
+ retrieval
+ tools
+ DB
```

System reliability is end-to-end.

---

# 22. Example — Internal knowledge assistant

```text
Employee browser
↓
Company web app
↓
Backend
├─ identity
├─ retrieval
│  └─ internal knowledge source
└─ hosted model API
↓
Answer + citations
```

Infrastructure decisions:

- where retrieval index runs;
- network to source systems;
- user permissions;
- model region;
- logging.

---

# 23. Example — Factory assistant

Possible hybrid:

```text
Factory device
↓
Local application
↓
Company network
↓
Cloud AI model
↓
Maintenance knowledge
```

If network is unreliable:

- caching;
- local fallback;
- edge capabilities

may matter.

---

# 24. Example — Customer-facing AI product

```text
Public web/mobile app
↓
API gateway
↓
backend/orchestrator
↓
AI service
↓
tools/data
```

Need:

- scaling;
- abuse protection;
- rate limiting;
- monitoring;
- multi-tenant isolation.

---

# 25. Hosted vs self-hosted comparison

| Area | Hosted/managed | Self-hosted |
|---|---|---|
| Model serving | Provider | Customer |
| Hardware | Provider | Customer |
| Scaling | Mostly managed | Customer manages |
| Upgrades | Provider-managed | Customer plans |
| Infra complexity | Lower | Higher |
| Custom infra control | Lower | Higher |
| Ops burden | Lower | Higher |

Neither is universally better.

---

# 26. Partner discovery questions

1. Where are users?
2. Where does business data live?
3. What systems need integration?
4. Is cloud allowed?
5. Any residency/region requirements?
6. Realtime or batch?
7. Expected scale?
8. Availability/SLA requirement?
9. Offline requirement?
10. Who operates the infrastructure?

---

# 27. Common mistakes

1. Model hosting = whole AI architecture.
2. Cloud means “no infrastructure work”.
3. Self-hosting is automatically cheaper.
4. On-prem is automatically safer.
5. Ignore network latency.
6. Ignore where enterprise data actually lives.
7. Let frontend own credentials directly.
8. Treat uptime as model-provider-only responsibility.

---

# 28. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Model hosting | Nơi model được phục vụ |
| Application hosting | Nơi application code chạy |
| Cloud | Hạ tầng điện toán đám mây |
| On-premises | Hạ tầng tại data center của tổ chức |
| Edge | Xử lý gần thiết bị/người dùng |
| Hybrid | Kết hợp nhiều môi trường |
| GPU | Bộ xử lý song song phù hợp AI |
| Model serving | Hệ thống phục vụ inference |
| Data residency | Yêu cầu dữ liệu nằm tại region |
| Availability | Khả dụng |
| Redundancy | Dự phòng |
| Failover | Chuyển sang hệ thống dự phòng |
| Cache | Bộ nhớ đệm |

---

# 29. Section recap

Remember:

```text
User
↓
Application
↓
Backend/orchestration
↓
Model service
↓
Data/tools
↓
Enterprise systems
```

And deployment options:

```text
Cloud
On-prem
Edge
Hybrid
```

Key principle:

> **Where each component runs affects latency, data flow, cost, security, scale and operational responsibility.**

---

# 30. Self-check

1. Model hosting khác application hosting thế nào?
2. Cloud-hosted và self-hosted trade-off gì?
3. Edge phù hợp khi nào?
4. Tại sao network là một phần của AI infrastructure?
5. Hãy vẽ architecture cho internal knowledge assistant.
