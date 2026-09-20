# 02 — Understanding Opportunity Readiness

## 1. Readiness là gì?

**Opportunity readiness** là mức độ một cơ hội đã có đủ điều kiện thực tế để bắt đầu validation hoặc test.

Một opportunity có value cao nhưng vẫn có thể **chưa sẵn sàng**.

Ví dụ:

> Công ty muốn AI tự động review hợp đồng.

Value có thể cao, nhưng nếu:

- không rõ ai sở hữu workflow,
- dữ liệu không được phép đưa vào hệ thống,
- legal chưa tham gia,
- chưa có tiêu chí để đánh giá output,

thì opportunity chưa ready để triển khai.

Điều này không có nghĩa opportunity “bad”. Nó chỉ có nghĩa **cần chuẩn bị thêm trước khi test**.

---

## 2. Readiness khác Value

Đây là distinction rất quan trọng.

### Value
> Nếu giải quyết được, nó có đáng không?

### Readiness
> Chúng ta đã có đủ điều kiện để bắt đầu chưa?

Một opportunity có thể nằm trong 4 tình huống:

| Value | Readiness | Ý nghĩa |
|---|---|---|
| Cao | Cao | Candidate tốt để test |
| Cao | Thấp | Đáng theo đuổi nhưng cần chuẩn bị/sequence |
| Thấp | Cao | Dễ làm nhưng chưa chắc đáng làm |
| Thấp | Thấp | Thường không nên ưu tiên |

---

## 3. Các thành phần của readiness

### 3.1 Clear workflow

Cần biết:

- workflow bắt đầu ở đâu,
- kết thúc ở đâu,
- ai làm từng bước,
- input là gì,
- output là gì,
- handoff nằm ở đâu,
- exception thường gặp là gì.

Nếu workflow quá rộng như:

> “Cải thiện customer service bằng AI”

thì chưa đủ rõ.

Scope tốt hơn:

> “Hỗ trợ support agent tóm tắt ticket history và đề xuất 3 next actions trước khi trả lời khách.”

---

### 3.2 Defined user group

Phải biết ai sẽ sử dụng hoặc bị ảnh hưởng bởi solution.

Ví dụ:

- 8 support agents,
- 3 QA reviewers,
- 1 team lead.

“Cả công ty” thường là scope quá rộng cho first test.

---

### 3.3 Willing test group

Có user thật sẵn sàng test là một readiness signal mạnh.

Tại sao?

Vì một demo có thể hoạt động tốt nhưng production workflow lại khác hoàn toàn.

Người dùng thực giúp phát hiện:

- missing context,
- usability issues,
- exceptions,
- trust problems,
- hidden steps,
- behavior change required.

---

### 3.4 Process owner

Cần một người có trách nhiệm với workflow hoặc outcome.

Owner giúp:

- xác nhận current process,
- cho phép test,
- quyết định trade-off,
- giải quyết conflict,
- review evidence,
- quyết định next step.

Không có owner → rất khó chuyển từ demo sang adoption.

---

### 3.5 Access to tools and data

Cần kiểm tra:

- Data có tồn tại không?
- Có đủ chất lượng không?
- Có quyền truy cập không?
- Có chứa sensitive information không?
- Có cần integration không?
- Data format có usable không?
- Có historical examples để eval không?

Không nên nói “technical feasibility cao” chỉ vì model về lý thuyết có capability phù hợp.

Feasibility còn phụ thuộc vào **actual environment**.

---

### 3.6 Necessary approvals

Các approval có thể đến từ:

- Security
- Privacy
- Legal
- Compliance
- IT
- Data owner
- Functional owner

Một “quick win” không còn quick nếu cần 4 tháng approval.

Đừng bỏ qua governance khi đánh giá readiness.

---

### 3.7 Measurable first outcome

Trước khi test, cần biết:

> “Chúng ta sẽ quan sát điều gì để biết test có ích?”

Ví dụ:

Không tốt:

> “User thấy AI hữu ích.”

Tốt hơn:

- triage time giảm từ baseline,
- fewer re-routed tickets,
- reviewer acceptance rate,
- correction rate,
- task completion time,
- quality score theo rubric.

First outcome không cần là ROI hoàn chỉnh. Nó chỉ cần đủ rõ để support next decision.

---

## 4. User readiness vs Technical readiness

### User readiness

Câu hỏi:

- User có nhu cầu thật không?
- Họ có sẵn sàng thử cách làm mới không?
- Workflow mới có phù hợp cách họ làm việc không?
- Có cần training không?
- Có human review ở đâu?

### Technical readiness

Câu hỏi:

- Capability cần thiết đã có chưa?
- Có data/context không?
- Có API/integration cần thiết không?
- Performance/latency/cost có phù hợp không?
- Có cách evaluate output không?

Một opportunity cần cả hai.

Technical demo tốt + user không adopt = không tạo value.

User rất muốn + technical/data chưa đủ = chưa thể test đúng cách.

---

## 5. Process stability

Một workflow không cần hoàn hảo, nhưng phải đủ hiểu để biết mình đang cải thiện cái gì.

Nếu process liên tục thay đổi hoặc ownership mơ hồ, AI có thể làm sự hỗn loạn khó thấy hơn.

Dấu hiệu process chưa ổn định:

- Mỗi team dùng một cách khác nhau.
- Không có standard input/output.
- Không ai đồng ý “good result” là gì.
- Handoff thay đổi liên tục.
- Exception nhiều hơn happy path.
- Mọi người phải dùng nhiều workaround.

Trong trường hợp này, first step có thể là:

> map workflow → chuẩn hóa → thu thập baseline → rồi mới test AI.

---

## 6. Dependency mapping

Readiness không chỉ nằm trong một team.

Hãy map:

### Upstream dependency
Điều gì phải xảy ra trước workflow?

Ví dụ:

- ticket phải có customer ID,
- code phải pass CI,
- document phải được uploaded.

### Downstream dependency
Kết quả được dùng ở đâu tiếp theo?

Ví dụ:

- suggestion được human approve,
- result ghi vào CRM,
- output trở thành input cho payment process.

### Cross-functional dependency
Team nào khác phải tham gia?

Ví dụ:

- Security,
- Data,
- Platform,
- Legal,
- Ops.

Dependency chưa rõ = readiness thấp hơn.

---

## 7. Ba mức readiness hữu ích

### Ready to test
Dùng khi:

- workflow rõ,
- value có evidence đáng tin,
- user/test group rõ,
- owner rõ,
- data/tools đủ dùng,
- approvals manageable,
- có measurable first outcome.

### Needs validation
Dùng khi:

Opportunity có vẻ có giá trị nhưng còn assumption quan trọng cần kiểm tra.

Ví dụ:

- chưa rõ user có dùng không,
- chưa đo current baseline,
- chưa biết data quality,
- chưa test capability trên real examples.

### Not ready yet
Dùng khi:

- workflow quá mơ hồ,
- owner chưa có,
- data/system access chưa giải quyết,
- governance blocker lớn,
- process cần sửa trước,
- không có tiêu chí thành công.

“Not ready yet” không đồng nghĩa “never”.

---

## 8. Example — AI hỗ trợ PR review

### Ý tưởng
Dùng AI review pull request trước khi senior reviewer đọc.

### Readiness check

#### Workflow
Rõ: PR opened → automated checks → reviewer → merge.

#### Users
12 frontend developers.

#### Test group
3 developers đồng ý test trong 2 tuần.

#### Owner
Engineering Manager.

#### Data
Có 6 tháng PR history.

#### Systems
Cần Git provider integration.

#### Governance
Không được gửi private source code sang environment chưa approved.

#### Outcome
Đề xuất:

- reviewer acceptance rate,
- false positive rate,
- time-to-first-review,
- number of useful issues caught.

### Judgment về readiness

Opportunity có thể **needs validation** nếu security approval cho source code chưa xong.

Value có thể tốt, nhưng chưa thể gọi là “ready to test” trong environment thật.

---

## 9. Checklist section 02

- [ ] Workflow đã được scope rõ chưa?
- [ ] Input/output có rõ không?
- [ ] User group là ai?
- [ ] Có nhóm nhỏ sẵn sàng test không?
- [ ] Ai là process owner?
- [ ] Data cần thiết có tồn tại không?
- [ ] Có quyền truy cập data/tools không?
- [ ] Có technical dependency nào chưa giải quyết?
- [ ] Security/legal/privacy approval nào cần có?
- [ ] User có cần training hoặc thay đổi behavior không?
- [ ] Có measurable first outcome không?
- [ ] Có baseline để so sánh không?

---

## 10. Vocabulary

| English | Nghĩa |
|---|---|
| Readiness | Mức độ sẵn sàng |
| Process owner | Người sở hữu/chịu trách nhiệm workflow |
| Test group | Nhóm người dùng thử |
| Approval | Phê duyệt |
| Technical readiness | Mức sẵn sàng kỹ thuật |
| User readiness | Mức sẵn sàng của người dùng |
| Process stability | Mức ổn định của quy trình |
| Upstream | Phần xảy ra trước workflow |
| Downstream | Phần xảy ra sau workflow |
| Baseline | Mức hiện tại dùng làm mốc so sánh |
| Blocker | Trở ngại khiến chưa thể tiến tiếp |
| Measurable outcome | Kết quả có thể đo |

---

## Key takeaway

> **Một cơ hội tốt chưa chắc đã sẵn sàng. Readiness là khả năng chuyển từ “ý tưởng có giá trị” sang “một test thực tế có owner, user, data, approvals và outcome đo được”.**
