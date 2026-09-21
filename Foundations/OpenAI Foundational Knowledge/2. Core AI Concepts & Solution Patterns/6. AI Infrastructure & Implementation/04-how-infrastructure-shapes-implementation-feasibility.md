# 04 — How Infrastructure Shapes Implementation Feasibility

> **Course:** OpenAI Foundational Knowledge  
> **Sub-course:** AI Infrastructure & Implementation  
> **Section:** How infrastructure shapes implementation feasibility

---

# 1. Section objective

Sau section này, bạn cần:

- hiểu infrastructure không chỉ là “DevOps detail” mà là phần của feasibility;
- biết các constraint chính: compute, network, data, security, scale, integration, operations;
- biết phân biệt technically possible với practically deployable;
- biết đưa infrastructure readiness vào qualification;
- tránh recommend solution chỉ dựa trên model capability.

---

# 2. Big picture

Một use case có thể:

> **AI-capable**

nhưng chưa:

> **implementation-feasible**

Mental model:

```text
Model can do task
        ≠
Customer can deploy solution
```

Feasibility depends on:

```text
Capability
+ Data
+ Infrastructure
+ Integration
+ Security
+ Operations
+ Cost
+ People
```

---

# 3. Technical possibility vs operational feasibility

Example:

A model can analyze video.

But customer may lack:

- bandwidth;
- storage;
- processing pipeline;
- permissions;
- budget;
- monitoring.

Therefore:

```text
technical capability
→ necessary
but not sufficient
```

---

# 4. Feasibility dimension 1 — Compute

Questions:

- hosted API or self-hosted?
- large-scale batch?
- realtime workload?
- GPU needed locally?
- enough quota/capacity?

Compute constraints affect:

- model choice;
- scale;
- cost;
- architecture.

---

# 5. Feasibility dimension 2 — Network

Questions:

- reliable internet?
- cross-region calls?
- factory/offline environment?
- corporate proxy?
- latency requirement?

A cloud-dependent realtime solution may fail in poor-connectivity environment.

Possible alternatives:

- edge/local processing;
- asynchronous workflow;
- local cache.

---

# 6. Feasibility dimension 3 — Data availability

AI can only use data if accessible.

Need:

- source system;
- API;
- export;
- document repository;
- permissions.

Common blocker:

> “Data exists” but cannot be reliably accessed.

---

# 7. Data quality

Even accessible data may be:

- incomplete;
- stale;
- duplicated;
- inconsistent;
- unstructured;
- poorly owned.

RAG on bad data still gives poor system behavior.

Infrastructure readiness includes data readiness.

---

# 8. Feasibility dimension 4 — Integration

Ask:

- Does system have API?
- Can partner authenticate?
- Is there sandbox?
- Is write access allowed?
- Are legacy systems involved?

Many enterprise AI projects are integration projects.

---

# 9. Legacy systems

Legacy systems may lack:

- modern APIs;
- reliable schemas;
- realtime access;
- clear ownership.

Possible patterns:

- adapter layer;
- middleware;
- batch export;
- RPA;
- human-in-the-loop.

Infrastructure determines implementation pattern.

---

# 10. Feasibility dimension 5 — Security

Need consider:

- identity;
- authentication;
- authorization;
- secrets;
- network boundaries;
- logging;
- data classification.

A POC can work technically but fail security review.

Security should not start at the end.

---

# 11. Identity and permissions

If AI acts for a user:

```text
Who is the AI acting as?
What can it access?
What can it change?
```

Permission design is especially important for agents.

Principle:

> **Least privilege.**

Give only necessary access.

---

# 12. Feasibility dimension 6 — Data/privacy requirements

Potential constraints:

- personal data;
- confidential data;
- regulated data;
- retention;
- regional requirements.

Partner should verify current product controls/documentation rather than invent guarantees.

---

# 13. Feasibility dimension 7 — Latency

Use case may require:

- sub-second-ish interaction;
- several seconds;
- minutes;
- hours.

Latency requirement can eliminate some architectures.

Example:

```text
Realtime voice
```

has stricter architecture than:

```text
overnight document analysis
```

---

# 14. Feasibility dimension 8 — Scale

POC:

```text
10 users
```

Production:

```text
50,000 users
```

Questions:

- concurrency;
- peak volume;
- rate limits;
- queueing;
- cost;
- storage;
- monitoring.

A POC architecture may not scale unchanged.

---

# 15. Feasibility dimension 9 — Reliability

Production needs:

- retries;
- failover;
- timeout;
- idempotency;
- degradation strategy;
- incident response.

If model/tool unavailable:

> What does workflow do?

Need fallback.

---

# 16. Feasibility dimension 10 — Observability

Can you answer:

- how many requests fail?
- latency by step?
- cost per workflow?
- which tools are called?
- why users escalate?
- quality regression?

If not, operation is difficult.

---

# 17. Feasibility dimension 11 — Cost

Cost includes more than model tokens.

```text
Model usage
+ infrastructure
+ storage
+ retrieval
+ data transfer
+ integration
+ monitoring
+ human review
+ operations
```

Business case must consider total cost.

---

# 18. Cost per task

A useful metric:

```text
total solution cost
÷
completed business tasks
```

Example:

- cost per resolved support case;
- cost per processed document.

More meaningful than token cost alone.

---

# 19. Feasibility dimension 12 — Operations

Who will:

- monitor system?
- update prompts?
- maintain retrieval?
- handle incidents?
- rotate secrets?
- review eval regressions?
- approve model upgrades?

No owner = operational risk.

---

# 20. Feasibility dimension 13 — Skills

Customer may need:

- backend engineering;
- data engineering;
- security;
- AI evaluation;
- product/UX;
- domain experts.

Infrastructure can be available but team capability may not.

---

# 21. Feasibility dimension 14 — Procurement / governance

Enterprise deployment may require:

- vendor review;
- security review;
- architecture review;
- legal/compliance;
- budget approval.

These affect timeline.

Implementation feasibility includes organizational process.

---

# 22. A readiness stack

```text
Business readiness
↓
Data readiness
↓
Integration readiness
↓
Security readiness
↓
Infrastructure readiness
↓
Operational readiness
↓
Adoption readiness
```

Weakness in one layer can block production.

---

# 23. Hosted service can reduce infrastructure burden

Managed AI service can remove need to:

- buy GPUs;
- serve model;
- maintain training infrastructure.

But customer still owns:

- app;
- data;
- tools;
- integration;
- security architecture;
- operations.

Hosted model ≠ no infrastructure.

---

# 24. Feasibility triangle

A useful mental model:

```text
          QUALITY
           /\
          /  \
         /    \
      COST ---- LATENCY
```

Often cannot maximize all three.

Add constraints:

- scale;
- security;
- availability.

Solution design is trade-off management.

---

# 25. Example — Realtime contact center assistant

Requirements:

- low latency;
- audio;
- CRM access;
- high concurrency.

Infrastructure needs:

- realtime model;
- streaming;
- fast network;
- CRM integration;
- scalable backend;
- observability.

Feasibility depends on all, not just voice model capability.

---

# 26. Example — Contract analysis

Requirements:

- large docs;
- high accuracy;
- batch acceptable;
- sensitive data.

Infrastructure priorities:

- document pipeline;
- storage;
- access control;
- retrieval/context;
- async processing;
- audit logs.

Latency less critical than quality/security.

---

# 27. Example — Factory troubleshooting

Constraints:

- unreliable connectivity;
- local equipment data;
- safety-critical environment.

Possible architecture:

```text
Local/edge component
+ cloud AI when available
+ cached/manual fallback
```

Infrastructure context changes solution recommendation.

---

# 28. Example — Customer support agent

POC:

```text
AI drafts answer
```

Production:

```text
identity
+ account tools
+ policy retrieval
+ action controls
+ audit
+ monitoring
+ escalation
```

Infrastructure complexity often grows with autonomy.

---

# 29. Autonomy amplifies infrastructure requirements

Compare:

### Assistant
Output is draft.

### Agent
Output triggers action.

Agent needs stronger:

- permissions;
- reliability;
- audit;
- retry;
- idempotency;
- rollback;
- monitoring.

More autonomy → higher implementation burden.

---

# 30. Feasibility framework — SCALE

## S — Systems
What existing systems must integrate?

## C — Connectivity/compute
Can workload run reliably?

## A — Access/data
Is required data accessible and permitted?

## L — Latency/load
Can performance requirements be met?

## E — Economics/operations
Is cost and operational ownership sustainable?

Use alongside business/use-case evaluation.

---

# 31. Extended readiness questions

### Systems
- APIs?
- legacy?
- write access?

### Data
- source of truth?
- freshness?
- permission?

### Infra
- cloud allowed?
- region?
- network?

### Performance
- latency?
- volume?

### Ops
- who runs it?
- monitoring?

### Cost
- acceptable per task?

---

# 32. Feasibility is evidence-based

Don't say:

> “This will scale.”

without evidence.

Need:

- load testing;
- pilot;
- latency measurement;
- cost model;
- rate-limit checks;
- integration proof.

Capability statement is not production evidence.

---

# 33. POC vs production

POC proves:

> “Can this idea work at all?”

Production requires:

```text
security
scale
monitoring
reliability
cost
ownership
support
```

Do not confuse demo success with readiness.

---

# 34. Architecture should evolve with evidence

Start simple:

```text
Prototype
→ validate value
→ discover constraints
→ harden architecture
→ pilot
→ scale
```

Avoid overbuilding before proving value.

But don't ignore known hard blockers.

---

# 35. Partner role

Partner should connect:

```text
Business ambition
↓
AI capability
↓
Infrastructure reality
↓
Implementation plan
```

This is why consultative discovery needs both business and technical stakeholders.

---

# 36. Common mistakes

1. If model can do it, implementation is feasible.
2. POC = production.
3. Infrastructure = only cloud/GPU.
4. Ignore legacy integration.
5. Ignore data permissions.
6. Ignore operations/ownership.
7. Estimate cost only from model price.
8. Scale after launch without testing.
9. Add high autonomy before foundational controls.

---

# 37. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Feasibility | Tính khả thi |
| Infrastructure readiness | Mức sẵn sàng hạ tầng |
| Integration readiness | Sẵn sàng tích hợp |
| Data readiness | Sẵn sàng dữ liệu |
| Operational readiness | Sẵn sàng vận hành |
| Legacy system | Hệ thống cũ |
| SLA | Cam kết mức dịch vụ |
| Failover | Chuyển sang dự phòng |
| Idempotency | Lặp action an toàn |
| Observability | Khả năng quan sát |
| Load testing | Kiểm thử tải |
| Rate limit | Giới hạn request |
| Total cost of ownership | Tổng chi phí sở hữu/vận hành |

---

# 38. Section recap

Implementation feasibility depends on:

```text
Compute
Network
Data
Integration
Security
Latency
Scale
Reliability
Cost
Operations
Skills
Governance
```

Core principle:

> **Model capability tells you what may be possible. Infrastructure determines what can actually be deployed reliably, securely and economically.**

---

# 39. Self-check

1. Technical possibility và implementation feasibility khác nhau thế nào?
2. Tại sao data readiness là infrastructure concern?
3. Agent autonomy ảnh hưởng infrastructure requirements ra sao?
4. POC và production khác nhau ở những layer nào?
5. Hãy dùng SCALE framework cho contact-center assistant.
6. Vì sao cost per task hữu ích hơn chỉ nhìn token cost?
