# 02. Scenario Activity 1

> Course: **OpenAI Consultative Solutions Practitioner – Foundations**  
> Sub-course: **Early Opportunity Progression Application**  
> Section: **Scenario Activity 1**

---

## 1. Mục tiêu của activity

Scenario Activity 1 nhiều khả năng kiểm tra khả năng **chẩn đoán opportunity** trước khi đưa ra recommendation.

Vì bạn chưa cung cấp nội dung activity thực tế, file này không giả định customer scenario cụ thể. Thay vào đó, đây là một **complete solving framework** để bạn dùng khi course đưa scenario.

Activity 1 nên được tiếp cận theo câu hỏi:

> **What do we know about the opportunity, and what is still missing before it can progress?**

---

# 2. Activity 1 thường kiểm tra những skill nào?

Dựa trên toàn bộ Foundations flow trước đó, activity đầu tiên của một progression scenario thường yêu cầu kết hợp:

```text
Discovery evidence
Qualification
Workflow understanding
Stakeholder ownership
Use-case definition
Value hypothesis
Readiness
```

Tức là trọng tâm chưa nhất thiết là product.

---

# 3. Step 1 — Extract only facts

Tạo danh sách:

```text
FACTS
```

Chỉ ghi những gì scenario nói rõ.

Example:

```text
- Support team handles 5,000 tickets/week.
- Agents search multiple policy sources.
- Support leader wants faster response times.
```

Không thêm:

```text
- AI can save 50%.
```

nếu scenario không nói.

---

# 4. Step 2 — Identify assumptions

Assumptions thường đến từ:

```text
customer belief
seller hypothesis
benchmark
case study
estimated impact
unverified technical path
```

Example:

```text
- 70% of tickets may be eligible.
- AI may save 3 minutes per ticket.
```

Write them explicitly as:

```text
Assumption:
...
```

---

# 5. Step 3 — Identify unknowns

Unknowns drive discovery.

Common unknown categories:

```text
Workflow
User
Owner
Frequency
Baseline
Data
Integration
Permissions
Governance
Adoption
Quality bar
Success criteria
```

Example:

```text
Unknown:
Which policy source is authoritative?
```

---

# 6. Step 4 — Determine opportunity maturity

Use this scale:

## Stage A — Interest only

```text
AI interest
but no clear workflow
```

→ discovery

## Stage B — Problem identified

```text
workflow/pain exists
but evidence/owner/value unclear
```

→ deeper discovery / qualification

## Stage C — Use case formed

```text
workflow change is clear
value hypothesis emerging
```

→ validation

## Stage D — Route formed

```text
surface/capability/architecture understood
```

→ technical/deployment validation

## Stage E — Handoff ready

```text
evidence/value/readiness/route sufficiently clear
```

→ structured handoff

---

# 7. Step 5 — Write the workflow

Use:

```text
Input
→ Step
→ Decision
→ Handoff
→ Output
```

Example:

```text
Customer ticket
→ read context
→ search policy
→ interpret
→ draft
→ review
→ send
```

Then identify:

```text
where is the friction?
```

---

# 8. Step 6 — Identify stakeholder roles

Fill:

```text
Primary user:
...

Workflow owner:
...

Business sponsor:
...

Technical owner:
...

Governance stakeholder:
...
```

If any role matters but is missing, mark as readiness gap.

---

# 9. Step 7 — Build candidate use case

Use this pattern:

```text
[User]
uses AI to
[change a specific workflow step]
so that
[operational metric may improve].
```

Example:

```text
Support agents use AI to retrieve approved policy information
and draft first responses,
so average search/handling time may decrease.
```

---

# 10. Step 8 — Evaluate candidate use case

Use dimensions learned earlier:

```text
Value
Frequency / reach
Evidence
Complexity
Dependencies
Readiness
Testability
```

Do not convert this into a fake numeric score unless the course asks.

---

# 11. Step 9 — Build value hypothesis

Template:

```text
If [user]
uses AI to [workflow change],
then [operational metric] may improve,
which could contribute to [business outcome],
because [evidence].
```

Example:

```text
If agents use AI to retrieve policy and draft responses,
then handling time may decrease,
which could increase support capacity,
because policy search is a repeated delay.
```

---

# 12. Step 10 — Separate evidence from directional benefit

Do not say:

```text
AI will save 28 hours/week
```

unless measured.

Say:

```text
Based on assumptions X/Y/Z,
directional capacity unlocked could be...
```

The course emphasizes confidence proportional to evidence.

---

# 13. Step 11 — Assess readiness

Use checklist:

```text
Workflow clear?
Owner clear?
User group clear?
Data accessible?
Integration path?
Governance?
Adoption path?
Quality bar?
Success measures?
```

---

# 14. Step 12 — Decide whether to progress

Possible Activity 1 conclusions:

```text
Continue discovery
Validate further
Sequence later
Deprioritize for now
Proceed to routing
```

The answer depends on evidence.

---

# 15. Worked practice example

## Scenario

A finance team manually assembles a weekly business performance pack. Analysts gather data from spreadsheets and internal reports, summarize changes, and draft commentary. Leadership says the process is slow and wants AI support. A finance director owns the process, but there is no confirmed baseline for preparation time or agreement on which sources can be connected.

### Facts

```text
Weekly workflow
Multiple sources
Manual analysis/drafting
Named owner
Leadership wants improvement
```

### Unknowns

```text
Preparation baseline
Source access
Quality bar
```

### Candidate use case

```text
AI gathers approved source material,
analyzes changes,
and prepares first-draft performance commentary.
```

### Value hypothesis

```text
Reduce preparation time
→ increase finance capacity
```

### Readiness

```text
Owner ✅
Workflow ✅
Source access ?
Baseline ?
```

### Activity 1 conclusion

This is stronger than vague AI interest, but not ready for deployment.

Likely next progression:

```text
Validation session / representative workflow test
```

---

# 16. “Best answer” reasoning pattern

When multiple answers look possible, use:

```text
Which option is best supported by current evidence?
```

Not:

```text
Which option sounds most ambitious?
```

Common pattern:

```text
If answer assumes facts not in scenario
→ likely weaker

If answer directly addresses missing evidence
→ likely stronger
```

---

# 17. Knowledge Check clue table

| Scenario clue | Likely implication |
|---|---|
| “Interested in AI” only | More discovery |
| No owner | Ownership gap |
| Use case/value clear but requirements unclear | Validation |
| Replacing current tool | Migration discovery |
| Live integration / security | Technical validation |
| Owner/adoption/governance/success clear | Deployment readiness |
| Case study / benchmark only | Evidence is directional, not proof |

---

# 18. Frontend Developer analogy

Imagine product manager says:

> “AI could generate dashboards.”

You should not code yet.

You first ask:

```text
Who uses dashboard?
Current workflow?
Data?
Pain?
Frequency?
Success?
Owner?
```

Activity 1 is essentially:

> **Turn a fuzzy requirement into a qualified opportunity.**

---

# 19. Activity 1 answer template

```md
## 1. Opportunity summary
...

## 2. Evidence
...

## 3. Assumptions
...

## 4. Unknowns
...

## 5. Workflow
...

## 6. Stakeholders
...

## 7. Candidate use case
...

## 8. Value hypothesis
...

## 9. Readiness assessment
...

## 10. Biggest gap
...

## 11. Recommended progression
...
```

---

# 20. Common mistakes

## ❌ Fill gaps from general knowledge

Use only scenario evidence unless asked to research.

## ❌ Assume product fit from industry

Industry ≠ workflow.

## ❌ Treat customer enthusiasm as readiness

Interest is not ownership/data/governance.

## ❌ Skip the owner question

Owner matters for progression.

## ❌ Overclaim value

Directional hypothesis ≠ realized ROI.

---

# 21. Cheat Sheet

```text
ACTIVITY 1 = DIAGNOSE

Facts
↓
Assumptions
↓
Unknowns
↓
Workflow
↓
Stakeholders
↓
Use case
↓
Value
↓
Readiness
↓
What is missing?
↓
Next progression
```

One sentence:

> **Activity 1 is about earning the right to route the opportunity.**

---

# 22. Vocabulary

| Term | Nghĩa dễ hiểu |
|---|---|
| Diagnose | Chẩn đoán trạng thái opportunity |
| Opportunity maturity | Độ trưởng thành của cơ hội |
| Evidence gap | Bằng chứng còn thiếu |
| Qualification | Xác định cơ hội có đủ mạnh không |
| Directional value | Giá trị ước lượng theo hướng |
| Readiness gap | Điều kiện sẵn sàng còn thiếu |
| Testability | Khả năng test nhỏ để học |
| Progression | Bước đi tiếp theo |

---

# 23. Self-check

1. Activity 1 nên bắt đầu bằng product hay evidence?
2. Opportunity maturity có những stage nào?
3. Unknown khác assumption thế nào?
4. Một candidate use case tốt phải cụ thể ở đâu?
5. Value hypothesis viết như thế nào?
6. Readiness gồm những dimension nào?
7. Khi nào validation tốt hơn deployment?

---

## Nguồn và mức độ grounding

Hiện chưa có nội dung Scenario Activity 1 thực tế.

File này là **solving framework** tổng hợp từ các sub-course trước để bạn có thể xử lý activity khi xuất hiện.

> Khi bạn gửi Activity 1 screenshot/text, phần facts, assumptions, answer reasoning và Knowledge Check mapping cần được cập nhật chính xác theo scenario thật.
