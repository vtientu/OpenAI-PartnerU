# 01 — Why Safety and Responsible AI Matter

> **Course:** Foundation — OpenAI Foundational Knowledge  
> **Sub-course:** AI Safety & Responsible AI  
> **Section:** Why safety and responsible AI matter
>
> **Lưu ý nguồn:** Đây là study guide tổng hợp dựa trên tên section PartnerU và các tài liệu công khai của OpenAI. Không phải transcript nguyên văn của khóa học.

---

# 1. Section objective

Sau section này, bạn cần có thể:

- giải thích **AI safety** và **responsible AI** bằng ngôn ngữ đơn giản;
- hiểu tại sao safety không phải một “feature phụ”;
- phân biệt **model capability**, **system behavior** và **business risk**;
- hiểu tại sao AI có giá trị càng lớn thì responsibility càng quan trọng;
- biết cách đưa safety vào discovery, solution design và deployment.

---

# 2. Big picture

Một cách hiểu ngắn:

> **AI safety** tập trung vào việc giảm khả năng AI gây ra hoặc góp phần gây ra kết quả có hại.

> **Responsible AI** rộng hơn: nó bao gồm cách con người và tổ chức lựa chọn, thiết kế, triển khai, giám sát và chịu trách nhiệm đối với AI.

Mental model:

```text
Powerful capability
        ↓
Real-world use
        ↓
Potential value + potential harm
        ↓
Safety + responsibility
        ↓
Trusted, useful deployment
```

Điểm cần nhớ:

> Safety không đối lập với business value. Trong production, safety thường là điều kiện để value có thể tồn tại bền vững.

---

# 3. AI safety là gì?

AI safety không chỉ có nghĩa:

> “Model không nói nội dung xấu.”

Nó có thể liên quan đến nhiều lớp:

```text
Model behavior
Application behavior
Data
Tools / actions
Permissions
User interaction
Human oversight
Monitoring
Organizational process
```

Một hệ thống AI có thể tạo risk dù model “trả lời tốt” nếu:

- được cấp quyền quá rộng;
- dùng dữ liệu không phù hợp;
- thực hiện action mà không có review;
- người dùng hiểu nhầm output là fact tuyệt đối;
- không có monitoring;
- không có owner khi xảy ra lỗi.

Do đó:

> **AI safety là system-level concern.**

---

# 4. Responsible AI là gì?

Responsible AI hỏi không chỉ:

> “AI có làm được không?”

mà còn:

- Có **nên** dùng AI ở workflow này không?
- Ai chịu trách nhiệm về outcome?
- User có biết họ đang tương tác với AI không?
- Data có được sử dụng phù hợp không?
- Có human review ở điểm cần thiết không?
- Có đo quality không?
- Có fallback khi AI không chắc không?
- Có process để xử lý incident không?

Responsible AI là cách tổ chức biến các nguyên tắc thành:

```text
Decisions
+ Controls
+ Ownership
+ Measurement
```

---

# 5. Vì sao safety quan trọng?

## 5.1. AI có thể tạo output không chính xác

Generative AI không phải database fact engine.

Model có thể:

- hiểu sai context;
- thiếu information;
- tạo unsupported claims;
- chọn sai step;
- bỏ sót exception.

Nếu user sử dụng output mà không có controls phù hợp, lỗi model có thể trở thành lỗi business.

---

## 5.2. AI có thể được dùng trong workflow có consequence thật

Ví dụ:

```text
AI draft email
```

risk thấp hơn:

```text
AI decides financial action
```

hoặc:

```text
AI provides information used in a high-impact decision
```

Risk không chỉ phụ thuộc vào model.

Nó phụ thuộc:

```text
Risk
≈
Probability of failure
×
Impact of failure
×
Degree of autonomy/exposure
```

Đây không phải công thức toán chính thức; nó là mental model để tư duy.

---

# 6. Capability creates responsibility

Một model càng có khả năng:

- reason;
- use tools;
- browse;
- execute actions;
- operate across systems;

thì system designer càng phải suy nghĩ về:

- scope;
- permission;
- verification;
- escalation;
- monitoring.

Ví dụ:

### AI chỉ draft

```text
AI → draft → human sends
```

### AI có action authority

```text
AI → decides → tool → external action
```

Case thứ hai cần nhiều control hơn.

---

# 7. Safety và trust liên quan thế nào?

Customer trust không nên dựa trên lời nói:

> “Model này an toàn.”

Trust nên dựa trên:

```text
Clear scope
+ Evaluation
+ Controls
+ Transparency
+ Monitoring
+ Ownership
```

Safety là một trong những nền tảng để tạo trust.

Nhưng trust không phải cảm giác.

Nó cần evidence.

---

# 8. Safety và business value không phải trade-off đơn giản

Một cách hiểu sai:

```text
More safety = less useful
```

Trong production, nhiều safety control giúp solution **hữu ích hơn**.

Ví dụ:

- grounding giúp answer chính xác hơn;
- permission giúp tránh action sai;
- human escalation xử lý edge case tốt hơn;
- monitoring giúp cải thiện system;
- evals giúp team biết khi nào solution đủ tốt.

Tức là:

```text
Responsible design
→ reliability
→ adoption
→ sustainable value
```

---

# 9. Responsible AI cần bắt đầu từ use-case selection

Không phải risk nào cũng nên giải quyết bằng guardrail.

Đôi khi lựa chọn đúng là:

> Không sử dụng AI cho một phần của workflow.

Ví dụ, nếu task:

- consequence rất cao;
- không có reliable data;
- không có owner;
- không thể evaluate;
- không có escalation;
- regulatory constraints chưa rõ;

thì opportunity có thể chưa ready.

Điều này nối trực tiếp với qualification:

```text
Business value
+
Feasibility
+
Readiness
+
Trust
```

---

# 10. Safety-by-design

**Safety-by-design** có nghĩa:

> Xem safety là requirement ngay từ lúc thiết kế, không phải patch ở cuối.

Traditional anti-pattern:

```text
Build demo
→ integrate everything
→ prepare launch
→ ask security/legal at the end
```

Better:

```text
Discover
↓
Identify risk
↓
Define controls
↓
Prototype
↓
Evaluate
↓
Pilot
↓
Review
↓
Deploy
```

---

# 11. Risk-based thinking

Không phải mọi workflow cần cùng mức control.

### Low-consequence example

> AI brainstorm internal meeting titles.

Có thể cần ít control.

### Higher-consequence example

> AI tạo recommendation có thể ảnh hưởng đến customer account action.

Có thể cần:

- trusted context;
- constrained tool permission;
- human approval;
- audit logs;
- evaluation;
- escalation.

Mental model:

> **Controls should be proportional to risk.**

---

# 12. Responsible AI lifecycle

Hãy ghi nhớ lifecycle:

```text
1. Choose use case
2. Identify stakeholders
3. Map possible harms/failures
4. Design controls
5. Build
6. Evaluate
7. Pilot
8. Monitor
9. Respond
10. Improve
```

Safety không kết thúc ở step 6.

Production evidence rất quan trọng.

---

# 13. Partner perspective

Một OpenAI partner không chỉ chịu trách nhiệm về technical integration.

Partner cần giúp customer đặt đúng câu hỏi:

### Business
- outcome là gì?
- consequence nếu sai?

### Technical
- data từ đâu?
- tool nào?
- permission nào?

### Safety
- failure mode nào?
- control nào?
- escalation nào?

### Governance
- ai là owner?
- ai approve?
- ai monitor?

### Measurement
- metric nào chứng minh system đủ tốt?

---

# 14. Example — Customer support assistant

Customer muốn AI trả lời support.

### Không đủ

```text
Model can answer questions
→ deploy chatbot
```

### Responsible design

```text
Supported topics
↓
Approved knowledge base
↓
Grounded answers
↓
Evaluation
↓
Low-risk questions → answer
↓
Sensitive/uncertain cases → human agent
↓
Monitor failures
```

Safety không làm solution “kém AI”.

Nó làm solution deployable.

---

# 15. Example — Internal coding assistant

Risk có thể gồm:

- code không đúng;
- insecure pattern;
- dependency problem;
- developer overreliance.

Controls có thể gồm:

```text
AI suggests code
↓
Developer review
↓
Tests
↓
Static/security checks
↓
Code review
↓
Deployment pipeline
```

AI được đặt trong software engineering control system hiện có.

---

# 16. Responsible AI ≠ zero risk

Không có production technology nào bảo đảm zero risk.

Mục tiêu thực tế là:

```text
Understand risk
↓
Reduce risk
↓
Define acceptable boundaries
↓
Monitor remaining risk
↓
Respond when needed
```

Một partner nên tránh câu:

> “Hệ thống này hoàn toàn an toàn.”

Nên nói:

> “Đây là risk profile, các controls hiện tại và evidence chúng ta có.”

---

# 17. Common mistakes

## Mistake 1 — Safety = content filtering

Quá hẹp.

Safety còn gồm action, permissions, data, reliability, misuse và monitoring.

## Mistake 2 — Safety team xử lý sau

Sai.

Safety cần tham gia solution design.

## Mistake 3 — Model safety = application safety

Sai.

Một model có safeguard vẫn có thể được tích hợp vào system design kém.

## Mistake 4 — Zero risk

Không thực tế.

Cần risk management.

## Mistake 5 — Compliance = responsible AI

Compliance quan trọng nhưng responsible AI rộng hơn.

Một system có thể “compliant” theo một requirement nhưng vẫn có UX, reliability hoặc accountability problem.

---

# 18. Practical framework — VALUE × RISK

Khi nghe một candidate use case, hỏi song song hai nhóm.

## VALUE

- Problem là gì?
- Ai được lợi?
- KPI nào cải thiện?
- Scale bao nhiêu?

## RISK

- AI có thể sai kiểu nào?
- Sai thì ảnh hưởng ai?
- AI có action authority không?
- Data sensitivity?
- Có human review không?
- Có thể evaluate không?

Không đánh giá value mà bỏ risk.

Cũng không đánh giá risk mà bỏ value.

---

# 19. English–Vietnamese glossary

| Term | Nghĩa dễ hiểu |
|---|---|
| **AI safety** | An toàn AI |
| **Responsible AI** | AI có trách nhiệm |
| **Harm** | Tác hại |
| **Risk** | Rủi ro |
| **Failure mode** | Kiểu hệ thống có thể thất bại |
| **Consequence** | Hậu quả |
| **Safety-by-design** | Thiết kế safety ngay từ đầu |
| **Human oversight** | Sự giám sát của con người |
| **Control** | Cơ chế kiểm soát |
| **Accountability** | Trách nhiệm giải trình |
| **Risk-based** | Thiết kế theo mức rủi ro |
| **Residual risk** | Rủi ro còn lại sau khi đã giảm thiểu |
| **Mitigation** | Biện pháp giảm thiểu |
| **Incident** | Sự cố |

---

# 20. Section recap

1. AI safety là system concern, không chỉ model concern.
2. Responsible AI gồm cách con người lựa chọn, thiết kế, sử dụng và chịu trách nhiệm với AI.
3. Capability càng lớn → responsibility càng lớn.
4. Controls nên proportional với risk.
5. Safety nên bắt đầu từ use-case selection.
6. Responsible deployment cần evaluation, monitoring và ownership.
7. Safety hỗ trợ trust và sustainable business value.
8. Mục tiêu không phải zero risk mà là **understand → mitigate → monitor → improve**.

---

# 21. Self-check

1. AI safety và responsible AI khác nhau như thế nào?
2. Vì sao model safety không đồng nghĩa application safety?
3. Safety-by-design nghĩa là gì?
4. Tại sao use-case selection là một safety decision?
5. Hãy nêu ít nhất 5 thành phần của responsible AI lifecycle.
