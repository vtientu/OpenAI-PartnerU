# 04 — Recognizing Common Solution Paths

> **Course:** OpenAI Foundational Knowledge  
> **Sub-course:** OpenAI Product Portfolio Overview  
> **Section:** Recognizing Common Solution Paths

---

# 1. Section objective

Sau section này, bạn cần:

- nhận ra common solution paths từ customer problem;
- route giữa productivity, knowledge, embedded AI, coding, analytics và agents;
- hiểu mỗi path có maturity progression;
- biết khi nào solution path cần chuyển từ product configuration sang custom build.

---

# 2. Big picture

Most opportunities can start from a small set of paths:

```text
1. Employee productivity
2. Knowledge / retrieval
3. Coding / engineering
4. Embedded AI product
5. Data / analytics
6. Workflow automation
7. Agentic execution
8. Enterprise agent operations
```

These paths can overlap.

---

# 3. Path 1 — Employee productivity

Customer pain:

- too much writing;
- research;
- analysis;
- meetings;
- documents;
- context switching.

Typical route:

```text
ChatGPT
→ organization workspace
→ connections/plugins
→ reusable shared workflows
```

Primary metrics:

- time saved;
- quality;
- adoption;
- task coverage.

---

# 4. Productivity maturity path

```text
Individual prompts
↓
team best practices
↓
shared workspace/context
↓
repeatable agents/workflows
↓
tool-connected execution
```

Not every company needs the last step.

---

# 5. Path 2 — Knowledge assistant

Pain:

> Employees cannot find trusted information.

Typical route:

```text
ChatGPT/custom app
+
retrieval
+
approved knowledge
+
citations
```

Key questions:

- source of truth;
- permissions;
- freshness;
- no-answer behavior.

---

# 6. Knowledge path maturity

```text
Search
↓
AI answer
↓
grounded answer
↓
permission-aware answer
↓
answer + workflow action
```

At final stage, knowledge assistant may become agentic.

---

# 7. Path 3 — Coding / engineering

Pain:

- codebase complexity;
- implementation effort;
- tests;
- maintenance.

Route:

```text
Codex / coding AI
→ repository context
→ execution/testing
→ agentic coding
```

Metrics:

- lead time;
- cycle time;
- review effort;
- defect quality.

---

# 8. Path 4 — Embedded AI product

Customer wants AI in their own product.

Route:

```text
Product UX
↓
customer backend
↓
OpenAI API
↓
models/tools
↓
customer data
```

Examples:

- support feature;
- writing assistant;
- personalized recommendation;
- research feature;
- analytics assistant.

---

# 9. Embedded product maturity

```text
Single model call
↓
structured output
↓
retrieval
↓
tools
↓
agentic workflow
```

Add complexity only as needed.

---

# 10. Path 5 — Data and analytics

Pain:

- slow analysis;
- specialized skills;
- reporting bottlenecks.

Route:

```text
Natural language
↓
governed data tool/connector
↓
analysis
↓
explanation
```

Can live in:

- ChatGPT;
- custom app;
- enterprise analytics workflow.

---

# 11. Analytics controls

Need:

- governed data;
- correct metric definitions;
- query safety;
- validation;
- access control.

LLM should not invent business data.

---

# 12. Path 6 — Workflow automation

Pain:

- repetitive handoffs;
- copy/paste;
- classification;
- document processing.

Route:

```text
Event/input
↓
AI interpretation
↓
deterministic rules
↓
tools
↓
output/action
```

May not require a full agent.

---

# 13. Path 7 — Agentic execution

Pain:

- workflow has multiple steps;
- dynamic decisions;
- tool use;
- human coordination.

Route:

```text
Goal
↓
agent
↓
retrieval + tools
↓
actions
↓
completion/escalation
```

Need strong:

- evals;
- permissions;
- observability.

---

# 14. Path 8 — Enterprise agent operations

Pain:

- many agents;
- cross-system business context;
- governance;
- improvement at scale.

Route may involve enterprise platforms such as current OpenAI Frontier positioning.

Needs:

- shared business context;
- permissions;
- audit;
- evaluation loops;
- operational ownership.

---

# 15. Path 9 — Customer-facing voice/chat agent

Pain:

- high-volume conversational service;
- need production-grade agent operations.

Possible paths:

- custom API/realtime/agent stack;
- specialized managed enterprise agent product.

Choice depends on:

- build control;
- channels;
- integrations;
- operations;
- time-to-value.

---

# 16. Solution path is not one product

Example knowledge agent:

```text
ChatGPT
+ plugin
+ retrieval
+ policy source
+ identity
```

or:

```text
Custom UI
+ API
+ file search
+ CRM tool
+ agent
```

Path defines **solution shape**, not exact product list.

---

# 17. Common routing questions

### Q1
Will users work directly in ChatGPT?

If yes:
→ product/workspace path.

### Q2
Need AI inside customer product?

If yes:
→ API path.

### Q3
Need private documents?

→ retrieval.

### Q4
Need live data/action?

→ tools/plugins/MCP.

### Q5
Need multiple adaptive steps?

→ agent candidate.

---

# 18. Build vs configure path

## Configure-first

Use when:

- standard workflow;
- existing product supports it;
- speed matters;
- lower engineering desired.

## Build-first

Use when:

- proprietary UX;
- differentiated workflow;
- deep custom integrations;
- embedded customer experience.

---

# 19. Product-first pilot vs platform-first program

A single department may start:

```text
ChatGPT pilot
```

A company with many agent workflows may need:

```text
enterprise platform + governance strategy
```

Scale changes solution path.

---

# 20. Path transition signals

Move from simple to custom when:

- manual prompt reuse becomes bottleneck;
- data integration required;
- consistent workflow needed;
- action required;
- stronger audit/evals needed;
- end users are external.

---

# 21. Common path — Support

Stage 1:

```text
Agent assist
```

Stage 2:

```text
knowledge retrieval
```

Stage 3:

```text
tool-connected assistant
```

Stage 4:

```text
low-risk agentic resolution
```

Stage 5:

```text
broader agent operations
```

Maturity should be evidence-driven.

---

# 22. Common path — Sales

Stage 1:
research/drafting.

Stage 2:
CRM context.

Stage 3:
follow-up automation.

Stage 4:
agent handles scoped sales operations.

Actions affecting customers may still require human approval.

---

# 23. Common path — Engineering

Stage 1:
code Q&A.

Stage 2:
repo-aware coding.

Stage 3:
test/run.

Stage 4:
scoped coding agent.

Stage 5:
long-running engineering tasks.

---

# 24. Common path — Operations

Stage 1:
document summarization.

Stage 2:
structured extraction.

Stage 3:
validation/routing.

Stage 4:
system updates.

Stage 5:
end-to-end exception-aware agent.

---

# 25. Path scoring framework — ROUTE

## R — Role
Who is the user?

## O — Outcome
What business result?

## U — User surface
Where should experience live?

## T — Tools/context
What does AI need access to?

## E — Execution level
Answer, assist, action, or multi-step agent?

Use ROUTE to map opportunity.

---

# 26. Add BUILD

## B — Business differentiation
Is workflow proprietary?

## U — User control
Need custom UX?

## I — Integration depth
How complex?

## L — Lifecycle operations
Who owns updates/evals?

## D — Delivery speed
How quickly must value appear?

This helps build-vs-configure.

---

# 27. Partner lens

Instead of:

> “Customer needs ChatGPT.”

Say:

> “The workflow looks like an employee-productivity path; let's determine whether standard workspace capability, connected context, or a custom workflow is required.”

This preserves optionality.

---

# 28. Common mistakes

1. Product name mistaken for solution path.
2. Jump directly to agent.
3. Build custom before testing configure path.
4. Force users into ChatGPT when experience must be embedded.
5. Force custom app when product-native capability fits.
6. Ignore maturity path.
7. Design end state before validating first measurable step.

---

# 29. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Solution path | Hướng giải pháp |
| Productivity path | Hướng tăng productivity |
| Knowledge path | Hướng knowledge/retrieval |
| Embedded AI | AI nhúng |
| Maturity path | Lộ trình trưởng thành |
| Configure-first | Ưu tiên cấu hình capability có sẵn |
| Build-first | Ưu tiên custom build |
| Agentic resolution | Agent xử lý case |
| Enterprise operations | Vận hành quy mô enterprise |
| Differentiation | Khác biệt cạnh tranh |

---

# 30. Section recap

Common paths:

```text
Employee productivity
Knowledge assistant
Coding
Embedded AI
Analytics
Workflow automation
Agentic execution
Enterprise agent operations
```

Use:

```text
ROUTE
Role
Outcome
User surface
Tools/context
Execution level
```

Core rule:

> **Recognize the solution path before naming the product.**

---

# 31. Self-check

1. Solution path khác product như thế nào?
2. Knowledge path có thể evolve thành agentic path như thế nào?
3. Khi nào configure-first hợp lý?
4. Embedded AI path cần gì khác employee productivity?
5. ROUTE framework gồm gì?
6. Hãy map customer support từ assist → agentic resolution.
