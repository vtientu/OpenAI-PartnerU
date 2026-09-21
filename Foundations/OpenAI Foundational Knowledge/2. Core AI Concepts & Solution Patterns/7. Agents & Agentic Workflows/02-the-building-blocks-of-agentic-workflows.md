# 02 — The Building Blocks of Agentic Workflows

> **Course:** OpenAI Foundational Knowledge  
> **Sub-course:** Agents & Agentic Workflows  
> **Section:** The building blocks of agentic workflows

---

# 1. Section objective

Sau section này, bạn cần:

- hiểu các building blocks chính của agentic system;
- biết vai trò của model, instructions, tools, state, orchestration, guardrails, evals và human handoff;
- hiểu execution loop;
- biết system reliability phụ thuộc vào toàn bộ architecture chứ không chỉ model.

---

# 2. Big picture

Một agentic workflow thường có:

```text
Goal
↓
Model / reasoning
↓
Instructions
↓
Tools
↓
State / context
↓
Orchestration loop
↓
Guardrails
↓
Human handoff
↓
Evals / monitoring
```

Một block yếu có thể làm cả workflow fail.

---

# 3. Building block 1 — Goal

Agent cần biết:

> “Success là gì?”

Bad goal:

> “Handle support.”

Better:

> “Resolve eligible password-reset tickets according to policy, otherwise escalate.”

Goal nên có:

- scope;
- completion criteria;
- constraints.

---

# 4. Completion criteria

Agent phải biết khi nào dừng.

Examples:

```text
Ticket resolved
Order status confirmed
Code tests pass
Required record created
Human handoff accepted
```

Without stop condition:

- loops can continue;
- duplicate actions;
- cost/latency increase.

---

# 5. Building block 2 — Model / reasoning engine

Model interprets:

- goal;
- state;
- tool results;
- instructions.

It may decide:

- what to do next;
- which tool to call;
- whether to ask clarification;
- whether to escalate.

Model quality matters, but system design still matters.

---

# 6. Model selection for agents

Consider:

- reasoning;
- tool-use quality;
- latency;
- cost;
- context;
- modality.

Don't assume highest-capability model for every step.

Some workflows can route tasks.

---

# 7. Building block 3 — Instructions

Instructions define expected behavior.

Include:

- role;
- scope;
- priorities;
- allowed/disallowed behavior;
- tool-use rules;
- escalation rules;
- output format.

Example:

```text
Resolve only password-reset requests.
Never change billing settings.
Escalate if identity verification fails.
```

Instructions are part of control.

---

# 8. Instructions are not enough

You cannot rely only on prompt:

> “Do not access unauthorized data.”

Security should also be enforced by actual permissions.

Rule:

```text
Policy in prompt
+
technical enforcement
```

not prompt alone.

---

# 9. Building block 4 — Tools

Tools let agent access data or perform actions.

Examples:

- search knowledge;
- query CRM;
- create ticket;
- send email;
- run code;
- update account;
- inspect repository.

Tools convert language capability into operational capability.

---

# 10. Tool contract

Each tool should have clear:

- name;
- purpose;
- inputs;
- outputs;
- permissions;
- error behavior.

Think of tool like an API contract.

Bad:

```text
do_everything()
```

Better:

```text
get_order_status(order_id)
issue_refund(order_id, amount)
```

Scoped tools are easier to secure/evaluate.

---

# 11. Read tools vs write tools

## Read

- query;
- search;
- retrieve.

Lower consequence.

## Write

- update;
- create;
- delete;
- send;
- transfer.

Higher consequence.

Write tools often need:

- stronger auth;
- limits;
- confirmation;
- audit.

---

# 12. Building block 5 — Identity and permissions

Agent should act with defined identity.

Ask:

- acting as user?
- service account?
- delegated authority?

Permissions should follow:

> **least privilege**

Only access/actions needed for task.

---

# 13. Building block 6 — Context

Context may include:

- user request;
- prior messages;
- relevant documents;
- tool outputs;
- workflow state;
- business rules.

Too little context → poor decisions.

Too much irrelevant context → noise/cost.

Context engineering matters.

---

# 14. Building block 7 — State

State tells agent:

> “Where are we in the workflow?”

Examples:

```text
identity_verified = true
policy_checked = true
refund_status = pending
```

State can be:

- conversation state;
- workflow state;
- external system state.

State should not rely only on model memory.

---

# 15. Stateful vs stateless

Stateless:

```text
each request independent
```

Stateful:

```text
system remembers workflow progress
```

Agents often need state.

But storing state creates requirements:

- persistence;
- consistency;
- access control;
- recovery.

---

# 16. Building block 8 — Orchestration

Orchestration coordinates:

- model calls;
- tools;
- state;
- branching;
- retries;
- approvals.

Simplified:

```text
while not done:
    ask model next action
    validate action
    execute tool
    update state
```

Real systems add more controls.

---

# 17. Deterministic orchestration

Some steps should be deterministic.

Example:

```text
If refund > $500
→ require manager approval
```

Don't rely on model to “remember” this rule if it can be enforced in code.

Principle:

> **Use model for ambiguity; use code for hard rules.**

---

# 18. Building block 9 — Guardrails

Guardrails can enforce:

- allowed tools;
- input/output validation;
- amount limits;
- policy checks;
- content restrictions;
- approval gates.

Layered guardrails are stronger than one check.

---

# 19. Building block 10 — Human-in-the-loop

Human roles:

- approve;
- review;
- resolve exception;
- provide missing context;
- override;
- investigate incident.

HITL can occur:

```text
before action
after action
only on exception
random sampling
```

---

# 20. Escalation triggers

Examples:

- uncertain identity;
- policy conflict;
- tool failure;
- amount above threshold;
- repeated loop;
- missing evidence;
- customer asks for human.

Escalation is part of good agent design.

---

# 21. Building block 11 — Memory

Memory may mean:

- conversation history;
- user preference;
- prior task state;
- retrieved knowledge.

Important:

> Application memory ≠ model training.

Store only what is needed and appropriate.

---

# 22. Short-term vs long-term memory

## Short-term

Current task/session context.

## Long-term

Persisted user/workflow info across sessions.

Long-term memory requires stronger:

- privacy;
- retention;
- access controls;
- update/delete logic.

---

# 23. Building block 12 — Evaluation

Agent eval must test more than final text.

Evaluate:

- task completion;
- correct tool choice;
- correct arguments;
- policy compliance;
- safe actions;
- escalation;
- loops;
- final result.

---

# 24. Step-level vs end-to-end eval

## Step-level

Did agent call correct tool?

## End-to-end

Did workflow achieve business goal?

Both matter.

---

# 25. Building block 13 — Observability

Need visibility into:

- model decisions;
- tool calls;
- latency;
- errors;
- retries;
- cost;
- escalation;
- completion.

Without traces/logs, agent debugging is hard.

---

# 26. Trace

A trace can capture sequence:

```text
User request
→ model decision
→ tool call
→ tool result
→ next decision
→ final action
```

This helps:

- debugging;
- evaluation;
- audit.

---

# 27. Building block 14 — Failure handling

Tools fail.

Data missing.

Model misinterprets.

Need:

- retry;
- timeout;
- fallback;
- idempotency;
- rollback;
- escalation.

Agent should fail safely.

---

# 28. Idempotency

Important for write actions.

If tool call repeats due to retry:

```text
charge_customer()
```

must not accidentally charge twice.

Idempotency ensures repeated request does not create duplicate unintended effects.

---

# 29. Building block 15 — Cost/latency controls

Agent loops can be expensive.

Need limits:

- max steps;
- max tool calls;
- timeout;
- budget;
- model routing.

Otherwise agent can overrun.

---

# 30. Reference architecture

```text
User / event
↓
Agent orchestrator
├─ instructions
├─ model
├─ state
├─ tools
├─ guardrails
└─ human escalation
↓
Enterprise systems
↓
Tracing / eval / monitoring
```

---

# 31. Example — Refund agent

Goal:

> Resolve eligible refund request.

Blocks:

### Model
Interprets request.

### Retrieval
Gets policy.

### Tool 1
Gets order.

### Tool 2
Issues refund.

### Rule
Refund > threshold requires approval.

### State
Tracks eligibility/approval.

### Human
Handles exceptions.

### Eval
Measures correct policy/action.

---

# 32. Example — Coding agent

Goal:

> Implement bug fix.

Tools:

- repo search;
- file edit;
- test runner.

State:

- files changed;
- tests run;
- failures.

Guardrails:

- scoped repository;
- no production deploy.

Human:

- code review.

---

# 33. Developer mental model

Agentic system resembles:

```text
Workflow engine
+
LLM decision node
+
tool adapters
+
state store
+
policy layer
+
observability
```

This is closer to distributed systems/backend engineering than “just prompting.”

---

# 34. Partner discovery questions

1. What goal?
2. Completion criteria?
3. What tools?
4. Read or write?
5. Who authorizes actions?
6. What state must persist?
7. What rules must be deterministic?
8. What triggers human handoff?
9. How many steps are acceptable?
10. How is success evaluated?

---

# 35. Common mistakes

1. Model = agent.
2. Prompt = security boundary.
3. No state design.
4. Broad “do everything” tool.
5. No max-step limit.
6. No escalation.
7. Only evaluate final text.
8. Ignore idempotency.
9. Let AI enforce business rules that code should enforce.

---

# 36. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Goal | Mục tiêu |
| Completion criteria | Tiêu chí hoàn thành |
| Instruction | Chỉ dẫn |
| Tool contract | Hợp đồng input/output của tool |
| State | Trạng thái |
| Orchestration | Điều phối |
| Guardrail | Cơ chế kiểm soát |
| Handoff | Bàn giao |
| Trace | Dấu vết execution |
| Idempotency | Lặp action an toàn |
| Rollback | Hoàn tác |
| Retry | Thử lại |
| Timeout | Giới hạn chờ |

---

# 37. Section recap

Agentic building blocks:

```text
Goal
Model
Instructions
Tools
Identity
Context
State
Orchestration
Guardrails
Human handoff
Memory
Evaluation
Observability
Failure handling
Cost/latency limits
```

Core rule:

> **Agent reliability comes from the whole system, not from the model alone.**

---

# 38. Self-check

1. Tool contract cần gồm gì?
2. State khác context thế nào?
3. Vì sao prompt không nên là security boundary duy nhất?
4. Khi nào dùng deterministic rule?
5. Agent eval cần đo gì ngoài final answer?
6. Tại sao idempotency quan trọng với write actions?
