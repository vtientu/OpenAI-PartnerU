# 02 — Recognizing Common AI Safety Concerns

> **Course:** Foundation — OpenAI Foundational Knowledge  
> **Sub-course:** AI Safety & Responsible AI  
> **Section:** Recognizing common AI safety concerns
>
> **Lưu ý:** Mục tiêu của section là nhận diện concern để thiết kế solution an toàn hơn, không phải mô tả cách khai thác hay vượt safeguard.

---

# 1. Section objective

Sau section này, bạn cần:

- nhận diện các nhóm concern phổ biến trong AI system;
- phân biệt **model limitation**, **misuse risk**, **system risk** và **organizational risk**;
- biết concern nào cần hỏi trong discovery;
- hiểu rằng một use case có thể có nhiều risk cùng lúc;
- biết áp dụng framework **Risk → Impact → Control → Evidence**.

---

# 2. Big picture

Không có một danh sách risk duy nhất phù hợp cho mọi AI system.

Tuy nhiên, trong enterprise AI thường gặp các nhóm:

```text
1. Accuracy / hallucination
2. Bias / fairness
3. Privacy / data handling
4. Security
5. Misuse
6. Overreliance
7. Tool / action risk
8. Transparency
9. Sensitive or high-impact contexts
10. Governance / accountability
```

Điều quan trọng không phải thuộc tên.

Điều quan trọng là biết hỏi:

> “Concern này biểu hiện thế nào trong workflow cụ thể của customer?”

---

# 3. Concern #1 — Incorrect or unsupported output

Generative models có thể:

- trả lời sai;
- hiểu nhầm;
- thiếu context;
- tạo unsupported claim;
- suy luận quá xa dữ liệu.

Đây thường được gọi là:

- **hallucination**;
- factual error;
- ungrounded output.

### Example

AI assistant được hỏi policy nội bộ nhưng không có policy hiện tại.

Nếu nó tự tạo answer → risk.

### Controls

- grounding;
- retrieval;
- citations;
- evals;
- fallback;
- human review.

### Partner question

> “Đối với workflow này, một câu trả lời sai có consequence gì?”

---

# 4. Concern #2 — Bias and fairness

AI có thể tạo outcome khác nhau giữa các nhóm hoặc phản ánh bias trong:

- training data;
- prompt;
- business process;
- evaluation data;
- downstream decision rules.

Responsible thinking không nên đơn giản là:

> “Model có bias hay không?”

Mà là:

```text
Who is affected?
↓
What decision/output?
↓
What evidence?
↓
What safeguards?
```

### High-impact context

Nếu AI ảnh hưởng tới quyết định quan trọng về con người, fairness cần được xem xét cẩn thận hơn.

---

# 5. Concern #3 — Privacy and data handling

AI workflow có thể xử lý:

- personal data;
- confidential business data;
- customer records;
- intellectual property;
- internal documents.

Các câu hỏi chính:

- Data nào được gửi?
- Vì sao cần data đó?
- Ai có access?
- Data lưu ở đâu?
- Retention/configuration hiện tại là gì?
- Customer policy có cho phép không?

### Principle

> **Use the minimum necessary data and verify current product/data controls from official documentation.**

Partner không nên tự suy đoán data policy.

---

# 6. Concern #4 — Security

AI application mở thêm một “intelligence interface” với hệ thống.

Security concern có thể gồm ở mức khái niệm:

- unauthorized access;
- unsafe tool invocation;
- malicious/untrusted input;
- prompt injection;
- data exposure;
- excessive permissions.

Không cần hiểu các kỹ thuật tấn công chi tiết để nắm principle:

```text
Untrusted input
should not automatically
become trusted instruction
```

### Controls

- least privilege;
- authentication;
- authorization;
- input isolation;
- tool constraints;
- approval for high-impact actions;
- monitoring.

---

# 7. Prompt injection — hiểu ở mức solution design

**Prompt injection** xảy ra khi nội dung không đáng tin cố gắng làm AI thay đổi hành vi ngoài intent của application.

Ví dụ abstract:

```text
App retrieves external document
↓
Document contains instructions
↓
Model may interpret instructions as task direction
```

Điểm cần nhớ:

> Retrieval data và user-provided content không nên mặc nhiên có cùng authority với developer/system instructions.

Partner lens:

- nguồn input có đáng tin không?
- model có quyền action không?
- tool có permission gì?
- high-impact action có approval không?

---

# 8. Concern #5 — Misuse

Một capability hữu ích cũng có thể bị sử dụng theo cách không phù hợp.

Responsible deployment cần:

- acceptable-use boundaries;
- policies;
- access controls;
- abuse monitoring;
- escalation.

Misuse khác model error.

### Model error

System cố gắng làm đúng nhưng sai.

### Misuse

User hoặc actor cố sử dụng system theo cách không được phép.

---

# 9. Concern #6 — Overreliance / automation bias

**Overreliance** = user tin AI quá mức.

Ví dụ:

```text
AI answer
→ user assumes correct
→ no verification
```

AI output có thể được trình bày rất tự tin dù thiếu evidence.

Controls:

- UX communication;
- source links;
- uncertainty handling;
- review requirements;
- training;
- clear responsibility.

---

# 10. Concern #7 — Action and autonomy risk

Khi AI chỉ draft text, impact thường thấp hơn khi AI có tool access.

Compare:

```text
A. AI drafts refund recommendation
```

vs.

```text
B. AI executes refund
```

B cần cân nhắc:

- amount limits;
- allowed actions;
- approval;
- authentication;
- audit log;
- exception handling.

Mental model:

> **More authority → stronger controls.**

---

# 11. Concern #8 — Transparency

User cần đủ context để hiểu:

- họ đang tương tác với AI hay người?
- output là draft hay final?
- source nào được dùng?
- limit nào quan trọng?
- khi nào phải verify?

Transparency không có nghĩa hiển thị mọi technical detail.

Nó có nghĩa:

> cung cấp information cần thiết để user sử dụng system đúng cách.

---

# 12. Concern #9 — Sensitive / high-impact contexts

Một số use case cần mức scrutiny cao hơn vì error có thể ảnh hưởng đáng kể đến:

- safety;
- rights;
- financial outcomes;
- access/opportunity;
- vulnerable users.

Partner nên:

- involve appropriate domain experts;
- review current law/policy;
- define strict controls;
- avoid unsupported claims;
- establish human accountability.

AI không loại bỏ professional responsibility.

---

# 13. Concern #10 — Governance and ownership

Một system có thể fail organizationally nếu không ai biết:

- ai own use case;
- ai approve changes;
- ai review incidents;
- ai maintain evals;
- ai update knowledge;
- ai decide when to disable system.

Technical controls không thay thế ownership.

---

# 14. Risk taxonomy theo 4 nguồn

Một framework dễ nhớ:

```text
MODEL
- incorrect output
- inconsistent behavior

DATA
- poor quality
- privacy
- stale context

SYSTEM
- tools
- permissions
- security
- integration failure

HUMAN / ORGANIZATION
- misuse
- overreliance
- unclear ownership
- weak process
```

Điều này giúp tránh lỗi:

> “Mọi vấn đề đều do model.”

---

# 15. Risk = context dependent

Cùng một behavior có thể có risk khác nhau.

### Example

AI viết draft internal note:

- error impact thấp;
- human review tự nhiên.

AI tạo customer-facing policy answer:

- error impact cao hơn;
- cần grounding và evals.

AI có quyền update account:

- action risk cao hơn nữa.

Tức là risk phụ thuộc:

```text
Task
× User
× Data
× Authority
× Impact
× Controls
```

---

# 16. Practical framework — RICE

Không phải product prioritization RICE.

Ở đây dùng mnemonic học tập:

## R — Risk

Điều gì có thể sai?

## I — Impact

Nếu sai thì hậu quả là gì?

## C — Control

Control nào giảm risk?

## E — Evidence

Evidence nào chứng minh control hoạt động?

Ví dụ:

```text
Risk:
AI trả lời sai policy

Impact:
employee receives wrong guidance

Control:
approved knowledge base + grounded answers + escalation

Evidence:
evaluation on representative policy questions
```

---

# 17. Example — Sales assistant

Use case:

> AI chuẩn bị account brief cho salesperson.

Possible concerns:

### Accuracy
Tóm tắt sai customer history.

### Data
Expose information salesperson không có permission.

### Overreliance
Salesperson không verify critical account fact.

### Staleness
Context cũ.

### Governance
Không ai own source data quality.

Controls:

```text
Permission-aware retrieval
+ source citation
+ freshness metadata
+ user verification for key facts
+ evals
```

---

# 18. Example — Agent with enterprise tools

AI có thể gọi internal tools.

Safety thinking:

```text
Which tools?
↓
Which actions?
↓
Which user identity?
↓
What permission?
↓
Which actions need confirmation?
↓
What gets logged?
```

Không bắt đầu bằng:

> “Agent có thể làm mọi thứ.”

Bắt đầu bằng:

> “Agent cần quyền tối thiểu nào để hoàn thành task?”

Đó là **least privilege**.

---

# 19. Safety concern ≠ reason to reject AI

Nhận diện concern không có nghĩa:

> “Không nên dùng AI.”

Mục tiêu:

```text
Concern
↓
Assess
↓
Mitigate
↓
Evaluate
↓
Decide
```

Có ba outcome hợp lý:

1. deploy với controls;
2. redesign use case;
3. chưa deploy nếu risk/readiness chưa phù hợp.

---

# 20. Common mistakes

## Mistake 1
Chỉ nghĩ về hallucination.

## Mistake 2
Treat every use case as same risk.

## Mistake 3
Model-only thinking.

## Mistake 4
Give agent broad permissions for convenience.

## Mistake 5
Không đo effectiveness của control.

## Mistake 6
Gọi mọi uncertainty là “bias”.

Cần xác định concern cụ thể.

---

# 21. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| **Hallucination** | Output không có căn cứ phù hợp |
| **Bias** | Thiên lệch |
| **Fairness** | Công bằng |
| **Privacy** | Quyền riêng tư |
| **Confidential data** | Dữ liệu mật |
| **Prompt injection** | Input không đáng tin cố ảnh hưởng instruction của AI |
| **Misuse** | Sử dụng sai/misuse |
| **Overreliance** | Tin tưởng AI quá mức |
| **Automation bias** | Thiên hướng tin quyết định tự động |
| **Autonomy** | Mức tự chủ |
| **Transparency** | Minh bạch |
| **Least privilege** | Chỉ cấp quyền tối thiểu cần thiết |
| **Audit log** | Nhật ký phục vụ kiểm tra |
| **Governance** | Quản trị |
| **Failure mode** | Kiểu thất bại |

---

# 22. Section recap

Hãy nhớ taxonomy:

```text
Accuracy
Bias/fairness
Privacy
Security
Misuse
Overreliance
Actions/autonomy
Transparency
High-impact contexts
Governance
```

Và luôn dùng:

```text
Risk
→ Impact
→ Control
→ Evidence
```

---

# 23. Self-check

1. Hallucination và misuse khác nhau thế nào?
2. Vì sao tool permission là safety concern?
3. Overreliance là gì?
4. “Least privilege” có ý nghĩa gì trong agent design?
5. Hãy áp dụng Risk → Impact → Control → Evidence cho một AI coding assistant.
