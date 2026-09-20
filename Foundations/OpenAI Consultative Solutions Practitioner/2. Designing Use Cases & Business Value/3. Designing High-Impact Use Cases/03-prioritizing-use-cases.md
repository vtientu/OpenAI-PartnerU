# 03. Prioritizing Use Cases

> Course: **OpenAI Consultative Solutions Practitioner – Foundations**  
> Module: **Designing High-Impact Use Cases**  
> Section: **Prioritizing use cases**

---

## 1. Section này nói về điều gì?

Sau Discovery, chúng ta có thể tìm ra nhiều **candidate use cases** (các use case tiềm năng).

Ở section trước – **Evaluating candidate use cases** – mục tiêu là đánh giá từng candidate dựa trên các yếu tố như:

- Value / Impact – giá trị, tác động
- Frequency / Reach – tần suất và phạm vi ảnh hưởng
- Complexity / Effort – độ phức tạp và công sức
- Readiness – mức độ sẵn sàng
- Evidence – bằng chứng
- Dependencies / Governance – phụ thuộc, phê duyệt, quản trị

Nhưng biết từng use case “tốt hay chưa” vẫn chưa đủ.

Ta còn phải trả lời:

> **Trong tất cả các use case này, use case nào nên được làm trước?**

Đó chính là **Prioritization – ưu tiên hóa**.

---

# 2. Evaluating và Prioritizing khác nhau như thế nào?

## Evaluating

Đánh giá từng use case độc lập.

Ví dụ:

```text
Use Case A
Impact     = High
Effort     = Low
Readiness  = High
```

```text
Use Case B
Impact     = High
Effort     = High
Readiness  = Medium
```

Ta đang xây dựng một **profile** cho từng opportunity.

---

## Prioritizing

Đặt A, B, C... cạnh nhau và quyết định:

```text
Which should move first?
Which should come later?
Which needs more validation?
Which should be deprioritized?
```

Nói ngắn gọn:

```text
Evaluation  → How good is this opportunity?
Prioritization → What should we do first?
```

---

# 3. Vì sao cần prioritization?

Trong thực tế doanh nghiệp:

```text
Ideas > Time
Ideas > Budget
Ideas > People
Ideas > Implementation capacity
```

Do đó không thể build mọi AI idea cùng lúc.

Nếu không prioritization, team rất dễ chọn use case vì:

- nó nghe thú vị
- demo đẹp
- stakeholder cấp cao thích nó
- AI technically có thể làm được
- công nghệ mới đang được chú ý

Nhưng đây không nhất thiết là use case tạo ra giá trị tốt nhất.

Một prioritization tốt phải dựa trên **evidence và trade-offs**, chứ không chỉ dựa trên enthusiasm.

---

# 4. Core framework: Impact vs Effort

Một framework rất hữu ích là đặt use case lên hai trục:

```text
               HIGH IMPACT
                    ↑
                    |
   QUICK WINS       |     STRATEGIC
                    |     INITIATIVES
                    |
LOW EFFORT ---------+---------- HIGH EFFORT
                    |
   SELF-SERVICE /   |     DEPRIORITIZE
   NICE-TO-HAVE     |
                    |
                    ↓
               LOW IMPACT
```

Hai câu hỏi chính:

### Impact / Value

> Nếu workflow này được cải thiện thành công, nó tạo ra bao nhiêu giá trị?

### Effort / Complexity

> Cần bao nhiêu công sức, dependency và thay đổi để triển khai nó đáng tin cậy?

---

# 5. Quadrant 1 – High Impact + Low Effort

## Quick Wins

Đây thường là nhóm hấp dẫn để bắt đầu.

Ví dụ:

```text
Developer mất nhiều thời gian đọc một codebase cũ.

AI use case:
AI giải thích component, function và dependency
trong codebase dựa trên source code được cung cấp.
```

Giả sử:

```text
Impact     = High
Frequency  = High
Effort     = Low / Medium
Readiness  = High
```

Có thể thử nghiệm với một nhóm developer nhỏ mà không cần thay đổi toàn bộ SDLC.

### Tại sao quick wins quan trọng?

Quick win giúp:

- tạo value sớm
- thu thập evidence thực tế
- xây dựng confidence
- tăng adoption
- giúp stakeholder hiểu AI tốt hơn
- tạo momentum cho các initiative lớn hơn

Cần nhớ:

> **Quick win không có nghĩa là use case nhỏ hoặc không quan trọng.**

Nó có nghĩa là **tỷ lệ giữa value và effort đang thuận lợi để bắt đầu**.

---

# 6. Quadrant 2 – High Impact + High Effort

## Strategic Initiatives

Những use case này có thể tạo value lớn nhưng cũng chứa nhiều complexity.

Ví dụ:

```text
AI customer-support agent
↓
Read customer history
↓
Retrieve company knowledge
↓
Access CRM
↓
Generate response
↓
Take actions in internal systems
```

Potential value có thể rất cao.

Nhưng effort cũng cao vì cần:

- system integration
- data access
- authentication / permissions
- evaluations
- reliability controls
- security
- privacy
- governance
- human escalation
- monitoring

Do đó:

```text
High value ≠ Build everything immediately
```

Một lựa chọn tốt hơn có thể là:

```text
Full autonomous workflow
        ↓ narrow scope
AI drafts support responses
        ↓ validate
AI retrieves approved knowledge
        ↓ expand
Limited workflow automation
        ↓
Broader deployment
```

Đây gọi là **sequencing** – triển khai theo trình tự.

---

# 7. Quadrant 3 – Low Impact + Low Effort

Có thể được gọi là:

- Nice-to-have
- Self-service opportunity

Ví dụ:

```text
AI tạo tên vui cho internal sprint mỗi tuần.
```

Effort rất thấp nhưng business impact cũng thấp.

Không nhất thiết phải cấm những use case như vậy.

Người dùng cá nhân vẫn có thể dùng AI cho các task nhỏ.

Nhưng khi doanh nghiệp phải lựa chọn nơi đầu tư:

```text
Low effort alone
is not enough reason
for organizational priority.
```

---

# 8. Quadrant 4 – Low Impact + High Effort

## Deprioritize

Ví dụ:

```text
Xây một hệ thống AI phức tạp
chỉ để tự động hóa một task xảy ra 2 lần/năm,
chỉ ảnh hưởng tới 1 người,
và task hiện tại chỉ mất 10 phút.
```

Nếu:

```text
Impact = Low
Effort = High
```

thì investment rất khó justify.

Do đó use case có thể được:

```text
Deprioritized
```

Tức là:

> **Không phải “AI không làm được”, mà là hiện tại nó không đáng để ưu tiên.**

Điểm này rất quan trọng.

---

# 9. Prioritization không chỉ là Impact / Effort

Impact / Effort là framework dễ dùng nhất để so sánh.

Nhưng trước khi quyết định, cần nhìn lại các tín hiệu từ Evaluation.

## 9.1 Frequency

Workflow xảy ra bao nhiêu lần?

Ví dụ:

```text
Task A: 20 lần/ngày
Task B: 2 lần/năm
```

Nếu mỗi lần đều tiết kiệm 5 phút thì tổng value rất khác nhau.

---

## 9.2 Reach

Bao nhiêu người hoặc team bị ảnh hưởng?

```text
Use case A → 2 users
Use case B → 500 users
```

Reach lớn có thể làm cumulative impact tăng mạnh.

---

## 9.3 Repeatability

Workflow có lặp lại theo pattern tương đối ổn định không?

```text
Repeatable workflow
→ easier to test
→ easier to evaluate
→ easier to reuse
```

---

## 9.4 Readiness

Use case có đủ điều kiện để test chưa?

Hỏi:

- Input đã rõ chưa?
- Output mong muốn đã rõ chưa?
- Workflow owner là ai?
- Users có sẵn sàng test không?
- Có representative examples không?
- Success criteria có rõ không?

Một idea impact cao nhưng readiness thấp có thể chưa phải lựa chọn đầu tiên.

---

## 9.5 Dependencies

Use case phụ thuộc vào những gì?

Ví dụ:

```text
CRM access
API access
internal database
legal approval
security review
another team
workflow change
```

Dependencies càng nhiều thì delivery risk và effort thường càng tăng.

---

## 9.6 Risk / Governance

Nếu AI output sai thì hậu quả là gì?

Ví dụ:

```text
AI giúp brainstorm UI copy
```

và

```text
AI tự động quyết định một hành động quan trọng
đối với khách hàng
```

có risk profile rất khác nhau.

Risk cao có thể yêu cầu:

- stronger evaluations
- human review
- governance
- permissions
- narrower scope

---

# 10. Evidence và Confidence trong prioritization

Không nên có:

```text
Impact = High
```

chỉ vì stakeholder nói:

> “I think this would save a lot of time.”

Ta cần hỏi:

```text
What evidence supports that rating?
```

Ví dụ tốt hơn:

```text
20 support agents
× 15 minutes searching per case
× 12 cases/day
```

Đây là evidence giúp hiểu magnitude của problem.

---

## Confidence

Hai use case có thể cùng được đánh giá High Impact nhưng confidence khác nhau.

### Candidate A

```text
Impact = High
Evidence:
- measured workflow time
- 30 users affected
- clear owner
- repeated daily

Confidence = High
```

### Candidate B

```text
Impact = High
Evidence:
- one stakeholder believes it would help
- frequency unknown
- users not interviewed

Confidence = Low
```

Hai chữ **High Impact** này không nên được coi là giống nhau.

Vì vậy cần luôn hỏi:

> **How confident are we in this prioritization?**

---

# 11. Prioritization là một bài toán trade-off

**Trade-off** = sự đánh đổi.

Không tồn tại use case hoàn hảo với:

```text
Maximum impact
Zero effort
Zero risk
Zero dependencies
100% readiness
```

Do đó phải cân bằng.

Ví dụ:

| Candidate | Impact | Effort | Readiness | Evidence |
|---|---|---|---|---|
| A | High | Low | High | Strong |
| B | Very High | High | Medium | Strong |
| C | Medium | Low | Low | Weak |

Một team có thể quyết định:

```text
A → Test first
B → Strategic initiative / sequence later
C → Validate further
```

Đây là prioritization.

Không phải:

```text
B has the biggest potential impact
therefore B must always be first.
```

---

# 12. Priority ≠ Importance

Một concept rất đáng nhớ:

```text
Not first
≠
Not important
```

Một strategic initiative có thể cực kỳ quan trọng nhưng vẫn không phải **first move**.

Ví dụ:

```text
Long-term goal:
AI-powered autonomous customer service
```

Nhưng first move có thể là:

```text
AI-assisted response drafting
```

vì bước này:

- nhỏ hơn
- dễ test
- ít dependencies hơn
- tạo evidence
- giúp hiểu user behavior
- giúp xác định quality requirements

Sau đó evidence từ bước đầu có thể hỗ trợ initiative lớn hơn.

---

# 13. Narrowing Scope – giảm scope để tăng khả năng thực hiện

Một use case High Impact / High Effort không nhất thiết phải để nguyên.

Ta có thể hỏi:

> Can we narrow the scope?

Ví dụ ban đầu:

```text
AI handles every customer support request.
```

Quá rộng.

Narrow thành:

```text
AI drafts responses
for one category of repetitive support requests,
using approved internal documentation,
with human review before sending.
```

Kết quả:

```text
Complexity ↓
Risk ↓
Evaluation easier
Readiness ↑
```

Đây là kỹ năng cực kỳ quan trọng khi design AI use cases.

---

# 14. Sequencing – không chỉ chọn winner

Prioritization không nhất thiết tạo ra:

```text
Winner
Loser
```

Nó có thể tạo ra roadmap:

```text
NOW
↓
NEXT
↓
LATER
```

Ví dụ:

```text
NOW
AI explains code and suggests changes

NEXT
AI generates tests and validates changes

LATER
AI handles bounded implementation tasks
with repository/tool access
```

Các use case có thể hỗ trợ lẫn nhau.

Use case đầu tiên giúp tạo:

- user adoption
- evaluation data
- governance experience
- reusable integrations
- technical patterns

cho use case tiếp theo.

---

# 15. Reuse Potential

Khi hai candidate có impact tương tự, hãy hỏi:

> Nếu chúng ta build capability này, nó có thể được reuse ở nơi khác không?

Ví dụ:

```text
Capability:
Retrieve trusted internal knowledge
```

ban đầu dùng cho:

```text
Customer Support
```

nhưng pattern tương tự có thể hỗ trợ:

```text
HR
IT support
Sales enablement
Legal knowledge retrieval
```

Reuse có thể làm long-term value tăng lên.

---

# 16. Ví dụ tổng hợp dành cho Frontend Developer

Giả sử một engineering team tìm ra 4 candidates.

## Candidate A – Code Explanation

```text
AI explains unfamiliar components and dependencies.
```

Evidence:

- developers thường phải đọc legacy code
- xảy ra hàng ngày
- source code đã tồn tại

Profile:

```text
Impact      = High
Effort      = Low
Readiness   = High
Frequency   = High
```

→ **Quick win / good candidate to test early**

---

## Candidate B – Test Generation

```text
AI generates initial unit tests
for existing React components.
```

Profile:

```text
Impact      = High
Effort      = Medium
Readiness   = High
Frequency   = High
```

→ Có thể là next candidate sau khi xác định rõ evaluation criteria.

---

## Candidate C – Autonomous PR Merge

```text
AI reviews code,
approves PR,
merges it,
and deploys automatically.
```

Potential value:

```text
High
```

Nhưng:

```text
Risk          = High
Dependencies  = High
Complexity    = High
Governance    = High
```

→ Không nên ưu tiên chỉ vì nó advanced.

Có thể narrow thành:

```text
AI reviews PR
and produces recommendations,
while humans retain approval responsibility.
```

---

## Candidate D – Sprint Name Generator

```text
AI generates a funny sprint name.
```

```text
Impact = Low
Effort = Low
```

→ Có thể dùng self-service, nhưng không phải organizational priority.

---

# 17. Một cách ra quyết định đơn giản

Khi có nhiều candidate, đi qua pipeline:

```text
1. List candidates
        ↓
2. Compare business value
        ↓
3. Compare effort / complexity
        ↓
4. Check readiness
        ↓
5. Check evidence and confidence
        ↓
6. Check risks and dependencies
        ↓
7. Identify quick wins
        ↓
8. Identify strategic initiatives
        ↓
9. Narrow or sequence where needed
        ↓
10. Define the first test
```

---

# 18. Những lỗi thường gặp

## Mistake 1 – Prioritize the coolest AI idea

```text
“Agent nghe rất hiện đại → làm agent.”
```

Sai mindset.

Bắt đầu từ workflow value, không phải technology excitement.

---

## Mistake 2 – Highest potential impact = first priority

Potential impact cao nhưng effort, risk hoặc readiness có thể chưa phù hợp.

---

## Mistake 3 – Lowest effort = first priority

Dễ làm nhưng không có meaningful value thì cũng không nên chiếm organizational focus.

---

## Mistake 4 – Ignore evidence quality

```text
Stakeholder opinion
≠
Strong evidence
```

---

## Mistake 5 – Ignore hidden complexity

Một workflow nhìn ngoài có vẻ đơn giản nhưng thực tế có:

```text
handoffs
approvals
permissions
edge cases
multiple systems
business rules
```

---

## Mistake 6 – Treat prioritization as permanent

Priorities có thể thay đổi khi:

- AI capability cải thiện
- integration dễ hơn
- process được chuẩn hóa
- data trở nên accessible
- policy thay đổi
- evidence mới xuất hiện

Do đó portfolio cần được re-evaluate theo thời gian.

---

# 19. Vocabulary cần nhớ

| English | Nghĩa dễ hiểu |
|---|---|
| Prioritize | Xác định thứ tự ưu tiên |
| Priority | Mức độ ưu tiên |
| Impact | Tác động / giá trị tạo ra |
| Effort | Công sức cần bỏ ra |
| Quick win | Use case có value tốt với effort tương đối thấp |
| Strategic initiative | Sáng kiến giá trị cao nhưng cần đầu tư lớn hơn |
| Deprioritize | Hạ mức ưu tiên / chưa làm lúc này |
| Trade-off | Sự đánh đổi |
| Sequence | Sắp xếp theo trình tự triển khai |
| Narrow scope | Thu hẹp phạm vi |
| Dependency | Thành phần/team/hệ thống mà use case phụ thuộc vào |
| Readiness | Mức độ sẵn sàng để thử hoặc triển khai |
| Evidence | Bằng chứng thực tế hỗ trợ nhận định |
| Confidence | Mức độ tin cậy của đánh giá |
| Reuse | Khả năng tái sử dụng |
| Momentum | Đà tiến triển / động lực tiếp tục |
| Portfolio | Tập hợp nhiều use case / initiative được quản lý cùng nhau |

---

# 20. Công thức ghi nhớ

## Evaluating

```text
Candidate
→ Value
→ Frequency / Reach
→ Complexity
→ Readiness
→ Evidence
```

## Prioritizing

```text
Compare candidates
+ Impact / Effort trade-off
+ Evidence confidence
+ Readiness
+ Risk / Dependencies
        ↓
Decide sequence
```

---

# 21. Mental model quan trọng nhất

```text
Do not ask only:
“Which AI idea is most impressive?”

Ask:
“Which opportunity is the strongest responsible place to start,
and what should come next?”
```

Hay rút gọn:

```text
PRIORITY
=
VALUE
× CONFIDENCE
× READINESS
÷ EFFORT
```

> Đây là mental model để ghi nhớ, **không phải công thức toán chính thức của OpenAI**.

---

# 22. Liên kết với các section trước

Toàn bộ flow lúc này là:

```text
DISCOVERY
↓
Understand workflow + pain + evidence
↓
TRANSLATE DISCOVERY INTO USE CASES
↓
Create candidate use cases
↓
EVALUATE CANDIDATE USE CASES
↓
Understand value, complexity, readiness, evidence
↓
PRIORITIZE USE CASES
↓
Choose what to test now, validate, sequence, or defer
↓
NEXT STEP
Design a bounded, testable use case
```

---

# 23. Cheat Sheet

Khi cần ưu tiên use case, hỏi 7 câu:

1. **What value could this create?**  
   Giá trị có đáng kể không?

2. **How often does the workflow occur?**  
   Workflow xảy ra thường xuyên không?

3. **Who and how many people are affected?**  
   Reach lớn đến đâu?

4. **How much effort and complexity is required?**  
   Build / deploy / change khó đến mức nào?

5. **Are we ready to test it?**  
   Inputs, users, owner, process và success criteria đã đủ rõ chưa?

6. **What evidence supports our judgment?**  
   Có evidence hay mới chỉ là assumption?

7. **Should it be tested now, narrowed, sequenced later, or deprioritized?**  
   Hành động tiếp theo là gì?

---

# Key Takeaway

> **Prioritization không phải tìm use case “ngầu nhất”. Nó là quyết định use case nào tạo ra sự cân bằng tốt nhất giữa value, effort, readiness và evidence để trở thành bước đi phù hợp tiếp theo.**

Một cách nhớ cực ngắn:

```text
Evaluate → Understand each candidate
Prioritize → Compare candidates
Sequence → Decide what happens when
```

---

## Nguồn đối chiếu công khai của OpenAI

Nội dung trên là bản diễn giải học tập, không phải transcript nguyên văn của PartnerU. Các khung chính được đối chiếu với tài liệu công khai hiện hành của OpenAI:

- OpenAI – **Identifying and scaling AI use cases**: Impact/Effort framework và bốn nhóm ưu tiên.
- OpenAI Academy – **Prioritize AI workflow opportunities**: value, effort, frequency, repeatability, reach, readiness.
- OpenAI Academy – **Evaluate AI workflow readiness**: evidence, dependencies, governance, test/validate/sequence/deprioritize.
- OpenAI – **From experiments to deployments**: impact, effort, risk và reuse potential trong prioritization.

