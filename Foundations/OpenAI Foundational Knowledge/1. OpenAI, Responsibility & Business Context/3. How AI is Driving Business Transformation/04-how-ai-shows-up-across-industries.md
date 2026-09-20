# 04 — How AI Shows Up Across Industries

> **Course:** Foundation — OpenAI Foundational Knowledge  
> **Course:** How AI is Driving Business Transformation  
> **Section:** How AI shows up across industries
>
> **Source note:** Các ví dụ dưới đây là representative patterns từ OpenAI public enterprise materials và general solution framing. Chúng không thay thế industry-specific regulatory, legal, safety hoặc customer discovery.

---

# 1. Section objective

Sau section này, bạn cần:

- phân biệt **horizontal capability** và **vertical/industry solution**;
- hiểu AI pattern giống nhau nhưng context, data, trust và KPI thay đổi theo industry;
- nhận diện examples across technology, finance, healthcare, manufacturing, professional services, retail và các vertical khác;
- không pitch industry bằng generic AI claims;
- biết chuyển từ industry context → workflow → value → trust.

---

# 2. Big picture

AI không thay đổi hoàn toàn khi đổi ngành.

Core capabilities vẫn có thể là:

```text
Research
Content
Coding
Analysis
Reasoning
Automation
```

Nhưng industry context thay đổi:

```text
Data
Workflow
Terminology
Regulation
Risk
Users
Systems
Metrics
```

Do đó:

> **Vertical solution = horizontal AI capability adapted to industry context.**

---

# 3. Industry lens

Khi bước vào một vertical, partner cần hiểu 5 thứ:

```text
1. Industry economics
2. Core workflows
3. Domain data
4. Trust / regulatory constraints
5. Business KPIs
```

Nếu thiếu context này, pitch dễ trở thành:

> “AI can summarize, automate, and analyze.”

Đúng nhưng không có giá trị consultative.

---

# 4. Technology / Software

Technology companies có natural fit với AI ở:

- coding;
- product development;
- in-product AI;
- customer support;
- search/assistant;
- automation.

OpenAI's 2025 enterprise report mô tả technology là một trong các sector tăng trưởng mạnh và API usage lớn cho customer-facing applications.

---

## 4.1. Engineering

```text
Issue
→ codebase understanding
→ implementation
→ tests
→ review
```

Potential metrics:

- lead time;
- developer throughput;
- issue resolution.

---

## 4.2. AI inside product

A software company có thể embed AI thành:

- search;
- assistant;
- content feature;
- analytics;
- workflow automation.

Value có thể là:

- customer experience;
- product differentiation;
- new revenue.

---

# 5. Financial Services

Finance is information-rich and often highly controlled.

AI patterns:

- customer support;
- research;
- document analysis;
- coding;
- operations;
- compliance workflow support;
- analyst productivity.

OpenAI public enterprise report notes customer support, coding/developer tools, agentic workflows, in-app assistant/search, and data analysis among common API categories for finance customers.

---

## 5.1. Customer service

Potential workflow:

```text
Customer query
→ retrieve account context
→ retrieve approved knowledge
→ draft/respond
→ permitted action
→ escalation
```

Need:

- privacy;
- permission;
- accuracy;
- auditability.

---

## 5.2. Analyst/research support

AI can:

- synthesize filings;
- compare information;
- draft research;
- analyze data.

Human professional remains responsible for high-impact decisions.

---

# 6. Healthcare

Healthcare is a domain where:

- information load is high;
- workflows are complex;
- consequences can be high.

Potential uses should be described carefully.

Examples at lower-risk/support layer:

- administrative documentation;
- knowledge retrieval;
- summarization;
- operational support;
- coding/software workflows.

Clinical/high-impact usage requires appropriate validation, professional oversight and current policy/regulatory review.

---

## 6.1. Key principle

Do not say:

> “AI can replace clinical judgment.”

Better:

> “AI may support specific workflows under appropriate professional oversight and evidence.”

---

# 7. Manufacturing

Manufacturing combines:

- physical operations;
- engineering;
- supply chain;
- documentation;
- maintenance;
- quality;
- enterprise systems.

Potential patterns:

```text
Technical knowledge assistant
Document analysis
Engineering support
Planning analysis
Quality issue synthesis
Maintenance workflow support
```

OpenAI's enterprise report identified manufacturing among fast-growing sectors in its 2025 customer data.

---

# 8. Professional Services

Examples:

- research;
- document synthesis;
- client deliverable drafting;
- coding/internal tooling;
- knowledge management;
- workflow automation.

Core value:

```text
Expert time
is expensive
↓
AI reduces lower-value effort
↓
Experts spend more time on judgment/client work
```

But quality/review is central because output often reaches clients.

---

# 9. Retail / Consumer

Retail combines:

- merchandising;
- marketing;
- support;
- analytics;
- commerce operations.

AI can support:

- product content;
- customer Q&A;
- personalization support;
- campaign localization;
- feedback analysis;
- internal knowledge.

Metrics:

- conversion;
- support cost;
- content cycle time;
- customer satisfaction.

---

# 10. Media / Creative

AI capabilities can support:

- ideation;
- research;
- first drafts;
- editing;
- localization;
- visual creation;
- production support.

Value:

- creative iteration;
- more variants;
- faster production.

Need attention to:

- rights;
- brand;
- source accuracy;
- human creative direction.

---

# 11. Education

AI can support:

- explanation;
- tutoring;
- content preparation;
- administrative work;
- teacher support;
- research.

Industry context changes design:

- learner age;
- assessment integrity;
- curriculum;
- privacy;
- educator oversight.

---

# 12. Public Sector

Potential patterns:

- document processing;
- knowledge retrieval;
- citizen/service information;
- administrative workflows;
- analysis.

Need strong attention to:

- fairness;
- accessibility;
- accountability;
- procurement;
- legal requirements;
- public trust.

---

# 13. Life sciences / R&D

Potential workflows:

- literature research;
- document synthesis;
- coding/data analysis;
- knowledge management;
- operational support.

Domain experts are essential where scientific conclusions have consequence.

AI can accelerate information processing without replacing scientific validation.

---

# 14. Energy / Utilities

Potential patterns:

- engineering knowledge;
- maintenance documentation;
- operations analysis;
- customer support;
- field-work documentation;
- data synthesis.

Physical infrastructure context increases importance of:

- reliability;
- permissions;
- human review;
- operational safety.

---

# 15. Industry value is workflow-specific

“AI in healthcare” is not a use case.

“AI summarizes approved clinical documentation for professional review” is much more specific.

“AI in finance” is not a use case.

“AI prepares a cited customer-service response from approved policy and account context” is closer.

Formula:

```text
Industry
+ User
+ Workflow
+ AI role
+ Data
+ Controls
+ KPI
=
Vertical use case
```

---

# 16. Same capability, different vertical

Capability:

> document summarization.

### Finance
Summarize filings/policy.

### Healthcare
Summarize documentation.

### Manufacturing
Summarize technical/manual content.

### Legal/professional services
Summarize contract/client document.

Core capability same.

Definition of:

- correctness;
- acceptable error;
- reviewer;
- source;

can be very different.

---

# 17. Industry-specific trust

Trust is not generic.

### Finance

- audit;
- data;
- regulatory controls.

### Healthcare

- professional oversight;
- evidence;
- patient safety/privacy.

### Manufacturing

- operational safety;
- engineering verification.

### Retail

- brand/customer experience;
- privacy.

Thus:

```text
Same model
≠
same deployment design
```

---

# 18. Industry-specific data

AI value often depends on proprietary context.

Examples:

- finance → policies/account data;
- manufacturing → manuals/maintenance history;
- software → codebase;
- retail → product catalog;
- professional services → knowledge corpus.

This is why integration matters.

---

# 19. Industry-specific systems

Tool integration also changes:

```text
Finance → core banking / CRM
Healthcare → clinical/admin systems
Manufacturing → ERP / MES / maintenance systems
Retail → commerce / catalog / CRM
Technology → code repo / issue tracker
```

Agent design must respect system permission model.

---

# 20. Industry-specific KPI

Generic:

> “Productivity improved.”

Better:

### Support-heavy industry
- cost per resolution;
- first-contact resolution.

### Manufacturing
- downtime;
- quality cycle.

### Software
- release cycle;
- engineering throughput.

### Professional services
- delivery time;
- expert utilization.

---

# 21. Vertical adaptation framework — VERTICAL

Mnemonic học tập:

## V — Value
Business value ở industry này?

## E — Environment
Systems/data/process?

## R — Risk
Industry-specific risk?

## T — Task
Exact workflow/task?

## I — Integration
Tool/data integration?

## C — Controls
Safety/governance?

## A — Adoption
Users/change?

## L — Leading metric
Measure nào chứng minh value?

---

# 22. Example — Manufacturing knowledge assistant

### Generic capability

Question answering.

### Vertical context

Factory technicians need technical documentation.

### Data

Approved manuals, maintenance guides.

### Workflow

```text
Technician question
→ retrieve relevant manual
→ summarize instruction
→ cite source
→ escalate uncertain/safety-critical case
```

### Value

- faster information access.

### Trust

- source grounding;
- version control;
- expert review for critical actions.

Đây là vertical adaptation.

---

# 23. Example — Financial support assistant

### Capability

Reason + retrieve + generate.

### Workflow

```text
Query
→ identify customer
→ check permitted account context
→ retrieve approved policy
→ answer
→ allowed tool action / escalation
```

### Metrics

- handling time;
- resolution;
- error/exception.

### Trust

- privacy;
- permission;
- audit.

---

# 24. Partner lens

Trước khi pitch industry:

### Learn vocabulary
Customer gọi workflow là gì?

### Learn economics
Cost/revenue driver?

### Learn system
Data/system of record?

### Learn risk
Which error matters?

### Learn stakeholder
Who owns process?

### Learn metric
What proves value?

---

# 25. Avoid shallow verticalization

Shallow:

> “AI for healthcare: summarize things.”

Better:

> “Which documentation workflow? Which user? Which source? What review? What KPI?”

Shallow vertical pitch often chỉ đổi tên ngành trên slide.

Real vertical solution thay đổi:

- context;
- workflow;
- integration;
- trust;
- success metric.

---

# 26. Industry trends vs customer facts

OpenAI reports can tell us broad patterns.

Ví dụ:

- sectors growing in adoption;
- popular API use-case categories.

Nhưng không được suy ra:

> “Mọi company trong industry này cần use case X.”

Industry evidence là **starting hypothesis**.

Discovery xác nhận customer reality.

---

# 27. Common mistakes

## Mistake 1
Industry = use case.

## Mistake 2
Copy same solution across industries.

## Mistake 3
Use sector adoption trend as customer proof.

## Mistake 4
Ignore domain experts.

## Mistake 5
Overlook systems of record.

## Mistake 6
Lead with regulation only and forget value.

Need both value + trust.

---

# 28. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| **Industry / vertical** | Ngành/lĩnh vực |
| **Horizontal capability** | Năng lực dùng rộng qua nhiều ngành |
| **Vertical solution** | Giải pháp thích ứng cho một ngành |
| **Domain context** | Bối cảnh chuyên ngành |
| **Domain expert** | Chuyên gia lĩnh vực |
| **System of record** | Hệ thống chứa dữ liệu nghiệp vụ chuẩn |
| **Operational safety** | An toàn trong vận hành |
| **Proprietary data** | Dữ liệu riêng của organization |
| **Industry economics** | Cách value/cost/revenue vận hành trong ngành |
| **Verticalization** | Điều chỉnh solution theo vertical |

---

# 29. Section recap

1. AI capabilities are horizontal; solutions become vertical through context.
2. Industry changes workflow, data, risk, systems and metrics.
3. Industry trend is hypothesis, not customer proof.
4. Technology often emphasizes coding/product embedding.
5. Finance emphasizes customer service, analysis, controls.
6. Healthcare requires careful professional/high-impact framing.
7. Manufacturing combines knowledge, engineering and operations.
8. Professional services use AI to leverage expert time.
9. Use:
   **Industry + workflow + data + controls + KPI**.
10. Avoid shallow verticalization.

---

# 30. Self-check

1. Horizontal capability và vertical solution khác nhau thế nào?
2. Tại sao cùng summarization capability có risk khác nhau theo industry?
3. Hãy áp dụng VERTICAL framework cho ngành software.
4. Vì sao industry growth report không chứng minh customer use case?
5. “AI in manufacturing” cần được cụ thể hóa thành những thành phần nào?

---

# 31. Official public references

- OpenAI — *The state of enterprise AI* (2025)
- OpenAI — *Solutions for Business*
- OpenAI Academy — industry resources
- OpenAI — *Identifying and scaling AI use cases*
