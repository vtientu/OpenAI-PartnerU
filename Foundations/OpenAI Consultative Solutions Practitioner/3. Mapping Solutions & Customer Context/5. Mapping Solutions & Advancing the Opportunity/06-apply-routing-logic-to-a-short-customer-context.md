# 06. Apply Routing Logic to a Short Customer Context

> Course: **OpenAI Consultative Solutions Practitioner – Foundations**  
> Sub-course: **Mapping Solutions & Advancing the Opportunity**  
> Section: **Apply routing logic to a short customer context**

---

## 1. Mục tiêu

Section cuối cùng là bài **integration**.

Bạn phải có khả năng đọc một customer context ngắn và suy luận:

```text
What is the workflow?
Who is the user?
What surface fits?
What capabilities are needed?
What architecture/deployment constraints matter?
Is the route credible?
What should happen next?
```

Đây là nơi tất cả section trước được nối lại.

---

# 2. End-to-end routing framework

```text
CUSTOMER CONTEXT
      ↓
WORKFLOW
      ↓
USER / OWNER
      ↓
VALUE HYPOTHESIS
      ↓
SURFACE
      ↓
CAPABILITY
      ↓
ARCHITECTURE
      ↓
DEPLOYMENT / OPERATING MODEL
      ↓
CREDIBILITY / READINESS
      ↓
PROGRESSION MOTION
      ↓
HANDOFF
```

---

# 3. A disciplined reading order

Khi đọc một đoạn customer context, đừng nhìn product names trước.

Đọc theo 8 passes:

## Pass 1 — Workflow

```text
What work is happening?
Where is pain?
```

## Pass 2 — User

```text
Who performs it?
Who owns outcome?
```

## Pass 3 — Value

```text
Why does it matter?
```

## Pass 4 — Interaction model

```text
Chat?
Delegate?
Engineering?
Embedded?
Agent?
```

## Pass 5 — Requirements

```text
What must AI do/connect to?
```

## Pass 6 — Constraints

```text
Latency?
Sensitive data?
Identity?
Approvals?
Customer-managed?
```

## Pass 7 — Readiness

```text
Owner?
Data?
Governance?
Adoption?
Success measure?
```

## Pass 8 — Next step

```text
Discovery?
Validation?
Migration?
Technical?
Deployment?
Handoff?
```

---

# 4. Composite example A — Customer Support

### Customer context

> A retailer’s support team handles high ticket volume. Agents spend time checking order status, searching policies, drafting replies, and escalating exceptions. Management wants faster response times. Certain account actions require approval.

### Step 1 — Workflow

```text
Ticket
→ check order
→ search policy
→ draft
→ escalate exception
→ approval when required
→ respond
```

### Step 2 — User

```text
Support agent
```

Owner should be identified:

```text
Support operations / workflow owner
```

### Step 3 — Value

```text
less search/check time
→ faster response
→ increased support capacity
```

### Step 4 — Surface

Could be:

```text
embedded support experience
or agentic workflow
```

Need more context before naming exact surface.

### Step 5 — Capability

```text
check order status
retrieve policy
draft reply
escalate
request approval
```

### Step 6 — Architecture

```text
ticketing
order system
policy sources
identity
permissions
```

### Step 7 — Operating

```text
approval for sensitive action
human review
escalation ownership
```

### Step 8 — Credibility

Need validate:

```text
system integration
permissions
representative quality
approval flow
```

### Next step

If use case/value clear but requirements uncertain:

→ **Validation session**

If identity/integration are materially complex:

→ **Technical handoff**

---

# 5. Composite example B — Finance

### Context

> Finance team wants to delegate weekly source gathering, analysis, and creation of a review-ready performance pack.

### Workflow pattern

```text
multi-step knowledge work
+ finished deliverable
```

### Surface

→ **ChatGPT Work**

### Capabilities

```text
gather sources
analyze
synthesize
create artifact
```

### Operating

```text
finance review before use
```

### Value

```text
reduce preparation effort
increase productive capacity
improve consistency
```

### Validation

```text
source access
output quality
review criteria
```

---

# 6. Composite example C — Engineering

### Context

> Engineering team wants to reduce testing, code review and modernization bottlenecks.

### Surface

→ **Codex**

### Value

```text
shorter development cycle
more engineering capacity
better review/test coverage
```

### Architecture

```text
repository
CI/test environment
permissions
```

### Operating

```text
engineer review controls what ships
```

### Next step

If repository/security integration is material:

→ technical validation / technical handoff

---

# 7. Composite example D — Customer-facing onboarding

### Context

> SaaS product needs personalized onboarding guidance embedded inside the product.

### Surface

→ **Application/process built with API**

### Why?

```text
customer-facing
embedded
custom UX/context
```

### Capability

```text
understand onboarding state
generate personalized guidance
possibly invoke product actions
```

### Architecture

```text
app state
customer profile
identity
backend systems
```

### Operating

```text
boundaries on actions
monitor quality
```

---

# 8. Composite example E — Existing AI consolidation

### Context

> Customer is replacing multiple AI pilots and wants to consolidate workflows and vendors.

Primary implication:

→ **Migration discovery**

Need to map:

```text
Current tools
Current workflows
Data dependencies
User groups
Current contracts/constraints
Target-state capabilities
Target surfaces
Migration sequencing
```

This is a progression decision before final solution design.

---

# 9. Composite example F — Customer-managed execution

### Context

> Hosted controls were evaluated, but customer requires self-managed execution and will operate the model.

Implication:

→ **Deployment and operating model; open-weight consideration**

Need to validate:

```text
why hosted is insufficient
infrastructure
operations ownership
security
model serving
monitoring
support expectations
```

Do not treat this as merely “pick another model”.

---

# 10. How to answer matching questions

Method:

```text
1. Find the strongest clue.
2. Ask which decision layer it belongs to.
3. Ignore weaker secondary clues.
4. Match the option that resolves the dominant concern.
```

Example:

> “Technicians must change how they create shift handoff notes.”

Possible clues:

- manufacturing;
- notes;
- AI drafting.

Strongest clue:

```text
must change behavior
```

Therefore:

→ adoption/readiness question.

---

# 11. Decision clue dictionary

```text
"embedded in product"
→ API surface

"delegate multi-step work"
→ Work

"code review/testing/modernization"
→ Codex

"iteratively explore/draft"
→ Chat

"self-managed / customer operates"
→ deployment model

"apps/actions/schedules/approvals"
→ capability/architecture

"replacing existing tool"
→ migration discovery

"live system / near-real-time"
→ technical validation

"no owner"
→ ownership/readiness

"sensitive data / unclear approval"
→ governance

"broad AI interest"
→ more discovery

"owner + adoption + governance + success measures"
→ deployment handoff
```

---

# 12. Full case — Manufacturing

### Context

> Manufacturing customer wants technicians to receive near-real-time guidance from live equipment data and create consistent shift handoff notes. The proposed route uses live integrations. Technicians would need to change their current note-taking behavior. No workflow owner has yet been named.

### Analysis

#### Workflow

```text
equipment events
→ technician interpretation
→ handoff note
→ next shift
```

#### Value

```text
faster handoff
better consistency
possibly lower operational burden
```

#### Capability

```text
retrieve live data
summarize
draft note
flag exception
```

#### Architecture

```text
equipment systems
live data integration
identity/permissions
```

#### Technical risk

```text
latency
integration
```

#### Adoption risk

```text
technicians must change behavior
```

#### Ownership risk

```text
no owner named
```

### Credibility verdict

Not deployment-ready.

### Best next step

Likely:

```text
continue/targeted discovery to establish owner
+
technical validation for live integration/latency
```

If forced to choose one strongest next action, use dominant gap identified by question wording/options.

---

# 13. Full case — Frontend SaaS

### Context

> SaaS company wants customer-facing AI onboarding. It must personalize guidance based on user state. The business owner is clear. Data and identity integration are not yet validated.

### Route

```text
Surface:
API-built embedded experience

Capability:
personalize + generate guidance

Architecture:
app state + user identity + backend data

Readiness:
owner clear
technical path unclear

Next step:
technical validation / handoff
```

---

# 14. Common mistakes in applied routing

## ❌ Match on one keyword without context

Example:

```text
"approval"
```

could be capability or operating model.

Read the whole sentence.

## ❌ Choose the most advanced solution

The course rewards **credible**, not impressive.

## ❌ Ignore progression

Sometimes the correct answer is “migration discovery”, not a product.

## ❌ Conflate surface and architecture

```text
API surface
```

does not mean architecture is solved.

---

# 15. One-page exam strategy

```text
1. Underline user/workflow clue.
2. Circle constraint clue.
3. Identify decision layer.
4. Ask: what uncertainty is dominant?
5. Select the action/surface that directly addresses it.
```

---

# 16. Final mental model

```text
ROUTE =

Workflow
+ User
+ Value
+ Surface
+ Capability
+ Architecture
+ Operating model
+ Readiness
+ Next step
```

Shortest version:

```text
WHERE
WHAT
HOW
READY?
NEXT?
```

Where:

```text
WHERE = surface
WHAT = capability
HOW = architecture/deployment/operation
READY? = credibility
NEXT? = progression
```

---

# 17. Vocabulary recap

| Term | Meaning |
|---|---|
| Surface | Nơi AI xuất hiện |
| Capability | AI/solution làm gì |
| Architecture | Kết nối data/system ra sao |
| Deployment | Chạy ở đâu/cách nào |
| Operating model | Ai kiểm soát/vận hành |
| Credibility | Route có đủ căn cứ chưa |
| Readiness | Customer có sẵn sàng không |
| Progression | Bước tiếp theo |
| Migration discovery | Mapping current → target |
| Validation | Kiểm chứng uncertainty |

---

# 18. Self-check

Bạn đã sẵn sàng kết thúc sub-course nếu có thể:

1. Đọc short context và chọn surface.
2. Tách capability, architecture, operating requirements.
3. Nhận diện open-weight/customer-managed requirement.
4. Nhận diện technical/adoption/ownership/governance blockers.
5. Chọn discovery vs validation vs migration vs technical vs deployment handoff.
6. Giải thích *vì sao* route credible hoặc chưa credible.

---

## Grounding

File này tổng hợp trực tiếp routing patterns từ tất cả Knowledge Checks bạn đã gửi trong sub-course.

OpenAI public docs chỉ được dùng để cập nhật ý nghĩa sản phẩm/surface:
- ChatGPT Work: https://openai.com/chatgpt-work/
- Codex: https://openai.com/business/solutions/engineering/
- API: https://openai.com/api/
- Workspace Agents: https://openai.com/business/workspace-agents/
- Open-weight: https://help.openai.com/en/articles/11870455

> Study synthesis, không phải transcript PartnerU.
