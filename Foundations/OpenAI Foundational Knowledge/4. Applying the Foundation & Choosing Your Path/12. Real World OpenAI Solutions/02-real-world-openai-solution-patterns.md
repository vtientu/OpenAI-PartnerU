# 02 — Real-World OpenAI Solution Patterns

> **Course:** OpenAI Foundational Knowledge  
> **Course:** Real World OpenAI Solutions  
> **Section:** Real-world OpenAI solution patterns
>
> **Important taxonomy note:** OpenAI's current public use-case guide officially describes **six use-case primitives**: Content creation, Research, Coding, Data analysis, Ideation & strategy, and Automation.  
> The solution patterns below are an **optimized study synthesis** for architecture/partner reasoning. They are not presented as an official OpenAI taxonomy.

---

# 1. Section objective

Sau section này, bạn cần:

- nhận diện recurring OpenAI solution patterns;
- hiểu user/workflow/data/tool shape của từng pattern;
- biết pattern nào dùng ChatGPT, Codex, API, retrieval, tools hoặc agents;
- hiểu pattern composition;
- biết success metrics và controls phổ biến.

---

# 2. Big picture

Real-world AI solutions often repeat a small number of shapes.

Study map:

```text
1. Knowledge-work copilot
2. Knowledge / RAG assistant
3. Research & synthesis
4. Document intelligence
5. Data & analytics assistant
6. Content workflow
7. Coding / software agent
8. Customer support
9. Tool-enabled workflow automation
10. Agentic operations
11. Realtime / voice assistant
12. Embedded AI product
```

These patterns can overlap.

---

# 3. Pattern 1 — Knowledge-work copilot

User:

- employee;
- analyst;
- manager;
- sales rep.

Tasks:

- write;
- summarize;
- compare;
- plan;
- brainstorm.

Typical technology:

```text
ChatGPT
or
ChatGPT Work
```

May add:

- Projects;
- files;
- plugins;
- business context.

---

# 4. Knowledge-work value

Potential value:

```text
less blank-page time
faster synthesis
more output capacity
better access to skills
```

Metrics:

- time saved;
- task completion;
- quality;
- adoption.

Controls:

- data policy;
- human verification.

---

# 5. Pattern 2 — Knowledge / RAG assistant

User asks about:

- company policy;
- product docs;
- technical knowledge;
- SOP.

Architecture:

```text
Question
↓
identity
↓
retrieve approved source
↓
model
↓
answer + citation
↓
escalate if no evidence
```

Technology:

- ChatGPT connected knowledge;
- custom API RAG;
- file search;
- MCP/plugin connection.

---

# 6. Knowledge-assistant success

Evaluate:

- retrieval success;
- groundedness;
- citation support;
- permission correctness;
- no-answer behavior.

Business metrics:

- search time;
- ticket reduction;
- onboarding speed.

---

# 7. Pattern 3 — Research & synthesis

User wants:

- current market research;
- competitive analysis;
- literature/background synthesis.

Architecture:

```text
Question
↓
research/search
↓
multiple sources
↓
analysis
↓
structured report
```

Technology may include:

- ChatGPT research tools;
- Work;
- API + web/search tools.

Controls:

- source quality;
- date;
- citations;
- fact vs inference.

---

# 8. Pattern 4 — Document intelligence

Input:

- PDF;
- email;
- form;
- image;
- contract;
- invoice.

Tasks:

```text
extract
classify
summarize
compare
validate
```

Architecture:

```text
Document
↓
multimodal/model
↓
structured output
↓
validation
↓
business system
```

---

# 9. Document-intelligence controls

Useful controls:

- schema;
- required fields;
- null/unknown handling;
- source evidence;
- deterministic validation;
- exception queue.

Metrics:

- field accuracy;
- manual review rate;
- processing time.

---

# 10. Pattern 5 — Data & analytics assistant

User asks business question.

Architecture:

```text
Question
↓
governed data/tool
↓
query/code
↓
analysis
↓
table/chart
↓
narrative
```

Technology:

- ChatGPT Work/data tools;
- plugin/data connection;
- custom API analytics app.

---

# 11. Analytics controls

Need:

- metric definitions;
- source data;
- query permissions;
- formula validation;
- reproducibility.

AI should not invent missing business numbers.

Metrics:

- time-to-insight;
- analyst capacity;
- decision speed.

---

# 12. Pattern 6 — Content workflow

Tasks:

- draft;
- edit;
- localize;
- create variants;
- transform.

Simple:

```text
brief
→ ChatGPT
→ draft
→ human review
```

Scaled:

```text
content data
→ API
→ generation
→ brand/policy check
→ CMS
```

---

# 13. Content value

Potential outcomes:

- faster campaign creation;
- localization at scale;
- more variants;
- reduced manual drafting.

Controls:

- factuality;
- brand;
- review;
- copyright/policy checks as applicable.

---

# 14. Pattern 7 — Coding / software agent

Technology:

```text
Codex
```

Workflow:

```text
Issue
→ inspect repo
→ plan
→ code
→ test
→ iterate
→ review-ready change
```

Metrics:

- cycle time;
- PR throughput;
- review effort;
- defect rate.

Human:

> controls what ships.

---

# 15. Pattern 8 — Customer support

Stages:

### Assist

```text
ticket
→ suggested answer
```

### Ground

```text
ticket
→ policy retrieval
→ answer
```

### Connect

```text
+ customer account tool
```

### Act

```text
+ approved business action
```

### Agentic

```text
multi-step resolution
```

---

# 16. Support solution stack

```text
User/ticket
↓
intent classification
↓
policy retrieval
↓
customer/account tool
↓
reasoning
↓
response/action
↓
escalation
```

Metrics:

- resolution;
- handling time;
- escalation;
- CSAT;
- policy compliance.

---

# 17. Pattern 9 — Tool-enabled workflow automation

Input/event:

```text
New ticket / email / record
```

AI:

- interprets;
- extracts;
- classifies.

Code/workflow:

- applies deterministic rules;
- calls API.

Architecture:

```text
Event
↓
AI interpretation
↓
structured output
↓
rules
↓
tool
```

No full agent required.

---

# 18. Pattern 10 — Agentic operations

Use when task needs:

- multiple steps;
- dynamic decisions;
- several tools;
- exception handling.

Architecture:

```text
Goal
↓
agent
├─ retrieval
├─ tools
├─ state
├─ rules
└─ human escalation
↓
completion
```

---

# 19. Agentic-operation fit

Good:

- support resolution;
- IT helpdesk;
- operational coordination;
- research workflows.

Poor:

- deterministic single-step calculation;
- simple rewrite.

Agent complexity must be justified.

---

# 20. Pattern 11 — Realtime / voice assistant

Architecture:

```text
Speech
↔
realtime AI
↔
tools/context
```

Use cases:

- customer service;
- field support;
- hands-free interfaces.

Key requirement:

- latency;
- turn-taking;
- identity;
- safe actions.

---

# 21. Pattern 12 — Embedded AI product

Customer wants AI inside own SaaS/app.

Architecture:

```text
Customer UI
↓
Customer backend
↓
OpenAI API
├─ model
├─ retrieval
├─ tools
└─ agents
```

Customer owns:

- UX;
- auth;
- permissions;
- business rules;
- operations.

---

# 22. Pattern composition

Most complete solutions combine patterns.

Example sales:

```text
Research
+
knowledge retrieval
+
content generation
+
CRM tool
```

Example finance:

```text
Data analysis
+
document intelligence
+
narrative generation
```

Example support:

```text
Knowledge
+
tool use
+
agentic execution
```

---

# 23. From primitive to pattern

OpenAI public primitives:

```text
Content creation
Research
Coding
Data analysis
Ideation & strategy
Automation
```

Potential mappings:

| Primitive | Example solution pattern |
|---|---|
| Content creation | Content workflow |
| Research | Research/synthesis |
| Coding | Codex/software agent |
| Data analysis | Analytics assistant |
| Ideation & strategy | Knowledge-work copilot |
| Automation | Tool-enabled/agentic workflow |

One solution may combine several.

---

# 24. Product-surface routing

```text
Broad employee work
→ ChatGPT / Work

Software engineering
→ Codex

Customer-owned application
→ API

Private knowledge
→ retrieval/plugin/MCP

Business actions
→ tools

Multi-step execution
→ agent
```

---

# 25. Trust layer

Every production pattern should ask:

- source?
- permission?
- eval?
- human review?
- monitoring?
- fallback?

Solution pattern without trust layer is incomplete.

---

# 26. Example — Internal policy assistant

```text
ChatGPT
+ approved HR knowledge
+ identity
+ citations
+ escalation
```

Pattern:

> Knowledge assistant.

Not:

> “Use latest model.”

---

# 27. Example — Invoice workflow

```text
Invoice PDF
↓
multimodal extraction
↓
JSON
↓
policy validation
↓
ERP tool
↓
human exception queue
```

Patterns:

- document intelligence;
- workflow automation.

---

# 28. Example — Sales preparation

```text
CRM/account context
+ current research
↓
synthesis
↓
meeting brief
```

Patterns:

- research;
- knowledge;
- generation.

No agent required unless actions become multi-step.

---

# 29. Example — Developer migration

```text
Migration goal
↓
Codex
↓
repo search
↓
changes
↓
tests
↓
review
```

Pattern:

> Coding/software agent.

---

# 30. Example — Retail support

```text
Shopper question
↓
product/catalog context
↓
recommendation
↓
inventory/order tool
↓
response
```

Potentially:

- knowledge;
- recommendation;
- tool-enabled workflow.

---

# 31. Solution-pattern selection framework — SHAPE

## S — Surface
Where user/workflow lives?

## H — Human role
Assist, approve, exception?

## A — Access
Data/tools?

## P — Process complexity
Single or multi-step?

## E — Evaluation
What proves success?

This framework ties patterns to implementation.

---

# 32. Common mistakes

1. Pattern = official product name.
2. Treat study synthesis as official OpenAI taxonomy.
3. Every support solution = agent.
4. Every private-data problem = fine-tuning.
5. Every AI application = chat.
6. Use free-form prose when software needs JSON.
7. Ignore trust/eval layer.
8. Stack every technology.

---

# 33. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Solution pattern | Mẫu giải pháp |
| Knowledge assistant | Trợ lý tri thức |
| Document intelligence | Xử lý tài liệu thông minh |
| Analytics assistant | Trợ lý phân tích |
| Embedded AI | AI nhúng vào product |
| Tool-enabled | Có tool/API |
| Agentic operations | Workflow vận hành bằng agent |
| Grounded | Bám vào source |
| Structured output | Output theo schema |
| Pattern composition | Kết hợp pattern |

---

# 34. Section recap

Study solution patterns:

```text
Knowledge-work copilot
Knowledge/RAG
Research
Document intelligence
Analytics
Content
Coding
Support
Tool automation
Agents
Realtime voice
Embedded AI
```

But remember:

> OpenAI's official public guide currently uses six **use-case primitives**; the list above is a synthesized architecture study map.

Core rule:

> **Pick the simplest pattern that solves the workflow, then add retrieval, tools or agents only when the requirement demands them.**

---

# 35. Self-check

1. Primitive và solution pattern khác nhau thế nào?
2. Knowledge assistant cần gì?
3. Document intelligence khác content generation thế nào?
4. Tool-enabled automation và agent khác gì?
5. SHAPE framework gồm gì?
6. Hãy decompose a customer-support solution into patterns.
