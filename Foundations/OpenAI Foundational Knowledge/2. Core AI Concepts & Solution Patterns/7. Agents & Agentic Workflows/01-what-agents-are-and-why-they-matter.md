# 01 — What Agents Are and Why They Matter

> **Course:** OpenAI Foundational Knowledge  
> **Course group:** Core AI Concepts & Solution Patterns  
> **Sub-course:** Agents & Agentic Workflows  
> **Section:** What agents are and why they matter
>
> **Source note:** Đây là study guide tổng hợp dựa trên tên section PartnerU và các khái niệm agentic AI phổ biến. Không phải transcript nguyên văn của PartnerU.

---

# 1. Section objective

Sau section này, bạn cần có thể:

- giải thích agent bằng ngôn ngữ đơn giản;
- phân biệt agent với chatbot, model và automation;
- hiểu vì sao agents quan trọng với business workflows;
- hiểu “agentic” là spectrum chứ không phải binary;
- biết khi nào agent tạo thêm value và khi nào chỉ tạo complexity.

---

# 2. Big picture

Một chatbot đơn giản:

```text
User
→ Model
→ Answer
```

Một agentic workflow:

```text
Goal
↓
Reason / plan
↓
Choose action
↓
Use tool
↓
Observe result
↓
Continue / adapt
↓
Complete or escalate
```

Điểm cốt lõi:

> **Agent không chỉ tạo câu trả lời; nó có thể quản lý nhiều bước để tiến gần tới một goal.**

---

# 3. Agent là gì?

Một definition hữu ích:

> **Agent là một AI-enabled system có thể nhận goal, sử dụng model để quyết định next step, dùng tools hoặc systems để thực hiện work, quan sát result, và tiếp tục cho tới khi complete hoặc handoff.**

Agent thường gồm:

- model;
- instructions;
- tools;
- state/context;
- loop/orchestration;
- policies/guardrails;
- evaluation;
- human escalation.

Do đó:

```text
Agent ≠ model
```

Model là intelligence component.

Agent là system.

---

# 4. Agent vs chatbot

## Chatbot

```text
Question
→ Answer
```

Primary value:

- information;
- explanation;
- drafting.

## Agent

```text
Goal
→ multiple steps
→ tools/actions
→ result
```

Primary value:

- completion;
- workflow execution;
- coordination.

Example:

### Chatbot
“Here is how to reset your password.”

### Agent
“Verify user → trigger reset workflow → confirm completion.”

---

# 5. Agent vs automation

Traditional automation:

```text
IF X
THEN Y
```

or:

```text
A → B → C
```

Agentic workflow:

```text
Goal
↓
Interpret context
↓
Choose among possible next steps
↓
Adapt based on result
```

Traditional automation is best when process is deterministic.

Agentic system adds value when workflow contains:

- ambiguity;
- unstructured input;
- dynamic branching;
- changing context;
- multiple tools;
- decisions between steps.

---

# 6. Agent vs RPA

RPA often follows fixed UI/process steps.

Agent may reason over changing context.

Simplified:

```text
RPA:
repeat known procedure

Agent:
decide which procedure/step is appropriate
```

They can also be combined.

---

# 7. Why agents matter

AI assistants improve **knowledge work**.

Agents potentially improve **workflow execution**.

Progression:

```text
Answer
↓
Assist
↓
Recommend
↓
Prepare action
↓
Execute scoped action
↓
Coordinate multi-step workflow
```

This expands potential business value.

---

# 8. From information to action

Traditional GenAI value:

```text
Generate information
```

Agentic value:

```text
Use information
+
take action
```

Example:

### Assistant
Summarizes a customer complaint.

### Agent
- reads complaint;
- checks customer account;
- checks refund policy;
- determines allowed next step;
- prepares or executes permitted action;
- logs result;
- escalates exception.

---

# 9. Why this can transform workflows

Many enterprise processes contain:

```text
Read
→ Decide
→ Find data
→ Update system
→ Communicate
→ Repeat
```

Foundation models can help with:

- reading;
- interpretation;
- planning;
- natural language.

Tools/APIs enable:

- retrieval;
- database access;
- transactions;
- notifications.

Combined, they can automate parts of end-to-end workflows.

---

# 10. Agents operate in a loop

Core agent pattern:

```text
1. Observe
2. Reason
3. Act
4. Observe result
5. Continue
```

This loop matters because real work often depends on results of previous actions.

Example:

```text
Check order
↓
Order delayed?
   ├─ no → explain status
   └─ yes → check compensation policy
           ↓
           eligible?
           ├─ yes → issue credit
           └─ no → escalate
```

---

# 11. Goal-oriented behavior

Traditional prompt:

> “Summarize this ticket.”

Agent goal:

> “Resolve this eligible support case according to policy.”

The second requires:

- intermediate decisions;
- tool use;
- policy checks;
- completion criteria.

---

# 12. Agents need boundaries

Goal-oriented does not mean unlimited freedom.

A good agent should have:

- allowed scope;
- allowed tools;
- permission limits;
- stop conditions;
- escalation rules;
- auditability.

Mental model:

```text
Capability
+ boundaries
=
deployable autonomy
```

---

# 13. Autonomy is a spectrum

Study model:

```text
Level 0 — AI suggests
Level 1 — AI drafts
Level 2 — AI proposes action
Level 3 — AI acts on low-risk cases
Level 4 — AI manages broader workflow
```

Higher autonomy does not automatically mean better solution.

Best level depends on:

- risk;
- trust;
- evidence;
- business value;
- readiness.

---

# 14. Agents and human work

Agents should not be framed only as:

> “replace people.”

Better framing:

```text
Agent handles repeatable/low-risk work
↓
Human handles exceptions/judgment
```

This can shift human effort toward:

- complex cases;
- relationship work;
- judgment;
- strategy;
- oversight.

---

# 15. Why agents matter for partners

Partner role becomes broader.

Instead of asking:

> “Can AI answer this?”

Ask:

> “Which steps of this workflow can AI observe, reason about, and safely execute?”

This requires understanding:

- business process;
- systems;
- permissions;
- risk;
- ownership;
- metrics.

Agents are therefore highly connected to consultative discovery.

---

# 16. Agentic value pattern

A useful formula:

```text
Agentic value
=
Manual coordination reduced
+ faster cycle time
+ fewer handoffs
+ higher capacity
+ more consistent execution
```

But only if:

- agent is reliable;
- integrations work;
- users trust workflow;
- controls are strong.

---

# 17. Agents can amplify both value and risk

When AI has no action authority:

```text
wrong answer
→ user may catch it
```

When AI can act:

```text
wrong reasoning
→ wrong action
→ real business impact
```

Therefore:

> More agency means stronger need for evaluation, permissions, monitoring, and fallback.

---

# 18. Example — Support agent

Goal:

> Resolve common account issues.

Possible flow:

```text
Ticket
↓
Identify intent
↓
Get account
↓
Retrieve policy
↓
Choose permitted action
↓
Execute / draft
↓
Confirm
↓
Log
↓
Escalate exception
```

Metrics:

- resolution rate;
- handling time;
- escalation rate;
- policy compliance;
- error rate.

---

# 19. Example — IT helpdesk agent

Goal:

> Resolve common internal IT issues.

Possible actions:

- retrieve user/device info;
- search internal docs;
- run approved diagnostic;
- trigger safe remediation;
- create/escalate ticket.

Agent value comes from connecting language understanding to existing IT systems.

---

# 20. Example — Coding agent

Goal:

> Implement scoped code change.

Possible loop:

```text
Read issue
→ inspect repo
→ modify code
→ run tests
→ inspect failures
→ revise
→ handoff for review
```

This is more agentic than autocomplete because system works across multiple steps.

---

# 21. When agents are not needed

Avoid agent when:

- task is single-step;
- output is simple draft;
- deterministic workflow is sufficient;
- tool access creates unnecessary risk;
- system cannot be evaluated;
- data/integration readiness is low.

Example:

```text
Translate this paragraph
```

does not need an agent.

---

# 22. Complexity cost

Agentic architecture adds:

- more tool calls;
- more latency;
- more failure points;
- more logging;
- more security concerns;
- more eval complexity.

Therefore:

> Agentic should be justified by workflow value, not novelty.

---

# 23. Developer mental model

Traditional state machine:

```text
state A
→ deterministic transition
→ state B
```

Agentic system:

```text
state/context
→ model decides next action
→ tool
→ new state
→ model decides again
```

This is like adding a probabilistic decision-maker inside orchestration.

That makes it powerful—and harder to test.

---

# 24. Partner discovery questions

1. What goal must be completed?
2. How many steps?
3. Are steps fixed or dynamic?
4. Which steps require judgment?
5. Which tools/systems are needed?
6. What actions can be safely automated?
7. What remains human-owned?
8. What is the cost of wrong action?
9. How do we know task is complete?
10. What should trigger escalation?

---

# 25. Common mistakes

1. Agent = chatbot.
2. Agent = model.
3. Agent = fully autonomous AI.
4. More autonomy = better.
5. Every workflow should become agentic.
6. Tool access automatically creates value.
7. Ignore completion criteria.
8. Ignore human handoff.
9. Ignore deterministic alternatives.

---

# 26. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Agent | Hệ thống AI hướng tới goal qua nhiều bước |
| Agentic | Có tính chủ động/thực thi theo goal |
| Goal | Mục tiêu |
| Tool | API/công cụ agent có thể dùng |
| Observation | Kết quả agent nhận sau action |
| Action | Hành động |
| Control loop | Vòng observe → reason → act |
| Autonomy | Mức tự chủ |
| Handoff | Bàn giao |
| Escalation | Chuyển case |
| Completion criteria | Tiêu chí hoàn thành |
| State | Trạng thái workflow |
| Agentic workflow | Workflow có AI quyết định/thực hiện nhiều bước |

---

# 27. Section recap

Core distinction:

```text
Chatbot
→ answer

Automation
→ fixed steps

Agent
→ goal + reasoning + tools + adaptive steps
```

Remember:

1. Agent is a system, not a model.
2. Agentic value comes from workflow execution.
3. Autonomy is a spectrum.
4. More agency increases control/eval requirements.
5. Use agents where ambiguity + multi-step work justify complexity.
6. Keep deterministic workflows deterministic when possible.

---

# 28. Self-check

1. Agent khác chatbot thế nào?
2. Agent khác traditional automation thế nào?
3. Tại sao agent cần control loop?
4. Autonomy spectrum có ý nghĩa gì?
5. Khi nào không nên dùng agent?
6. Hãy mô tả một support agent theo observe → reason → act.
