# 02. Adapt Solution Patterns to a Vertical Workflow

> Course: **OpenAI Consultative Solutions Practitioner – Foundations**  
> Sub-course: **Vertical Solution Application**  
> Section: **Adapt solution patterns to a vertical workflow**

---

## 1. Mục tiêu

Sau khi đọc vertical context, ta chưa nên copy một generic AI pattern rồi gọi đó là solution.

Mục tiêu section:

1. nhận diện một **solution pattern**;
2. map pattern vào bước workflow cụ thể;
3. điều chỉnh theo user, data, system, trust, latency và review;
4. xác định surface/architecture phù hợp;
5. tránh “same use case everywhere”.

Core principle:

> **Reuse the pattern, not the assumptions.**

---

# 2. Solution pattern là gì?

Solution pattern = một dạng capability/workflow lặp lại across industries.

Ví dụ:

```text
Retrieve
Summarize
Draft
Classify
Extract
Analyze
Recommend
Transform
Take action
Orchestrate multi-step work
```

Patterns có thể combine:

```text
Retrieve + summarize + draft
```

hoặc:

```text
Classify + route + act
```

hoặc:

```text
Gather + analyze + produce artifact
```

---

# 3. Generic pattern không phải final solution

Pattern:

```text
Retrieve + draft
```

có thể trở thành:

### Finance

```text
Retrieve approved filings/internal research
→ draft analysis memo
→ analyst review
```

### Healthcare

```text
Retrieve approved clinical/organizational sources
→ draft documentation/instruction
→ professional review
```

### Retail

```text
Retrieve product/policy information
→ draft associate response
→ associate uses it with shopper
```

Same pattern.

Different:

```text
source
user
quality bar
risk
surface
review
outcome
```

---

# 4. The adaptation stack

Adapt a pattern across 8 layers:

```text
1. Workflow step
2. User
3. Input/source
4. Capability
5. Surface
6. Architecture
7. Trust/operating controls
8. Business outcome
```

---

# 5. Step 1 — Anchor to workflow step

Bad:

```text
Use AI for research.
```

Better:

```text
AI gathers approved source material before analyst prepares weekly memo.
```

The narrower statement lets you evaluate:

```text
input
frequency
handoff
output
metric
```

---

# 6. Step 2 — Define user role

The same output can mean different things based on user.

Example:

```text
Product recommendation
```

For:

```text
Store associate
```

it may be decision support.

For:

```text
Shopper
```

it becomes a customer-facing experience.

For:

```text
Merchandiser
```

it may be planning/analysis.

User changes surface and trust.

---

# 7. Step 3 — Define source/input

Ask:

```text
What evidence should AI rely on?
Which source is authoritative?
How current must it be?
Is data permissioned?
```

This is especially important in vertical applications.

Example healthcare:

```text
approved organizational knowledge
trusted clinical evidence
authorized patient context
```

is qualitatively different from generic web information.

---

# 8. Step 4 — Define output and decision boundary

What exactly does AI produce?

```text
summary?
draft?
recommendation?
structured record?
action?
```

Then ask:

```text
Does AI inform a person?
Does a person approve?
Does AI act?
What happens on uncertainty?
```

Vertical adaptation often lives in this boundary.

---

# 9. Step 5 — Choose surface

Map interaction model:

```text
Interactive employee work
→ Chat

Delegated multi-step artifact creation
→ Work

Engineering
→ Codex

Embedded/customer-facing
→ API

Repeatable cross-tool workflow
→ agent pattern

Multiple workflows
→ combined
```

Do not choose surface before user/workflow is clear.

---

# 10. Step 6 — Adapt architecture

Generic capability may require vertical-specific systems.

Examples:

### Finance

```text
market/company data
internal documents
spreadsheets
risk/compliance systems
```

### Healthcare

```text
EHR context
approved clinical sources
organizational protocols
```

### Retail

```text
catalog
inventory
store systems
shopper data
```

Architecture is where vertical reality meets solution pattern.

---

# 11. Step 7 — Add trust controls

Question:

> “What control makes this pattern acceptable in this workflow?”

Examples:

```text
human review
citation/source traceability
approved source restriction
permission enforcement
write approval
audit log
escalation
confidence/uncertainty handling
```

---

# 12. Step 8 — Connect to business outcome

Don't stop at:

```text
AI drafts faster.
```

Ask:

```text
So what?
```

Examples:

```text
draft faster
→ shorter preparation time
→ more analyst capacity

search faster
→ faster customer response
→ better service

summarize store visit notes
→ faster action plan
→ more consistent store execution
```

---

# 13. Worked example — Financial research

### Generic pattern

```text
Gather + analyze + draft
```

### Vertical adaptation

```text
Filings/transcripts/internal sources
→ gather relevant evidence
→ analyze drivers
→ produce structured draft
→ analyst reviews
```

### Surface

Depending workflow:

```text
interactive research → Chat
delegated finished memo → Work
embedded research product → API
```

### Trust

```text
source traceability
approved data
human judgment remains
```

### Value

```text
less manual gathering
faster analysis
more capacity for judgment
```

---

# 14. Worked example — Retail associate

Public OpenAI retail examples include intelligent assistance for store teams.

### Generic pattern

```text
Retrieve + answer
```

### Adapted workflow

```text
Associate question
→ retrieve current product/policy information
→ concise answer
→ associate guides shopper
```

### Vertical requirements

```text
current catalog
inventory/policy freshness
multilingual support if needed
service consistency
```

### Value

```text
less search/training time
faster service
more consistent answers
```

---

# 15. Worked example — Healthcare admin

### Pattern

```text
Summarize + draft
```

### Workflow

```text
Authorized source context
→ summarize relevant information
→ draft administrative letter/instruction
→ human review
```

### Trust adaptation

```text
privacy
authorized access
review
source quality
```

### Value

```text
reduce rewriting/back-and-forth
free staff capacity
```

---

# 16. Worked example — Manufacturing handoff (illustrative)

This is an illustrative adaptation, not a claim from PartnerU vertical section.

### Generic pattern

```text
Summarize + draft
```

### Workflow

```text
equipment events + technician notes
→ summarize status
→ draft shift handoff
→ technician review
```

### Requirements

```text
near-real-time data
integration
adoption
human review
```

### Value

```text
less documentation effort
better consistency
faster handoff
```

---

# 17. Pattern vs automation depth

A useful ladder:

```text
Assist
→ Draft
→ Recommend
→ Take action with approval
→ Automate repeatable flow
```

Do not jump directly to maximum automation.

Choose based on:

```text
risk
readiness
workflow stability
value
trust
```

Example:

```text
High-risk workflow + low readiness
→ assist/draft first
```

---

# 18. Adaptation matrix

| Question | What to adapt |
|---|---|
| Who uses it? | Surface/UX |
| What source is trusted? | Retrieval/data |
| What quality bar applies? | Evaluation |
| What happens on error? | Review/escalation |
| What systems are involved? | Architecture |
| How fast must it respond? | Latency |
| Can it act? | Tool/action permissions |
| What business metric moves? | Value hypothesis |

---

# 19. Frontend Developer analogy

Generic UI pattern:

```text
modal
```

You would not use identical modal for:

- checkout payment;
- delete account;
- onboarding tip.

Same component pattern, different:

```text
content
risk
confirmation
state
behavior
```

AI solution patterns work similarly.

```text
Pattern is reusable.
Context determines implementation.
```

---

# 20. Common mistakes

## ❌ Copy a customer story

Customer stories prove possibility, not customer fit.

## ❌ Adapt only terminology

Replacing “customer” with “patient” is not vertical adaptation.

Real adaptation changes:

```text
source
review
risk
system
workflow
value
```

## ❌ Maximize automation

More automation is not automatically more value.

## ❌ Ignore surface

A valid capability placed in the wrong interaction model may fail adoption.

## ❌ Ignore exception handling

Vertical workflows often fail at edge cases, not happy path.

---

# 21. Pattern worksheet

```md
## Generic pattern
...

## Vertical workflow
...

## User
...

## Current pain
...

## Input/source
...

## AI capability
...

## Output
...

## Surface
...

## Architecture
...

## Review / approval
...

## Exception path
...

## Value
...

## Success signal
...
```

---

# 22. Cheat Sheet

```text
PATTERN
→ Workflow
→ User
→ Source
→ Output
→ Surface
→ Architecture
→ Trust controls
→ Business value
```

One sentence:

> **A vertical solution is a generic pattern made specific to a real workflow, source environment, risk model, and business outcome.**

---

# 23. Vocabulary

| Term | Nghĩa dễ hiểu |
|---|---|
| Solution pattern | Mẫu capability/workflow tái sử dụng |
| Adaptation | Điều chỉnh theo context |
| Decision boundary | Điểm AI dừng và con người/ hệ thống quyết định |
| Source authority | Nguồn được coi là chính thức |
| Exception path | Luồng xử lý trường hợp bất thường |
| Automation depth | Mức độ AI tự hành |
| Embedded | Tích hợp trực tiếp |
| Orchestration | Điều phối nhiều bước/tools |
| Workflow fit | Độ khớp với công việc thực tế |

---

# 24. Self-check

1. Pattern khác solution thế nào?
2. Những layer nào cần adapt?
3. Tại sao source authority quan trọng?
4. Decision boundary giúp quản lý trust ra sao?
5. Khi nào không nên tăng automation depth?
6. Bạn có thể adapt cùng một pattern cho finance và retail không?

---

## Nguồn và mức độ grounding

PartnerU source available: **section title only**.

Public OpenAI vertical materials used for examples:
- Financial Services: https://openai.com/solutions/industries/financial-services/
- Healthcare: https://openai.com/solutions/industries/healthcare/
- Retail: https://openai.com/solutions/industries/retail/
- API Platform: https://openai.com/api/

> Đây là study synthesis để học, không phải transcript PartnerU.
