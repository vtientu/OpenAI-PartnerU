# 05 — Effective Safety Communication

> **Course:** Foundation — OpenAI Foundational Knowledge  
> **Sub-course:** AI Safety & Responsible AI  
> **Section:** Effective safety communication
>
> **Mục tiêu:** Giúp partner giao tiếp về safety một cách chính xác, có evidence, không gây hoảng sợ và không overclaim.

---

# 1. Section objective

Sau section này, bạn cần:

- biết cách nói về safety với customer;
- tránh cả hai cực: **overpromise** và **fear-based communication**;
- phân biệt fact, evidence, assumption và recommendation;
- biết trả lời câu hỏi “AI này có an toàn/chính xác không?”;
- sử dụng framework **Scope → Risk → Control → Evidence → Ownership**.

---

# 2. Big picture

Safety communication tốt cần đồng thời:

```text
Accurate
+
Understandable
+
Relevant
+
Evidence-based
+
Actionable
```

Không chỉ đúng về technical detail.

Nó phải giúp customer ra quyết định tốt.

---

# 3. Hai lỗi cực đoan

## Extreme 1 — Overconfidence

> “Model này an toàn.”

> “Nó sẽ không hallucinate.”

> “AI sẽ không làm sai.”

Vấn đề:

- claim quá rộng;
- không có context;
- không có evidence;
- làm giảm credibility.

---

## Extreme 2 — Fear language

> “AI rất nguy hiểm nên phải cực kỳ cẩn thận với mọi thứ.”

Vấn đề:

- không giúp customer quyết định;
- không phân biệt risk;
- có thể tạo confusion;
- bỏ mất business value.

Tốt hơn:

> Nói risk cụ thể, consequence cụ thể và control cụ thể.

---

# 4. Safety communication = scoped communication

Thay vì:

> “AI có an toàn không?”

Hãy chuyển thành:

> “An toàn cho task nào, user nào, với data nào, trong workflow nào và dưới controls nào?”

Đây là **scope**.

---

# 5. Framework — SCORE

Một framework dễ nhớ:

## S — Scope

System làm gì?

Không làm gì?

## C — Concern

Failure/misuse concern là gì?

## O — Operational controls

Controls nào đang tồn tại?

## R — Results / evidence

Evals hoặc evidence nói gì?

## E — Escalation / ownership

Nếu system không chắc hoặc fail thì ai xử lý?

---

# 6. Fact vs interpretation vs recommendation

Partner nên phân biệt ba loại statement.

## Fact

> “System card báo cáo evaluation X.”

Đây là source-backed fact.

## Interpretation

> “Điều này cho thấy model có capability phù hợp để pilot.”

Đây là interpretation.

## Recommendation

> “Tôi khuyên nên giữ human approval trong phase đầu.”

Đây là recommendation.

Không nên trộn cả ba thành:

> “System card chứng minh ta có thể fully automate.”

Đó là overreach.

---

# 7. Evidence hierarchy

Khi nói về safety:

```text
Customer-specific eval
    +
Current official model/product docs
    +
System card / published evidence
    +
General statements
```

General statement yếu hơn evidence cụ thể cho use case.

Ví dụ:

> “Model có strong reasoning.”

không mạnh bằng:

> “Trên 500 representative cases của workflow, system đạt threshold đã thống nhất.”

---

# 8. Communicating limitations

Nói limitation tốt không có nghĩa làm sản phẩm trông tệ.

Mục tiêu là:

```text
What works
+
Where it may fail
+
How we control failure
```

Ví dụ:

> “Assistant hoạt động tốt trên các policy topic đã được index. Với câu hỏi ngoài source hoặc khi evidence conflict, hệ thống sẽ route tới HR.”

Đây là communication mạnh.

---

# 9. Communicating uncertainty

Uncertainty nên cụ thể.

Weak:

> “Có thể có rủi ro.”

Better:

> “Chúng ta chưa đo exception rate trên các invoice scan chất lượng thấp; pilot cần bổ sung nhóm case đó.”

Specific uncertainty tạo action.

---

# 10. Never guarantee unsupported accuracy

Nếu customer hỏi:

> “Có chính xác 100% không?”

Không nên trả lời bằng guarantee.

Better response structure:

```text
1. Define task
2. Explain variability
3. Present existing evidence
4. Identify remaining gaps
5. Propose controls/evaluation
```

Ví dụ:

> “Không nên đặt guarantee 100% khi chưa có evidence trên task cụ thể. Với workflow này, ta có thể định nghĩa correctness rõ, xây evaluation set và giữ human review cho các exception.”

---

# 11. “Safe” is not binary

Một system không chỉ có hai state:

```text
SAFE / UNSAFE
```

Thực tế:

```text
Use case
+ deployment conditions
+ controls
+ evidence
= risk posture
```

Vì vậy nên dùng ngôn ngữ như:

- “appropriate for this scope”;
- “tested under these conditions”;
- “remaining limitation”;
- “requires human review”.

---

# 12. Communicating with different stakeholders

## Executive

Quan tâm:

- risk vs value;
- governance;
- business exposure;
- adoption.

Nói:

> outcome, controls, ownership.

Không cần mở đầu bằng technical eval details.

---

## Security team

Quan tâm:

- architecture;
- access;
- data flow;
- permissions;
- monitoring.

Nói:

> threat boundaries, controls, logs.

---

## Legal / compliance

Quan tâm:

- obligations;
- governance;
- policy;
- affected users.

Nói:

> purpose, data, decision role, oversight.

---

## Developer

Quan tâm:

- implementation;
- failure modes;
- evals;
- tool boundaries.

Nói:

> system design và testing.

---

## End user

Quan tâm:

- dùng thế nào;
- có thể tin đến đâu;
- khi nào verify/escalate.

Nói:

> simple, actionable guidance.

---

# 13. Translating technical safety into business language

Technical:

> “We use retrieval grounding.”

Business:

> “Answers are based on the approved company knowledge source rather than relying only on the model’s general knowledge.”

Technical:

> “Tool calls use least privilege.”

Business:

> “The agent only gets the minimum permissions needed for its task.”

Technical:

> “We maintain an eval set.”

Business:

> “We continuously test the system against representative real cases.”

Partner cần nói được cả hai ngôn ngữ.

---

# 14. Avoid false certainty from benchmarks

Benchmark:

> useful for understanding general capability.

But customer asks:

> “Will it work for us?”

Need:

- customer data;
- workflow;
- architecture;
- evals.

Safety communication nên nói rõ distinction:

```text
Benchmark evidence
≠
Production guarantee
```

---

# 15. Source discipline

Nếu customer hỏi về:

- current product capability;
- data controls;
- security;
- policy;
- certifications;
- retention;
- model-specific safety results;

Partner nên:

1. mở source official;
2. kiểm tra date/version;
3. quote/paraphrase chính xác;
4. không suy rộng.

Nếu không biết:

> nói chưa xác minh và kiểm tra lại.

Credibility > instant answer.

---

# 16. Safety communication pattern for customer meetings

Một cấu trúc tốt:

### 1. Goal
“Workflow này nhằm giảm thời gian xử lý ticket.”

### 2. Scope
“Phase đầu chỉ xử lý 5 category low-risk.”

### 3. Main concerns
“Concern chính là factual error và action sai.”

### 4. Controls
“Grounded policy + restricted tools + escalation.”

### 5. Evidence
“Pilot sẽ dùng 1,000 historical cases.”

### 6. Ownership
“Support ops owns acceptance criteria; IT owns access.”

### 7. Next step
“Review eval result trước khi mở rộng scope.”

Đây là safety communication gắn với opportunity progression.

---

# 17. Communicating an incident

Nếu có issue:

Không nên:

- đoán nguyên nhân;
- downplay;
- blame ngay;
- hứa fix trước khi hiểu.

Nên:

```text
What happened?
↓
Known impact?
↓
What is confirmed vs unknown?
↓
Containment/control?
↓
Owner?
↓
Next update?
```

Incident communication cần accuracy cao.

---

# 18. Safety claims checklist

Trước khi nói một claim, hỏi:

- Claim có scope rõ không?
- Source là gì?
- Source có current không?
- Claim nói model hay application?
- Có assumption không?
- Có limitation không?
- Có customer-specific evidence không?
- Có vô tình biến likelihood thành guarantee không?

---

# 19. Example — “Is this safe for production?”

Customer:

> “Demo chạy tốt. Nó safe for production chưa?”

Bad:

> “Có, model đã có safeguard.”

Better:

> “Demo quality mới chỉ là một phần. Để đánh giá production readiness, chúng ta cần kiểm tra representative evals, access/permissions, data handling, escalation, monitoring và operational ownership. Sau đó mới xác định scope nào sẵn sàng production.”

---

# 20. Example — “Does OpenAI guarantee no data leakage?”

Bad:

> “Có.”

Better approach:

- xác định exact product;
- xem current data/security docs;
- mô tả documented controls;
- phân biệt platform behavior với app/customer architecture;
- không invent guarantee.

---

# 21. Example — “Can we remove human review?”

Không trả lời theo ideology.

Dùng evidence:

```text
What task?
What error cost?
What eval performance?
What exception rate?
What controls?
What rollback?
```

Human review là architecture choice dựa trên risk/evidence.

---

# 22. Common mistakes

## Mistake 1
Dùng từ “safe” mà không scope.

## Mistake 2
Nói “100%”.

## Mistake 3
Trộn model evidence với solution evidence.

## Mistake 4
Dùng jargon với executive.

## Mistake 5
Che giấu uncertainty.

## Mistake 6
Nói limitation mà không đưa path forward.

## Mistake 7
Invent policy/product facts.

---

# 23. Practical framework — SCOPE

Bạn cũng có thể dùng mnemonic:

## S — Situation
Use case gì?

## C — Concern
Risk cụ thể?

## O — Ownership
Ai chịu trách nhiệm?

## P — Protection
Controls?

## E — Evidence
Đo thế nào?

Ví dụ:

```text
Situation:
AI HR assistant

Concern:
wrong policy answer

Ownership:
HR owns policy

Protection:
grounding + escalation

Evidence:
policy Q&A eval set
```

---

# 24. Effective wording bank

Các câu partner có thể dùng:

### Khi chưa đủ evidence

> “Chúng ta chưa có đủ evidence để khẳng định điều đó trên workflow này.”

### Khi capability phù hợp nhưng cần test

> “Capability có vẻ phù hợp; bước tiếp theo là validate trên representative customer cases.”

### Khi nói limitation

> “Hệ thống hoạt động trong scope X; ngoài scope đó sẽ cần fallback/escalation.”

### Khi nói risk

> “Concern chính không phải chỉ là model output, mà là consequence nếu action sai.”

### Khi cần official verification

> “Phần này phụ thuộc product/version hiện tại; nên xác minh từ documentation chính thức trước khi đưa thành commitment.”

---

# 25. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| **Communication discipline** | Kỷ luật trong cách giao tiếp |
| **Overclaim** | Nói quá mức evidence |
| **Guarantee** | Cam kết/bảo đảm tuyệt đối |
| **Limitation** | Giới hạn |
| **Uncertainty** | Điều chưa chắc chắn |
| **Assumption** | Giả định |
| **Evidence-based** | Dựa trên bằng chứng |
| **Scope** | Phạm vi |
| **Risk posture** | Trạng thái/mức risk trong một deployment |
| **Production readiness** | Mức sẵn sàng production |
| **Incident** | Sự cố |
| **Containment** | Kiểm soát/phạm vi hóa sự cố |
| **Commitment** | Cam kết |

---

# 26. Section recap

1. Safety communication phải scoped.
2. Tránh cả overconfidence lẫn fear language.
3. Phân biệt fact, interpretation và recommendation.
4. Nói limitation cùng với controls/path forward.
5. Benchmark không phải production guarantee.
6. Stakeholder khác nhau cần cách diễn đạt khác nhau.
7. Product/policy facts cần official source.
8. Framework tốt:
   **Scope → Concern → Control → Evidence → Ownership.**

---

# 27. Self-check

1. Vì sao “AI này safe không?” là câu hỏi chưa đủ scope?
2. Fact, interpretation và recommendation khác nhau thế nào?
3. Nếu customer hỏi accuracy 100%, bạn nên cấu trúc câu trả lời ra sao?
4. Tại sao benchmark không phải production guarantee?
5. Hãy dùng SCORE hoặc SCOPE để trình bày safety của một AI support assistant.
