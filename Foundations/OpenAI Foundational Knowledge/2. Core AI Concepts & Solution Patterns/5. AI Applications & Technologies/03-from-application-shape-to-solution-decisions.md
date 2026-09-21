# 03 — From Application Shape to Solution Decisions

> **Course:** OpenAI Foundational Knowledge  
> **Sub-course:** AI Applications & Technologies  
> **Section:** From application shape to solution decisions
>
> **Goal:** Nối từ “AI application trông như thế nào?” sang “cần quyết định architecture, data, tools, controls và evals ra sao?”

---

## 1. Section objective

Sau section này, bạn cần:

- nhìn một use case và nhận ra application shape chính;
- biến application shape thành architecture decisions;
- biết decision nào thuộc model, data, tool, UX, controls và evals;
- hiểu autonomy/risk ảnh hưởng thiết kế solution như thế nào;
- tránh “model-first solutioning”.

---

# 2. Big picture

Một solution tốt nên đi theo flow:

```text
Business problem
↓
User + workflow
↓
Application shape
↓
Data / knowledge / tools
↓
Model capability
↓
UX + controls
↓
Evaluation
↓
Deployment
```

Không nên:

```text
Choose model
↓
Find a problem
```

---

# 3. What is “application shape”?

Application shape = cách AI xuất hiện ở mức high-level trong workflow.

Examples:

- chat assistant;
- embedded copilot;
- knowledge/RAG assistant;
- document extraction pipeline;
- analytics assistant;
- tool-using assistant;
- agent;
- multimodal workflow;
- batch processor.

Shape giúp ta đoán trước các requirement.

---

# 4. Why shape matters

Compare:

### A. Marketing draft assistant

```text
User
→ prompt
→ model
→ draft
```

### B. Financial service agent

```text
User
→ identity
→ policy/data
→ model
→ tools
→ action
→ audit
→ escalation
```

Cả hai đều dùng GenAI, nhưng architecture/risk hoàn toàn khác.

---

# 5. Decision dimension 1 — Interaction model

How does user interact?

## Chat
Flexible conversation.

## Form/workflow UI
Structured fields and actions.

## Inline copilot
AI embedded in existing application.

## Background/batch
No realtime user interaction.

## Event-driven
System invokes AI when an event occurs.

This affects:

- UX;
- latency;
- failure handling;
- expectations.

---

# 6. Decision dimension 2 — Input modality

Inputs may include:

- text;
- image;
- audio;
- video;
- documents;
- code;
- structured data.

A solution may require multiple model types.

Example:

```text
Audio
→ transcription
→ reasoning
→ text-to-speech
```

---

# 7. Decision dimension 3 — Output shape

Possible outputs:

## Free-form text
Draft/explanation.

## Structured JSON
Downstream system integration.

## Classification/ranking
Routing/prioritization.

## Tool call/action
Execution.

## Media
Image/audio.

Output type determines validation strategy.

---

# 8. Decision dimension 4 — Knowledge requirement

Ask:

> What information must the system know at runtime?

### General knowledge
Model may be enough.

### Private/current documents
RAG.

### Live structured data
API/tool.

### Large analytical data
Database/query/code tool.

### User state/preferences
Application context/memory.

Don't solve every knowledge problem by fine-tuning.

---

# 9. Decision dimension 5 — Actions/tools

Read-only assistant:

```text
AI → answer
```

Action-capable assistant:

```text
AI → tool → real system change
```

Once actions are involved, consider:

- authentication;
- authorization;
- least privilege;
- confirmation;
- transaction limits;
- audit logs;
- retries;
- rollback/escalation.

---

# 10. Decision dimension 6 — Autonomy

A useful study spectrum:

```text
L0 — AI suggests
L1 — AI drafts, human executes
L2 — AI prepares action, human approves
L3 — AI executes low-risk cases
L4 — AI executes broader multi-step workflow
```

Not an official universal standard.

Lesson:

> More autonomy generally requires stronger controls and stronger evidence.

---

# 11. Decision dimension 7 — Consequence of error

Ask:

> What happens if the system is wrong?

Low consequence:

- brainstorm title.

Medium:

- internal report draft.

Higher:

- financial action;
- customer account update;
- safety-sensitive recommendation.

Controls should be proportional to consequence.

---

# 12. Decision dimension 8 — Latency

Interactive UX:

- response time matters.

Batch:

- throughput/cost may matter more.

Complex reasoning:

- longer latency may be acceptable if quality benefit is meaningful.

Trade-off:

```text
Quality
↔ latency
↔ cost
```

---

# 13. Decision dimension 9 — Scale

Questions:

- requests/day?
- concurrent users?
- documents/day?
- average input size?
- peak load?
- batch vs realtime?

Scale affects:

- architecture;
- cost;
- retries;
- rate limits;
- caching;
- queueing;
- observability.

---

# 14. Decision dimension 10 — Evaluation

Different shape → different eval.

### Draft assistant
- relevance;
- factuality;
- tone.

### Extraction
- field-level correctness.

### RAG
- retrieval quality;
- groundedness;
- citation quality.

### Agent
- task completion;
- correct tool use;
- safe actions;
- escalation.

There is no single universal “AI accuracy” metric.

---

# 15. Shape 1 — Simple generation assistant

```text
User
→ instruction
→ model
→ output
```

Good for:

- drafting;
- brainstorming;
- rewriting.

Decisions:

- prompt;
- model quality;
- UX;
- review;
- simple evals.

Do not add RAG/tools if unnecessary.

---

# 16. Shape 2 — Knowledge assistant

```text
User
→ retrieval
→ model
→ answer + sources
```

Decisions:

- source governance;
- indexing;
- permissions;
- citations;
- no-answer behavior;
- retrieval and answer evals.

---

# 17. Shape 3 — Extraction pipeline

```text
Document
→ model
→ structured schema
→ validation
→ business system
```

Decisions:

- input modality;
- schema;
- field validation;
- exception handling;
- batch scale;
- field-level metrics.

No chat needed.

---

# 18. Shape 4 — Analytics assistant

```text
Question
→ semantic/business context
→ query/code tool
→ data
→ analysis
→ explanation
```

Decisions:

- governed data access;
- query safety;
- semantic definitions;
- calculation validation;
- analyst review.

---

# 19. Shape 5 — Copilot inside existing software

```text
Existing app
+ current workflow context
+ AI panel/inline action
```

Benefits:

- less context switching;
- current user/workflow state available;
- potentially easier adoption.

Questions:

- what context is shared automatically?
- what permissions?
- can user edit/accept/reject?
- what latency is acceptable?

---

# 20. Shape 6 — Tool-using assistant

```text
User
→ model
→ tool choice
→ API
→ result
→ response
```

Decisions:

- tool definitions;
- auth;
- allowed operations;
- confirmation;
- retries/errors;
- logging.

---

# 21. Shape 7 — Agent

```text
Goal
↓
reason/plan
↓
tools
↓
state
↓
loop
↓
finish / escalate
```

Use when task requires:

- multiple steps;
- changing plan;
- interpretation between steps;
- tools.

Agents add flexibility and complexity.

---

# 22. When not to use an agent

If workflow is deterministic:

```text
A → B → C
```

Traditional code/orchestration may be better.

Use AI where ambiguity/reasoning is useful.

Principle:

> **Keep deterministic logic deterministic when possible.**

Benefits:

- reliability;
- testability;
- security;
- lower cost.

---

# 23. Shape 8 — Multimodal workflow

Example:

```text
Equipment photo
+ technician question
↓
multimodal model
↓
manual retrieval
↓
answer
```

Decisions:

- image/audio quality;
- source grounding;
- user confirmation;
- domain risk.

---

# 24. Shape 9 — Batch pipeline

```text
10,000 contracts
↓
batch extraction
↓
structured outputs
↓
review exceptions
```

Decisions:

- throughput;
- queueing;
- retries;
- idempotency;
- cost;
- observability;
- sampling/review.

---

# 25. Framework — SHAPE

## S — Scope
What exact user/workflow?

## H — Human role
What remains human-owned?

## A — Access
What data/tools may AI access?

## P — Performance
What quality/latency/cost is required?

## E — Evaluation
How do we know it works?

---

# 26. Add RISK

For production:

## R — Risk/consequence
What happens if wrong?

## I — Identity/permissions
Who is AI acting as?

## S — Safety/security controls
What limits behavior?

## K — Kill switch / fallback
How do we stop, fail safely or escalate?

So:

```text
SHAPE + RISK
```

becomes a practical solution checklist.

---

# 27. Example — HR assistant

Customer says:

> “We want AI for HR.”

Clarify:

```text
User:
employees

Task:
policy questions

Knowledge:
private HR docs

Action:
none in phase 1

Risk:
wrong guidance

UX:
chat in intranet

Metric:
answer quality + ticket reduction
```

Solution shape:

```text
Permission-aware RAG assistant
+ citations
+ no-answer behavior
+ HR escalation
```

Now solution decisions are much clearer.

---

# 28. Example — Expense processing

Customer says:

> “Automate expense claims.”

Break down:

```text
Input:
receipt image + form

Need:
extract fields
check policy
look up employee/project
route approval

Action:
create expense record

Risk:
financial error/fraud
```

Likely architecture:

```text
Multimodal extraction
→ structured output
→ deterministic/policy checks
→ API lookup
→ human exception approval
→ controlled write
```

Not simply:

> “Use an agent.”

---

# 29. Choose the right mechanism per step

A strong workflow may mix:

```text
AI
+
deterministic code
+
human
```

Example:

```text
Receipt extraction → AI
Tax calculation → deterministic code
Policy ambiguity → AI
High-value approval → human
Database write → controlled API
```

This is often more reliable than forcing AI into every step.

---

# 30. Model selection comes later

After shape is clear, select candidate models based on:

- modality;
- reasoning;
- structured output;
- tool use;
- latency;
- cost;
- context.

Then run representative evals.

```text
Requirement
→ candidate models
→ eval
→ selection
```

---

# 31. Data decisions

For each application ask:

- what data enters?
- what is source of truth?
- how fresh must it be?
- what permissions?
- sensitive/confidential?
- where is output stored?
- who owns data quality?

Data architecture may determine feasibility more than model capability.

---

# 32. UX as a control layer

Useful UX patterns:

- source citations;
- draft label;
- editable output;
- confirmation before action;
- progress/status;
- escalation button;
- error/fallback state.

AI uncertainty should be reflected in UX.

---

# 33. Evaluation before production

For each critical behavior define:

```text
Input
Expected behavior
Failure mode
Metric
Threshold
```

Test:

- common cases;
- edge cases;
- no-answer;
- tool failures;
- permission cases;
- risky cases.

---

# 34. Observability

Production system should measure appropriately:

- task success;
- latency;
- errors;
- tool calls;
- escalation;
- user feedback;
- cost;
- workflow outcome.

Without observability, improvement becomes guesswork.

---

# 35. Rollout strategy

For complex/high-impact applications:

```text
Prototype
↓
Offline eval
↓
Internal testing
↓
Limited pilot
↓
Production scope
↓
Expand
```

Especially important for action-capable agents.

---

# 36. Discovery matrix

| Question | Why it matters |
|---|---|
| Who is user? | UX + permissions |
| What task? | Capability |
| What data? | RAG/tool choice |
| Current/live? | API vs retrieval |
| Need action? | Auth/tooling |
| What if wrong? | Controls |
| Realtime? | Latency |
| Volume? | Cost/scale |
| Human role? | Autonomy |
| Success metric? | Evaluation/value |

---

# 37. Common mistakes

1. Every AI app = chatbot.
2. Every enterprise app = RAG.
3. Every automation = agent.
4. Use AI for deterministic calculations without reason.
5. No human role defined.
6. Select model before requirements.
7. Build first, eval later.
8. Treat permissions as implementation detail.
9. Add complexity because it looks “more AI”.

---

# 38. Developer mental model

Separate concerns:

```text
UI
→ interaction

Backend/orchestrator
→ deterministic workflow/control

Model
→ language/reasoning/ambiguity

Retrieval
→ unstructured knowledge

Tools
→ live data/actions

Evals/monitoring
→ quality evidence
```

This is easier to debug and govern than:

> “AI does everything.”

---

# 39. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Application shape | Hình thái ứng dụng |
| Copilot | AI hỗ trợ bên trong workflow |
| Agent | System AI nhiều bước/tool |
| Orchestration | Điều phối workflow |
| Autonomy | Mức tự chủ |
| Least privilege | Quyền tối thiểu cần thiết |
| Fallback | Phương án dự phòng |
| Escalation | Chuyển case |
| Observability | Khả năng quan sát hệ thống |
| Throughput | Khối lượng xử lý |
| Idempotency | Lặp request/action mà không tạo side effect ngoài ý muốn |
| Acceptance threshold | Ngưỡng chất lượng chấp nhận |

---

# 40. Section recap

Use this flow:

```text
Problem
↓
Workflow
↓
Application shape
↓
Knowledge/data
↓
Tools/actions
↓
Human role
↓
Model capability
↓
Controls
↓
Eval
↓
Deployment
```

Core rules:

1. Chat is only one shape.
2. RAG solves knowledge access, not every problem.
3. Agents are for multi-step ambiguity, not every automation.
4. Live structured state often belongs in tools/APIs.
5. Keep deterministic logic deterministic when appropriate.
6. More autonomy → stronger controls.
7. Model selection follows requirements and evals.

---

# 41. Self-check

1. Application shape là gì?
2. Knowledge assistant và tool-using assistant khác nhau thế nào?
3. Khi nào không nên dùng agent?
4. Vì sao autonomy và consequence cần xem cùng nhau?
5. Hãy dùng SHAPE + RISK cho một support agent.
6. Hãy thiết kế high-level architecture cho expense processing.
