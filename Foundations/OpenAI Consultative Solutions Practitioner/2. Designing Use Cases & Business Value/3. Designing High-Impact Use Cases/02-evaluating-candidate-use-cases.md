# 02. Evaluating Candidate Use Cases

> Course: **OpenAI Consultative Solutions Practitioner – Foundations**  
> Module: **Designing High-Impact Use Cases**  
> Section: **Evaluating candidate use cases**

---

## 1. Mục tiêu của section

Sau bước **Translating discovery into use cases**, ta thường có nhiều **candidate use cases** (các use case tiềm năng).

Vấn đề tiếp theo là:

> **Use case nào đáng để ưu tiên kiểm chứng hoặc triển khai trước?**

Không phải use case nào AI *có thể* làm cũng là use case *nên* làm.

Ta cần đánh giá mỗi candidate dựa trên giá trị thực tế, mức độ phức tạp, tần suất sử dụng, mức độ sẵn sàng và bằng chứng thu được từ discovery.

---

## 2. Candidate use case là gì?

**Candidate use case** = một ý tưởng ứng dụng AI đã được hình thành từ discovery nhưng **chưa được xác nhận là đủ tốt để đầu tư hoặc triển khai**.

Ví dụ sau discovery với một đội Customer Support, ta có thể có các candidate:

1. AI tóm tắt ticket trước khi agent xử lý.
2. AI tìm thông tin từ knowledge base để hỗ trợ agent trả lời.
3. AI tạo bản nháp câu trả lời cho khách hàng.
4. AI phân loại ticket và gợi ý routing.
5. AI tự động xử lý toàn bộ ticket.

Tất cả đều là ý tưởng có thể xem xét, nhưng mức **value, risk, effort và readiness** của chúng khác nhau.

Do đó:

```text
Discovery evidence
       ↓
Candidate use cases
       ↓
Evaluation
       ↓
Prioritized use cases
       ↓
Test / validate / sequence / deprioritize
```

---

## 3. Sai lầm phổ biến: “AI làm được” ≠ “Use case tốt”

Một team rất dễ bắt đầu bằng câu hỏi:

> “AI có làm được việc này không?”

Nhưng câu hỏi quan trọng hơn là:

> “Nếu AI làm được việc này, nó có tạo ra giá trị đủ lớn và có thực tế để triển khai không?”

Ví dụ:

```text
AI can generate meeting summaries.
```

Điều này chỉ chứng minh **technical possibility**.

Để trở thành use case mạnh, ta còn cần biết:

```text
Ai cần summary?
↓
Họ đang gặp pain gì?
↓
Việc này xảy ra bao thường xuyên?
↓
Mất bao nhiêu thời gian hiện tại?
↓
AI output có thực sự hữu ích không?
↓
Có dữ liệu/input phù hợp không?
↓
Ai review output?
↓
Làm sao đo được value?
```

---

# 4. Khung đánh giá candidate use cases

Một cách dễ nhớ là đánh giá theo 4 nhóm chính:

```text
VALUE
+ FREQUENCY
+ COMPLEXITY
+ READINESS
```

Đây không nhất thiết là công thức chấm điểm cứng. Mục tiêu là tạo ra một cách suy nghĩ có hệ thống để so sánh các cơ hội.

---

## 5. Dimension 1 — Impact / Value

### Câu hỏi chính

> **Nếu use case này hoạt động tốt, nó sẽ tạo ra giá trị gì?**

Có thể xem xét các loại value như:

- tiết kiệm thời gian;
- giảm thao tác thủ công;
- tăng chất lượng output;
- tăng consistency;
- giảm rework;
- giảm lỗi;
- cải thiện customer/user experience;
- giúp con người ra quyết định nhanh hơn;
- hỗ trợ một business priority quan trọng.

### Ví dụ

Giả sử Support Agent mất trung bình 15 phút để tìm tài liệu trước khi trả lời một ticket.

Một use case:

> AI retrieves relevant information from approved support documentation.

Nếu việc này giảm đáng kể thời gian tìm kiếm và xảy ra hàng trăm lần mỗi ngày thì **potential value** có thể cao.

### Cẩn thận với value chỉ dựa trên assumption

Yếu:

```text
AI sẽ tiết kiệm rất nhiều thời gian.
```

Mạnh hơn:

```text
Agents currently spend approximately 10–15 minutes searching across
three internal sources for common support questions.
```

Điểm khác biệt là **evidence**.

---

# 6. Dimension 2 — Frequency / Reach

Một workflow xảy ra thường xuyên thường có cơ hội tạo ra **compounding value** lớn hơn.

### Frequency

Hỏi:

> Workflow này xảy ra bao thường xuyên?

Ví dụ:

```text
1 lần / năm
10 lần / tháng
100 lần / ngày
10,000 lần / ngày
```

### Reach

Hỏi:

> Bao nhiêu người, team hoặc customer bị ảnh hưởng?

Ví dụ:

```text
2 analysts
vs
500 support agents
```

### Ý nghĩa

Một improvement nhỏ nhưng lặp lại hàng nghìn lần có thể tạo ra value lớn hơn một improvement rất lớn nhưng chỉ xảy ra hiếm khi.

Ví dụ:

```text
5 phút tiết kiệm
× 1,000 tasks / ngày
= 5,000 phút / ngày
```

Do đó đừng chỉ nhìn vào **value per task**. Hãy nhìn cả **value at scale**.

---

# 7. Dimension 3 — Complexity / Effort

Một use case có value cao nhưng quá phức tạp vẫn có thể chưa phù hợp để làm trước.

### Những nguồn complexity phổ biến

#### Process complexity

Workflow có rõ ràng và repeatable không?

```text
Stable workflow → dễ thiết kế hơn
Highly variable workflow → khó thiết kế hơn
```

#### System dependencies

Use case có cần kết nối với:

```text
CRM
ERP
Internal APIs
Databases
Knowledge bases
Legacy systems
```

Không?

Càng nhiều dependency thì implementation effort thường càng tăng.

#### Data / information access

AI có cần dữ liệu:

- chưa được chuẩn hóa;
- nằm ở nhiều hệ thống;
- khó truy cập;
- có permission phức tạp;
- có dữ liệu nhạy cảm?

#### Governance

Có cần approval từ:

```text
Security
Legal
Compliance
Privacy
IT
Business owner
```

không?

#### Change effort

Use case có yêu cầu người dùng thay đổi workflow lớn không?

Ví dụ:

```text
AI drafts an email
```

thường ít thay đổi hành vi hơn:

```text
AI completely restructures the end-to-end customer support process.
```

---

# 8. Dimension 4 — Readiness

### Câu hỏi chính

> **Use case này đã đủ rõ và đủ điều kiện để test chưa?**

Readiness không chỉ là technical readiness.

Nó còn gồm nhiều phần.

### Workflow readiness

Ta đã hiểu workflow đủ rõ chưa?

```text
Inputs → Steps → Decisions → Outputs
```

### User readiness

Có user thật sẵn sàng thử nghiệm không?

### Owner readiness

Có người/team chịu trách nhiệm cho workflow không?

### Data readiness

Các input cần thiết có tồn tại và có thể truy cập không?

### Success criteria readiness

Ta có biết **success trông như thế nào** không?

Ví dụ:

```text
Reduce average search time
Improve response consistency
Reduce first-draft preparation time
Reduce number of revisions
```

Nếu không biết success được đo bằng gì, rất khó đánh giá pilot sau này.

---

# 9. Evidence vs Assumption

Đây là một trong những kỹ năng quan trọng nhất khi đánh giá use case.

## Evidence

Thông tin đã quan sát hoặc xác nhận được.

Ví dụ:

```text
Support agents handle around 50 tickets per day.
```

```text
Agents currently search three systems before answering common requests.
```

```text
Users report that this search step is one of the slowest parts of the workflow.
```

## Assumption

Điều ta nghĩ có thể đúng nhưng chưa xác nhận.

Ví dụ:

```text
AI will reduce ticket handling time by 50%.
```

```text
Agents will trust AI-generated answers.
```

```text
All required data can be accessed through APIs.
```

### Nguyên tắc

```text
Evidence → dùng để đưa ra quyết định
Assumption → dùng để xác định điều cần validate
```

Đừng biến assumption thành fact.

---

# 10. Hidden workflow complexity

Một workflow nhìn bên ngoài có thể rất đơn giản:

```text
Receive request
→ Generate answer
→ Send answer
```

Nhưng discovery sâu hơn có thể cho thấy:

```text
Receive request
↓
Classify request
↓
Check customer account
↓
Search policy
↓
Check exception rules
↓
Ask another team
↓
Wait for approval
↓
Draft answer
↓
Manager review
↓
Send answer
```

Đây gọi là **hidden workflow complexity**.

Cần tìm các yếu tố như:

- hidden handoffs;
- approval bottlenecks;
- manual workarounds;
- duplicated steps;
- unclear ownership;
- undocumented business rules;
- upstream/downstream dependencies.

Nếu vấn đề thật sự nằm ở một process bị thiết kế kém thì thêm AI vào có thể chỉ **automate a bad process**.

---

# 11. Value vs Effort Matrix

Một framework đơn giản để so sánh candidate use cases là:

```text
                    VALUE
                      ↑
                      │
        Strategic     │      Strong candidate
        initiative    │      / Quick win
                      │
High Effort ──────────┼────────── Low Effort
                      │
        Deprioritize  │      Nice to have
                      │
                      ↓
                   LOW VALUE
```

Có thể hiểu thành bốn nhóm:

| Value | Effort | Cách suy nghĩ |
|---|---|---|
| High | Low | Candidate tốt để xem xét test sớm |
| High | High | Có tiềm năng lớn nhưng cần planning / sequencing |
| Low | Low | Có thể hữu ích nhưng priority thấp |
| Low | High | Thường nên deprioritize |

> Lưu ý: “High value + low effort” không tự động có nghĩa là phải triển khai. Vẫn cần xem readiness, risk, evidence và ownership.

---

# 12. Một cách đánh giá thực tế

Khi gặp một candidate use case, có thể đi lần lượt qua 7 câu hỏi:

```text
1. What problem are we solving?
        ↓
2. What evidence shows the problem matters?
        ↓
3. Who experiences the problem?
        ↓
4. How often does it happen?
        ↓
5. What value could AI create?
        ↓
6. What complexity or dependencies exist?
        ↓
7. Are we ready to test it?
```

Nếu không trả lời được các câu hỏi trên, use case có thể cần **more discovery** thay vì implementation.

---

# 13. Ví dụ hoàn chỉnh — Customer Support

## Candidate A

> AI summarizes customer tickets before the agent opens them.

### Value

- giảm thời gian đọc ticket dài;
- giúp agent nắm context nhanh hơn.

### Frequency

Nếu mọi ticket đều được tóm tắt thì frequency cao.

### Complexity

Khá thấp nếu ticket text đã có sẵn và không cần nhiều hệ thống bên ngoài.

### Readiness

Nếu có user group, ticket samples và metric về handling time thì dễ pilot.

---

## Candidate B

> AI automatically resolves every customer support ticket without human review.

### Potential value

Có thể rất lớn nếu hoạt động tốt.

### Complexity

Rất cao:

```text
Policies
Customer data
Account actions
Risk
Escalations
Exceptions
Security
Quality control
```

### Readiness

Có thể thấp nếu workflow chưa ổn định hoặc thiếu guardrails/evaluation.

### Kết luận về cách suy nghĩ

Candidate B không nhất thiết là use case “xấu”.

Nhưng Candidate A có thể là **smaller, more testable step** để thu thập evidence trước.

Đây là tư duy quan trọng trong consultative solution design:

> **Tìm bước nhỏ nhất có thể tạo ra evidence hữu ích.**

---

# 14. Ví dụ dành cho Frontend Developer

Giả sử discovery từ một engineering team cho thấy:

```text
Developers spend significant time understanding unfamiliar components
before making changes.
```

Ta có ba candidate use cases.

---

## Use case A — Code explanation

```text
AI explains an unfamiliar React component,
including props, state, dependencies and data flow.
```

### Evaluation

```text
Value       → Medium / High
Frequency   → High
Complexity  → Low
Readiness   → High
```

Có thể thử nhanh với code samples hiện tại.

---

## Use case B — Unit test generation

```text
AI generates first-draft unit tests for React components.
```

### Evaluation

```text
Value       → High
Frequency   → High
Complexity  → Medium
Readiness   → Medium / High
```

Cần xác định:

- testing framework;
- coding conventions;
- definition of acceptable test quality;
- human review.

---

## Use case C — Fully autonomous production deployment

```text
AI reads requirements,
changes the frontend,
runs tests,
merges the PR,
and deploys directly to production.
```

### Evaluation

```text
Potential Value → High
Complexity      → Very High
Risk            → High
Dependencies    → Many
Readiness       → likely lower
```

Nếu team mới bắt đầu áp dụng AI thì A hoặc B có thể tạo ra evidence nhanh hơn trước khi tiến tới C.

---

# 15. Candidate evaluation table

Một bảng đơn giản bạn có thể dùng khi làm discovery workshop:

| Candidate Use Case | Value | Frequency | Complexity | Readiness | Evidence | Key Dependency |
|---|---|---|---|---|---|---|
| Ticket summarization | High | High | Low | High | Strong | Ticket access |
| Response drafting | High | High | Medium | Medium | Medium | Knowledge base |
| Full ticket automation | Very High potential | High | High | Low | Weak | Systems + governance |

Điểm quan trọng không phải là con số tuyệt đối.

Mục tiêu là **so sánh cơ hội một cách nhất quán và giải thích được reasoning**.

---

# 16. Các outcome sau evaluation

Sau khi đánh giá, candidate không chỉ có hai trạng thái “do” hoặc “don't do”.

Một cách hữu ích là chia thành:

### Test now

Use case có:

- credible value;
- manageable complexity;
- clear owner;
- real users;
- đủ readiness cho một pilot nhỏ.

### Validate further

Value có vẻ tốt nhưng còn assumption quan trọng cần xác nhận.

Ví dụ:

```text
Do users actually perform this task frequently?
```

### Sequence later

Use case có giá trị nhưng phụ thuộc vào thứ khác trước:

```text
Data access
API integration
Security approval
Process redesign
Ownership decision
```

### Avoid / deprioritize for now

Khi:

- value thấp;
- problem chưa rõ;
- effort quá lớn so với value;
- AI không xử lý được nguyên nhân thật của pain.

---

# 17. Một principle rất quan trọng

```text
Do not optimize for the most impressive AI demo.
Optimize for a valuable, testable workflow improvement.
```

Một demo AI rất ấn tượng chưa chắc tạo ra business value.

Một use case tốt thường có:

```text
Clear problem
+ real evidence
+ frequent/relevant workflow
+ measurable value
+ manageable complexity
+ enough readiness
```

---

# 18. Relationship với section trước

Section trước:

```text
Translating discovery into use cases
```

trả lời:

> **Từ những gì discovery tìm ra, ta có thể hình thành những AI use case nào?**

Section hiện tại:

```text
Evaluating candidate use cases
```

trả lời:

> **Trong các use case đó, cái nào đủ mạnh và thực tế để tiếp tục?**

Flow tổng thể:

```text
Discovery
↓
Workflow + Pain + Evidence
↓
Translate into candidate use cases
↓
Evaluate candidates
↓
Prioritize opportunities
↓
Define / test the strongest candidates
```

---

# 19. Cheat Sheet

## Candidate Use Case Evaluation

```text
1. VALUE
   Does it solve a meaningful problem?

2. FREQUENCY / REACH
   How often and for how many users?

3. EVIDENCE
   What proves the problem actually exists?

4. COMPLEXITY
   How hard is the workflow to change?

5. DEPENDENCIES
   Data? Systems? Approvals? Teams?

6. READINESS
   Are users, owner, inputs and metrics ready?

7. TESTABILITY
   Can we run a small test and learn something useful?
```

Một câu để nhớ:

> **High-impact use case = meaningful value + credible evidence + manageable complexity + sufficient readiness.**

---

# 20. Vocabulary cần nhớ

| Term | Nghĩa dễ hiểu |
|---|---|
| Candidate use case | Use case tiềm năng đang được xem xét |
| Evaluate | Đánh giá |
| Impact / Value | Giá trị/tác động nếu use case thành công |
| Frequency | Tần suất workflow xảy ra |
| Reach | Số người/team/customer bị ảnh hưởng |
| Complexity | Mức độ phức tạp |
| Effort | Công sức cần bỏ ra |
| Readiness | Mức độ sẵn sàng để thử/triển khai |
| Evidence | Bằng chứng đã quan sát/xác nhận |
| Assumption | Giả định chưa được kiểm chứng |
| Dependency | Thứ use case phụ thuộc vào |
| Governance | Các yêu cầu/quy trình kiểm soát |
| Prioritize | Xếp thứ tự ưu tiên |
| Deprioritize | Hạ mức ưu tiên |
| Validate | Kiểm chứng |
| Pilot | Thử nghiệm có giới hạn |
| Repeatability | Khả năng lặp lại workflow/kết quả |
| Human review | Bước con người kiểm tra/phê duyệt |

---

# 21. Cách tự kiểm tra khi học xong section

Nếu nhìn vào một AI idea như:

> “Dùng AI để generate code.”

Bạn chưa nên hỏi ngay:

```text
Which model should we use?
Which API should we call?
```

Hãy hỏi trước:

```text
For whom?
For what task?
What problem exists today?
What evidence supports it?
How frequently does it happen?
What value would improve?
What dependencies exist?
How would we know it worked?
Can we test it safely on a small scope?
```

Nếu bạn làm được việc đó, bạn đang suy nghĩ như một **Consultative Solutions Practitioner**, thay vì chỉ suy nghĩ như một developer đang tìm chỗ để gắn AI vào sản phẩm.

---

## Nguồn tham khảo

Nội dung trên là bản diễn giải học tập, được căn chỉnh với các tài liệu công khai hiện tại của OpenAI Academy về:

- use case discovery workshops;
- workflow opportunity evaluation;
- workflow discovery & prioritization matrix;
- evidence-based AI workflow evaluation.

Nó không phải transcript nguyên văn của bài PartnerU “Evaluating candidate use cases”.
