# 01. Read the Vertical Context

> Course: **OpenAI Consultative Solutions Practitioner – Foundations**  
> Sub-course: **Vertical Solution Application**  
> Section: **Read the vertical context**

---

## 1. Mục tiêu của section

Sau khi đã học cách:

```text
discover
→ define use cases
→ build business value
→ route solutions
```

bước tiếp theo là học cách đặt tất cả những logic đó vào **một vertical cụ thể**.

**Vertical** = ngành / lĩnh vực kinh doanh cụ thể, ví dụ:

- Financial Services
- Healthcare
- Retail
- Manufacturing
- Public Sector
- Education
- Professional Services

Mục tiêu của section:

1. đọc một vertical context mà không bị cuốn vào buzzword;
2. xác định business priorities đặc thù;
3. tìm workflow có giá trị;
4. nhận diện user/stakeholder;
5. hiểu data/system environment;
6. phát hiện trust/risk constraints;
7. đánh giá readiness trước khi recommend.

Mental model:

```text
VERTICAL
  ↓
Business priorities
  ↓
Critical workflows
  ↓
Users / stakeholders
  ↓
Data / systems
  ↓
Trust / risk
  ↓
Readiness
  ↓
Opportunity
```

---

# 2. “Vertical context” thực sự là gì?

Một vertical không chỉ là tên ngành.

Ví dụ:

```text
"Healthcare customer"
```

gần như chưa nói gì về use case.

Trong healthcare, customer có thể đang nói về:

```text
clinical workflow
administrative workflow
research
software engineering
patient communication
care coordination
operations
```

Mỗi workflow có:

```text
different users
different data
different quality bar
different risk
different value
```

Do đó:

> **Industry label is context, not the use case.**

---

# 3. Tại sao phải đọc vertical context?

Nếu bỏ qua vertical context, ta dễ mắc lỗi:

```text
Generic AI capability
→ Generic value claim
→ Generic product pitch
```

Ví dụ:

> “AI can summarize documents.”

Trong finance, document summarization có thể liên quan:

```text
filings
transcripts
compliance documents
KYC files
internal research
```

Trong healthcare:

```text
clinical evidence
patient context
administrative forms
referral letters
care documentation
```

Trong retail:

```text
product knowledge
store operations
supplier inputs
shopper data
store visit notes
```

Cùng capability “summarize”, nhưng:

```text
source authority
risk
review
latency
user
business outcome
```

khác nhau.

---

# 4. Six-layer vertical reading model

## Layer 1 — Business priority

Ask:

```text
What is the organization trying to improve?
```

Common priorities:

- productivity/capacity;
- cycle time;
- customer/patient/shopper experience;
- revenue;
- quality;
- cost;
- risk;
- compliance;
- speed of research/analysis;
- employee enablement.

### Example — Financial Services

Public OpenAI financial-services materials emphasize workflows such as:

- research and analysis;
- financial modeling;
- document processing;
- client service;
- legacy modernization.

The business story is not “use AI”.

It is:

```text
faster analysis
more capacity
better consistency
trusted deployment
```

---

## Layer 2 — Workflow reality

Ask:

```text
What work actually happens?
```

Need to map:

```text
Input
→ steps
→ judgment
→ handoffs
→ output
```

Example:

```text
Retail store associate question
→ find product/policy information
→ interpret
→ guide shopper
```

Possible pain:

```text
search time
training burden
inconsistent answers
```

---

## Layer 3 — User and stakeholder

Separate:

```text
User
= person doing the workflow

Workflow owner
= accountable for process

Business sponsor
= cares about outcome

Technical owner
= integration/deployment

Trust/governance stakeholder
= security/compliance/privacy/risk
```

Do not treat “the customer” as one person.

---

## Layer 4 — Data and systems

Ask:

```text
What information makes the workflow possible?
Where does it live?
Who can access it?
How current must it be?
Which systems are involved?
```

Example finance:

```text
market data
filings
transcripts
spreadsheets
internal research
client data
```

Example healthcare:

```text
authorized patient context
EHR workflow
clinical evidence
organizational knowledge
```

Example retail:

```text
inventory
product catalog
shopper signals
historical sales
internal policy
```

---

## Layer 5 — Trust / risk

Trust requirements are vertical-sensitive.

Questions:

```text
What happens if output is wrong?
What data is sensitive?
What needs citation/traceability?
Where is human review needed?
What permissions apply?
What must be auditable?
```

Different workflows have different consequences.

Example:

```text
Marketing draft
≠
Clinical support
```

Both may use generative AI, but trust bar differs greatly.

---

## Layer 6 — Readiness

Ask:

```text
Is workflow clear?
Is owner named?
Is data accessible?
Is integration path known?
Is adoption path credible?
Are success measures defined?
Is governance path understood?
```

High business value with low readiness may mean:

```text
good opportunity
but wrong next step
```

---

# 5. Read “vertical language” carefully

Vertical context often contains specialized terms.

You do **not** need to become an industry expert overnight.

Instead, translate terms into workflow primitives.

Example:

```text
"KYC review"
```

Don't stop at acronym.

Ask:

```text
What documents?
Who reviews?
What is extracted?
What exceptions matter?
What must be verified?
What is the output?
```

Similarly:

```text
"care coordination"
```

Ask:

```text
Who coordinates?
What information?
Which handoffs?
What timing?
What review?
```

Consultative skill = turn domain language into an observable workflow.

---

# 6. Source authority matters

In some verticals, **where the answer comes from** is as important as the answer.

Examples:

```text
Healthcare:
trusted clinical evidence, authorized patient context

Finance:
approved market/company/internal data

Retail:
current product/inventory/policy information
```

Thus discovery should ask:

```text
Which sources are authoritative?
Which are merely helpful?
Which must not be used?
```

This becomes architecture + trust requirements later.

---

# 7. Vertical context ≠ stereotype

Bad thinking:

```text
Healthcare = compliance
Finance = cost
Retail = recommendations
```

Too simplistic.

A finance software engineering team may care most about:

```text
legacy modernization
testing
developer capacity
```

A healthcare admin team may care about:

```text
documentation burden
cycle time
```

A retail corporate team may care about:

```text
supplier negotiation analysis
```

Always route from actual workflow.

---

# 8. Example — Financial Services

### Context

Analysts spend substantial time gathering information from filings, decks and spreadsheets before preparing internal analysis.

### Business priority

```text
Faster research
More analyst capacity
Consistent analysis
```

### Workflow

```text
Gather
→ compare
→ analyze
→ draft
→ review
```

### Users

```text
Analysts
Reviewers
Research leadership
```

### Data

```text
filings
transcripts
internal spreadsheets
approved market/company data
```

### Trust

```text
source traceability
data control
review
auditability
```

### Readiness

```text
source access?
workflow owner?
quality bar?
success metrics?
```

Only now should solution pattern be adapted.

---

# 9. Example — Healthcare

### Context

Operations staff repeatedly prepare patient-facing administrative instructions from approved information.

### Priority

```text
reduce administrative burden
improve consistency
```

### Workflow

```text
collect approved context
→ draft
→ review
→ deliver
```

### Trust

Potentially:

```text
privacy
approved data access
human review
accuracy
```

### Readiness

Need to know:

```text
who owns workflow
what information is permitted
what review is mandatory
```

Do not jump from “healthcare” to a clinical recommendation use case.

---

# 10. Example — Retail

Public OpenAI retail materials illustrate multiple distinct vertical workflows:

```text
store associate product/policy questions
marketing localization
conversational shopping
supplier negotiation preparation
store visit insights
```

This demonstrates an important principle:

> **One vertical contains many workflow families.**

Reading context means identify which family you are in.

---

# 11. Frontend Developer analogy

Imagine a request:

> “We need AI for ecommerce.”

This is not enough.

Possible contexts:

```text
Customer onboarding
Product discovery
Support
Merchandising
Marketing content
Internal operations
Engineering
```

As a frontend developer, you would not design UI before knowing the user flow.

Same principle here:

```text
Vertical context
= domain version of user-flow discovery
```

---

# 12. Context extraction template

Use this when reading a case:

```md
## Vertical
...

## Business priority
...

## Workflow
Input:
Steps:
Decision:
Output:

## Primary user
...

## Workflow owner
...

## Other stakeholders
...

## Data / systems
...

## Trust / risk
...

## Readiness
Known:
Unknown:

## Potential value
...

## Open questions
...
```

---

# 13. Common mistakes

## ❌ Industry = use case

No.

## ❌ Use public industry example as proof

A published use case is a pattern, not evidence for this customer.

## ❌ Ignore vertical vocabulary

If a term is unclear, unpack workflow behind it.

## ❌ Assume regulation is the only trust factor

Trust also includes:

```text
quality
source authority
permissions
review
auditability
operational reliability
```

## ❌ Start recommendation before identifying workflow

This creates generic pitches.

---

# 14. Relationship to Mapping Solutions

Previous sub-course:

```text
Workflow
→ Surface
→ Capability
→ Architecture
→ Operating
→ Next step
```

Vertical Application adds:

```text
Industry context
→ changes priorities, data, trust and readiness
```

So:

```text
Generic routing logic
+
Vertical context
=
Vertical solution application
```

---

# 15. Cheat Sheet

```text
READ THE VERTICAL:

1. What does the business care about?
2. What workflow is involved?
3. Who does/owns the work?
4. What data/systems matter?
5. What trust/risk applies?
6. Is the organization ready?
7. What value could change?
```

One sentence:

> **Do not sell to an industry; solve a workflow inside an industry.**

---

# 16. Vocabulary

| Term | Nghĩa dễ hiểu |
|---|---|
| Vertical | Ngành/lĩnh vực |
| Vertical context | Bối cảnh đặc thù ngành |
| Domain | Miền nghiệp vụ |
| Workflow family | Nhóm workflow tương tự trong ngành |
| Source authority | Mức độ nguồn được xem là đáng tin/chính thức |
| Trust | Điều kiện để dùng solution một cách đáng tin |
| Readiness | Mức sẵn sàng |
| Business priority | Ưu tiên kinh doanh |
| Operational workflow | Quy trình vận hành |
| Stakeholder | Người liên quan/ra quyết định |

---

# 17. Self-check

1. Vì sao “healthcare customer” chưa đủ để route?
2. Vertical context gồm những layer nào?
3. Source authority ảnh hưởng solution ra sao?
4. Vertical stereotype khác workflow evidence thế nào?
5. Readiness khác value thế nào?
6. Bạn có thể chuyển một domain term thành workflow questions không?

---

## Nguồn và mức độ grounding

### PartnerU
Bạn hiện chỉ cung cấp **tên section**, chưa có transcript/Knowledge Check của Vertical Solution Application. Vì vậy nội dung trên là **comprehensive study synthesis**, không được trình bày như transcript.

### OpenAI public materials dùng để mở rộng vertical examples
- Financial Services: https://openai.com/solutions/industries/financial-services/
- Healthcare: https://openai.com/solutions/industries/healthcare/
- Retail: https://openai.com/solutions/industries/retail/
- Business Solutions: https://openai.com/solutions/

Khi bạn gửi lesson/KC của section này, các điểm course-specific nên được cập nhật vào file.
