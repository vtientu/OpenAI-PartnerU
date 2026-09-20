# 05 — Trust, Accuracy, and Communication Discipline

> **Course:** Foundation — OpenAI Foundational Knowledge  
> **Step:** Introduction to OpenAI  
> **Section:** Trust, accuracy, and communication discipline

---

## 1. Section objective

Sau section này, bạn cần:

- hiểu trust trong AI solution được xây bằng gì;
- hiểu vì sao “accuracy” phải gắn với task;
- hiểu hallucination, evals, guardrails và human-in-the-loop;
- biết cách tránh overclaim;
- biết cách trao đổi với customer theo hướng evidence-based.

---

# 2. Trust trong AI là gì?

Trust không có nghĩa:

> “Customer tin lời partner.”

Trust tốt hơn được hiểu là:

> Customer có đủ bằng chứng và controls để sử dụng hệ thống trong phạm vi đã xác định.

Mental model:

```text
Trust
=
Evidence
+ Controls
+ Transparency
+ Experience
```

---

# 3. Trust phải có scope

Một system có thể đáng tin cho task A nhưng không phù hợp với task B.

Ví dụ:

```text
AI summarizes meeting
```

có risk khác:

```text
AI approves financial transaction
```

Do đó trust luôn phải hỏi:

> **Trusted for what? Under what conditions?**

---

# 4. Accuracy không phải một con số chung

Câu hỏi:

> “Model accuracy là bao nhiêu?”

thường chưa đủ context.

Accuracy phụ thuộc:

- task;
- dataset;
- prompt;
- tools;
- context;
- definition of correct;
- evaluation method.

---

# 5. Ví dụ các loại accuracy khác nhau

## Task A — Extraction

Input:

> Invoice

Output:

> invoice number

Có thể đo:

```text
Exact match
Field-level accuracy
```

---

## Task B — Summarization

Không có một exact answer duy nhất.

Có thể đánh giá:

- factual correctness;
- completeness;
- relevance;
- unsupported claims.

---

## Task C — Agentic workflow

Ví dụ refund agent.

Phải đo:

- chọn policy đúng?
- lấy data đúng?
- gọi tool đúng?
- amount đúng?
- có escalate đúng lúc?
- có vi phạm permission không?

Đây là **system accuracy**, không chỉ model text accuracy.

---

# 6. Probabilistic behavior

Traditional code:

```js
if (status === "paid") {
  return "complete";
}
```

Behavior được quy định rõ.

AI model hoạt động probabilistic hơn.

Do đó cùng task có thể có variation.

Production system cần bổ sung:

```text
Model
+ Context
+ Tools
+ Evals
+ Guardrails
+ Monitoring
+ Human review
```

---

# 7. Hallucination

**Hallucination** = AI tạo information không được support bởi facts/context nhưng trình bày như thật.

Ví dụ:

User hỏi:

> “Policy nghỉ phép mới nhất của công ty là gì?”

Nếu model không có policy nội bộ nhưng tự tạo câu trả lời → hallucination risk.

---

# 8. Hallucination là system-design problem

Không nên nghĩ giải pháp duy nhất là:

> “Dùng model thông minh hơn.”

Có thể cần:

- trusted knowledge source;
- retrieval;
- grounding;
- citations;
- constrained response;
- tool use;
- fallback;
- abstention;
- human escalation.

Mental model:

```text
Better model
≠
Guaranteed truth
```

---

# 9. Evaluation / evals

**Eval** = cách đo behavior của AI system một cách có hệ thống.

Câu hỏi đầu tiên:

> “Successful behavior trông như thế nào?”

Ví dụ support assistant:

- correct intent;
- correct answer;
- grounded in policy;
- correct action;
- correct escalation;
- acceptable tone.

---

# 10. Eval-driven development

Có thể liên hệ với testing.

Traditional:

```text
Code
→ unit test
→ integration test
```

AI:

```text
Prompt/model/system
→ evaluation cases
→ scoring
→ error analysis
→ improve
```

Một eval set tốt nên có:

- common cases;
- edge cases;
- risky cases;
- representative customer data.

---

# 11. Guardrails

**Guardrail** = mechanism giúp giới hạn hoặc kiểm soát behavior.

Ví dụ:

- input validation;
- output filtering;
- policy checks;
- tool permission;
- rate limits;
- approval gates;
- safety classifiers.

Không guardrail nào là perfect.

Tốt hơn là dùng layered controls.

---

# 12. Trust architecture

Một AI solution đáng tin có thể gồm:

```text
1. Right use case
2. Trusted context
3. Clear instructions
4. Minimum permissions
5. Evaluations
6. Guardrails
7. Human escalation
8. Monitoring
9. Continuous improvement
```

Đây là **defense in depth**.

---

# 13. Human-in-the-loop

**Human-in-the-loop (HITL)** = con người tham gia vào decision/action ở các điểm đã thiết kế.

Ví dụ:

```text
AI drafts legal summary
↓
Lawyer reviews
↓
Final action
```

Hoặc:

```text
AI handles normal ticket
↓
High-risk / uncertain
↓
Human agent
```

---

# 14. Khi nào HITL đặc biệt hữu ích?

- cost of error cao;
- workflow regulated;
- legal impact;
- financial impact;
- model confidence không đủ;
- exceptions nhiều;
- deployment còn mới.

HITL không nhất thiết là temporary.

Đôi khi nó là thiết kế production đúng.

---

# 15. Communication discipline

Một partner đáng tin phải nói chính xác.

Không chỉ system cần guardrail.

Communication cũng cần discipline.

---

# 16. Rule 1 — Do not overclaim

Tránh:

> “AI luôn chính xác.”

> “Không có risk.”

> “Nó sẽ thay toàn bộ team.”

> “Hệ thống này sẽ work ngay.”

Thay bằng:

> “Ta cần validate trên representative customer cases.”

---

# 17. Rule 2 — Capability ≠ evidence

Capability statement:

> “Model có thể reason trên tài liệu.”

Evidence statement:

> “Trong pilot trên customer dataset, system đạt metric X.”

Hai câu không thể dùng thay nhau.

Mental model:

```text
General capability
≠
Customer-specific proof
```

---

# 18. Rule 3 — State assumptions

Ví dụ:

> “Architecture này giả định company knowledge base được cập nhật và có API access.”

Nếu assumption không đúng, recommendation có thể thay đổi.

---

# 19. Rule 4 — State uncertainty

Nói uncertainty không làm bạn yếu.

Nó làm communication chính xác hơn.

Ví dụ:

> “Hiện chưa có đủ evidence để khẳng định full automation. Pilot nên đo exception rate và những case cần human review.”

---

# 20. Rule 5 — Verify product facts

Đặc biệt với các claim về:

- product availability;
- data retention;
- security;
- compliance;
- pricing;
- regional availability;
- limits.

Không đoán.

Nên dùng tài liệu chính thức và thông tin hiện hành.

---

# 21. Rule 6 — Benchmark ≠ customer outcome

Benchmark có thể cho biết capability tương đối.

Nhưng customer cần biết:

```text
Does it work
on my task
with my data
inside my workflow
under my constraints?
```

Đó là lý do evaluation trên customer use case rất quan trọng.

---

# 22. Communication ladder

Khi customer hỏi:

> “AI làm được X không?”

Đừng chỉ trả lời “Có”.

Hãy đi theo 5 bước:

```text
1. Clarify task
2. State relevant capability
3. Identify dependencies
4. Define evidence needed
5. Define controls
```

---

# 23. Ví dụ

Customer:

> “ChatGPT có thể trả lời đúng HR policy 100% không?”

### Bad answer

> “Có, model mới rất mạnh.”

### Better answer

> “Model có thể phù hợp với workflow hỏi đáp policy, nhưng không nên coi đó là guarantee 100%. Ta nên kết nối nguồn policy được kiểm soát, evaluate trên tập câu hỏi đại diện, giới hạn câu trả lời theo nguồn và có fallback/escalation cho trường hợp không chắc chắn.”

Câu trả lời tốt:

- không hạ thấp capability;
- không overclaim;
- tạo path to trust.

---

# 24. Accuracy ≠ business success

Một AI system có thể technical quality cao nhưng vẫn fail.

Ví dụ:

- quá chậm;
- chi phí quá cao;
- user không sử dụng;
- integration phức tạp;
- workflow không thay đổi;
- KPI không cải thiện.

Do đó success rộng hơn:

```text
Success
=
Quality
+ Speed
+ Cost
+ Adoption
+ Business KPI
+ Risk management
```

---

# 25. Common mistakes

## Mistake 1
Hứa một con số accuracy chung.

## Mistake 2
Tin rằng model mạnh hơn tự giải quyết hallucination.

## Mistake 3
Không build eval set.

## Mistake 4
Cho AI quá nhiều permission.

## Mistake 5
Không define escalation.

## Mistake 6
Dùng benchmark thay cho customer evidence.

## Mistake 7
Nói “safe” mà không mô tả controls.

---

# 26. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| **Trust** | Mức độ đáng tin |
| **Accuracy** | Mức độ đúng |
| **Hallucination** | Thông tin AI tạo ra nhưng không được support |
| **Evaluation / eval** | Đánh giá hành vi hệ thống |
| **Guardrail** | Cơ chế kiểm soát |
| **Grounding** | Neo output vào source/context |
| **Human-in-the-loop** | Con người tham gia vào loop |
| **Escalation** | Chuyển case lên người/hệ thống phù hợp |
| **Assumption** | Giả định |
| **Uncertainty** | Mức độ chưa chắc chắn |
| **Overclaim** | Khẳng định vượt quá bằng chứng |
| **Representative cases** | Các case đại diện cho thực tế |
| **Monitoring** | Theo dõi hệ thống |
| **Abstention** | Hệ thống chọn không trả lời/không hành động khi không đủ tin cậy |

---

# 27. Section recap

1. Trust phải gắn với specific task và conditions.
2. Accuracy không có một con số chung cho mọi use case.
3. Hallucination cần được xử lý ở system level.
4. Evals là nền tảng để tạo evidence.
5. Guardrails nên layered.
6. Human-in-the-loop là một design pattern quan trọng.
7. Partner phải tránh overclaim.
8. Capability không phải customer-specific evidence.
9. Benchmark không thay thế pilot/evaluation.
10. Trust = **evidence + controls + transparency**.

---

# 28. Self-check

1. Tại sao accuracy cần gắn với task?
2. Hallucination là gì?
3. Eval khác benchmark thế nào?
4. Human-in-the-loop phù hợp khi nào?
5. Nếu customer hỏi “AI này có làm được X không?”, bạn nên trả lời theo 5 bước nào?
