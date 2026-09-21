# 04 — Agentic Workflows Across Common Technology Paths

> **Course:** OpenAI Foundational Knowledge  
> **Sub-course:** Agents & Agentic Workflows  
> **Section:** Agentic workflows across common technology paths
>
> **Source note:** “Technology paths” ở đây được giải thích như các cách phổ biến để đưa agentic capability vào solution: SaaS/product, API/custom app, enterprise platform/integration, developer workflow, and hybrid automation. Đây là study synthesis vì chưa có transcript PartnerU xác nhận exact taxonomy.

---

# 1. Section objective

Sau section này, bạn cần:

- hiểu agentic workflows có thể xuất hiện qua nhiều technology paths;
- phân biệt product-configured agent, custom API agent, embedded agent và workflow automation;
- hiểu trade-off build vs buy;
- biết architecture/ownership thay đổi theo path;
- tránh nghĩ agent chỉ tồn tại trong một “agent platform”.

---

# 2. Big picture

Same business goal can be implemented through different technology paths.

```text
Business workflow
↓
Choose technology path
├─ Configure existing product
├─ Build custom application/API
├─ Embed into enterprise platform
├─ Developer/coding workflow
└─ Hybrid orchestration
```

The “best” path depends on:

- control;
- speed;
- integration;
- customization;
- skills;
- operations.

---

# 3. Path 1 — Agent capability inside an existing SaaS/product

Examples conceptually:

- support platform assistant;
- CRM assistant;
- productivity suite agent;
- ITSM agent.

Benefits:

- fast setup;
- existing user identity;
- workflow context already available;
- lower implementation burden.

Constraints:

- limited customization;
- product-defined tools;
- vendor roadmap;
- integration boundaries.

---

# 4. When SaaS-native path fits

Good when:

- workflow already lives in that SaaS;
- needed actions are already supported;
- customer wants speed;
- standard workflow sufficient.

Example:

```text
Sales work in CRM
→ configure CRM-native agent
```

No need to rebuild entire CRM integration externally.

---

# 5. Path 2 — Custom application using model APIs

Architecture:

```text
Custom UI
→ backend/orchestrator
→ model
→ custom tools
→ enterprise systems
```

Benefits:

- maximum workflow control;
- custom UX;
- custom tools;
- tailored guardrails/evals.

Costs:

- engineering;
- operations;
- security;
- monitoring.

---

# 6. When custom app fits

Use when:

- workflow spans multiple systems;
- SaaS-native capability insufficient;
- UX differentiates product;
- need custom business rules;
- need deep proprietary integration.

---

# 7. Path 3 — Embedded agent inside existing internal application

Instead of standalone chatbot:

```text
Existing app
+ AI action panel
```

Benefits:

- user stays in workflow;
- current context is available;
- easier adoption;
- permissions can inherit app role.

Example:

```text
Claims system
→ agent analyzes case
→ prepares next action inline
```

---

# 8. Embedded copilot vs autonomous agent

Embedded copilot:

```text
AI suggests
→ human accepts
```

Embedded agent:

```text
AI executes scoped tasks
→ human handles exceptions
```

Same UX surface can support different autonomy.

---

# 9. Path 4 — Backend workflow agent

No chat UI required.

Example:

```text
New invoice event
↓
agent
↓
extract
↓
validate
↓
lookup PO
↓
route/record
```

Trigger can be:

- event;
- queue;
- schedule;
- API request.

This is important:

> Agentic systems can be invisible background workers.

---

# 10. Path 5 — Developer/coding agent

Runs in:

- IDE;
- terminal;
- repository environment;
- CI-like workflow.

Agent can:

- inspect files;
- edit;
- run tests;
- debug;
- propose changes.

Technology path is tightly coupled to developer tools.

---

# 11. Path 6 — Data/analytics agent

Possible flow:

```text
Business question
↓
semantic layer
↓
SQL/code tool
↓
warehouse
↓
analysis
↓
explanation
```

Requires:

- governed data;
- safe query permissions;
- metric definitions;
- validation.

---

# 12. Path 7 — Browser/computer-use style workflow

Some agents may interact with graphical interfaces when API is unavailable.

Conceptually:

```text
observe UI
→ decide action
→ click/type
→ observe result
```

Useful for legacy systems.

Trade-offs:

- fragility;
- UI changes;
- slower execution;
- stronger monitoring.

API integration is often more reliable when available.

---

# 13. Path 8 — RPA + agent hybrid

RPA handles deterministic UI steps.

Agent handles interpretation.

Example:

```text
Agent interprets email
↓
RPA performs fixed legacy-system steps
```

This can modernize workflows without replacing all legacy infrastructure.

---

# 14. Path 9 — Multi-agent architecture

Multiple specialized agents may coordinate.

Example:

```text
Coordinator
├─ research agent
├─ coding agent
└─ QA agent
```

Potential benefits:

- separation of roles;
- specialized tools/context.

Costs:

- more complexity;
- more latency;
- harder debugging/evals.

Do not use multi-agent just because it sounds advanced.

---

# 15. Single agent vs multi-agent

Single agent:

- simpler;
- easier tracing;
- fewer handoffs.

Multi-agent:

- useful if subproblems have distinct roles/tools/context.

Default:

> Start simple.

Split only when evidence supports it.

---

# 16. Path 10 — Human-agent workflow

Technology path includes humans intentionally.

```text
Agent
→ human approval
→ tool
```

or:

```text
Agent handles standard cases
→ human exception queue
```

Human workflow is part of architecture.

---

# 17. Build vs buy

A classic decision.

## Buy/configure

Pros:

- faster;
- lower engineering;
- integrated workflow.

Cons:

- less control;
- vendor constraints.

## Build

Pros:

- tailored workflow;
- deeper integration;
- differentiation.

Cons:

- more engineering/ops.

---

# 18. Technology path selection framework — PATH

## P — Process location
Where does work already happen?

## A — Access/integration
Which systems/tools needed?

## T — Tailoring
How customized must behavior/UX be?

## H — Hosting/operations
Who will build/run/support it?

---

# 19. Add CONTROL

For agent path:

## C — Compliance/security
Any hard constraints?

## O — Ownership
Who owns workflow?

## N — Network/data
Where does data live?

## T — Tooling
APIs available?

## R — Reliability
What uptime/fallback?

## O — Observability
Can we trace/evaluate?

## L — Latency/load
Performance needs?

---

# 20. Example — Sales workflow

Options:

### SaaS-native
CRM agent.

### Custom
Company sales portal with agent.

### Embedded
Agent side panel in CRM.

### Hybrid
Agent interprets request + RPA updates legacy system.

Same use case, different technology path.

---

# 21. Example — Support

Option A:

```text
Support platform native agent
```

Option B:

```text
Custom backend agent
+ ticketing API
+ CRM
+ policy retrieval
```

Selection depends on:

- integration;
- control;
- time-to-value.

---

# 22. Example — Finance operations

If ERP exposes APIs:

```text
custom/tool-using agent
```

If legacy UI only:

```text
agent + RPA/computer interaction
```

But evaluate reliability carefully.

---

# 23. Example — Coding

Technology path may be:

- IDE assistant;
- repo agent;
- CI agent;
- internal developer portal.

Different path changes:

- permissions;
- execution environment;
- latency;
- review.

---

# 24. Technology path affects responsibility

SaaS-native:

Vendor owns more platform behavior.

Custom:

Customer/partner owns more:

- orchestration;
- tool auth;
- state;
- logging;
- evals.

More control usually means more responsibility.

---

# 25. Technology path affects time-to-value

Rough mental model:

```text
Configure existing capability
→ faster

Custom deep integration
→ slower but potentially more tailored
```

Not always, but useful default.

---

# 26. Technology path affects lock-in

Vendor-specific features may increase:

- implementation speed;
- workflow integration.

But can also increase:

- switching cost;
- architectural coupling.

This should be considered if strategically important.

---

# 27. Partner role

Partner should not force favorite technology.

Instead:

```text
Workflow
→ requirements
→ technology path options
→ trade-offs
→ recommendation
```

Need neutral solution judgment.

---

# 28. Common mistakes

1. Agent = standalone chat app.
2. Build custom when SaaS-native solves it.
3. Buy/configure when workflow requires deep customization.
4. Use multi-agent by default.
5. Ignore legacy systems.
6. Ignore operational ownership.
7. Ignore human workflow.
8. Treat computer-use path as equally robust as API integration without testing.

---

# 29. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Technology path | Cách/đường triển khai công nghệ |
| SaaS-native | Capability có sẵn trong SaaS |
| Custom application | Ứng dụng tự xây |
| Embedded agent | Agent nhúng trong app |
| Backend agent | Agent chạy nền/backend |
| RPA | Robotic Process Automation |
| Multi-agent | Nhiều agent phối hợp |
| Build vs buy | Tự xây hay mua/configure |
| Lock-in | Phụ thuộc vendor/platform |
| Time-to-value | Thời gian để tạo value |

---

# 30. Section recap

Common technology paths:

```text
SaaS-native
Custom API app
Embedded agent
Backend workflow agent
Developer/coding agent
Analytics agent
UI/computer-use
RPA hybrid
Multi-agent
Human-agent workflow
```

Use PATH:

```text
Process
Access
Tailoring
Hosting
```

Core rule:

> **Choose the technology path from the workflow and constraints, not from whichever agent platform is newest.**

---

# 31. Self-check

1. SaaS-native và custom agent trade-off gì?
2. Embedded agent khác standalone chat thế nào?
3. Khi nào RPA + agent hybrid hợp lý?
4. Multi-agent nên dùng khi nào?
5. PATH framework gồm gì?
6. Technology path ảnh hưởng responsibility ra sao?
