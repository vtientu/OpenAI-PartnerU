# 03. Connect Vertical Value, Trust, and Readiness

> Course: **OpenAI Consultative Solutions Practitioner – Foundations**  
> Sub-course: **Vertical Solution Application**  
> Section: **Connect vertical value, trust, and readiness**

---

## 1. Mục tiêu

Một vertical solution không nên được recommend chỉ vì:

```text
AI can do the task.
```

Cần ba lớp cùng hợp lý:

```text
VALUE
Why does it matter?

TRUST
Why is it acceptable and reliable enough?

READINESS
Can this customer move forward now?
```

Mental model:

```text
Value
+ Trust
+ Readiness
→ Credible vertical recommendation
```

---

# 2. Value — why should the business care?

Value starts from workflow change.

```text
Workflow pain
→ AI-enabled change
→ operational outcome
→ business outcome
```

Examples:

### Finance

```text
Manual research
→ faster source gathering/analysis
→ shorter preparation cycle
→ more analyst capacity
```

### Retail

```text
Associates search product/policy info
→ faster trusted answers
→ faster service + consistency
→ better shopper experience / lower training burden
```

### Healthcare admin

```text
Repeated rewriting
→ draft assistance
→ less admin time
→ more staff capacity
```

---

# 3. Value must be customer-specific

Public industry examples are not a value estimate.

Bad:

```text
Retail AI improves conversion.
```

Maybe, but not established for this customer.

Better:

```text
This workflow currently creates X friction.
If AI reduces Y step, metric Z should move.
We will validate the size of that improvement.
```

Use prior-course discipline:

```text
Known
Assumed
Need to validate
```

---

# 4. Trust — broader than security

Trust includes:

```text
accuracy
source quality
privacy
security
permissions
governance
review
auditability
reliability
escalation
```

The mix depends on workflow consequence.

Question:

> **What has to be true for the customer to use the output confidently?**

---

# 5. Trust by workflow consequence

## Low consequence example

Internal brainstorm.

Trust needs may be lighter:

```text
basic privacy
user judgment
```

## Higher consequence example

Output informs regulated or sensitive workflow.

May require:

```text
approved sources
access controls
citations
review
auditability
clear decision boundary
```

Do not make a blanket rule based only on vertical.

Within one vertical, consequence varies.

---

# 6. Readiness — can they actually move?

Readiness dimensions:

```text
Workflow clarity
Owner
Data
Integration
Adoption
Governance
Success measurement
Technical feasibility
```

A strong value hypothesis with no owner is not ready.

A trusted technical platform with no workflow is not ready.

---

# 7. The three-way matrix

## High Value + High Trust + High Readiness

```text
Strong candidate to progress.
```

Could move to:

```text
structured handoff / deployment planning
```

depending on route.

---

## High Value + Low Trust

Example:

```text
big efficiency opportunity
but unclear approval/data rules
```

Next step:

```text
governance/validation
```

Not full rollout.

---

## High Value + Low Readiness

Example:

```text
meaningful pain
but data inaccessible / no owner
```

Next:

```text
resolve readiness gaps
```

---

## Low Value + High Readiness

Easy does not mean worthwhile.

Possible outcome:

```text
deprioritize
or find a stronger workflow
```

---

## Low Value + Low Trust + Low Readiness

Likely:

```text
not a strong opportunity yet
```

---

# 8. Trust is part of value realization

Trust is not merely a legal checkbox.

If users do not trust output:

```text
adoption falls
→ usage falls
→ value falls
```

If review burden is too heavy:

```text
time saved by AI
-
time spent reviewing
→ maybe no net value
```

Therefore:

```text
Trust design
can change economics.
```

---

# 9. Readiness affects timing, not necessarily attractiveness

A use case can be:

```text
high potential value
low current readiness
```

That does not mean “bad”.

It may mean:

```text
sequence later
or
run prerequisite validation first
```

This links back to prioritization.

---

# 10. Financial Services example

OpenAI public materials emphasize security, control, connected financial data, research/analysis, document processing and system modernization.

### Candidate workflow

Analyst research memo.

### Value

```text
less source gathering
faster analysis
more analyst capacity
```

### Trust

```text
approved data
traceable sources
review
data control
```

### Readiness

```text
connected sources?
review criteria?
owner?
success baseline?
```

### Credible next step

If source access and review criteria unknown:

```text
validation
```

---

# 11. Healthcare example

Public OpenAI materials emphasize enterprise controls, trusted clinical sources, authorized patient context, and support for clinical/research/admin workflows.

### Candidate workflow

Administrative documentation.

### Value

```text
reduce paperwork
free staff time
```

### Trust

```text
privacy
authorized access
review
approved knowledge
```

### Readiness

```text
workflow owner
data path
governance
success signals
```

Again:

> High value does not bypass trust/readiness.

---

# 12. Retail example

Candidate:

```text
store associate knowledge assistant
```

### Value

```text
faster answers
lower training burden
service consistency
```

### Trust

```text
current product/policy data
avoid stale information
appropriate access
```

### Readiness

```text
source integration
associate adoption
workflow owner
```

---

# 13. Trust/readiness questions by vertical

These are **question prompts**, not stereotypes.

## Finance

```text
Which data is approved?
What needs traceability?
Who reviews?
What control/audit requirements apply?
```

## Healthcare

```text
What patient/context access is authorized?
Which evidence sources are trusted?
Where is human review required?
What privacy/governance applies?
```

## Retail

```text
How current is product/inventory data?
Does advice need real-time availability?
Who owns store adoption?
What happens if information is stale?
```

---

# 14. Value hypothesis + trust hypothesis + readiness hypothesis

A useful extension:

### Value hypothesis

```text
If workflow changes,
metric X may improve,
creating outcome Y.
```

### Trust hypothesis

```text
If output is grounded in approved sources
and reviewed at boundary Z,
users can rely on it for this task.
```

### Readiness hypothesis

```text
If data access, owner and integration are confirmed,
customer can pilot this workflow.
```

This separates three uncertainties.

---

# 15. Evidence table

| Dimension | Known | Assumed | Validate |
|---|---|---|---|
| Value | Current prep takes hours | AI can reduce prep | Representative task timing |
| Trust | Approved sources exist | Output quality sufficient | Quality evaluation |
| Readiness | Business owner named | Data can connect | Technical review |

This is far stronger than:

```text
"Use case looks good."
```

---

# 16. Tradeoff: automation vs trust

More automation may:

```text
increase potential efficiency
```

but can also:

```text
increase trust/control requirements
```

Example ladder:

```text
Suggest
→ Draft
→ Recommend
→ Act with approval
→ Act autonomously
```

As autonomy grows, evaluate:

```text
error consequence
permissions
approval
monitoring
escalation
```

---

# 17. Tradeoff: latency vs architecture complexity

A real-time workflow may create value, but demand:

```text
live integration
low latency
high availability
```

If value is modest, this may be disproportionate.

Ask:

```text
Would near-real-time materially change the business outcome?
```

Maybe a batch workflow is enough.

---

# 18. Frontend Developer analogy

Feature idea:

> AI suggests checkout recovery message.

Value:

```text
could improve completion rate
```

Trust:

```text
must not invent price/policy
```

Readiness:

```text
need cart state + policy source + experiment metric
```

If policy integration is missing:

```text
high idea value
≠
ready feature
```

---

# 19. Common mistakes

## ❌ Treat trust as yes/no

Trust is a design problem with controls and boundaries.

## ❌ Treat readiness as technical only

Owner/adoption/success metrics matter.

## ❌ Use industry benchmark as customer value

External evidence is directional.

## ❌ Ignore cost of review

Human review can erase expected benefit.

## ❌ Over-engineer high-trust path before proving value

Find proportionate validation.

---

# 20. Decision framework

```text
1. Is value meaningful?
2. Is value evidenced?
3. What trust bar applies?
4. What controls satisfy it?
5. Is customer ready?
6. What readiness gaps exist?
7. Is solution complexity proportional?
8. What is the next validation step?
```

---

# 21. Cheat Sheet

```text
VALUE
= Why care?

TRUST
= Why believe/use it?

READINESS
= Can we move?
```

Strong opportunity:

```text
Meaningful value
+ appropriate trust controls
+ sufficient readiness
```

---

# 22. Vocabulary

| Term | Nghĩa dễ hiểu |
|---|---|
| Value hypothesis | Giả thuyết giá trị |
| Trust requirement | Điều kiện để output được tin/dùng |
| Readiness | Mức sẵn sàng |
| Grounding | Dựa output trên nguồn/context |
| Auditability | Khả năng kiểm tra/truy vết |
| Decision boundary | Điểm phân chia AI vs human decision |
| Adoption | Mức user thực sự sử dụng |
| Governance path | Cách vượt review/controls |
| Proportionality | Complexity tương xứng value/readiness |
| Directional | Ước lượng/hướng, chưa phải proof |

---

# 23. Self-check

1. Value, trust, readiness khác nhau thế nào?
2. High value + low readiness nên làm gì?
3. Vì sao trust ảnh hưởng realized value?
4. More automation làm trust requirements thay đổi thế nào?
5. Làm sao tránh dùng vertical benchmark như customer proof?
6. Bạn có thể viết 3 hypotheses riêng cho một use case không?

---

## Nguồn và mức độ grounding

PartnerU source available: section title only.

OpenAI public vertical context:
- Financial Services: https://openai.com/solutions/industries/financial-services/
- Healthcare: https://openai.com/solutions/industries/healthcare/
- Retail: https://openai.com/solutions/industries/retail/
- Business Solutions/security/control framing: https://openai.com/solutions/

> Comprehensive study synthesis; không phải PartnerU transcript.
