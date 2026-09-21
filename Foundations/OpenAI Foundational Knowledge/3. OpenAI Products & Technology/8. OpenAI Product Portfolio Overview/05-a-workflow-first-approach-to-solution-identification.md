# 05 — A Workflow-First Approach to Solution Identification

> **Course:** OpenAI Foundational Knowledge  
> **Sub-course:** OpenAI Product Portfolio Overview  
> **Section:** A Workflow-First Approach to Solution Identification

---

# 1. Section objective

Sau section này, bạn cần:

- dùng workflow làm unit of analysis;
- đi từ customer problem → workflow → capabilities → technology path;
- tránh product-led selling;
- biết xác định user, steps, data, tools, actions, risks và metrics;
- tạo solution recommendation có logic rõ ràng.

---

# 2. Big picture

Weak solutioning:

```text
Product
→ find use case
```

Strong solutioning:

```text
Business problem
↓
Workflow
↓
Pain / bottleneck
↓
AI opportunity
↓
Required capabilities
↓
Portfolio path
↓
Evaluation
↓
Next step
```

---

# 3. Why workflow-first?

Business outcomes happen in workflows.

Example:

> “Improve sales.”

Too broad.

Workflow:

```text
Research account
→ prepare meeting
→ conduct call
→ summarize
→ follow up
→ update CRM
```

Now AI opportunities become visible.

---

# 4. Step 1 — Define business outcome

Ask:

- What business metric matters?
- What is changing?
- Why now?

Examples:

- reduce support cost;
- shorten close cycle;
- increase developer throughput;
- improve knowledge access.

Outcome gives direction.

---

# 5. Step 2 — Identify user

Who performs the work?

- employee;
- developer;
- customer;
- operations analyst;
- support agent;
- manager.

User determines product surface.

---

# 6. Step 3 — Map current workflow

Write steps:

```text
1. Receive request
2. Find information
3. Analyze
4. Decide
5. Update system
6. Communicate
```

Do not jump to AI yet.

Understand current work.

---

# 7. Step 4 — Find pain

Look for:

- repetitive effort;
- information overload;
- skill bottleneck;
- manual handoff;
- slow decision;
- copy/paste;
- inconsistent quality;
- difficult knowledge access.

Pain must connect to value.

---

# 8. Step 5 — Identify AI-suitable steps

For each step ask:

```text
Language-heavy?
Information-heavy?
Ambiguous?
Pattern recognition?
Content creation?
Analysis?
Tool coordination?
```

Then identify AI role.

---

# 9. Step 6 — Classify AI role

Possible role:

```text
Assist
Generate
Transform
Extract
Classify
Retrieve
Analyze
Recommend
Act
Coordinate
```

This is capability/application language.

---

# 10. Step 7 — Determine knowledge needs

Ask:

- general knowledge?
- company documents?
- live account data?
- current public web?
- user memory/state?

Map:

```text
Company docs
→ retrieval

Live structured data
→ tool/API

Public current data
→ web/search

User/workflow state
→ app state/memory
```

---

# 11. Step 8 — Determine action needs

### No action

Answer/draft.

### Single action

Tool-enabled assistant.

### Multiple adaptive actions

Agent candidate.

Do not add agent if answer is enough.

---

# 12. Step 9 — Determine user surface

Where should AI live?

### ChatGPT
User already works in general AI workspace.

### Codex
Developer workflow.

### Customer app
Embedded custom UX.

### Existing SaaS
Native/plugin/embedded path.

### Background
No user UI required.

Surface follows workflow.

---

# 13. Step 10 — Choose configure vs build

Ask:

```text
Can standard product capability solve most requirement?
```

If yes:
→ configure-first.

If no:
→ custom build.

Custom build is justified by:

- proprietary workflow;
- external customer UX;
- deep integration;
- custom controls.

---

# 14. Step 11 — Choose capability stack

Example:

```text
ChatGPT
+
plugin
+
CRM
```

or:

```text
Custom app
+
API
+
retrieval
+
tools
+
agent
```

Each component should have a job.

---

# 15. Step 12 — Define controls

Ask:

- identity?
- permissions?
- source of truth?
- human approval?
- escalation?
- sensitive data?
- audit?

Controls are part of solution, not postscript.

---

# 16. Step 13 — Define evaluation

Before pilot, define:

- task quality;
- error types;
- business metric;
- baseline;
- success threshold.

Example:

```text
Support:
baseline handling time
correct resolution rate
escalation rate
CSAT
```

---

# 17. Step 14 — Choose next step

Possible next step:

- product pilot;
- API prototype;
- integration workshop;
- data readiness assessment;
- eval design;
- security review.

Solution identification should end in actionable progression.

---

# 18. Workflow-first framework — FLOW

## F — Function / user
Who owns the work?

## L — Lifecycle / workflow
What steps happen?

## O — Opportunity
Where is friction/value?

## W — Way forward
Which technology path + next step?

This is a quick mental framework.

---

# 19. Add PATH for technology selection

## P — Product surface
Where should AI live?

## A — Access
What data/tools?

## T — Task complexity
Single-step or multi-step?

## H — Human role
Who reviews/approves?

Combined:

```text
FLOW → PATH
```

---

# 20. Example — HR policy questions

### Business problem
HR overloaded with repetitive policy questions.

### Workflow
Employee asks → HR searches → responds.

### Opportunity
Knowledge access.

### Capability
Retrieval + grounded generation.

### Surface
Could be ChatGPT workspace or internal app.

### Data
Approved HR docs.

### Actions
None initially.

### Controls
Permissions + citations + escalation.

### Metric
Ticket reduction + answer quality.

Now product selection is evidence-based.

---

# 21. Example — Sales research

### Workflow

```text
Rep chooses account
→ researches public/company context
→ creates brief
→ plans meeting
```

Potential path:

```text
ChatGPT/Work + connected business context
```

or custom if integration/output is proprietary.

No need for a fully autonomous agent at first.

---

# 22. Example — Support resolution

### Workflow

```text
Ticket
→ classify
→ retrieve policy
→ read account
→ decide
→ act
→ respond
```

Capabilities:

- classification;
- RAG;
- account tool;
- action tool;
- agentic coordination.

Surface:

- support platform/custom backend.

This is stronger agent candidate.

---

# 23. Example — SaaS AI feature

### User
External customer.

### Workflow
Uses company's product.

Therefore:

```text
ChatGPT workspace
```

is probably not correct primary surface.

Route:

```text
Customer app
→ API
→ required capability stack
```

User surface alone can determine major technology choice.

---

# 24. Example — Engineering

### User
Developer.

### Workflow
Issue → code → test → review.

Start path:

```text
Codex / coding-oriented experience
```

Only custom-build if company needs proprietary workflow/integration not covered.

---

# 25. Product-led selling anti-pattern

Bad:

> “Let's show you agents.”

Good:

> “You described a six-step support workflow with three manual system handoffs. Let's map where AI assistance vs action adds value.”

Product is introduced only after need is clear.

---

# 26. Avoid premature architecture

Discovery stage does not need exact model IDs immediately.

First define:

```text
capability
data
tool
action
risk
metric
```

Then architecture.

This prevents stale or over-specific recommendation.

---

# 27. Avoid capability overreach

Model can:

> reason over support ticket.

Does not mean system can:

> safely refund customer.

Refund requires:

- account access;
- policy;
- permission;
- business rule;
- audit;
- tool.

Workflow-first makes these dependencies visible.

---

# 28. Evidence ladder

Recommend with increasing evidence:

```text
Hypothesis
↓
Prototype
↓
Offline eval
↓
Pilot
↓
Production metric
```

Don't convert capability demo directly into ROI claim.

---

# 29. Recommendation structure

A partner recommendation can follow:

```text
1. Current workflow
2. Pain / business impact
3. AI-suitable steps
4. Proposed product/technology path
5. Data/tool dependencies
6. Trust/controls
7. Success metrics
8. Next validation step
```

This is consultative and defensible.

---

# 30. Portfolio verification checklist

Before naming exact current feature/model:

- verify official OpenAI docs;
- check product/plan availability;
- check region;
- check integration support;
- check pricing if commitment depends on it;
- check security/data controls;
- record verification date.

Capability story can remain stable.

---

# 31. Common mistakes

1. Start with product demo.
2. Skip workflow mapping.
3. Use department name as use case.
4. Select agent before action requirements.
5. Select RAG before knowledge requirements.
6. Ignore user surface.
7. No success metric.
8. No next validation step.
9. Commit exact current features from memory.

---

# 32. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Workflow-first | Bắt đầu từ workflow |
| Product-led selling | Bán theo product trước problem |
| User surface | Nơi user tương tác |
| Capability stack | Tập capability cần dùng |
| Dependency | Thành phần phụ thuộc |
| Success threshold | Ngưỡng thành công |
| Verification | Xác minh |
| Recommendation | Đề xuất solution |
| Pilot | Thử nghiệm giới hạn |
| Evidence ladder | Các mức bằng chứng |

---

# 33. Section recap

Use this sequence:

```text
Business outcome
↓
User
↓
Workflow
↓
Pain
↓
AI-suitable steps
↓
Capability
↓
Knowledge/tools
↓
Action/autonomy
↓
Product/technology path
↓
Controls
↓
Evals
↓
Next step
```

Framework:

```text
FLOW
Function/user
Lifecycle/workflow
Opportunity
Way forward

→

PATH
Product surface
Access
Task complexity
Human role
```

Core rule:

> **Never let the portfolio choose the workflow. Let the workflow choose the portfolio path.**

---

# 34. Self-check

1. Tại sao workflow-first tốt hơn product-first?
2. User surface ảnh hưởng solution choice như thế nào?
3. Khi nào RAG xuất hiện trong flow?
4. Khi nào agent xuất hiện?
5. FLOW → PATH framework gồm gì?
6. Hãy route một sales workflow thành product/technology path.
