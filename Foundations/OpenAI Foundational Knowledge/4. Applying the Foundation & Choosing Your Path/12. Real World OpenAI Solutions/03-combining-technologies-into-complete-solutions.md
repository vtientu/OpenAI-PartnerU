# 03 — Combining Technologies Into Complete Solutions

> **Course:** OpenAI Foundational Knowledge  
> **Course:** Real World OpenAI Solutions  
> **Section:** Combining technologies into complete solutions
>
> **Freshness note:** OpenAI product surfaces and exact model/tool names evolve. This section emphasizes durable architecture composition. Exact current capabilities should be verified from official OpenAI docs when implementation depends on them.

---

# 1. Section objective

Sau section này, bạn cần:

- hiểu một complete solution gồm nhiều layers;
- biết role của ChatGPT, Codex, API, model, retrieval, plugins/MCP, tools, agents và evals;
- biết khi nào kết hợp technology;
- tránh “technology stacking” không có requirement;
- thiết kế solution architecture từ workflow.

---

# 2. Big picture

A complete AI solution is usually not:

```text
User
→ model
```

It may be:

```text
User / event
↓
Product surface / custom UX
↓
Identity + application logic
↓
AI model / agent
├─ retrieval / knowledge
├─ web/current sources
├─ tools / business systems
├─ state
└─ deterministic rules
↓
Output / action
↓
Human review / workflow
↓
Evals + monitoring + governance
```

---

# 3. Layer 1 — User/workflow surface

Possible surfaces:

- ChatGPT;
- ChatGPT Work;
- Codex;
- existing SaaS;
- custom app;
- backend event.

Question:

> Where does the work naturally happen?

Don't force a new UI unnecessarily.

---

# 4. Layer 2 — Identity

Before AI accesses business context:

```text
Who is user?
What can they access?
What can they do?
```

Identity/authorization should propagate through tools.

This is especially important for:

- plugins;
- RAG;
- agents;
- write actions.

---

# 5. Layer 3 — Model capability

Choose based on:

- reasoning;
- coding;
- modality;
- latency;
- cost;
- context;
- tool use.

Model is one component.

Don't let model selection dominate early solution design.

---

# 6. Layer 4 — Instructions/context

Model needs:

- task instruction;
- business rules;
- relevant context;
- output format.

This can be:

- project instructions;
- system/developer instructions;
- runtime context.

---

# 7. Layer 5 — Retrieval

Use for:

- private documents;
- approved policies;
- technical knowledge;
- source-backed answers.

Pattern:

```text
query
→ retrieve
→ context
→ model
```

Retrieval solves knowledge access.

---

# 8. Layer 6 — Current public information

Use web/search when workflow needs:

- current market;
- news;
- recent external facts.

Pattern:

```text
question
→ current source search
→ synthesis
→ citation
```

Static model knowledge is not enough for current facts.

---

# 9. Layer 7 — Tools

Use tools for:

- live structured data;
- actions;
- calculations;
- business systems.

Examples:

```text
CRM
ERP
ticketing
warehouse
email
calendar
internal API
```

Tools solve access/action.

---

# 10. Plugins / connected apps

Product-side integration can provide business context/actions without full custom app development.

Use when:

- ChatGPT/Work is acceptable surface;
- supported business system integration fits.

Benefits:

- faster time-to-value;
- existing workspace controls.

---

# 11. MCP

MCP can standardize how tools/context are exposed.

Concept:

```text
AI client
→ MCP server
→ business tool/data
```

MCP helps integration reuse.

It does not replace:

- authorization;
- governance;
- tool design.

---

# 12. Deterministic code

Important:

> Not every step should be AI.

Use code for:

- calculations;
- hard thresholds;
- validation;
- state transitions;
- policy gates.

Example:

```text
AI:
extract expense category

Code:
if amount > threshold → approval
```

---

# 13. Structured output

Bridge AI → software.

```text
Model
→ JSON/schema
→ deterministic workflow
```

Benefits:

- validation;
- integration;
- testing.

Use when software consumes AI output.

---

# 14. Agent layer

Use agent when workflow requires:

- multiple steps;
- dynamic decisions;
- several tools;
- state;
- feedback.

Agent coordinates components.

```text
Goal
↓
reason
↓
tool
↓
observe
↓
continue
```

---

# 15. State/memory

Multi-step workflows need state.

Examples:

- account checked;
- document retrieved;
- approval pending;
- task completed.

State should be managed explicitly when necessary.

Do not rely only on conversational memory.

---

# 16. Human role

Complete solution defines:

```text
AI does...
Human does...
```

Patterns:

- review;
- approve;
- exception handling;
- escalation.

Human role is part of architecture.

---

# 17. Evaluation layer

Each component can fail differently.

Evaluate:

### Retrieval
Did we get correct source?

### Model
Did it reason correctly?

### Tool
Was correct action called?

### Agent
Did task complete safely?

### Business
Did KPI improve?

---

# 18. Observability

Production solution should observe:

- latency;
- errors;
- tool calls;
- model usage;
- cost;
- escalation;
- task success.

Without observability:

> improvement is guesswork.

---

# 19. Governance

Complete enterprise solution may need:

- admin;
- identity;
- permissions;
- retention;
- data controls;
- audit;
- incident response.

Exact OpenAI product controls depend on product/plan and should be verified.

---

# 20. Technology-composition rule

Ask:

```text
Need general productivity?
→ ChatGPT

Need larger delegated knowledge work?
→ Work

Need software engineering?
→ Codex

Need custom product?
→ API

Need private documents?
→ retrieval

Need current public info?
→ web/search

Need live business system?
→ tool/plugin/MCP

Need multi-step dynamic execution?
→ agent
```

---

# 21. Complete solution example — Support

```text
Customer portal
↓
identity
↓
custom backend
↓
OpenAI API / agent
├─ policy retrieval
├─ account tool
├─ refund tool
└─ deterministic refund limit
↓
response/action
↓
human escalation
↓
evals/monitoring
```

This is more than “a chatbot.”

---

# 22. Complete solution example — Finance

```text
Finance user
↓
ChatGPT Work
↓
authorized data plugin
↓
analysis
↓
spreadsheet/model
↓
leadership-ready narrative
↓
finance review
```

No custom API necessarily required.

---

# 23. Complete solution example — Engineering

```text
Issue
↓
Codex
↓
repo/worktree
↓
implementation
↓
tests
↓
PR
↓
engineer review
```

Technology fit follows workflow.

---

# 24. Complete solution example — Knowledge

```text
Employee
↓
ChatGPT / internal app
↓
identity
↓
approved knowledge
↓
retrieval
↓
answer + citation
↓
no-answer escalation
```

Core architecture is the same even if surface changes.

---

# 25. Complete solution example — Research

```text
Analyst
↓
Work/research experience
├─ public sources
├─ internal documents
└─ company data
↓
synthesis
↓
report
↓
human verification
```

Technology composition follows evidence needs.

---

# 26. Complete solution example — Retail agent

```text
Shopper
↓
brand app
↓
API agent
├─ catalog/search
├─ inventory tool
├─ recommendation logic
└─ order tool
↓
answer/action
```

Need:

- permissions;
- product accuracy;
- live inventory;
- safe transaction rules.

---

# 27. Composition framework — STACK

## S — Surface
Where does experience live?

## T — Trusted context
What data/source?

## A — Actions
What tools/system changes?

## C — Controls
What permissions/rules/human review?

## K — KPI
What proves value?

```text
STACK
```

Then choose technology per layer.

---

# 28. Technology architecture worksheet

For every solution:

```text
Surface:
[ChatGPT / Codex / custom app]

Model capability:
[reasoning / coding / multimodal...]

Knowledge:
[retrieval / files / web]

Tools:
[CRM / ERP / email...]

State:
[what must persist]

Controls:
[permissions / rules / human approval]

Eval:
[task quality / business KPI]
```

---

# 29. Build-vs-configure check

Before custom architecture ask:

> Can ChatGPT/Work/Codex + approved connections satisfy the workflow?

If yes:

- faster;
- lower engineering.

Build custom API when:

- custom UX;
- external users;
- proprietary logic;
- deep custom integrations;
- background automation.

---

# 30. Avoid redundant intelligence

Bad:

```text
Model reasons
→ agent reasons
→ another agent reasons
```

with no need.

Use one agent/model step where sufficient.

More calls mean:

- latency;
- cost;
- failure points.

---

# 31. Avoid data duplication

Don't copy entire knowledge base into every prompt.

Use:

- retrieval;
- tools;
- structured access.

Relevant context > maximum context.

---

# 32. Avoid putting policy only in prompts

Critical business rule:

```text
"Never refund > $500"
```

should be enforced in code/tool permissions, not only instruction.

Prompt is not a security boundary.

---

# 33. Failure-mode thinking

Ask:

- source missing?
- tool down?
- model uncertain?
- conflicting data?
- action partially fails?

Design:

- timeout;
- retry;
- fallback;
- escalation;
- idempotency.

Complete solution includes failure behavior.

---

# 34. Pilot architecture vs production

Pilot may be:

```text
manual upload
+ model
```

Production may need:

```text
identity
+ live data
+ tools
+ monitoring
+ audit
+ scalability
```

Do not mistake POC architecture for production architecture.

---

# 35. Partner lens

When explaining solution:

> “This workflow needs a custom customer surface, private policy knowledge, live account state and one controlled action. That maps to API + retrieval + account/refund tools, with a deterministic limit and human escalation.”

This is clearer than a list of product names.

---

# 36. Common mistakes

1. Complete solution = model.
2. Stack every OpenAI technology.
3. Ignore identity.
4. Use retrieval for structured live state.
5. Use agent for deterministic flow.
6. Put hard policy only in prompt.
7. No human role.
8. No evaluation/monitoring.
9. POC architecture = production.

---

# 37. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Technology composition | Kết hợp công nghệ |
| Solution stack | Stack giải pháp |
| Identity | Danh tính user/system |
| Authorization | Phân quyền |
| Deterministic rule | Rule cố định bằng code |
| Structured output | Output theo schema |
| State | Trạng thái workflow |
| Observability | Khả năng quan sát |
| Governance | Quản trị |
| Failure mode | Cách hệ thống có thể fail |
| Fallback | Phương án dự phòng |

---

# 38. Section recap

Complete solution:

```text
Surface
+ identity
+ model
+ context
+ retrieval
+ tools
+ deterministic code
+ agent (if needed)
+ human role
+ evals
+ monitoring/governance
```

Use:

```text
STACK

Surface
Trusted context
Actions
Controls
KPI
```

Core rule:

> **Every technology in the solution should have a clearly defined job.**

---

# 39. Self-check

1. Retrieval và tool đóng role khác nhau thế nào?
2. Why should deterministic rules stay in code?
3. When should agent layer be added?
4. STACK framework gồm gì?
5. How does pilot architecture differ from production?
6. Design a complete support solution stack.
