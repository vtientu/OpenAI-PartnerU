# 01. Scenario Briefing

> Course: **OpenAI Consultative Solutions Practitioner – Foundations**  
> Sub-course: **Early Opportunity Progression Application**  
> Section: **Scenario briefing**

---

## 1. Mục tiêu của section

Đây là phần chuyển từ **học từng framework riêng lẻ** sang **đọc một opportunity như một tình huống thật**.

Trong các module trước, ta đã học cách:

```text
Discovery
→ Qualification
→ Use-case design
→ Business value
→ Solution routing
→ Vertical application
```

Ở sub-course này, các kỹ năng đó được ghép lại để trả lời một câu hỏi lớn hơn:

> **Given an early-stage customer opportunity, what should we conclude, what should we recommend, and what should happen next?**

Mục tiêu của Scenario Briefing là:

1. đọc customer context mà không vội chọn solution;
2. tách **facts, evidence, assumptions và unknowns**;
3. nhận diện workflow, stakeholder, value, readiness và route;
4. hiểu opportunity đang ở **stage nào**;
5. chuẩn bị reasoning cho các Scenario Activities tiếp theo.

---

# 2. “Early opportunity progression” là gì?

Có thể hiểu:

> **Early opportunity progression** = đưa một cơ hội AI từ mức “customer interest” đến một trạng thái đủ rõ để quyết định bước tiếp theo một cách có căn cứ.

Nó không nhất thiết có nghĩa:

```text
progress = sell / deploy immediately
```

Một progression tốt đôi khi là:

```text
Continue discovery
Run validation
Bring technical owner
Start migration discovery
Prepare structured handoff
```

Điểm quan trọng:

> **Progress the opportunity only as far as the evidence supports.**

---

# 3. Opportunity maturity ladder

Một way để hình dung:

```text
AI interest
↓
Workflow problem identified
↓
Evidence gathered
↓
Use case defined
↓
Value hypothesis formed
↓
Readiness assessed
↓
Route identified
↓
Critical assumptions validated
↓
Next owner / handoff ready
```

Customer có thể đang ở bất kỳ điểm nào trong ladder này.

Scenario activity thường kiểm tra khả năng nhận ra:

```text
"Where are we now?"
and
"What is the next credible step?"
```

---

# 4. Cách đọc scenario: 8 lớp thông tin

Khi nhận scenario, đừng đọc như một đoạn văn bình thường.

Hãy bóc thành 8 lớp:

```text
1. Customer priority
2. Workflow
3. Pain / friction
4. Stakeholders / ownership
5. Evidence
6. Value hypothesis
7. Readiness / constraints
8. Solution route / next step
```

---

## 4.1 Customer priority

Hỏi:

```text
What does the customer care about?
Why now?
```

Có thể là:

- cost;
- capacity;
- cycle time;
- quality;
- customer experience;
- risk;
- compliance;
- growth;
- modernization;
- vendor consolidation.

Đừng nhầm customer priority với AI use case.

Ví dụ:

```text
Priority:
Reduce support response time

Use case:
AI-assisted policy retrieval and drafting
```

---

## 4.2 Workflow

Map:

```text
Input
→ steps
→ decisions
→ handoffs
→ output
```

Nếu chưa map được workflow thì chưa đủ cơ sở để route solution.

---

## 4.3 Pain / friction

Tìm pain cụ thể:

```text
searching
manual rework
duplicate entry
long preparation
waiting for approval
inconsistent output
handoff delay
legacy bottleneck
```

Avoid generic statements:

```text
"They want to be more innovative."
```

Đó là motivation, chưa phải workflow pain.

---

## 4.4 Stakeholders / ownership

Tách:

```text
User
Workflow owner
Business sponsor
Technical owner
Governance / security stakeholder
Executive sponsor
```

Một opportunity có thể attractive nhưng chưa progress được nếu:

```text
no owner
```

---

## 4.5 Evidence

Evidence là thông tin đã được xác nhận.

Ví dụ:

```text
Agents spend 8 minutes searching policy.
Finance team creates the pack every week.
The workflow touches three internal systems.
```

Evidence mạnh hơn:

```text
"We observed..."
"The customer measured..."
"The workflow owner confirmed..."
```

---

## 4.6 Assumptions

Assumption = điều đang nghĩ có thể đúng nhưng chưa được chứng minh.

Ví dụ:

```text
AI can save 3 minutes per ticket.
70% of tickets are eligible.
Users will adopt the new flow.
The API integration is straightforward.
```

Assumption không phải lỗi.

Lỗi là:

```text
Assumption → treated as fact
```

---

## 4.7 Readiness / constraints

Kiểm tra:

```text
Workflow clarity
Owner
Data access
Integration
Security
Governance
Adoption
Approval
Latency
Success measures
```

---

## 4.8 Route / next step

Cuối cùng hỏi:

```text
Do we know enough to:
- continue discovery?
- validate?
- migrate?
- handoff to technical?
- handoff to deployment?
- prepare structured handoff?
```

---

# 5. Evidence vs Assumption vs Unknown

Một table nên dùng khi đọc scenario:

| Type | Meaning | Example |
|---|---|---|
| Evidence | Đã xác nhận | Agents search 3 systems |
| Assumption | Giả định có cơ sở | AI may reduce search time |
| Unknown | Chưa biết | Whether system supports live integration |

Mental model:

```text
Evidence
→ supports decision

Assumption
→ defines validation

Unknown
→ defines discovery question
```

---

# 6. Scenario extraction template

Dùng template này trước mọi activity:

```md
## Customer priority
...

## Current workflow
...

## Pain
...

## Users
...

## Owner
...

## Other stakeholders
...

## Evidence
...

## Assumptions
...

## Unknowns
...

## Candidate use case
...

## Value hypothesis
...

## Readiness
...

## Likely route
...

## Biggest unresolved risk
...

## Recommended next step
...
```

---

# 7. Opportunity qualification lens

Trước khi routing, hỏi:

```text
Is there a real problem?
Is it meaningful?
Is there evidence?
Is there an owner?
Is the workflow clear?
Is AI relevant to the problem?
```

Nếu chưa:

```text
Continue discovery
```

Không cần ép mọi scenario thành “solution recommendation”.

---

# 8. Use-case lens

Một candidate use case mạnh thường có:

```text
Clear user
+ clear workflow step
+ meaningful pain
+ repeatability/frequency
+ measurable outcome
+ enough readiness
```

Avoid:

```text
"Use AI for customer service."
```

Prefer:

```text
"Support agents use AI to retrieve approved policy information
and draft a response before human review."
```

---

# 9. Business-value lens

Map:

```text
Workflow change
→ operational metric
→ business outcome
```

Example:

```text
Less search time
→ lower average handling time
→ more support capacity
```

Avoid jumping:

```text
AI
→ revenue
```

without causal chain.

---

# 10. Solution-routing lens

Use the decision layers from the prior sub-course:

```text
User / product surface
Capability / architecture
Deployment / operating model
Progression motion
```

Questions:

```text
WHERE does AI appear?
WHAT must it do/connect to?
HOW/WHERE is it run and controlled?
WHAT should happen next?
```

---

# 11. Vertical lens

If scenario names an industry, ask:

```text
Which vertical workflow?
What data/source authority matters?
What trust bar applies?
What readiness constraint is industry/workflow-specific?
```

Do not use vertical stereotypes.

---

# 12. The “dominant uncertainty” principle

A scenario may contain many gaps.

Choose the one that most affects progression.

Examples:

```text
No workflow
→ discovery dominates

Workflow/value clear but approval/data unclear
→ validation dominates

Integration/security material
→ technical handoff dominates

Replacing existing tool
→ migration discovery dominates

Owner/adoption/governance/success ready
→ deployment handoff
```

---

# 13. Worked example — Customer Support

### Scenario

A support team handles a high volume of tickets. Agents search internal policies before responding. Leadership wants faster response time. The workflow owner is identified. It is not yet clear how policy data can be accessed or which responses require approval.

### Extraction

```text
Priority:
Faster customer response

Workflow:
Ticket → search policy → draft → review → send

Pain:
Search delay

Owner:
Known

Value:
Reduce search time → faster response

Unknown:
Data access
Approval rules
```

### Opportunity state

Use case/value are reasonably clear.

Requirements are not.

### Next step

```text
Validation session
```

Not deployment handoff.

---

# 14. Worked example — Broad AI interest

### Scenario

Hospital operations contact says the organization wants to “use AI”, but cannot name the workflow, user group or owner.

### Analysis

```text
AI interest ✅
Specific workflow ❌
User ❌
Owner ❌
Value hypothesis ❌
```

### Next step

```text
More discovery
```

The correct progression is not to pick a healthcare solution.

---

# 15. Worked example — Engineering modernization

### Scenario

Engineering leadership wants to reduce code review, testing and modernization bottlenecks. The repository environment and security review still need technical assessment.

### Analysis

```text
Workflow:
Software engineering

Surface:
Codex

Value:
Engineering capacity / cycle time

Unknown:
Repo/security integration

Next:
Technical validation / technical handoff
```

---

# 16. Frontend Developer analogy

Think of a vague feature request:

> “Add AI to onboarding.”

Before coding, you would need:

```text
User?
Current onboarding?
Pain?
Data?
UX?
Success metric?
Permissions?
```

Scenario briefing is the consultative equivalent of writing a strong technical requirement before implementation.

---

# 17. Common mistakes

## ❌ Read the scenario and immediately choose product

First extract context.

## ❌ Treat all stated numbers as evidence

Check whether they are customer-confirmed or merely estimates.

## ❌ Ignore missing owner

Ownership is often a progression blocker.

## ❌ Focus only on technical feasibility

Opportunity progression also depends on value and readiness.

## ❌ Overlook wording like “may”, “could”, “expects”

These often signal hypotheses, not facts.

---

# 18. Exam / activity strategy

When reading activity:

```text
Step 1: underline facts
Step 2: circle assumptions
Step 3: identify missing information
Step 4: map workflow
Step 5: identify value
Step 6: identify route
Step 7: identify dominant uncertainty
Step 8: choose next credible action
```

---

# 19. Cheat Sheet

```text
SCENARIO BRIEFING

Priority
↓
Workflow
↓
Pain
↓
User / Owner
↓
Evidence
↓
Use case
↓
Value
↓
Readiness
↓
Route
↓
Dominant uncertainty
↓
Next step
```

One sentence:

> **Do not solve the scenario before you structure the scenario.**

---

# 20. Vocabulary

| Term | Nghĩa dễ hiểu |
|---|---|
| Scenario | Tình huống customer giả lập |
| Briefing | Phần cung cấp context trước activity |
| Opportunity progression | Đưa opportunity sang bước hợp lý tiếp theo |
| Dominant uncertainty | Điểm chưa chắc chắn quan trọng nhất |
| Evidence | Bằng chứng xác nhận |
| Assumption | Giả định chưa kiểm chứng |
| Unknown | Thông tin chưa có |
| Opportunity maturity | Mức trưởng thành của opportunity |
| Progression motion | Hành động tiếp theo |
| Structured handoff | Handoff đầy đủ context/evidence |

---

# 21. Self-check

1. Early opportunity progression khác deployment thế nào?
2. Scenario cần bóc thành những lớp nào?
3. Evidence khác assumption và unknown thế nào?
4. Dominant uncertainty dùng để làm gì?
5. Khi nào more discovery là progression đúng?
6. Khi nào technical handoff là hợp lý?
7. Vì sao không nên chọn product ngay khi đọc scenario?

---

## Nguồn và mức độ grounding

Bạn hiện mới cung cấp **tên 3 section**, chưa có nội dung Scenario Briefing thực tế của PartnerU.

Vì vậy file này là **study framework đầy đủ để chuẩn bị học section**, dựa trên các framework và Knowledge Checks của các sub-course trước trong cuộc học của bạn.

> Khi bạn gửi screenshot/text của Scenario Briefing thực tế, file này nên được cập nhật bằng customer facts, scenario wording, stakeholders và constraints đúng theo course.
