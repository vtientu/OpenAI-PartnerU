# 02 — Understanding Where Technologies Fit

> **Course:** OpenAI Foundational Knowledge  
> **Sub-course:** OpenAI Product Portfolio Overview  
> **Section:** Understanding Where Technologies Fit

---

# 1. Section objective

Sau section này, bạn cần:

- biết technology nào fit với workflow nào;
- phân biệt direct-use, embedded, retrieval, tool-use, agentic và enterprise-operation paths;
- hiểu “fit” dựa trên requirement, không dựa trên product popularity;
- xây một mental map để route opportunity nhanh.

---

# 2. Big picture

Technology fit nên được xác định theo:

```text
User
+ workflow
+ data
+ action
+ autonomy
+ integration
+ governance
```

Không phải:

```text
Newest product
→ use everywhere
```

---

# 3. Fit dimension 1 — Who is the user?

## Knowledge worker

Needs:

- write;
- research;
- analyze;
- create.

Likely direct-use AI product.

## Developer

Needs:

- codebase work;
- implementation;
- testing.

Coding product/capability.

## Application end user

Needs AI inside customer's product.

API/custom application.

## Operations team

Needs repeatable multi-step workflow.

Agent/workflow path.

---

# 4. Fit dimension 2 — Is the user working in OpenAI's product or the customer's product?

### OpenAI product surface

```text
User → ChatGPT / Work / Codex
```

Faster deployment.

### Customer-owned surface

```text
User → Customer app → API
```

More UX/control/customization.

This is one of the most important routing decisions.

---

# 5. ChatGPT fit

Strong when:

- broad knowledge work;
- employee productivity;
- individual/team workflows;
- users benefit from flexible interaction;
- no need for fully custom end-user product.

Typical tasks:

- research;
- drafting;
- analysis;
- file work;
- problem solving.

---

# 6. ChatGPT Work fit

Strong when user wants AI to carry larger work units:

```text
research
→ analyze files
→ produce artifact
→ use tools
```

Useful for knowledge workers with substantial deliverables rather than only quick chat.

---

# 7. Codex fit

Strong when core workflow is software engineering.

Needs:

- repo understanding;
- coding;
- tests;
- debugging;
- review.

Do not route coding workflow to generic technology purely because it supports text.

Use specialized coding experience where fit is stronger.

---

# 8. API Platform fit

Strong when customer needs:

- AI embedded in own product;
- custom workflow;
- custom backend;
- external customer experience;
- proprietary tool integration;
- programmable control.

API path means more implementation ownership.

---

# 9. Model selection fit

After selecting API/application path, choose model based on:

- task difficulty;
- modality;
- latency;
- cost;
- context;
- tool requirements.

Model selection is **inside** the technology path.

It should not replace solution identification.

---

# 10. Retrieval / file search fit

Use when AI needs:

- private documents;
- current knowledge;
- source-based answers.

Conceptual path:

```text
Question
→ retrieve
→ model
→ grounded answer
```

Do not use retrieval if no external knowledge is needed.

---

# 11. Web/search fit

Use when task depends on current public information.

Examples:

- latest research;
- current market info;
- updated external facts.

Need:

- source quality;
- citations;
- freshness.

---

# 12. Tool / connector fit

Use when model needs:

- live business state;
- business-system actions.

Examples:

```text
get CRM account
create ticket
query warehouse
update workflow
```

Tools move system from:

> “knows”

to:

> “knows and can act.”

---

# 13. Plugin fit

Plugins can be strong when customer needs packaged connection between AI and existing business tools.

Benefits:

- faster connection;
- standardized integration;
- governed workflow context.

Custom integration may still be needed for non-standard behavior.

---

# 14. MCP fit

MCP fits when organization wants a standardized method to expose tools/context to compatible AI systems.

Good for:

- internal tool connection;
- reusable integrations;
- separating AI client from tool server.

MCP does not decide business logic or security policy automatically.

---

# 15. Responses-style API fit

A combined model/tool response API fits when developer wants:

- model reasoning;
- built-in tools;
- structured multi-step application behavior

without assembling every low-level mechanism separately.

Exact API features should be verified from current docs.

---

# 16. Agents API/SDK fit

Use when workflow needs:

- multiple steps;
- tool coordination;
- state/context;
- longer-running execution;
- agent orchestration.

Examples:

```text
Research a market
→ gather sources
→ analyze
→ generate report
```

or:

```text
Inspect repo
→ modify code
→ run tests
→ iterate
```

---

# 17. Workspace agent fit

Good when:

- business users need repeatable shared workflow;
- organization wants lower-code/no-code configuration;
- workflow should live within ChatGPT workspace;
- shared team knowledge/tools matter.

This can be faster than custom building.

---

# 18. Managed enterprise agent product fit

A managed enterprise product may fit when customer needs:

- production agent experience;
- enterprise operational support;
- security/governance;
- repeatable voice/chat or other managed workflows.

Exact current offerings should be verified.

---

# 19. Enterprise agent platform fit

A platform such as current OpenAI Frontier positioning fits when organization needs broader agent operations:

- enterprise context;
- system-of-record integration;
- execution;
- eval/optimization;
- permissions;
- audit/governance.

This is beyond a single API call.

---

# 20. Fit dimension 3 — Is knowledge static/general or private/current?

```text
General model knowledge
→ model

Private/current documents
→ retrieval

Live structured state
→ API/tool

Persistent user/workflow state
→ app memory/state
```

This routing is often more important than model brand.

---

# 21. Fit dimension 4 — Is action required?

### No action

- answer;
- draft;
- analyze.

Simple product/API path may be enough.

### One controlled action

Tool-enabled assistant.

### Multiple adaptive actions

Agent candidate.

Autonomy raises controls.

---

# 22. Fit dimension 5 — How standardized is workflow?

## Standard workflow

Existing product/native agent may fit.

## Highly proprietary workflow

Custom API/agent may fit.

Build-vs-configure is driven by differentiation.

---

# 23. Fit dimension 6 — How much control is required?

More custom build allows:

- custom UX;
- custom orchestration;
- custom tools;
- tailored controls.

But adds:

- engineering;
- security;
- operations;
- eval burden.

Fit includes organizational readiness.

---

# 24. Decision table

| Need | Likely path |
|---|---|
| General employee AI | ChatGPT |
| Substantial knowledge work | ChatGPT Work |
| Developer coding work | Codex |
| AI inside own product | API |
| Private docs | Retrieval/file search |
| Live system state/actions | Tools/plugins/MCP |
| Multi-step custom workflow | Agents API/SDK |
| Shared configurable team workflow | Workspace agent |
| Enterprise-wide agent operations | Enterprise agent platform |

This is a study map, not a rigid catalog.

---

# 25. Example — HR knowledge

Need:

- employee users;
- policy documents;
- citations;
- no write actions.

Possible paths:

```text
ChatGPT + connected knowledge
or
custom RAG app
```

Decision depends on UX/integration/governance requirements.

---

# 26. Example — SaaS support feature

Need:

- end customers;
- custom UI;
- account data;
- actions.

Likely:

```text
Customer app
→ API
→ retrieval
→ account tools
→ agentic workflow
```

---

# 27. Example — Engineering team

Need:

- codebase work.

Likely start:

```text
Codex
```

If company needs custom internal coding workflow:

```text
custom agent/tooling
```

---

# 28. Technology fit framework — FIT

## F — Flow
Where does user work today?

## I — Integration
What data/tools/systems?

## T — Tailoring
How custom must UX/workflow be?

Add:

```text
G — Governance
A — Autonomy
M — Measurement
```

So a fuller framework:

```text
FIT + GAM
```

---

# 29. Partner lens

When customer names a product:

> “We need an agent.”

Translate to requirement.

Ask:

- what workflow?
- who uses it?
- where do they work?
- data?
- actions?
- custom UX?
- autonomy?
- governance?

Then validate product fit.

---

# 30. Common mistakes

1. Route by buzzword.
2. Choose API when product configuration would solve faster.
3. Choose SaaS product when custom UX is core requirement.
4. Use RAG for live structured data.
5. Use agent for one-step task.
6. Choose enterprise platform for small isolated experiment.
7. Ignore operating responsibility.

---

# 31. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Technology fit | Mức phù hợp của công nghệ |
| Product-native | Tính năng có sẵn trong product |
| Embedded AI | AI nhúng vào app |
| Custom workflow | Workflow riêng |
| Retrieval | Lấy knowledge liên quan |
| Connector | Kết nối hệ thống |
| Tool calling | AI gọi API/công cụ |
| Build vs configure | Xây mới hay cấu hình |
| Governance | Quản trị |
| Operating responsibility | Trách nhiệm vận hành |

---

# 32. Section recap

Route by requirement:

```text
Employee use
→ ChatGPT/Work

Coding
→ Codex

Embedded/custom app
→ API

Private knowledge
→ retrieval

Live data/action
→ tools/plugins/MCP

Multi-step adaptive work
→ agents

Enterprise-wide agent operations
→ enterprise platform
```

Core rule:

> **Technology fit follows workflow fit.**

---

# 33. Self-check

1. ChatGPT và API fit khác nhau ở đâu?
2. Khi nào retrieval phù hợp?
3. Khi nào tool/API tốt hơn RAG?
4. Workspace agent và custom agent khác nhau ở tailoring thế nào?
5. FIT framework gồm gì?
6. Hãy route một customer support use case qua portfolio.
