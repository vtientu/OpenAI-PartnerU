# 03 — How AI Shows Up Across Business Functions

> **Course:** Foundation — OpenAI Foundational Knowledge  
> **Course:** How AI is Driving Business Transformation  
> **Section:** How AI shows up across business functions
>
> **Source note:** Examples được tổng hợp từ OpenAI public business guides/solutions và được diễn giải theo workflow. Chúng là patterns/examples, không phải lời hứa về outcome cho mọi company.

---

# 1. Section objective

Sau section này, bạn cần:

- hiểu cùng một AI capability có thể tạo value khác nhau theo function;
- nhận diện use cases phổ biến trong engineering, sales, marketing, finance, operations, support và các function khác;
- nói bằng language của từng stakeholder;
- map function workflow → AI pattern → metric;
- tránh generic pitch kiểu “AI helps every team.”

---

# 2. Big picture

AI capability horizontal.

Business value vertical theo function.

```text
Same AI capability
        ↓
Different workflow context
        ↓
Different value metric
```

Example:

**Summarization**

Sales:
→ summarize customer calls.

Finance:
→ summarize variance commentary.

Legal:
→ summarize contract clauses.

Engineering:
→ summarize incident/code context.

Capability giống nhau.

Outcome khác nhau.

---

# 3. Functional value map

Một mental model:

| Function | Typical value focus |
|---|---|
| Engineering | delivery speed, code quality, developer capacity |
| Sales | selling time, conversion, cycle time |
| Marketing | campaign velocity, content scale, insight |
| Finance | analysis speed, reporting, control |
| Operations | throughput, cycle time, consistency |
| Customer support/success | resolution, handling time, experience |
| HR/People | employee support, knowledge access, admin efficiency |
| Legal | review/research efficiency, consistency |
| Data/Analytics | time-to-insight, broader self-service |
| Leadership | synthesis, planning, decision support |

Không phải metric duy nhất.

---

# 4. Engineering

OpenAI public materials mô tả coding là một trong những use-case primitives mạnh.

AI có thể hỗ trợ:

```text
Understand
→ Design
→ Code
→ Test
→ Review
→ Debug
→ Document
```

---

## 4.1. Code understanding

Use cases:

- explain unfamiliar codebase;
- trace data flow;
- find implementation;
- summarize architecture;
- investigate incident context.

### Value

- faster onboarding;
- reduce context-switching;
- faster maintenance.

---

## 4.2. Code generation and modification

Use cases:

- first-draft code;
- refactoring;
- migration;
- test generation;
- repetitive implementation.

### Controls

- tests;
- code review;
- CI;
- security checks.

### Metrics

- lead time;
- PR cycle time;
- throughput;
- defect rate.

---

# 5. Sales

Sales has large amounts of:

- information gathering;
- account context;
- customer communication;
- CRM admin.

AI can assist across cycle:

```text
Research account
↓
Prepare meeting
↓
Generate questions
↓
Summarize call
↓
Draft follow-up
↓
Update CRM
```

---

## 5.1. Prospect/account research

Input:

- public information;
- CRM;
- account notes.

Output:

- brief;
- stakeholder map;
- relevant signals.

Value:

- less research time;
- better preparation.

---

## 5.2. Follow-up and CRM administration

AI can:

- summarize call;
- extract next steps;
- draft follow-up;
- prepare CRM fields.

Metric:

- time spent selling vs admin;
- follow-up latency;
- CRM completeness.

---

# 6. Marketing

Common AI patterns:

- research;
- ideation;
- content creation;
- localization;
- campaign analysis.

Workflow example:

```text
Market research
↓
Audience insight
↓
Campaign strategy
↓
Creative variants
↓
Localization
↓
Performance analysis
```

AI can touch every stage.

---

## 6.1. Content

- campaign brief;
- email;
- ad variants;
- social copy;
- landing page first draft.

## 6.2. Research

- competitors;
- market trend;
- audience.

## 6.3. Localization

Transform content for:

- languages;
- channels;
- audiences.

Metrics:

- campaign launch time;
- content throughput;
- localization time;
- engagement/conversion.

Caution:

> Content volume không phải business value nếu performance không improve.

---

# 7. Finance

Finance combines:

- structured data;
- recurring processes;
- narrative;
- control requirements.

AI can support:

```text
Data
→ Analysis
→ Explanation
→ Reporting
→ Workflow automation
```

---

## 7.1. Analysis

- variance analysis;
- scenario exploration;
- spreadsheet analysis;
- anomaly investigation.

## 7.2. Reporting

- management commentary draft;
- executive summary;
- board material support.

## 7.3. Operations

- document extraction;
- reconciliation support;
- monthly-close scripts/workflow.

Metrics:

- close cycle;
- analyst hours;
- report turnaround;
- error/exception rate.

---

# 8. Data & Analytics

AI reduces barrier between business question and analysis.

Workflow:

```text
Natural-language question
↓
Data exploration
↓
SQL/Python
↓
Visualization
↓
Interpretation
```

Potential value:

- faster time-to-insight;
- analyst leverage;
- broader data self-service.

Risks:

- wrong query;
- poor data;
- misleading interpretation.

Need:

- governed data;
- validation;
- semantic context.

---

# 9. Operations

Operations often contains repeatable workflows.

Examples:

- program updates;
- document processing;
- planning;
- exception handling;
- reporting;
- process monitoring.

AI value often comes from:

```text
Standardize
+
Automate repeatable steps
+
Route exceptions
```

Metrics:

- cycle time;
- throughput;
- cost per transaction;
- exception rate;
- SLA.

---

# 10. Customer support

A classic AI opportunity because support has:

- high volume;
- repeated questions;
- knowledge retrieval;
- structured workflows.

Maturity spectrum:

```text
Agent assist
↓
Response drafting
↓
Knowledge retrieval
↓
Case classification
↓
Low-risk automation
↓
Agentic resolution
```

---

## 10.1. Agent assist

AI helps human support agent.

Value:

- lower handling time;
- faster onboarding.

## 10.2. Self-service

AI directly assists customer.

Need stronger:

- grounding;
- evaluation;
- escalation.

## 10.3. Action

AI uses tools to resolve permitted cases.

Need:

- permissions;
- policy;
- audit;
- human exceptions.

---

# 11. Customer success

Different from reactive support.

Use cases:

- account brief;
- QBR preparation;
- customer health synthesis;
- renewal prep;
- action-item tracking.

Metrics:

- preparation time;
- coverage;
- retention;
- expansion;
- customer engagement.

---

# 12. HR / People

Possible lower-risk knowledge/admin patterns:

- employee policy Q&A;
- internal knowledge;
- learning content;
- communication drafting;
- survey theme analysis;
- admin workflow assistance.

Important:

> High-impact employment decisions require extra care and may be subject to policy/legal restrictions.

AI should not casually become uncontrolled decision maker.

---

# 13. Legal

Legal professionals process large volumes of text and research.

Possible uses:

- document summarization;
- clause extraction;
- first-pass comparison;
- research support;
- drafting support;
- knowledge retrieval.

Need:

- source grounding;
- confidentiality controls;
- expert review;
- appropriate legal oversight.

Metric examples:

- review cycle time;
- document throughput;
- research time.

---

# 14. Product

AI can support:

```text
Research
→ customer feedback synthesis
→ ideation
→ PRD
→ prototype
→ launch documentation
```

Value:

- faster learning;
- faster iteration;
- better synthesis.

Metric:

- discovery cycle;
- prototype time;
- time-to-market.

---

# 15. Leadership / managers

AI may support:

- briefing;
- synthesis;
- strategy exploration;
- scenario thinking;
- document review;
- meeting preparation.

But:

> AI should support judgment, not erase executive accountability.

Use it to expand option space and improve information processing.

---

# 16. Security / IT

OpenAI business materials increasingly show AI across technical operations.

Use cases:

- knowledge retrieval;
- incident investigation assistance;
- ticket triage;
- documentation;
- repetitive operational workflows.

When tools/actions are involved:

- permissions;
- logging;
- approval;
- rollback

become central.

---

# 17. Same pattern, different function

### Content creation

Marketing:
campaign copy.

Finance:
management memo.

Product:
PRD.

Sales:
follow-up.

Engineering:
documentation.

This is why learning **primitives/patterns** before department examples is useful.

---

# 18. Function workflow mapping

Đừng brainstorm isolated prompts.

Map workflow:

```text
Step 1
Step 2
Step 3
Step 4
Step 5
```

For each step ask:

- repetitive?
- information-heavy?
- skill bottleneck?
- ambiguous?
- tool/action required?
- metric?

---

# 19. Example — Sales workflow mapping

```text
1. Find account
   → Research

2. Prepare brief
   → Synthesis

3. Plan approach
   → Ideation

4. Meeting
   → Human-led

5. Summarize
   → Content/extraction

6. Follow-up
   → Content

7. Update CRM
   → Automation
```

One workflow, many AI patterns.

---

# 20. Example — Engineering workflow mapping

```text
1. Understand issue
   → research/code understanding

2. Locate code
   → coding assistant

3. Design fix
   → reasoning/ideation

4. Implement
   → coding

5. Test
   → code generation/tool execution

6. Review
   → human + AI

7. Document
   → content creation
```

---

# 21. Function ≠ use case

“AI for finance” không phải use case.

“AI generates variance commentary from approved financial data for analyst review” mới gần use case.

Use case cần:

```text
User
+ task
+ input/context
+ AI role
+ output/action
+ metric
```

---

# 22. Partner communication by function

## Engineering leader

Speak:

- developer velocity;
- quality;
- maintainability.

## Sales leader

Speak:

- seller capacity;
- conversion;
- cycle time.

## CFO

Speak:

- close cycle;
- control;
- analyst productivity.

## Marketing leader

Speak:

- campaign velocity;
- performance;
- content scale.

## COO

Speak:

- throughput;
- SLA;
- exceptions.

Avoid same pitch for all.

---

# 23. Identify function-specific constraints

Same capability may face different constraints.

### Marketing content

Brand/tone/review.

### Finance

Accuracy/control/auditability.

### Support

Knowledge freshness/escalation.

### Engineering

Security/testing/repository access.

### Legal

Confidentiality/expert review.

Use case is capability **inside context**.

---

# 24. Business function maturity ladder

```text
Individual use
↓
Team playbook
↓
Shared assistant
↓
Integrated workflow
↓
Agentic execution
↓
Function redesign
```

Again, higher is not always automatically better.

Choose based on value/risk/readiness.

---

# 25. Common mistakes

## Mistake 1
“Every department should use AI the same way.”

## Mistake 2
List generic prompts instead of workflows.

## Mistake 3
No function KPI.

## Mistake 4
Ignore constraints.

## Mistake 5
Pitch technical capability rather than business language.

---

# 26. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| **Business function** | Bộ phận/chức năng doanh nghiệp |
| **Functional workflow** | Workflow của một function |
| **Account brief** | Bản tóm tắt thông tin account |
| **Variance analysis** | Phân tích chênh lệch |
| **Agent assist** | AI hỗ trợ nhân viên |
| **Self-service** | Khách hàng tự phục vụ |
| **Localization** | Bản địa hóa nội dung |
| **Time-to-insight** | Thời gian để có insight |
| **Developer velocity** | Tốc độ/hiệu suất delivery của developer |
| **Handling time** | Thời gian xử lý case |
| **Exception handling** | Xử lý trường hợp ngoại lệ |
| **Function redesign** | Thiết kế lại cách một bộ phận vận hành |

---

# 27. Section recap

1. AI capability là horizontal; value phụ thuộc function context.
2. Không nói “AI for X function” quá chung.
3. Map **workflow → AI role → KPI**.
4. Engineering: coding/understanding/testing.
5. Sales: research/prep/follow-up/admin.
6. Marketing: research/ideation/content/localization/analysis.
7. Finance: analysis/reporting/operations.
8. Support: knowledge → assist → automation.
9. Same primitive có thể xuất hiện ở mọi function.
10. Partner phải dùng language của stakeholder.

---

# 28. Self-check

1. Vì sao summarization tạo value khác nhau giữa Sales và Legal?
2. Hãy map 5 bước của một workflow Marketing vào AI primitives.
3. Tại sao “AI for Finance” chưa phải use case?
4. Function-specific constraint là gì?
5. Engineering leader và CFO nên nghe value story khác nhau thế nào?

---

# 29. Official public references

- OpenAI — *Solutions for Business*
- OpenAI — *Identifying and scaling AI use cases*
- OpenAI Academy — *ChatGPT for work*
- OpenAI — *How OpenAI uses Codex*
- OpenAI — *The state of enterprise AI*
