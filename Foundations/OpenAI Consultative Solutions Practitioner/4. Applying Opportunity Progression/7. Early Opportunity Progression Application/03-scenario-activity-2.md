# 03. Scenario Activity 2

> Course: **OpenAI Consultative Solutions Practitioner – Foundations**  
> Sub-course: **Early Opportunity Progression Application**  
> Section: **Scenario Activity 2**

---

## 1. Mục tiêu của activity

Nếu Activity 1 thiên về **diagnose the opportunity**, Activity 2 hợp lý nhất để thực hành:

> **Turn a qualified opportunity into a credible route, recommendation, and next step.**

Vì chưa có scenario chính thức từ PartnerU, file này không tự tạo “đáp án course”.

Nó cung cấp một complete framework để giải Activity 2 khi bạn nhận được scenario.

---

# 2. Activity 2 reasoning flow

```text
Qualified opportunity
↓
Workflow change
↓
Surface
↓
Capability / architecture
↓
Deployment / operating model
↓
Credibility test
↓
Value + trust + readiness
↓
Recommendation
↓
Progression motion
↓
Handoff
```

---

# 3. Step 1 — Reconfirm problem before routing

Before route:

```text
What problem is actually being solved?
```

Write one sentence:

```text
[User] struggles with [workflow pain],
which affects [operational/business outcome].
```

If you cannot write this, go back to discovery.

---

# 4. Step 2 — Choose interaction model / surface

Use prior logic:

```text
Iterative exploration/drafting
→ ChatGPT Chat

Delegated multi-step knowledge work
→ ChatGPT Work

Software engineering
→ Codex

Embedded product/process
→ API-built solution

Multiple distinct interaction models
→ Combined solution
```

Remember:

```text
Surface answers WHERE.
```

---

# 5. Step 3 — Define capability

Ask:

```text
What must AI do?
```

Examples:

```text
retrieve
summarize
analyze
draft
classify
use apps
take action
escalate
ask approval
schedule
```

---

# 6. Step 4 — Define architecture

Ask:

```text
What must it connect to?
```

Examples:

```text
CRM
ticketing
ERP
knowledge base
repository
identity system
permissioned data
live equipment source
```

Also:

```text
What latency?
What data freshness?
What identity?
What read/write permissions?
```

---

# 7. Step 5 — Define deployment and operating model

Ask:

```text
Hosted or customer-managed?
Who operates it?
Who reviews?
What actions need approval?
How are exceptions handled?
What monitoring is needed?
```

A self-managed/open-weight requirement belongs here.

---

# 8. Step 6 — Check trust

Trust questions:

```text
What data is sensitive?
Which sources are authoritative?
What must be traceable?
Where is human review?
What if output is wrong?
Who approves action?
```

---

# 9. Step 7 — Check readiness

```text
Owner?
Data?
Integration?
Governance?
Adoption?
Success metrics?
Technical feasibility?
```

---

# 10. Step 8 — Test proportionality

Ask:

```text
Is this route too complex for the evidence/value/readiness?
```

Example:

```text
Weak value hypothesis
+ custom real-time multi-system agent
```

may be overdesigned.

A smaller first route may be:

```text
AI-assisted draft
+ human review
```

---

# 11. Step 9 — Build recommendation

Template:

```text
Because [customer priority],
the current [workflow] creates [pain].

We recommend [surface / pattern]
to change [workflow step].

This could improve [metric]
and contribute to [business outcome].

The route requires [data/integration/trust controls].

The remaining uncertainty is [X].

The next step is [progression motion]
to validate [X].
```

---

# 12. Step 10 — Choose progression motion

Use this mapping:

```text
No clear workflow/owner/value
→ More discovery

Use case/value clear; requirements unclear
→ Validation session

Replacing/consolidating existing tools
→ Migration discovery

Integration/data/security material
→ Technical handoff

Owner/adoption/governance/success ready
→ Deployment handoff

Evidence/value/readiness/routing clear enough
→ Structured handoff
```

---

# 13. Worked practice example — Retail Support

## Scenario

Retailer wants associates to answer product and policy questions faster. Associates currently search several internal sources. The customer wants the experience embedded into an existing associate app. Product/policy data access and identity permissions still need technical confirmation.

### Problem

```text
Associates lose time searching
→ slower shopper support
```

### Surface

```text
Embedded app experience
→ API-based solution
```

### Capability

```text
retrieve current approved information
summarize
generate concise answer
```

### Architecture

```text
associate app
product/policy sources
identity
permissions
```

### Trust

```text
approved sources
freshness
avoid stale policy
```

### Readiness gap

```text
data access + identity integration
```

### Recommendation

A credible route is embedded AI assistance in the associate app.

### Next step

```text
Technical validation / technical handoff
```

not deployment yet.

---

# 14. Worked practice example — Finance Work

## Scenario

Finance team has a clear weekly reporting workflow and named owner. It wants AI to gather approved sources, analyze variance and prepare a review-ready pack. Review criteria are clear, but source integrations have not been validated.

### Surface

```text
ChatGPT Work
```

because workflow is:

```text
delegated
multi-step
finished artifact
```

### Architecture requirement

```text
approved source access
```

### Trust

```text
source integrity
finance review
```

### Next step

```text
validation / technical validation
```

depending on option wording.

---

# 15. Worked practice example — Migration

## Scenario

Customer has three AI pilots from different vendors and wants one target-state workflow.

### Dominant issue

```text
Current-state → target-state transition
```

### Next step

```text
Migration discovery
```

Before final route, need:

```text
current tools
users
workflows
dependencies
data
target capability
decommission/migration constraints
```

---

# 16. Worked practice example — Deployment-ready employee use case

## Scenario

Employee knowledge workflow has:

```text
clear business owner
defined user group
approved data
governance review
adoption plan
success measures
```

Route already established.

### Next step

```text
Deployment handoff
```

---

# 17. How to build a handoff

Activity 2 may ask what information should move to the next owner.

Use:

```md
## Customer priority
...

## Workflow
...

## Evidence
...

## Value hypothesis
...

## User/product surface
...

## Capability requirements
...

## Architecture requirements
...

## Deployment/operating model
...

## Trust requirements
...

## Readiness
...

## Assumptions
...

## Open questions
...

## Success signals
...

## Recommended next step
...

## Next owner
...
```

---

# 18. Structured recommendation example

```text
The customer’s goal is to reduce support response time.

Agents currently spend meaningful time searching approved policies.

A credible route is AI-assisted retrieval and drafting
inside the existing support workflow.

The solution needs approved policy access,
ticket context, identity-aware permissions,
and human review for high-risk cases.

The value hypothesis is lower search/handling time
leading to more support capacity.

Because integration and approval requirements remain unclear,
the next step should be a validation session with the workflow
and technical owners.
```

This is much stronger than:

```text
"Use AI for support."
```

---

# 19. Confidence language

Use the right language:

## Facts

```text
"The customer confirmed..."
```

## Hypothesis

```text
"This could..."
"The route appears credible if..."
```

## Unknown

```text
"We still need to validate..."
```

## Recommendation

```text
"The next credible step is..."
```

---

# 20. Common distractors in Activity 2

## Distractor A — Most ambitious solution

Often wrong because not proportional.

## Distractor B — Product name without reasoning

Weak unless workflow clearly maps.

## Distractor C — ROI claim before validation

Overclaims.

## Distractor D — Deployment when technical blockers remain

Too early.

## Distractor E — More discovery when enough evidence already exists

Too slow.

The correct answer usually matches:

```text
current maturity + dominant uncertainty
```

---

# 21. Activity 2 solving template

```md
## 1. Customer priority
...

## 2. Problem/workflow
...

## 3. Value hypothesis
...

## 4. Recommended surface
...

## 5. Capabilities
...

## 6. Architecture
...

## 7. Deployment / operating requirements
...

## 8. Trust
...

## 9. Readiness
...

## 10. Biggest uncertainty
...

## 11. Recommendation
...

## 12. Next step
...

## 13. Handoff owner
...
```

---

# 22. Final Foundations integration

By this point, the complete practitioner flow is:

```text
Discover
↓
Qualify
↓
Translate into use cases
↓
Evaluate
↓
Prioritize
↓
Define success
↓
Build value hypothesis
↓
Estimate directional benefit
↓
Route solution
↓
Test credibility
↓
Apply vertical context
↓
Recommend next step
↓
Handoff
```

Early Opportunity Progression Application is where you prove you can use the **whole chain**.

---

# 23. Frontend Developer analogy

Think of the course as software delivery:

```text
Discovery
= requirements

Use case
= feature definition

Value
= product outcome

Routing
= architecture choice

Credibility
= feasibility review

Vertical context
= domain constraints

Progression
= choose next engineering phase

Handoff
= design/implementation handoff
```

Activity 2 is similar to turning a validated product requirement into:

```text
architecture + risks + next implementation step
```

---

# 24. Cheat Sheet

```text
ACTIVITY 2 = ROUTE + PROGRESS

Problem
↓
Value
↓
Surface
↓
Capability
↓
Architecture
↓
Operating model
↓
Trust
↓
Readiness
↓
Biggest uncertainty
↓
Recommendation
↓
Next step
↓
Handoff
```

One sentence:

> **Recommend only what the evidence can support, and make the next step reduce the most important remaining uncertainty.**

---

# 25. Vocabulary

| Term | Nghĩa dễ hiểu |
|---|---|
| Route | Hướng solution |
| Surface | Nơi user tương tác |
| Capability | Solution phải làm gì |
| Architecture | Kết nối hệ thống/data |
| Deployment | Cách/nơi chạy |
| Operating model | Cách vận hành/kiểm soát |
| Proportionality | Complexity tương xứng value/readiness |
| Recommendation | Đề xuất dựa trên evidence |
| Handoff | Chuyển context sang owner tiếp theo |
| Confidence language | Cách nói phù hợp mức evidence |

---

# 26. Self-check

1. Activity 2 khác Activity 1 ở đâu?
2. Surface trả lời câu hỏi nào?
3. Capability khác architecture thế nào?
4. Deployment/operating model quan tâm gì?
5. Khi nào migration discovery là next step?
6. Khi nào technical handoff?
7. Khi nào deployment handoff?
8. Recommendation tốt phải nêu uncertainty không?

---

## Nguồn và mức độ grounding

Hiện chưa có Scenario Activity 2 thực tế từ PartnerU.

File này là **complete application framework** dựa trên toàn bộ các section và Knowledge Checks đã học trước đó.

> Khi bạn gửi Activity 2 thực tế, chúng ta nên cập nhật file bằng exact scenario facts, course-specific answer choices và reasoning.
