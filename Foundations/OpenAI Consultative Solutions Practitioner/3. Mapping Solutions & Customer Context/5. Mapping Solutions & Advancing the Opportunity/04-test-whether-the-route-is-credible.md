# 04. Test Whether the Route Is Credible

> Course: **OpenAI Consultative Solutions Practitioner – Foundations**  
> Sub-course: **Mapping Solutions & Advancing the Opportunity**  
> Section: **Test whether the route is credible**

---

## 1. Mục tiêu

Sau khi có candidate route, ta phải quyết định:

> **Route này đã đủ credible để tiến tiếp chưa?**

Credible không có nghĩa:

```text
100% proven
```

Credible nghĩa:

> Có đủ evidence để tin rằng route đáng được validate / handoff / advance, đồng thời các uncertainty quan trọng đã được nhận diện rõ.

---

# 2. Credible route = nhiều lớp cùng hợp lý

Một route có thể được test qua:

```text
Workflow fit
Value fit
User/adoption fit
Capability fit
Architecture fit
Governance/trust fit
Ownership fit
Proportionality
Readiness
```

Nếu bất kỳ layer quan trọng nào quá yếu, next step có thể là discovery/validation chứ chưa phải rollout.

---

# 3. Five readiness/tradeoff questions

Knowledge Check đưa ra 5 loại constraint rất quan trọng.

## A. Technical feasibility

Example:

> Workflow needs near-real-time guidance from live equipment data.

Question:

> **Do latency and integration needs require technical validation?**

Mental model:

```text
real-time + live system
→ feasibility depends on latency/integration
→ technical validation
```

---

## B. Adoption / behavior change

Example:

> Technicians will need to change how they create shift handoff notes.

Question:

> **Who will adopt the solution, and what behavior must change?**

AI success is not only technical.

If users must work differently:

```text
adoption path
training
workflow ownership
behavior change
```

matter.

---

## C. Ownership

Example:

> No customer owner has been named for the workflow or outcome.

Question:

> **Who owns the outcome and can drive the next step?**

No owner often means:

```text
no decision authority
no adoption driver
no success accountability
```

Thus route credibility is weak even if tech is feasible.

---

## D. Proportionality

Example:

> Proposed route is complex, but the value hypothesis is still weak.

Question:

> **Is the route proportional to the customer’s maturity, urgency, and expected value?**

This is a core consultative principle:

```text
Complexity should be justified by value and readiness.
```

Do not design a huge solution for a weakly evidenced outcome.

---

## E. Governance / data / review

Example:

> Workflow may involve sensitive data, but approval requirements are unclear.

Question:

> **What governance, data, and review requirements apply?**

Trust is part of feasibility.

---

# 4. Credibility checklist

## 4.1 Workflow clarity

```text
Do we understand current state?
Do we know the exact step being changed?
Do we know users and handoffs?
```

## 4.2 Value evidence

```text
Is there a meaningful pain?
Is value linked to a business outcome?
Is the value hypothesis supported?
```

## 4.3 Technical path

```text
Can required data/systems be accessed?
Are latency requirements plausible?
Do integrations exist?
```

## 4.4 Operating path

```text
Who owns?
Who reviews?
Who approves?
Who monitors?
```

## 4.5 Adoption path

```text
Who uses it?
What behavior changes?
What friction is introduced?
```

## 4.6 Trust path

```text
Sensitive data?
Security?
Governance?
Auditability?
Human review?
```

---

# 5. Evidence ladder

Credibility increases as evidence moves closer to real workflow.

```text
Generic claim
↓
Customer statement
↓
Observed workflow
↓
Real examples
↓
Representative task test
↓
Pilot
↓
Production evidence
```

Do not confuse:

```text
"Another customer achieved X"
```

with:

```text
"This customer can achieve X."
```

External case studies strengthen a hypothesis but do not prove customer-specific outcomes.

---

# 6. Assumption register

A practical technique:

| Assumption | Why it matters | How to validate |
|---|---|---|
| Live data accessible | Required for guidance | Integration review |
| Latency acceptable | Workflow is time-sensitive | Technical test |
| Technicians adopt new notes flow | Value depends on use | Pilot/user study |
| Sensitive data permitted | Governance blocker | Security/governance review |
| Value justifies complexity | Investment decision | Value hypothesis refinement |

This turns uncertainty into action.

---

# 7. Proportionality

A route should be **proportional** to:

```text
customer maturity
urgency
business value
workflow criticality
risk
readiness
```

Example:

```text
Weak value hypothesis
+ large custom architecture
+ multiple integrations
+ unclear owner
```

→ likely over-routed.

Better:

```text
smaller validation step
```

The goal is not to recommend the most impressive architecture.

The goal is:

> **Recommend the smallest credible route that can produce useful evidence.**

---

# 8. Technical validation triggers

Likely triggers:

```text
near-real-time requirement
live integration
security review
complex identity/permissions
critical data access
customer-managed deployment
uncertain feasibility
```

Technical validation should answer a specific uncertainty, not become generic engineering work.

---

# 9. Adoption readiness

If a workflow changes, ask:

```text
Who uses it?
What do they do today?
What will they do differently?
What step disappears?
What new step appears?
What review burden is added?
Who trains/supports?
```

Example:

```text
AI drafts handoff note
```

sounds easy.

But if technicians currently use a paper flow and new workflow requires app login, data review, correction and approval, adoption may be the hardest problem.

---

# 10. Ownership readiness

At minimum:

```text
Workflow owner
Business outcome owner
Technical/deployment owner when needed
Governance/security owner when needed
```

No named owner is a strong signal to slow down.

---

# 11. Trust/readiness in sensitive workflows

Sensitive data does not automatically mean “no AI”.

It means requirements must be explicit.

Questions:

```text
Which data?
Who can access it?
What is retained?
What requires approval?
What actions are allowed?
What needs auditability?
What output requires human review?
```

---

# 12. Example — Healthcare operations

Context:

```text
Hospital operations contact is interested in AI.
```

If they cannot name:

```text
workflow
user group
owner
```

route is not credible yet.

→ **More discovery**

If later:

```text
workflow clear
value clear
but sensitive data + approval unclear
```

→ **validation/governance work**

Credibility evolves with evidence.

---

# 13. Example — Frontend platform

Proposal:

> AI agent can modify production configuration automatically.

Check:

```text
Value?
Maybe reduces ops time.

Architecture?
Can access config service.

Operating?
Who approves production writes?

Security?
What identity does agent use?

Adoption?
Will engineers trust it?

Proportionality?
Is auto-write justified, or should it only draft changes first?
```

Often a smaller route:

```text
AI drafts config change
→ engineer reviews
```

may be more credible initially.

---

# 14. Red flags

```text
"The model can do it."
```

Not enough.

```text
"The customer liked the demo."
```

Not enough.

```text
"Security can be handled later."
```

Dangerous to credibility.

```text
"We'll figure out ownership after pilot."
```

Often a sign of weak readiness.

```text
"The architecture is advanced."
```

Advanced ≠ appropriate.

---

# 15. Knowledge Check mapping

```text
Near-real-time live equipment data
→ latency/integration technical validation

Technicians change shift handoff behavior
→ adoption + behavior change

No customer owner
→ ownership question

Complex route + weak value hypothesis
→ proportionality

Sensitive data + unclear approvals
→ governance/data/review requirements
```

---

# 16. Credibility scorecard (qualitative)

You can use:

```text
Workflow clarity       High / Medium / Low
Value evidence         High / Medium / Low
Technical path         High / Medium / Low
Data readiness         High / Medium / Low
Ownership              High / Medium / Low
Adoption readiness     High / Medium / Low
Governance clarity     High / Medium / Low
Proportionality        Good / Questionable
```

Do not treat this as rigid numeric scoring.

Use it to make reasoning explicit.

---

# 17. Cheat Sheet

```text
TECH
Can it work?

ADOPTION
Will people change?

OWNER
Who drives it?

VALUE
Is complexity worth it?

GOVERNANCE
Can it be controlled safely?
```

Credible route:

```text
valuable enough
+ feasible enough
+ owned enough
+ trusted enough
+ adoptable enough
```

---

# 18. Vocabulary

| Term | Nghĩa dễ hiểu |
|---|---|
| Credible | Có căn cứ đủ để đáng tin và tiến tiếp |
| Readiness | Mức sẵn sàng |
| Tradeoff | Đánh đổi |
| Proportionality | Độ tương xứng giữa complexity và value/readiness |
| Adoption | Việc user thực sự sử dụng |
| Technical validation | Kiểm chứng feasibility kỹ thuật |
| Governance | Quy tắc/kiểm soát |
| Sensitive data | Dữ liệu nhạy cảm |
| Ownership | Ai chịu trách nhiệm |
| Assumption register | Danh sách giả định cần validate |

---

# 19. Self-check

1. Credible khác proven thế nào?
2. Near-real-time data tạo ra loại uncertainty nào?
3. Vì sao owner là readiness concern?
4. Proportionality nghĩa là gì?
5. Sensitive data nên dẫn tới câu hỏi nào?
6. Khi nào route nên thu nhỏ thay vì tăng complexity?

---

## Grounding

### Từ Knowledge Check bạn cung cấp
5 constraint ↔ 5 readiness/tradeoff questions được giữ nguyên logic.

### OpenAI public context
- Enterprise solutions emphasize governance, secure integrations, permissions, and controls.
- Workspace agents include permissions/approvals/monitoring.
- API platform supports agent workflows and business-system actions.

Sources:
- https://openai.com/solutions/
- https://openai.com/business/workspace-agents/
- https://openai.com/api/

> Study synthesis, không phải transcript PartnerU.
