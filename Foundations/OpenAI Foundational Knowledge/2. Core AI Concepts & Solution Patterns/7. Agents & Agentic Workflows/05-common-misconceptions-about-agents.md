# 05 — Common Misconceptions About Agents

> **Course:** OpenAI Foundational Knowledge  
> **Sub-course:** Agents & Agentic Workflows  
> **Section:** Common misconceptions about agents

---

# 1. Section objective

Sau section này, bạn cần:

- nhận diện các hiểu lầm phổ biến về agents;
- sửa cách nói quá đơn giản hoặc overhyped;
- biết phân biệt agent với model, automation, RAG, chatbot;
- tránh design anti-patterns;
- giao tiếp về agentic AI chính xác hơn với customer.

---

# 2. Big picture

Agents thường bị hype vì chúng kết hợp nhiều capability:

```text
reasoning
+ tools
+ autonomy
+ workflow execution
```

Nhưng cần nhớ:

> **Agent là system design pattern, không phải magic intelligence layer.**

---

# 3. Misconception 1 — “Agent is a model”

Sai.

Model:

```text
input → output
```

Agent:

```text
goal
→ model
→ tools
→ state
→ loop
→ outcome
```

Agent uses model.

Agent is system.

---

# 4. Misconception 2 — “Agent is just a chatbot”

Sai.

Chatbot may only answer.

Agent can:

- use tools;
- update systems;
- perform multi-step work;
- adapt based on tool results.

A chatbot can be agentic, but not all chatbots are agents.

---

# 5. Misconception 3 — “Agent means fully autonomous”

Sai.

Autonomy is a spectrum.

```text
suggest
→ draft
→ prepare action
→ execute low-risk action
→ broader autonomy
```

Human approval can be intentionally designed.

---

# 6. Misconception 4 — “More autonomy is better”

Wrong.

More autonomy increases:

- risk;
- permission requirements;
- eval complexity;
- monitoring burden.

The right autonomy level maximizes:

```text
value
while maintaining
acceptable risk
```

---

# 7. Misconception 5 — “Agents replace workflows”

Usually agents become part of workflows.

Existing workflow still includes:

- humans;
- systems;
- policies;
- approval;
- reporting.

Agent should integrate, not exist in vacuum.

---

# 8. Misconception 6 — “Agent can access company systems by itself”

No.

Agent needs tools/integrations.

```text
Model capability
≠
system access
```

To access CRM:

- API/tool;
- credentials;
- permissions;
- business logic

are needed.

---

# 9. Misconception 7 — “If model is smart enough, guardrails aren't needed”

Wrong.

Even strong models need:

- permissions;
- validation;
- policy checks;
- limits;
- monitoring.

System safety cannot be delegated entirely to model intelligence.

---

# 10. Misconception 8 — “Prompt is enough for security”

Wrong.

Prompt:

> “Do not issue refunds over $500.”

should be backed by code:

```text
if amount > 500:
    require_approval()
```

Security/control must be enforced technically.

---

# 11. Misconception 9 — “Agent can remember everything”

Not automatically.

Memory requires:

- storage;
- retrieval;
- retention policy;
- access control.

Context window is not infinite long-term memory.

---

# 12. Misconception 10 — “Agent learns from every interaction”

Not necessarily.

Agent may update:

- state;
- memory;
- context.

That is different from model weight training.

```text
Stateful behavior
≠
model learning
```

---

# 13. Misconception 11 — “Agent = RAG”

No.

RAG gives knowledge.

Agent manages multi-step goal execution.

Agent may use RAG as one tool.

```text
Agent
├─ retrieval
├─ CRM
├─ email
└─ payment tool
```

---

# 14. Misconception 12 — “Agent = workflow automation”

Not always.

Traditional workflow:

```text
A → B → C
```

Agent adds adaptive decision-making.

If process is deterministic, an agent may be unnecessary.

---

# 15. Misconception 13 — “Every business process is an agent opportunity”

No.

Poor candidates:

- trivial single-step tasks;
- low volume;
- no measurable value;
- no tool access;
- high consequence with no controls;
- unclear goal.

Use agent only where value justifies complexity.

---

# 16. Misconception 14 — “Agents eliminate human review”

No.

Human review can be part of production design.

Patterns:

```text
Agent prepares
→ human approves
```

or:

```text
Agent handles standard cases
→ human exceptions
```

---

# 17. Misconception 15 — “Agent accuracy = model accuracy”

Wrong.

Agent success depends on:

```text
model
+ retrieval
+ tool reliability
+ state
+ orchestration
+ policy
```

System-level evaluation is required.

---

# 18. Misconception 16 — “If final answer looks right, agent worked correctly”

Not necessarily.

Maybe agent:

- called wrong tool;
- accessed unauthorized data;
- repeated action;
- violated policy.

Need trace-level evaluation.

---

# 19. Misconception 17 — “Agents are deterministic”

No.

Model-driven decisions are probabilistic.

Same context may lead to variation.

Therefore use:

- validation;
- deterministic rules;
- evals;
- bounded actions.

---

# 20. Misconception 18 — “Agents should plan everything dynamically”

Not always.

Better pattern:

```text
Deterministic workflow skeleton
+
agent reasoning at ambiguous steps
```

Hybrid design can be more reliable.

---

# 21. Misconception 19 — “Multi-agent is automatically better”

No.

More agents add:

- communication overhead;
- latency;
- cost;
- debugging complexity.

Use multiple agents when clear specialization/benefit exists.

---

# 22. Misconception 20 — “Agent failure can be solved only by better model”

Not always.

Root cause may be:

- wrong tool;
- bad data;
- bad permission;
- missing state;
- weak instruction;
- poor orchestration.

System debugging matters.

---

# 23. Misconception 21 — “Agents reduce all operational cost”

Agent may reduce manual effort but add:

- model usage;
- tool calls;
- engineering;
- monitoring;
- review.

Need total cost analysis.

---

# 24. Misconception 22 — “Agent demo proves production readiness”

A demo may prove:

> concept works once.

Production needs:

- evals;
- security;
- scale;
- reliability;
- audit;
- operations.

Demo ≠ production.

---

# 25. Misconception 23 — “We need an agent because competitors have one”

Technology choice should follow workflow.

Partner question:

> “What problem are we solving?”

Not:

> “How do we get an agent?”

---

# 26. Misconception 24 — “Agent success = automation rate”

High automation rate can be bad if error rate also high.

Need multiple metrics:

```text
automation
quality
safety
business outcome
customer/user experience
```

---

# 27. Misconception 25 — “Agents remove accountability”

No.

Organization still owns:

- policy;
- risk acceptance;
- tool permission;
- incident response;
- business outcome.

AI autonomy does not remove human accountability.

---

# 28. A better mental model

Instead of:

> “Agent = autonomous digital employee.”

Use:

> **“Agent = bounded AI system that can reason and act across multiple steps toward a defined goal.”**

“Bounded” is important.

---

# 29. Misconception correction table

| Misconception | Better understanding |
|---|---|
| Agent = model | Agent uses model inside system |
| Agent = chatbot | Chat is only one interface |
| Agent = autonomy | Autonomy is configurable |
| Agent = RAG | RAG may be one component |
| Agent = automation | Agent adds adaptive reasoning |
| Smart model = safe agent | System controls still needed |
| Prompt = permission | Real auth/authorization required |
| More agents = better | Complexity must be justified |

---

# 30. Communication pattern

Customer:

> “We want autonomous agents.”

Better partner response:

```text
What workflow?
↓
What goal?
↓
What systems?
↓
Which decisions are dynamic?
↓
What actions are safe?
↓
Where should humans remain?
↓
What metrics?
```

This converts hype into solution discovery.

---

# 31. Anti-hype language

Avoid:

> “Agents can run the business.”

Prefer:

> “Agents can automate or coordinate scoped multi-step workflows when tools, permissions, controls and evaluation are in place.”

Avoid:

> “No humans required.”

Prefer:

> “The appropriate human role depends on risk and evidence.”

---

# 32. Developer anti-pattern

Bad:

```text
while true:
    ask model what to do
```

without:

- max steps;
- tool validation;
- timeouts;
- state checks;
- completion criteria.

This can create runaway loops.

---

# 33. Bounded-agent design

A bounded agent has:

```text
clear goal
allowed tools
permission limits
step limit
time limit
budget
completion criteria
escalation path
```

This is much safer and easier to evaluate.

---

# 34. Agent trust

Trust is not:

> “The agent seemed good in demo.”

Trust comes from:

```text
Evidence
+ controls
+ transparency
+ observability
+ ownership
```

Same principle from Responsible AI course.

---

# 35. Common partner mistakes

1. Oversell autonomy.
2. Use “agent” as marketing label.
3. Promise end-to-end before tool readiness.
4. Ignore human role.
5. Skip baseline/evals.
6. Quote demo success as ROI proof.
7. Ignore operational cost.
8. Confuse model capability with business authority.

---

# 36. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Misconception | Hiểu lầm |
| Bounded agent | Agent có phạm vi/giới hạn rõ |
| Runaway loop | Vòng lặp kéo dài ngoài ý muốn |
| Business authority | Quyền thực hiện hành động nghiệp vụ |
| Trace-level evaluation | Đánh giá từng bước execution |
| System-level evaluation | Đánh giá toàn hệ thống |
| Accountability | Trách nhiệm giải trình |
| Automation rate | Tỷ lệ tự động hóa |
| Human oversight | Giám sát của con người |
| Deterministic skeleton | Khung workflow cố định |

---

# 37. Section recap

Never assume:

```text
Agent = model
Agent = chatbot
Agent = RAG
Agent = full autonomy
Agent = no humans
Agent = deterministic
Agent = production-ready demo
```

Better definition:

> **Agent = bounded AI system that uses reasoning, tools and state to complete a defined multi-step goal under explicit controls.**

Core rule:

> **Use the least autonomy and complexity needed to achieve the business outcome reliably.**

---

# 38. Self-check

1. Tại sao agent không phải model?
2. Tại sao prompt không đủ để enforce permission?
3. Agent memory khác model learning thế nào?
4. Tại sao multi-agent không mặc nhiên tốt hơn?
5. Bounded agent cần những giới hạn nào?
6. Hãy sửa câu “We want a fully autonomous agent” thành discovery questions.
