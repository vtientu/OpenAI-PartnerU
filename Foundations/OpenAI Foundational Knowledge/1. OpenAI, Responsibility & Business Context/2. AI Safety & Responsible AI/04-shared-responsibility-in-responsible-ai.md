# 04 — Shared Responsibility in Responsible AI

> **Course:** Foundation — OpenAI Foundational Knowledge  
> **Sub-course:** AI Safety & Responsible AI  
> **Section:** Shared responsibility in responsible AI
>
> **Lưu ý:** “Shared responsibility” ở đây là mental model để phân chia ownership trong solution lifecycle; responsibility cụ thể còn phụ thuộc sản phẩm, hợp đồng, pháp luật, organization và use case.

---

# 1. Section objective

Sau section này, bạn cần:

- hiểu vì sao responsible AI không thuộc riêng OpenAI;
- phân biệt trách nhiệm của model provider, partner/builder, customer organization và end user;
- biết cách tạo ownership matrix;
- hiểu trách nhiệm thay đổi theo architecture và use case;
- tránh “responsibility gap”.

---

# 2. Big picture

Một AI application có nhiều bên tham gia:

```text
OpenAI
   ↓
Partner / builder
   ↓
Customer organization
   ↓
Business owner / IT / risk teams
   ↓
End users
```

Không một bên nào có toàn bộ context.

Do đó responsible AI cần:

> **Shared responsibility + explicit ownership.**

---

# 3. Shared responsibility không có nghĩa “mọi người chịu trách nhiệm như nhau”

Sai mental model:

```text
Everyone is responsible
→ nobody owns anything
```

Better:

```text
Shared responsibility
=
different parties
own different controls
```

Ví dụ:

- OpenAI: model-level safeguards;
- partner: application design;
- customer: business process/governance;
- end user: appropriate use and verification within policy.

---

# 4. Layer 1 — OpenAI responsibility

Ở mức khái quát, model/provider layer có thể chịu trách nhiệm về:

- model research;
- safety training/alignment;
- model-level evaluations;
- platform safeguards;
- public documentation;
- usage policies;
- monitoring/enforcement của service;
- product/security controls được cung cấp.

Nhưng OpenAI không tự biết:

- customer internal policy;
- exact workflow;
- employee role;
- customer-specific data quality;
- downstream integration logic.

Đó là nơi responsibility chuyển sang application/customer layers.

---

# 5. Layer 2 — Partner / builder responsibility

Partner/builders biến model thành solution.

Họ thường có influence lên:

- use-case design;
- architecture;
- prompt/instructions;
- data sources;
- tool integrations;
- permissions;
- workflow;
- guardrails;
- application evals;
- logging;
- escalation design;
- user experience.

Điểm quan trọng:

> Model safeguard không thể sửa mọi lỗi application architecture.

---

# 6. Layer 3 — Customer organization responsibility

Customer organization hiểu:

- business process;
- data classification;
- industry requirements;
- legal obligations;
- acceptable risk;
- internal policies;
- role permissions;
- escalation ownership.

Customer phải quyết định:

> “Use case này có phù hợp với organization của chúng tôi không?”

Partner hỗ trợ, nhưng không nên tự thay customer quyết định mọi business/governance matter.

---

# 7. Layer 4 — End-user responsibility

End user cũng có trách nhiệm:

- dùng system đúng purpose;
- follow workplace policy;
- verify khi workflow yêu cầu;
- không cố bypass controls;
- report unexpected behavior;
- không assume AI output luôn đúng.

Nhưng cần cẩn thận:

> Không nên dùng “user responsibility” để che giấu poor product design.

Nếu system biết user dễ hiểu nhầm, UX nên hỗ trợ.

---

# 8. Supporting functions

Responsible AI thường còn có:

- Security;
- Privacy;
- Legal;
- Compliance;
- Risk;
- Procurement;
- Internal audit;
- Data governance;
- HR/change management.

AI deployment là cross-functional work.

---

# 9. Responsibility changes by use case

### Low-risk internal drafting

Ownership đơn giản hơn.

### Tool-using agent

Cần thêm:

- identity;
- permissions;
- action policy;
- logging;
- confirmation;
- incident response.

### High-impact workflow

Có thể cần:

- domain expert;
- legal/compliance review;
- formal governance;
- stricter evaluation.

Do đó:

```text
Responsibility model
depends on
use case architecture + impact
```

---

# 10. Responsibility matrix

Hãy dùng matrix đơn giản.

| Area | OpenAI | Partner/Builder | Customer | End User |
|---|---|---|---|---|
| Model-level behavior | Primary | Understand | Understand | — |
| Application architecture | Platform support | Primary | Approve | — |
| Customer data | Platform controls | Implement | Primary owner | Use appropriately |
| Tool permissions | Capability support | Implement | Define/approve | Respect |
| Business policy | — | Encode correctly | Primary | Follow |
| App evals | Model docs/evidence | Build/run | Supply cases + accept criteria | Feedback |
| Adoption | Product UX | Enable | Primary | Participate |
| Monitoring | Service-level | App-level | Business-level | Report issues |
| Incident handling | Service incidents | App incidents | Org incidents | Report |

Đây là study framework, không phải legal allocation.

---

# 11. RACI thinking

Một organization có thể dùng RACI:

- **R — Responsible:** người thực hiện;
- **A — Accountable:** người chịu trách nhiệm cuối;
- **C — Consulted:** được tham vấn;
- **I — Informed:** được thông báo.

Ví dụ:

```text
Use case approval
A: Business owner
R: AI program team
C: Security + Legal + Partner
I: End users
```

RACI giúp tránh responsibility gap.

---

# 12. Responsibility gap

**Responsibility gap** xảy ra khi:

- không ai own metric;
- không ai monitor;
- partner nghĩ customer làm;
- customer nghĩ vendor làm;
- security không biết agent có tool access;
- business team không biết limitations.

Đây là organizational risk rất thật.

---

# 13. Shared responsibility across lifecycle

## Discovery

Partner + customer:

- define problem;
- identify affected users;
- classify risk.

## Design

Partner:

- architecture;
- controls.

Customer:

- policy;
- permissions;
- acceptance criteria.

## Evaluation

OpenAI:

- model-level evidence.

Partner/customer:

- customer-specific evals.

## Deployment

Partner:

- technical readiness.

Customer:

- organizational approval.

## Operation

Shared:

- monitor;
- incidents;
- feedback;
- updates.

---

# 14. Customer-specific evaluation is a shared responsibility

OpenAI có thể publish model evals.

Nhưng OpenAI không thể evaluate:

> “Model có xử lý đúng 5,000 ticket categories riêng của Company X không?”

Customer và partner cần:

- representative data;
- expected outcomes;
- acceptance thresholds;
- expert review.

Mental model:

```text
Provider evidence
+
Customer-specific evidence
=
Better deployment decision
```

---

# 15. Data responsibility

Một common mistake:

> “OpenAI handles data, nên customer không cần nghĩ về data governance.”

Sai.

Customer và builder vẫn cần quyết định:

- data nào được đưa vào;
- purpose;
- permissions;
- classification;
- source freshness;
- output storage;
- downstream use.

Platform controls hỗ trợ, nhưng không thay business governance.

---

# 16. Tool/action responsibility

Nếu agent có action:

```text
OpenAI model
→ partner orchestration
→ customer tool
→ real action
```

Responsibility trải qua nhiều layer.

Partner cần hỏi:

- tool nào?
- identity nào?
- permission nào?
- action limit?
- approval?
- audit?
- fallback?

Customer cần xác nhận business authority.

---

# 17. Human responsibility remains

AI không tự trở thành accountable business owner.

Ngay cả khi agent tự động:

- organization vẫn cần owner;
- người có authority vẫn cần define policy;
- incident vẫn cần response process.

Autonomy không xóa accountability.

---

# 18. Example — HR knowledge assistant

### OpenAI
- model/platform behavior and service controls.

### Partner
- retrieval design;
- application;
- evaluation;
- escalation.

### Customer HR
- approved policy source;
- policy freshness;
- business rules;
- owner.

### End user
- use assistant within scope;
- escalate when required.

Nếu answer sai vì policy source stale:

> Đó không phải tự động là “model failure”.

Có thể là data governance failure.

---

# 19. Example — Finance workflow

AI extracts and categorizes expense documents.

Possible ownership:

```text
Model behavior → OpenAI
Extraction pipeline → Partner
Finance policy → Customer
Approval rule → Customer
Application evals → Partner + finance team
Final high-risk approval → Authorized employee
```

Rõ ownership giúp debug và govern.

---

# 20. Partner handoff checklist

Trước production, partner nên xác nhận:

## Owner
- business owner là ai?
- technical owner là ai?

## Data
- source owner?
- update process?

## Controls
- permissions?
- escalation?

## Evaluation
- acceptance criteria?
- ongoing eval?

## Operations
- monitoring owner?
- incident owner?
- change process?

Nếu câu trả lời là:

> “Chưa biết”

thì readiness chưa hoàn chỉnh.

---

# 21. Shared responsibility vs blame

Mục tiêu của framework không phải:

> “Nếu xảy ra lỗi thì lỗi của ai?”

Mục tiêu tốt hơn:

> “Trước khi lỗi xảy ra, ai own control nào?”

Đây là proactive governance.

---

# 22. Common mistakes

## Mistake 1
“Vendor handles safety.”

## Mistake 2
“Customer owns everything.”

## Mistake 3
“Developer owns business policy.”

## Mistake 4
“No one owns evaluation.”

## Mistake 5
“AI agent owns the decision.”

AI không phải legal/organizational accountable actor.

---

# 23. Practical framework — OWNER

Mnemonic:

## O — Outcome owner
Ai chịu trách nhiệm business result?

## W — Workflow owner
Ai hiểu và approve process?

## N — Network/system owner
Ai quản lý integrations/access?

## E — Evaluation owner
Ai định nghĩa và duy trì quality evidence?

## R — Risk owner
Ai quyết định acceptable residual risk?

Một người có thể giữ nhiều role, nhưng role phải rõ.

---

# 24. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| **Shared responsibility** | Trách nhiệm được chia theo vai trò |
| **Ownership** | Quyền/chịu trách nhiệm sở hữu một phần công việc |
| **Accountability** | Trách nhiệm giải trình |
| **RACI** | Responsible, Accountable, Consulted, Informed |
| **Business owner** | Người chịu trách nhiệm business |
| **Risk owner** | Người chịu trách nhiệm quyết định/ quản lý risk |
| **Responsibility gap** | Khoảng trống trách nhiệm |
| **Acceptance criteria** | Tiêu chí chấp nhận |
| **Residual risk** | Rủi ro còn lại |
| **Handoff** | Bàn giao |
| **Cross-functional** | Liên chức năng / nhiều team |

---

# 25. Section recap

1. Responsible AI là shared responsibility.
2. Shared không có nghĩa responsibility mơ hồ.
3. OpenAI, partner, customer và user có các layer ownership khác nhau.
4. Customer-specific evals cần partner + customer.
5. Data governance vẫn là customer/application concern.
6. Autonomy không loại bỏ human accountability.
7. RACI/ownership matrix giúp tránh responsibility gap.
8. Hỏi luôn: **Who owns this control?**

---

# 26. Self-check

1. Vì sao model provider không thể chịu toàn bộ trách nhiệm cho application?
2. Partner thường own những layer nào?
3. Customer cần own những quyết định nào?
4. Responsibility gap là gì?
5. Hãy dùng OWNER framework cho một support AI agent.
