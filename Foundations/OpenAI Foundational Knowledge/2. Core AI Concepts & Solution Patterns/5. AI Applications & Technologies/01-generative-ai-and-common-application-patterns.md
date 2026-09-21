# 01 — Generative AI and Common Application Patterns

> **Course:** OpenAI Foundational Knowledge  
> **Course group:** Core AI Concepts & Solution Patterns  
> **Sub-course:** AI Applications & Technologies  
> **Section:** Generative AI and common application patterns
>
> **Source note:** Hiện mới có tên section, chưa có transcript/slides PartnerU. Vì vậy các application patterns bên dưới là **study synthesis** dựa trên các patterns phổ biến của generative AI; không khẳng định đây là taxonomy nguyên văn của PartnerU.

---

## 1. Section objective

Sau section này, bạn cần:

- phân biệt **model capability**, **application pattern** và **business use case**;
- nhận diện các dạng application phổ biến của Generative AI;
- hiểu một solution có thể kết hợp nhiều pattern;
- biết khi nào cần model, retrieval, tools, structured outputs hay human review;
- tránh tư duy “Generative AI = chatbot”.

---

# 2. Big picture

Generative AI là capability layer, không phải một application duy nhất.

```text
Model capability
      ↓
Application pattern
      ↓
Business workflow
      ↓
Business outcome
```

Ví dụ cùng một model có thể được dùng trong:

- chat assistant;
- document summarization;
- extraction pipeline;
- coding copilot;
- knowledge assistant;
- analytics assistant;
- tool-using workflow;
- agent.

**Điểm cần nhớ:** cùng capability, nhưng application shape khác nhau sẽ dẫn tới architecture, risk, UX và metric khác nhau.

---

# 3. Capability vs application pattern vs use case

## Capability

Khả năng model có thể thực hiện:

- understand language;
- summarize;
- classify;
- extract;
- reason;
- generate;
- understand images;
- use tools.

## Application pattern

Cách capability được tổ chức thành một dạng ứng dụng.

Ví dụ:

```text
Capability:
summarization

Application pattern:
meeting assistant
```

## Business use case

Application pattern + user + workflow + context + metric.

```text
Meeting assistant
+ Sales rep
+ Customer-call workflow
+ CRM context
+ Follow-up speed metric
=
Sales call follow-up use case
```

---

# 4. Pattern 1 — Conversational assistant

Shape cơ bản:

```text
User
↕
Chat UI
↕
Model
```

Assistant có thể:

- answer;
- explain;
- brainstorm;
- draft;
- summarize;
- guide.

Examples:

- employee assistant;
- support assistant;
- onboarding assistant;
- sales prep assistant.

Nhưng chat UI chỉ là **interaction shape**. Nó chưa nói application có retrieval/tools hay không.

---

# 5. Enterprise conversational assistant

Simple:

```text
User → Model → Answer
```

Enterprise:

```text
User
→ identity
→ instructions
→ relevant context
→ retrieval/tools
→ model
→ policy checks
→ answer/action
```

Value tăng khi assistant có:

- trusted knowledge;
- company context;
- permissions;
- tools;
- escalation;
- monitoring.

---

# 6. Pattern 2 — Content generation

Generative AI có thể tạo content mới.

Examples:

- email;
- report;
- campaign copy;
- code;
- documentation;
- product description;
- image.

Flow:

```text
Goal + context
→ model
→ draft
→ review/refine
```

Business value thường nằm ở:

- faster first draft;
- higher throughput;
- more variants;
- reduced blank-page effort.

---

# 7. Pattern 3 — Content transformation

Transformation sử dụng content có sẵn để tạo một dạng khác.

Examples:

```text
Long document → summary
Notes → report
English → Vietnamese
Technical text → plain language
Transcript → action items
```

Transformation thường dễ define evaluation hơn pure creative generation vì đã có source.

---

# 8. Pattern 4 — Extraction and structuring

Unstructured input:

```text
Invoice / PDF / Email
```

becomes structured output:

```json
{
  "vendor": "...",
  "invoice_number": "...",
  "amount": 0,
  "due_date": "..."
}
```

Applications:

- invoices;
- claims;
- contracts;
- forms;
- support tickets.

Nếu output sẽ đi vào code/system downstream, **structured output** thường phù hợp hơn free-form text.

---

# 9. Extraction design principle

Extraction should answer:

> “What is present in the source?”

not:

> “What sounds plausible?”

Useful controls:

- schema;
- validation;
- null/unknown behavior;
- source references;
- human exception queue.

---

# 10. Pattern 5 — Classification and routing

Examples:

```text
Ticket
→ billing / technical / cancellation
```

```text
Message
→ low / medium / high urgency
```

Classification thường là primitive bên trong workflow lớn hơn.

Example:

```text
Ticket
→ classify
→ retrieve policy
→ draft response
→ route exception
```

---

# 11. Pattern 6 — Knowledge/search assistant

A knowledge assistant combines retrieval + generation.

```text
Question
→ retrieve relevant sources
→ model synthesizes
→ answer + sources
```

Use cases:

- HR policies;
- product docs;
- technical docs;
- internal knowledge;
- sales enablement.

Đây là application shape thường dùng **RAG**, sẽ học kỹ ở Section 02.

---

# 12. Pattern 7 — Data analysis assistant

Flow:

```text
Business question
→ data/tool access
→ analysis
→ explanation / table / chart
```

Capabilities may include:

- SQL;
- Python;
- spreadsheet analysis;
- anomaly detection;
- narrative generation.

Important:

> Model không nên được xem như source of truth cho live business data.

Use governed data/tools.

---

# 13. Pattern 8 — Coding applications

AI can assist with:

```text
Understand
→ design
→ code
→ test
→ debug
→ review
→ document
```

Application shapes:

- IDE copilot;
- repo-aware chat;
- code review assistant;
- coding agent.

Controls:

- tests;
- code review;
- repo permissions;
- security checks.

---

# 14. Pattern 9 — Multimodal applications

A multimodal application handles more than one modality.

Examples:

```text
Screenshot + question → analysis
Receipt image → structured fields
Audio → transcript → summary
Text → image
```

A solution may use multiple specialized models/capabilities.

---

# 15. Pattern 10 — Tool-using application

Pure generation:

```text
Question
→ model
→ answer
```

Tool-enabled:

```text
Question
→ model decides data/action needed
→ tool/API
→ result
→ model response
```

Example:

```text
"Where is my order?"
→ getOrderStatus(order_id)
→ current status
→ answer
```

Tool use allows model to access:

- current data;
- enterprise systems;
- actions.

---

# 16. Pattern 11 — Agentic workflow

Agentic system handles multiple steps toward a goal.

```text
Goal
↓
reason / plan
↓
choose tool/action
↓
observe result
↓
continue
↓
complete or escalate
```

Example:

```text
Resolve a support ticket
```

Possible sequence:

1. classify;
2. retrieve account;
3. check policy;
4. call tool;
5. verify;
6. close or escalate.

---

# 17. Agent ≠ full autonomy

Agentic does not mean:

> “AI does everything without humans.”

Autonomy can be scoped:

```text
AI drafts
→ human acts
```

or:

```text
AI acts on low-risk cases
→ human handles exceptions
```

**Agenticity** and **autonomy level** are separate design decisions.

---

# 18. Pattern composition

Real solutions combine patterns.

Support solution:

```text
Classification
+ Retrieval
+ Generation
+ Tool use
+ Escalation
```

Invoice solution:

```text
Multimodal input
+ Extraction
+ Validation
+ API lookup
+ Workflow automation
```

Therefore:

> Don't force a solution into one label.

---

# 19. Common architecture mental model

```text
┌───────────────────────────────┐
│ User / business workflow      │
├───────────────────────────────┤
│ Application / UX              │
├───────────────────────────────┤
│ Orchestration                 │
├───────────────────────────────┤
│ Model(s)                      │
├───────────────┬───────────────┤
│ Retrieval     │ Tools/actions │
├───────────────┴───────────────┤
│ Enterprise systems/data       │
├───────────────────────────────┤
│ Evals / monitoring / controls │
└───────────────────────────────┘
```

Không phải app nào cũng cần mọi layer.

---

# 20. Developer mental model

Traditional app:

```text
UI
→ backend
→ database/API
```

AI app:

```text
UI
→ backend/orchestrator
→ model
→ retrieval/tools
→ database/APIs
```

Model xử lý ambiguity/reasoning.

Backend vẫn giữ:

- auth;
- deterministic rules;
- permissions;
- state;
- logging.

---

# 21. Interactive vs batch

## Interactive

Examples:

- chat;
- coding copilot;
- voice assistant.

Priorities:

- latency;
- UX;
- responsiveness.

## Batch

Examples:

- process 50,000 documents;
- nightly classification;
- historical backfill.

Priorities:

- throughput;
- cost;
- retry;
- reliability.

Same model capability, different system design.

---

# 22. Internal vs customer-facing

Internal:

- known employees;
- controlled context;
- company data.

Customer-facing:

- broader/untrusted users;
- stronger abuse handling;
- higher availability expectations.

This changes:

- authentication;
- monitoring;
- UX;
- safety;
- support model.

---

# 23. Human-in-the-loop

Human review can be deliberate architecture:

```text
AI output
↓
risk/confidence rule
↓
human approval
↓
action
```

Useful when:

- error consequence is high;
- exception rate matters;
- workflow is regulated;
- system is early-stage.

---

# 24. Partner discovery questions

Ask:

1. Who is the user?
2. What exact task?
3. What inputs?
4. What output/action?
5. Does it need private/current knowledge?
6. Does it need tools?
7. Realtime or batch?
8. What happens if wrong?
9. How is success measured?
10. What remains human-owned?

---

# 25. Example — Sales preparation

```text
Account context
+ approved product information
→ retrieval
→ synthesis
→ meeting brief
```

After call:

```text
Transcript
→ summary
→ next steps
→ CRM update
```

One business workflow can combine:

- retrieval;
- generation;
- extraction;
- tool use.

---

# 26. Example — Invoice operations

```text
PDF/image
↓
multimodal understanding
↓
structured extraction
↓
supplier/PO lookup
↓
validation
↓
record creation or exception queue
```

No chat UI required.

This is a good reminder:

> Generative AI applications are much broader than chatbots.

---

# 27. Common mistakes

1. Generative AI = chatbot.
2. Every app needs an agent.
3. Free-form text when downstream system needs structured fields.
4. Give tool access without permissions.
5. Start with model name instead of workflow.
6. Treat application pattern as business outcome.
7. Assume more autonomy automatically means more value.

---

# 28. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Application pattern | Mẫu ứng dụng |
| Conversational assistant | Trợ lý hội thoại |
| Generation | Tạo nội dung |
| Transformation | Biến đổi nội dung |
| Extraction | Trích xuất |
| Classification | Phân loại |
| Routing | Điều hướng |
| Structured output | Output có schema |
| Knowledge assistant | Trợ lý tri thức |
| Tool use | Sử dụng API/công cụ |
| Agentic workflow | Workflow nhiều bước do AI điều phối |
| Multimodal | Đa phương thức |
| Batch | Xử lý theo lô |
| Human-in-the-loop | Có con người tham gia vòng xử lý |

---

# 29. Section recap

Key application shapes:

```text
Assistant/chat
Generation
Transformation
Extraction
Classification
Knowledge/RAG
Data analysis
Coding
Multimodal
Tool use
Agentic workflow
```

Remember:

```text
Capability ≠ application
Application ≠ business use case
Chat ≠ all GenAI
Agent ≠ required for everything
```

Core rule:

> **Choose the simplest application shape that reliably solves the workflow.**

---

# 30. Self-check

1. Capability, application pattern và use case khác nhau thế nào?
2. Vì sao extraction thường nên dùng structured output?
3. Tool use khác plain generation thế nào?
4. Agentic workflow có đồng nghĩa full autonomy không?
5. Hãy map invoice processing vào các application patterns.
6. Vì sao một GenAI solution có thể không có chat UI?
