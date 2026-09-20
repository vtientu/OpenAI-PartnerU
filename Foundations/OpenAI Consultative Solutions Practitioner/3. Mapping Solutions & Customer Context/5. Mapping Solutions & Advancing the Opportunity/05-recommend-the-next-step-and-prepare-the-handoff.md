# 05. Recommend the Next Step and Prepare the Handoff

> Course: **OpenAI Consultative Solutions Practitioner – Foundations**  
> Sub-course: **Mapping Solutions & Advancing the Opportunity**  
> Section: **Recommend the next step and prepare the handoff**

---

## 1. Mục tiêu

Khi đã hiểu route và credibility, nhiệm vụ tiếp theo là:

> **Chọn next action phù hợp với uncertainty còn lại, rồi handoff context một cách có cấu trúc.**

Consultative selling không phải lúc nào cũng “advance as fast as possible”.

Đúng hơn là:

```text
Advance only as far as the evidence supports.
```

---

# 2. Next step phải giải quyết uncertainty lớn nhất

Mental model:

```text
What is still unclear?
        ↓
What risk does that uncertainty create?
        ↓
Who is best placed to resolve it?
        ↓
What action should happen next?
```

---

# 3. Các progression motions chính

Knowledge Checks cho thấy các motion sau:

- **More / continue discovery**
- **Validation session**
- **Migration discovery**
- **Technical handoff / involve technical owner**
- **Deployment handoff**
- **Structured handoff**

Mỗi motion có trigger khác nhau.

---

# 4. More / Continue Discovery

Use when customer has:

```text
broad AI interest
but no clear workflow
no user group
no owner
no value hypothesis
```

### Knowledge Check example

> Hospital operations contact says team is “interested in AI,” but cannot name workflow, user group, or owner.

→ **More discovery**

Another:

> Customer has broad AI interest but no clear workflow, owner, or value hypothesis.

→ **Continue discovery**

Rule:

```text
No concrete problem
→ Don't route yet.
```

---

# 5. Validation Session

Use when:

```text
Use case clear
Value hypothesis clear
BUT
requirements / data / approvals / review expectations uncertain
```

### Example

> A use case and value hypothesis are clear, but data access, approval steps, and review expectations are still uncertain.

→ **Validation session**

Purpose:

```text
turn assumptions into evidence
```

Typical agenda:

```text
Review workflow
Confirm data sources
Clarify approvals
Clarify review expectations
Test representative tasks
Define success signals
```

---

# 6. Migration Discovery

Use when customer is:

```text
replacing existing AI/automation tool
consolidating pilots/vendors
moving from current state to target state
```

### Examples

> Replacing an existing AI tool and needs to map current and target workflows.

→ Migration discovery

> Replacing multiple AI pilots and wants to consolidate workflows and vendors.

→ Migration discovery

Key question:

```text
What exists today?
What should target state become?
What must migrate/change/decommission?
```

---

# 7. Technical Handoff / Technical Owner

Use when material questions involve:

```text
technical feasibility
data access
integration
identity
permissions
security
latency
deployment
```

### Example

> Solution depends on ticketing integration, permissioned data, and customer identity rules.

→ **Technical handoff**

Another:

> Technical feasibility, data access, integration, or security questions are material.

→ **Involve appropriate technical/deployment owner**

Purpose:

```text
resolve technical uncertainty before making stronger commitment
```

---

# 8. Deployment Handoff

Use when route is much more mature:

```text
business owner clear
adoption path clear
governance review identified/completed
success measures clear
rollout context understood
```

### Example

> Employee-facing rollout opportunity has a clear business owner, adoption path, governance review, and success measures.

→ **Deployment handoff**

This is not the same as technical handoff.

Technical handoff asks:

```text
Can/how should this technically work?
```

Deployment handoff asks:

```text
How do we operationalize/roll out this ready opportunity?
```

---

# 9. Structured Handoff

When:

```text
evidence
value
readiness
routing
```

are clear enough for the next owner to validate or progress, prepare a structured handoff.

### Knowledge Check example

> Evidence, value, readiness, and routing are clear enough for the next owner to validate.

→ **Prepare a structured handoff**

---

# 10. Strong handoff contents

A handoff should preserve:

## Customer context

```text
Priority
Business problem
Relevant vertical/workflow context
```

## Workflow evidence

```text
Current workflow
Pain
Frequency/scale
Users
Handoffs
```

## Value

```text
Value hypothesis
Business outcome
Evidence
Success signals
```

## Route

```text
Recommended surface
Capability requirements
Architecture requirements
Operating/deployment needs
```

## Readiness

```text
Owner
Data
Adoption
Governance
Technical path
```

## Uncertainty

```text
Known
Assumed
Needs validation
```

## Next step

```text
Action
Owner
Purpose
Expected evidence
```

---

# 11. Keep evidence and assumptions separate

Bad handoff:

```text
"70% of workflows are eligible."
```

if it was only an estimate.

Good:

```text
Assumption:
Approximately 70% may be eligible.
Validate during representative workflow review.
```

Handoffs often fail when assumptions become facts.

---

# 12. Handoff template

```md
## Customer priority
...

## Current workflow
...

## Workflow pain
...

## Users / stakeholders
...

## Evidence
...

## Value hypothesis
...

## Recommended route
...

## User/product surface
...

## Capability requirements
...

## Architecture requirements
...

## Deployment / operating requirements
...

## Readiness
...

## Assumptions / open questions
...

## Success signals
...

## Recommended next step
...

## Next owner(s)
...
```

---

# 13. Next-step decision table

| Opportunity state | Most credible action |
|---|---|
| Broad AI interest, no workflow/owner/value | More discovery |
| Use case/value clear, requirements unclear | Validation session |
| Replacing existing tool / consolidating pilots | Migration discovery |
| Material integration/data/security questions | Technical handoff |
| Rollout has owner/adoption/governance/success measures | Deployment handoff |
| Evidence/value/readiness/routing sufficiently clear | Structured handoff |

---

# 14. Example end-to-end

### Context

Customer support team wants faster policy responses.

### Current state

```text
Search multiple sources
→ interpret
→ draft
→ escalate some cases
```

### Value hypothesis

```text
Less search time
→ faster response
→ more capacity
```

### Route

```text
AI-assisted retrieval + draft
```

### Open issues

```text
Approved policy access?
Review expectations?
Integration?
```

### Next action

Because use case/value are clear but requirements remain uncertain:

→ **Validation session**

After validation reveals integration and identity complexity:

→ **Technical handoff**

After technical path + governance + adoption plan are clear:

→ **Deployment handoff**

This shows progression can happen in stages.

---

# 15. Example — Frontend Developer

You propose embedded AI onboarding.

State A:

```text
"Users might want AI."
No user group, no workflow.
```

→ Discovery

State B:

```text
Workflow clear, but app data access + approval rules unclear.
```

→ Validation

State C:

```text
Needs CRM + identity + permission mapping.
```

→ Technical handoff

State D:

```text
Owner, success metrics, adoption, governance all clear.
```

→ Deployment handoff

---

# 16. Common mistakes

## ❌ “Next step = demo”

A demo may not address the biggest uncertainty.

## ❌ Premature deployment handoff

If data/security/integration still unclear, technical validation may come first.

## ❌ Continue discovery forever

Once enough evidence exists, progress.

## ❌ Handoff without assumptions

Next owner may unknowingly treat guesses as facts.

## ❌ Handoff only product name

```text
"Customer wants ChatGPT Work."
```

This loses why, workflow, value, readiness and constraints.

---

# 17. Knowledge Check mappings

```text
Evidence/value/readiness/routing clear
→ Structured handoff

Use case/value clear; requirements/approvals uncertain
→ Validation session

Replacing existing AI/automation tool
→ Migration discovery

Technical/data/integration/security material
→ Technical owner / technical handoff

Broad AI interest, no workflow/owner/value
→ Continue discovery

Employee rollout with owner/adoption/governance/success
→ Deployment handoff
```

---

# 18. Cheat Sheet

```text
VAGUE
→ Discovery

CLEAR USE CASE, UNCLEAR REQUIREMENTS
→ Validation

REPLACE / CONSOLIDATE
→ Migration discovery

INTEGRATION / DATA / SECURITY
→ Technical handoff

READY FOR ROLLOUT
→ Deployment handoff

ENOUGH CONTEXT FOR NEXT OWNER
→ Structured handoff
```

---

# 19. Vocabulary

| Term | Nghĩa dễ hiểu |
|---|---|
| Progression motion | Hành động giúp opportunity tiến đúng bước |
| Validation session | Buổi kiểm chứng requirements/assumptions |
| Migration discovery | Discovery cho current → target state |
| Technical handoff | Chuyển sang technical owner |
| Deployment handoff | Chuyển sang rollout/operations owner |
| Structured handoff | Handoff đầy đủ evidence/context |
| Current state | Trạng thái hiện tại |
| Target state | Trạng thái mong muốn |
| Open question | Câu hỏi chưa được giải quyết |
| Next owner | Người/team xử lý bước tiếp theo |

---

# 20. Self-check

1. Khi nào discovery vẫn là next step đúng?
2. Validation khác technical handoff thế nào?
3. Migration discovery được trigger bởi điều gì?
4. Deployment handoff cần dấu hiệu readiness nào?
5. Structured handoff phải giữ lại những gì?
6. Vì sao assumptions không được biến thành facts?

---

## Grounding

Section này bám trực tiếp các Knowledge Checks bạn đã cung cấp về:
- continue discovery;
- validation session;
- migration discovery;
- technical owner/handoff;
- deployment handoff;
- structured handoff.

> Study synthesis, không phải transcript PartnerU.
