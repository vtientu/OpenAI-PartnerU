# 03 — Where Agentic Workflows May Solve Customer Problems

> **Course:** OpenAI Foundational Knowledge  
> **Sub-course:** Agents & Agentic Workflows  
> **Section:** Where agentic workflows may solve customer problems

---

# 1. Section objective

Sau section này, bạn cần:

- nhận diện customer problems phù hợp với agentic workflows;
- hiểu signals cho thấy agentic approach có value;
- biết phân biệt agent opportunity với simple assistant/automation;
- biết use cases across support, IT, sales, finance, engineering, operations;
- biết qualification questions và success metrics.

---

# 2. Big picture

Agentic workflow phù hợp nhất khi process có:

```text
Multiple steps
+ ambiguity
+ changing context
+ tools/systems
+ decisions between steps
+ measurable completion
```

Nếu thiếu những yếu tố này, simpler pattern có thể tốt hơn.

---

# 3. Signal 1 — Too many manual handoffs

Workflow:

```text
Person A
→ Person B
→ System C
→ Person D
```

If handoffs mainly exist because humans must:

- read;
- interpret;
- copy;
- update;

an agent may coordinate parts of workflow.

Potential value:

- shorter cycle time;
- fewer handoffs.

---

# 4. Signal 2 — Repetitive multi-step knowledge work

Example:

```text
Read request
→ search info
→ compare policy
→ update system
→ send response
```

If repeated at high volume, agentic workflow may help.

---

# 5. Signal 3 — Humans act as “glue” between systems

Employee manually:

- reads email;
- copies CRM data;
- checks portal;
- updates ticket.

This indicates integration/coordination opportunity.

Agent + tools may reduce swivel-chair work.

---

# 6. Signal 4 — Workflow requires interpretation, not fixed rules

If process can be coded easily:

```text
if A then B
```

traditional automation may be best.

If process requires interpreting:

- text;
- documents;
- context;
- exceptions;

agent may add value.

---

# 7. Signal 5 — Task has clear completion criteria

Agent needs to know when done.

Good:

> “Close eligible support tickets.”

Less clear:

> “Improve customer happiness.”

The latter is business objective, not an executable agent goal.

---

# 8. Signal 6 — Tools/APIs already exist

Agent value increases when systems expose:

- APIs;
- search;
- databases;
- workflow actions.

Without integration capability, agent may only recommend rather than execute.

---

# 9. Signal 7 — Exceptions can be escalated

Agent doesn't need solve 100%.

Good design:

```text
Normal cases
→ agent

Complex/high-risk
→ human
```

This makes opportunities more feasible.

---

# 10. Use case — Customer support

Common agentic tasks:

- classify ticket;
- retrieve knowledge;
- check account;
- execute allowed action;
- draft/send response;
- close ticket;
- escalate exception.

Potential metrics:

- first-contact resolution;
- handling time;
- automation rate;
- escalation rate;
- CSAT;
- policy compliance.

---

# 11. Use case — IT helpdesk

Potential flow:

```text
Request
→ understand issue
→ inspect user/device
→ retrieve knowledge
→ execute approved remediation
→ verify
→ close/escalate
```

Good for repetitive issues.

High-risk admin actions require stronger approval.

---

# 12. Use case — Sales operations

Possible agentic workflow:

```text
New lead
→ research account
→ enrich CRM
→ prepare brief
→ draft outreach
→ schedule follow-up
```

Need careful rules around outbound actions and customer communication.

Metrics:

- prep time;
- admin time;
- follow-up speed;
- CRM completeness.

---

# 13. Use case — Customer success

Agent may:

- collect account context;
- summarize usage/support;
- prepare QBR;
- identify action items;
- create follow-ups.

Often starts as assistant before action automation.

---

# 14. Use case — Finance operations

Examples:

- invoice handling;
- expense review;
- reconciliation support;
- exception routing.

Flow:

```text
Document
→ extract
→ validate
→ lookup
→ classify
→ record/route
```

Deterministic financial calculations/policies should remain code/rules where appropriate.

---

# 15. Use case — Procurement

Potential workflow:

```text
Request
→ gather vendor info
→ check policy
→ compare options
→ prepare approval packet
→ route
```

Agent may coordinate information-heavy steps.

Final approval remains with authorized human where required.

---

# 16. Use case — HR operations

Lower-risk examples:

- employee knowledge;
- onboarding workflows;
- document collection;
- internal ticket routing.

High-impact employment decisions require special caution and may not be appropriate for autonomous agenting.

---

# 17. Use case — Engineering

Coding agents can:

- inspect issue;
- search code;
- edit;
- run tests;
- iterate;
- prepare change.

Other engineering agents:

- incident triage;
- documentation;
- dependency updates.

Metrics:

- lead time;
- issue resolution;
- review effort;
- defect rate.

---

# 18. Use case — Security operations

Potential support:

- triage alerts;
- gather context;
- enrich incident;
- prepare investigation;
- execute low-risk approved actions.

Security actions can have high consequence, so:

- strict permissions;
- human approval;
- audit

matter.

---

# 19. Use case — Operations / back office

Agentic workflows fit many operations tasks involving:

- documents;
- email;
- policies;
- system updates;
- exception handling.

Value often comes from reducing:

```text
manual coordination
```

rather than only writing text.

---

# 20. Where agentic workflows are weak

Poor fit if:

- task is single-step;
- rules are fully deterministic;
- no tools/API;
- no clear owner;
- no completion criteria;
- errors are unacceptable and no review;
- source data is unreliable;
- workflow volume too low to justify complexity.

---

# 21. Agent vs simple assistant decision

Ask:

```text
Does user only need information/draft?
→ assistant

Does system need to take one controlled action?
→ tool-enabled assistant

Does task require multiple adaptive steps?
→ agent candidate
```

---

# 22. Agent vs traditional automation

Ask:

```text
Is branching fixed and enumerable?
→ traditional workflow

Is branching context-dependent/unstructured?
→ agent may help
```

Use the least complex reliable pattern.

---

# 23. Agent opportunity framework — ACT

## A — Adaptive
Does workflow require interpretation/adaptation?

## C — Connected
Are required systems/tools accessible?

## T — Targeted
Is there a clear goal and completion criteria?

If one is missing, agent opportunity weakens.

---

# 24. Add VALUE

## V — Volume
Enough repetition?

## A — Avoided effort
Meaningful manual work reduced?

## L — Latency/cycle time
Can execution become faster?

## U — User/business impact
Does it move KPI?

## E — Exceptions manageable
Can risky cases escalate?

So:

```text
ACT + VALUE
```

is a useful discovery checklist.

---

# 25. Example — Refund workflow

Current:

```text
Agent reads ticket
→ opens CRM
→ checks order
→ checks policy
→ decides
→ issues refund
→ sends email
```

Candidate agent:

```text
Ticket
→ classify
→ order tool
→ policy retrieval
→ eligibility rule
→ refund tool
→ customer response
→ log
```

Human escalation:

- identity issue;
- high amount;
- policy conflict.

---

# 26. Define automation boundary

Don't ask:

> “Can agent automate support?”

Ask:

> “Which ticket categories can it handle end-to-end, under which conditions?”

Specific boundary makes evaluation possible.

---

# 27. Success metrics

Agent metrics should cover:

## Business
- cycle time;
- throughput;
- cost per case.

## Quality
- correct outcome;
- policy compliance.

## Autonomy
- automation rate;
- escalation rate.

## Reliability
- tool error;
- retries;
- failed tasks.

## User
- satisfaction;
- adoption.

---

# 28. Baseline first

Before agent:

Measure current workflow.

Example:

```text
Average case time: 12 min
Handoffs: 3
Error rate: 4%
Escalation: 20%
```

After pilot, compare.

Without baseline, value claim weak.

---

# 29. Pilot scope

Good pilot:

- narrow category;
- representative volume;
- clear tools;
- clear rules;
- measurable success;
- human oversight.

Avoid starting with:

> “Autonomously run the whole department.”

---

# 30. Readiness dimensions

Agent readiness requires:

```text
Workflow readiness
Data readiness
Tool/API readiness
Security readiness
Evaluation readiness
Operational readiness
Human handoff readiness
```

A strong use case may still be unready.

---

# 31. Partner discovery questions

1. What exact task/workflow?
2. How many steps?
3. What is manual today?
4. What causes delay?
5. Which systems?
6. Are APIs available?
7. Which decisions are rules vs judgment?
8. What error consequences?
9. Which cases can escalate?
10. What KPI moves?

---

# 32. Common mistakes

1. Choose agent because workflow is “complex”.
2. Ignore deterministic automation.
3. No baseline.
4. No narrow pilot scope.
5. No exception path.
6. No API/tool readiness.
7. Measure only automation rate.
8. Agentize high-impact decisions too early.

---

# 33. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Handoff | Bàn giao |
| Swivel-chair work | Công việc copy/chuyển giữa nhiều hệ thống |
| Exception | Trường hợp ngoại lệ |
| Automation boundary | Phạm vi tự động hóa |
| Baseline | Mốc hiện trạng |
| End-to-end | Từ đầu đến cuối |
| Adaptive | Có khả năng thích ứng |
| Workflow readiness | Mức sẵn sàng workflow |
| Automation rate | Tỷ lệ case tự động xử lý |
| Escalation rate | Tỷ lệ chuyển human |

---

# 34. Section recap

Good agent opportunities often have:

```text
multi-step
+ ambiguity
+ tools
+ repeated volume
+ clear goal
+ manageable exceptions
+ measurable value
```

Use:

```text
ACT
Adaptive
Connected
Targeted

+
VALUE
Volume
Avoided effort
Latency
User impact
Exceptions
```

Core rule:

> **Agentize a specific workflow, not an abstract business function.**

---

# 35. Self-check

1. Những signal nào cho thấy agentic workflow phù hợp?
2. Khi nào traditional automation tốt hơn agent?
3. ACT framework gồm gì?
4. VALUE framework gồm gì?
5. Hãy đánh giá một IT helpdesk use case theo ACT + VALUE.
6. Tại sao baseline quan trọng?
