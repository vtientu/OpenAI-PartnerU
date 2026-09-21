# 01 — From Customer Problem to Solution Pattern

> **Course:** OpenAI Foundational Knowledge  
> **Course:** Real World OpenAI Solutions  
> **Section:** From customer problem to solution pattern
>
> **PartnerU note:** Đây là optimized study guide dựa trên section title và các public OpenAI materials. Không phải transcript nguyên văn của PartnerU.

---

# 1. Section objective

Sau section này, bạn cần:

- đi từ một customer statement mơ hồ tới workflow cụ thể;
- phân biệt **problem**, **use case**, **solution pattern** và **technology choice**;
- biết cách nhận diện nơi AI có thể tạo value;
- map workflow step thành capability/application pattern;
- tạo một solution hypothesis có thể validate bằng pilot/eval.

---

# 2. Big picture

Customer thường bắt đầu bằng một statement kiểu:

> “We need AI for customer support.”

Đây chưa phải solution.

Cần chuyển thành:

```text
Business problem
↓
Current workflow
↓
Pain / evidence
↓
AI-suitable steps
↓
Solution pattern
↓
Technology path
↓
Controls / evals
↓
Business metric
```

Cốt lõi:

> **Solutioning bắt đầu từ workflow, không bắt đầu từ model/product.**

---

# 3. Problem vs use case vs solution pattern

## Problem

Business pain / friction.

Example:

> Support agents spend too much time searching policy and account information.

## Use case

A specific user/task/outcome.

Example:

> Help support agents answer refund questions using approved policy and current account data.

## Solution pattern

A reusable technical/business shape.

Example:

```text
Knowledge retrieval
+ account tool
+ response generation
+ human review
```

## Technology choice

Specific implementation.

Example:

```text
ChatGPT workspace + plugin
```

or:

```text
Custom support app
+ OpenAI API
+ RAG
+ CRM tool
```

---

# 4. Do not confuse department with use case

Weak:

> “AI for Finance.”

Better:

> “Generate monthly variance commentary from approved actuals and forecast data for analyst review.”

Why?

Because a real use case specifies:

- user;
- task;
- input;
- AI role;
- output;
- metric.

---

# 5. Start from business outcome

Ask:

- What business outcome matters?
- Why now?
- How is the problem visible?
- What happens if nothing changes?

Examples:

```text
Reduce support handling time
Shorten engineering cycle time
Improve knowledge access
Reduce document-processing effort
Increase campaign throughput
```

Outcome keeps AI tied to business value.

---

# 6. Map the current workflow

Example support workflow:

```text
1. Receive customer request
2. Identify issue
3. Search policy
4. Open CRM
5. Check account
6. Decide next step
7. Draft response
8. Update ticket
```

Now you can inspect each step.

Without workflow map, “AI support solution” remains vague.

---

# 7. Find the friction

Look for:

- repetitive work;
- manual search;
- copy/paste;
- handoffs;
- delays;
- skill bottlenecks;
- unstructured information;
- inconsistent quality;
- ambiguous judgment.

OpenAI's public use-case guide highlights three opportunity areas:

```text
Repetitive low-value tasks
Skill bottlenecks
Navigating ambiguity
```

These are useful discovery lenses.

---

# 8. Identify evidence

Pain should have evidence.

Examples:

- agents spend 7 minutes searching;
- 35% of tickets require escalation;
- engineers spend days on migration cleanup;
- analysts manually combine 6 spreadsheets.

Evidence helps distinguish:

```text
interesting idea
from
real opportunity
```

---

# 9. Break workflow into AI-suitable tasks

For each step ask:

### Language-heavy?
- summarize;
- classify;
- draft.

### Information-heavy?
- research;
- retrieve;
- synthesize.

### Analysis-heavy?
- compare;
- reason;
- detect patterns.

### Action-heavy?
- update system;
- call API;
- route case.

This maps work to capability.

---

# 10. OpenAI's six public use-case primitives

OpenAI's public guide currently describes six broad use-case primitives:

```text
1. Content creation
2. Research
3. Coding
4. Data analysis
5. Ideation & strategy
6. Automation
```

These are useful as **discovery primitives**.

They are not the same thing as complete solution architectures.

---

# 11. Primitive → application pattern

Example:

```text
Research
↓
knowledge assistant

Data analysis
↓
analytics assistant

Automation
↓
tool-enabled workflow

Coding
↓
Codex / coding agent
```

One use case can combine several primitives.

---

# 12. Application pattern → solution pattern

Example:

```text
Knowledge assistant
```

becomes stronger solution when we add:

```text
User identity
+ approved data
+ retrieval
+ citations
+ escalation
+ evaluation
```

A solution pattern includes enough architecture to solve the workflow credibly.

---

# 13. Solution pattern vs product

Do not say:

> “RAG is the product.”

RAG is a pattern.

Do not say:

> “ChatGPT is the use case.”

ChatGPT is a product surface.

Think:

```text
Problem
→ use case
→ solution pattern
→ product/technology
```

---

# 14. Key solution questions

For each use case identify:

## User
Who performs the work?

## Input
What information comes in?

## Knowledge
What does AI need to know?

## Action
What does AI need to do?

## Output
What should result look like?

## Human role
Who reviews/approves?

## Metric
How do we know value?

---

# 15. Knowledge routing

A powerful solution rule:

```text
General reasoning
→ model

Private/current documents
→ retrieval

Live structured business data
→ API/tool

Current public information
→ web/search

Persistent workflow state
→ application state/memory
```

This prevents trying to solve everything with model weights.

---

# 16. Action routing

### Answer only

```text
model / retrieval
```

### One controlled action

```text
tool-enabled assistant
```

### Multiple adaptive actions

```text
agent candidate
```

Do not jump directly to agent.

---

# 17. User-surface decision

Where should solution live?

### ChatGPT
Employee/general knowledge work.

### ChatGPT Work
Larger knowledge-work deliverables.

### Codex
Software engineering workflow.

### Customer application
Embedded AI via API.

### Background
No UI; event-driven API workflow.

Surface follows workflow.

---

# 18. Build vs configure

Ask:

> Can an existing OpenAI product solve most of this workflow?

If yes:

```text
configure/use
```

If customer needs:

- custom UX;
- proprietary logic;
- custom actions;
- external customer experience;

then:

```text
API/custom build
```

Simplest credible path is often best.

---

# 19. Define human role

Possible models:

```text
AI assists
Human decides

AI drafts
Human approves

AI executes low-risk cases
Human handles exceptions
```

Human role should be designed—not assumed.

---

# 20. Define controls

Controls may include:

- permissions;
- citations;
- schema validation;
- human approval;
- amount limits;
- deterministic policy checks;
- audit logs;
- escalation.

Controls depend on risk.

---

# 21. Define evaluation

Before implementation, ask:

> What would prove the solution works?

Examples:

### Support
- grounded answer correctness;
- handling time;
- escalation.

### Extraction
- field-level accuracy.

### Agent
- successful task completion;
- correct tool use;
- safe action.

### Coding
- tests;
- review outcome;
- cycle time.

---

# 22. Problem-to-pattern framework — TRACE

A study framework:

## T — Target outcome
What business result?

## R — Real workflow
What happens today?

## A — AI-suitable steps
Which tasks benefit from AI?

## C — Context & controls
What data/tools/risk?

## E — Evidence
What metric/eval validates value?

```text
TRACE
→ solution pattern
```

---

# 23. Add PATH

After TRACE:

## P — Product surface
Where should AI live?

## A — Access
What data/tools?

## T — Task complexity
Single-step vs adaptive multi-step?

## H — Human role
What remains human-owned?

```text
TRACE → PATH
```

---

# 24. Example — Customer support

Problem:

> Refund cases take too long.

Workflow:

```text
read ticket
→ search policy
→ check order
→ decide
→ act
→ respond
```

Pattern:

```text
classification
+ policy retrieval
+ account tool
+ deterministic eligibility rule
+ refund tool
+ escalation
```

Technology may be:

- support app + API;
- or product-native/plugin path.

---

# 25. Example — Finance

Problem:

> Analysts spend days preparing variance commentary.

Workflow:

```text
collect actuals
→ compare forecast
→ identify drivers
→ write commentary
```

Pattern:

```text
data access
+ analysis
+ narrative generation
+ analyst review
```

No agent required if one analysis flow is enough.

---

# 26. Example — Engineering

Problem:

> Migration backlog is growing.

Workflow:

```text
find deprecated API usage
→ update
→ test
→ fix
→ review
```

Pattern:

```text
Codex agentic software delivery
```

with:

- repo access;
- tests;
- human review.

---

# 27. Example — HR knowledge

Problem:

> HR answers repetitive policy questions.

Pattern:

```text
permission-aware knowledge assistant
+ citations
+ no-answer behavior
+ HR escalation
```

Could be ChatGPT workspace or custom app depending surface.

---

# 28. Avoid premature architecture

Early discovery does not need:

- exact model ID;
- exact vector DB;
- exact agent framework.

First understand:

```text
workflow
data
actions
risk
metric
```

Then choose implementation.

---

# 29. Common mistakes

1. Department = use case.
2. Product = solution pattern.
3. Start with newest model.
4. Treat primitive as complete architecture.
5. Add RAG without knowledge need.
6. Add agent without multi-step need.
7. Ignore human role.
8. No evidence/baseline.
9. Assume POC proves business value.

---

# 30. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Customer problem | Vấn đề customer |
| Use case | Trường hợp sử dụng cụ thể |
| Solution pattern | Mẫu giải pháp tái sử dụng |
| Primitive | Kiểu use case nền tảng |
| Workflow | Luồng công việc |
| Evidence | Bằng chứng |
| Baseline | Mốc hiện trạng |
| Product surface | Nơi user tương tác |
| Build vs configure | Xây mới hay cấu hình |
| Human role | Vai trò con người |
| Validation | Xác thực solution |

---

# 31. Section recap

Use this flow:

```text
Problem
↓
Workflow
↓
Pain/evidence
↓
AI-suitable tasks
↓
Primitive/application pattern
↓
Solution pattern
↓
Technology
↓
Controls/evals
↓
Outcome
```

Framework:

```text
TRACE
Target
Real workflow
AI-suitable steps
Context/controls
Evidence

→

PATH
Product surface
Access
Task complexity
Human role
```

Core rule:

> **Translate a customer problem into a workflow first; only then choose the solution pattern and technology.**

---

# 32. Self-check

1. Problem, use case và solution pattern khác nhau thế nào?
2. OpenAI's six public use-case primitives là gì?
3. Khi nào RAG xuất hiện?
4. Khi nào agent xuất hiện?
5. TRACE → PATH gồm gì?
6. Hãy chuyển “AI for support” thành một solution pattern cụ thể.
