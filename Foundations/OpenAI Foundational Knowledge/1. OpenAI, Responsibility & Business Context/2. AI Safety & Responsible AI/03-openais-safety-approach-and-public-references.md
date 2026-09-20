# 03 — OpenAI’s Safety Approach and Public References

> **Course:** Foundation — OpenAI Foundational Knowledge  
> **Sub-course:** AI Safety & Responsible AI  
> **Section:** OpenAI’s safety approach and public references
>
> **Nguồn:** Section này chủ động sử dụng các tài liệu công khai chính thức của OpenAI để giúp bạn biết **đọc ở đâu và dùng tài liệu nào cho loại câu hỏi nào**. Nội dung được cập nhật theo các nguồn công khai kiểm tra vào **20/09/2026** và không phải transcript PartnerU.

---

# 1. Section objective

Sau section này, bạn cần:

- hiểu safety của OpenAI là một **multi-layer approach**;
- biết vai trò của evaluations, red teaming, safeguards và monitoring;
- hiểu Preparedness Framework ở mức nền tảng;
- phân biệt **Model Spec**, **Usage Policies**, **System Cards** và các governance references;
- biết chọn đúng public source khi customer hỏi về safety.

---

# 2. Big picture

Không có một tài liệu duy nhất tên:

> “Everything about OpenAI safety.”

Public safety material được chia thành nhiều lớp.

Mental model:

```text
Desired model behavior
        ↓
Training / alignment
        ↓
Safety evaluations
        ↓
Risk-specific safeguards
        ↓
Deployment
        ↓
Monitoring / enforcement
        ↓
Transparency / updates
```

Các public references giúp quan sát những phần khác nhau của lifecycle.

---

# 3. Safety as a lifecycle

Một cách đơn giản để hiểu OpenAI safety approach:

```text
1. Define intended behavior
2. Train / align
3. Test and evaluate
4. Red team
5. Assess frontier risk
6. Add safeguards
7. Deploy
8. Monitor
9. Learn and update
```

Không nên hiểu safety như:

```text
One filter at the end
```

---

# 4. Layer 1 — Intended model behavior

Một public reference quan trọng là **Model Spec**.

Model Spec mô tả cách OpenAI muốn model hành xử.

Nó hỗ trợ:

- transparency;
- shared vocabulary;
- discussion of model behavior;
- alignment targets.

Điểm quan trọng:

> Model Spec là **behavior specification**, không phải system card và không phải usage policy.

---

# 5. Model Spec — dùng khi nào?

Dùng khi câu hỏi liên quan:

- model nên follow instruction theo thứ tự nào;
- intended behavior;
- trade-offs giữa helpfulness, safety và developer/user intent;
- cách OpenAI định nghĩa behavior goals.

Mental model:

```text
Model Spec
=
"What behavior do we want?"
```

Nó không có nghĩa mọi production model luôn hoàn hảo theo spec.

Spec là target/standard mà systems hướng tới.

---

# 6. Layer 2 — Evaluations

**Evaluation (eval)** giúp đo capability hoặc behavior.

Safety eval có thể hỏi:

- model có làm tốt một capability rủi ro không?
- model có tuân thủ safety behavior không?
- safeguard có hiệu quả không?
- system có fail ở edge case nào?

Evaluation quan trọng vì:

```text
No measurement
→ weak evidence
```

---

# 7. Red teaming

**Red teaming** là quá trình chủ động tìm failure modes và weaknesses trước/để cải thiện deployment.

Có thể gồm:

- internal experts;
- external experts;
- specialized evaluators.

Partner cần nhớ principle:

> Red teaming nhằm tìm ra vấn đề trước khi user hoặc production environment tìm ra nó.

Không phải red teaming nào cũng giống nhau.

Scope phụ thuộc model/product.

---

# 8. Layer 3 — Preparedness Framework

**Preparedness Framework** là public framework của OpenAI nhằm theo dõi và chuẩn bị cho các **frontier capabilities có thể tạo risk nghiêm trọng**.

Đây là một framework cho frontier risk, không phải checklist cho mọi lỗi application.

Các tài liệu hiện hành mô tả việc:

- theo dõi capability;
- đánh giá risk;
- xác định safeguard cần thiết;
- xem xét deployment posture.

Các category/framework chi tiết có thể thay đổi theo version.

Vì vậy:

> Khi cần factual detail, luôn mở phiên bản Preparedness Framework hiện hành thay vì học thuộc một snapshot cũ.

---

# 9. Preparedness Framework không thay thế application safety

Một enterprise solution vẫn cần:

- data controls;
- security;
- human review;
- app evals;
- permissions;
- customer governance.

Preparedness Framework tập trung vào frontier-model risk.

Mental model:

```text
OpenAI frontier safety
≠
Complete customer application safety
```

Hai lớp bổ sung cho nhau.

---

# 10. Layer 4 — System Cards

**System Card** là public report mô tả safety work và evaluations quanh một model/product cụ thể.

System Card có thể cung cấp:

- capabilities;
- limitations;
- evaluations;
- risk findings;
- mitigations/safeguards;
- release-specific safety information.

Mental model:

```text
System Card
=
"What did OpenAI test and observe for this model/product?"
```

---

# 11. Deployment Safety Hub

OpenAI hiện có **Deployment Safety Hub**, nơi tập hợp system cards và deployment safety material.

Đây là một nguồn rất hữu ích khi cần:

- model-specific evidence;
- release-specific safety detail;
- historical comparison;
- evaluation methodology.

Partner nên ưu tiên source này hơn việc nhớ từ một slide cũ.

---

# 12. Example — Why system cards matter

Nếu customer hỏi:

> “OpenAI đã safety-test model này chưa?”

Không nên trả lời chung:

> “Có, OpenAI test rất nhiều.”

Tốt hơn:

1. xác định exact model/product;
2. tìm system card hiện hành;
3. chỉ ra evaluation/safeguard relevant;
4. nói rõ limitation;
5. phân biệt model evidence với customer application evidence.

Đây là **communication discipline**.

---

# 13. Layer 5 — Safeguards

Sau evaluation, system có thể được triển khai cùng safeguard phù hợp.

Safeguard có thể tồn tại ở nhiều layer:

- training;
- model behavior;
- classifiers;
- access control;
- monitoring;
- tool confirmation;
- policy enforcement;
- product UX.

Không nên nghĩ safeguard = “refusal”.

Safeguards có mục tiêu rộng hơn:

> giảm risk trong khi vẫn giữ legitimate use hữu ích.

---

# 14. Layer 6 — Monitoring and enforcement

Safety không dừng ở pre-deployment.

OpenAI công khai mô tả việc sử dụng các cơ chế như:

- automated detection;
- human review trong các context phù hợp;
- user reports;
- policy enforcement.

Đây là post-deployment safety.

Mental model:

```text
Pre-deployment safety
+
Post-deployment monitoring
```

---

# 15. Usage Policies

**Usage Policies** trả lời loại câu hỏi:

> “Người dùng/developer được phép và không được phép dùng OpenAI services như thế nào?”

Mental model:

```text
Usage Policies
=
"What uses are allowed / restricted?"
```

Nó khác Model Spec.

### Model Spec

Behavior của model.

### Usage Policies

Expectation/rules về cách services được sử dụng.

---

# 16. Safety and alignment public pages

OpenAI cũng duy trì public safety materials mô tả:

- safety philosophy;
- alignment;
- research;
- deployment practices;
- public updates.

Những page này hữu ích để hiểu **approach**.

Nhưng với claim cụ thể về model:

> system card thường là source phù hợp hơn.

---

# 17. Frontier Governance Framework

Năm 2026, OpenAI công bố **Frontier Governance Framework** để mô tả cách safety/security practices liên hệ với các yêu cầu governance và regulation mới nổi.

Framework này đề cập ở cấp governance đến các chủ đề như:

- risk assessment;
- mitigation;
- model reporting;
- security risk management;
- incident response;
- external expert input;
- framework updates.

Partner không cần thuộc legal detail.

Điểm cần nhớ:

> Safety cũng có governance layer, không chỉ technical layer.

---

# 18. Public reference map

Hãy lưu bảng này.

| Câu hỏi | Source nên xem |
|---|---|
| Model nên hành xử thế nào? | **Model Spec** |
| OpenAI cho phép use như thế nào? | **Usage Policies** |
| Model/product cụ thể đã được đánh giá ra sao? | **System Card / Deployment Safety Hub** |
| OpenAI quản lý frontier catastrophic/severe risk thế nào? | **Preparedness Framework** |
| Safety philosophy / alignment approach? | **OpenAI Safety pages** |
| Governance / reporting framework mới? | **Frontier Governance Framework** |
| Data control cụ thể của API/product? | **Official product/platform documentation** |

Đây là một trong những bảng quan trọng nhất của section.

---

# 19. Current public examples

Tính đến 20/09/2026, Deployment Safety Hub tiếp tục xuất bản system cards cho các release mới.

Điều quan trọng với bạn không phải thuộc mọi model.

Điều cần học:

> **Safety evidence is version- and product-specific.**

Ví dụ:

```text
Claim about model A
should be supported by
model A's current documentation
```

Không nên lấy system card của model khác rồi suy rộng.

---

# 20. OpenAI safety approach — simplified stack

```text
┌──────────────────────────────┐
│ Public transparency          │
│ System cards / reports       │
├──────────────────────────────┤
│ Monitoring & enforcement     │
├──────────────────────────────┤
│ Product / deployment controls│
├──────────────────────────────┤
│ Risk-specific safeguards     │
├──────────────────────────────┤
│ Evals + red teaming          │
├──────────────────────────────┤
│ Model behavior / alignment   │
├──────────────────────────────┤
│ Research & training          │
└──────────────────────────────┘
```

Không phải official architecture diagram; đây là mental model học tập.

---

# 21. Partner use of public references

Partner nên dùng public references để:

- answer customer questions;
- avoid invented claims;
- distinguish current facts from assumptions;
- prepare security/safety discussions;
- point technical stakeholder tới evidence;
- stay current as systems change.

---

# 22. What not to do

## Don’t #1
Nói:

> “OpenAI is safe.”

Quá chung.

## Don’t #2
Trích một system card cũ cho model mới.

## Don’t #3
Dùng Model Spec để claim compliance certification.

Sai loại source.

## Don’t #4
Dùng Usage Policies như technical evaluation evidence.

Cũng sai loại source.

## Don’t #5
Invent current data retention/security details.

Phải xem product docs hiện tại.

---

# 23. Source hierarchy

Khi cần xác minh một claim:

```text
Exact product/model official docs
        ↓
Current system card
        ↓
Current policy/framework
        ↓
General OpenAI safety page
        ↓
Secondary commentary
```

Đây không phải thứ tự tuyệt đối cho mọi câu hỏi, nhưng là default tốt.

---

# 24. Public references — official

Các nguồn nên bookmark:

## 1. OpenAI Safety / Preparedness

**Purpose:** overview + Preparedness Framework.

https://openai.com/safety/preparedness

## 2. Deployment Safety Hub

**Purpose:** system cards, release-specific safety evaluations.

https://deploymentsafety.openai.com/

## 3. Model Spec

**Purpose:** intended model behavior.

https://model-spec.openai.com/

## 4. Usage Policies

**Purpose:** rules for use of OpenAI services.

https://openai.com/policies/usage-policies/

## 5. Frontier Governance Framework

**Purpose:** governance and safety/security framework alignment.

https://openai.com/index/openai-frontier-governance-framework/

## 6. OpenAI Safety approach

**Purpose:** safety/alignment philosophy and public explanation.

https://openai.com/safety/

## 7. OpenAI Platform documentation

**Purpose:** current technical/product-specific behavior, data controls and implementation guidance.

https://platform.openai.com/docs

---

# 25. Source-check workflow

Khi customer hỏi factual safety question:

```text
1. Identify exact claim
2. Identify exact product/model
3. Select correct official source
4. Check freshness/version
5. Read limitations
6. Answer only what source supports
7. Separate source fact from recommendation
```

---

# 26. Example

Customer:

> “Model mới có guarantee không hallucinate không?”

Bad:

> “Có safeguard nên không hallucinate.”

Better reasoning:

```text
Need claim:
hallucination behavior

Need evidence:
model-specific system card/evals

Need application evidence:
customer eval set

Conclusion:
No unsupported guarantee.
```

Partner response nên tập trung vào:

- measured performance;
- known limitations;
- grounding;
- evals;
- controls.

---

# 27. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| **Model Spec** | Tài liệu mô tả model behavior mong muốn |
| **System Card** | Báo cáo safety/evaluation cho model hoặc product |
| **Preparedness Framework** | Khung quản lý risk từ frontier capabilities |
| **Deployment Safety Hub** | Trung tâm public safety reports |
| **Usage Policies** | Chính sách sử dụng |
| **Red teaming** | Chủ động tìm weakness/failure mode |
| **Evaluation** | Đánh giá |
| **Safeguard** | Biện pháp bảo vệ/giảm risk |
| **Monitoring** | Theo dõi |
| **Enforcement** | Thực thi policy |
| **Governance** | Quản trị |
| **Frontier risk** | Rủi ro liên quan capability tiên tiến |
| **Transparency** | Minh bạch |

---

# 28. Section recap

Hãy nhớ mapping:

```text
Model behavior → Model Spec
Allowed use → Usage Policies
Model-specific safety evidence → System Card
Frontier risk process → Preparedness Framework
Release reports → Deployment Safety Hub
Governance → Frontier Governance Framework
Technical product facts → Product/Platform docs
```

Và nhớ:

> **Use the right source for the right claim.**

---

# 29. Self-check

1. Model Spec và Usage Policies khác nhau thế nào?
2. System Card dùng để trả lời loại câu hỏi nào?
3. Preparedness Framework tập trung vào điều gì?
4. Vì sao không nên lấy một system card cũ để nói về model mới?
5. Nếu customer hỏi API data retention, bạn nên ưu tiên source nào?
