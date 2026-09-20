# 04 — Applying Opportunity Judgment

## 1. Judgment là bước biến discovery thành decision

Sau khi hiểu:

- problem,
- value,
- evidence,
- readiness,
- complexity,

bạn vẫn phải đưa ra một recommendation thực tế.

**Opportunity judgment** là khả năng trả lời:

> “Với evidence hiện tại, bước tiếp theo hợp lý nhất là gì?”

Mục tiêu không phải đưa ra một verdict tuyệt đối như:

> “Use case này chắc chắn thành công.”

Mà là:

> “Evidence hiện tại đủ để làm bước nào tiếp theo?”

---

## 2. Bốn recommendation phổ biến

### 2.1 Test now

Dùng khi:

- workflow rõ,
- có credible potential value,
- complexity manageable,
- owner rõ,
- real users có thể tham gia,
- data/tools đủ cho test,
- approvals cần thiết đã có hoặc manageable,
- có measurable outcome.

Test nên nhỏ và giới hạn scope.

Ví dụ:

> Test AI-assisted ticket triage với 3 support agents trong 2 tuần trên một category ticket cụ thể.

Không cần rollout toàn bộ.

---

### 2.2 Validate further

Dùng khi opportunity có vẻ đáng giá nhưng assumption quan trọng vẫn chưa được kiểm chứng.

Ví dụ:

- chưa biết user pain có thực sự lớn không,
- chưa có baseline,
- chưa biết data quality,
- chưa test model trên representative examples,
- chưa rõ success criteria.

Next step có thể là:

- 5 interviews,
- workflow observation,
- sample analysis,
- data audit,
- offline eval.

---

### 2.3 Sequence later

Dùng khi value có thể cao nhưng dependency lớn khiến chưa nên test ngay.

Ví dụ:

- cần security approval,
- cần data cleanup,
- cần API integration,
- cần process redesign,
- cần ownership decision,
- cần platform capability khác hoàn thành trước.

Điểm quan trọng:

> “Later” không có nghĩa “không quan trọng”.

Nó có nghĩa **có prerequisite cần hoàn thành trước**.

---

### 2.4 Avoid for now

Dùng khi:

- expected value thấp,
- problem chưa rõ,
- effort quá lớn so với value,
- AI không giải quyết root cause,
- không có user demand đáng tin,
- risk/dependency không hợp lý ở hiện tại.

“For now” để giữ decision grounded trong current evidence.

Nếu evidence thay đổi, recommendation có thể thay đổi.

---

## 3. Judgment không phải scoring máy móc

Một matrix hoặc score có thể hỗ trợ comparison, nhưng không thay thế judgment.

Ví dụ:

Opportunity có:

- high value,
- medium effort,
- high frequency.

Nhưng nếu processing data vi phạm policy hoặc không có owner, nó vẫn chưa thể “test now”.

Judgment cần hiểu context và constraint.

---

## 4. Compare opportunities theo cùng một khung

Nếu có nhiều use case, có thể tạo bảng:

| Opportunity | Potential value | Complexity | Readiness | Key dependency | Recommendation |
|---|---|---|---|---|---|
| Ticket triage | High | Medium | Ready | CRM API | Test now |
| Contract review | High | High | Low | Legal + data access | Sequence later |
| Meeting summaries | Medium | Low | Ready | User group | Test now |
| AI avatar nội bộ | Low | Medium | Low | Unclear problem | Avoid for now |

Mục đích của bảng không phải tạo “điểm chính xác giả”.

Nó giúp các stakeholder thấy **why** phía sau recommendation.

---

## 5. Smallest useful next step

Một judgment tốt luôn đi cùng **next step cụ thể**.

Tránh:

> “Cần nghiên cứu thêm.”

Tốt hơn:

> “Trong tuần này, Support Lead chọn 100 historical tickets; QA tạo rubric 4 tiêu chí; team chạy offline eval để xác định classification accuracy và các category failure trước khi quyết định pilot.”

Một next step tốt nên trả lời:

- Ai owner?
- Ai cần tham gia?
- Scope là gì?
- Cần trả lời câu hỏi nào?
- Evidence nào sẽ được thu thập?
- Evidence nào đủ để move forward?

---

## 6. Nếu test — hãy định nghĩa lightweight test

Một test brief có thể gồm:

### Test group
Ai dùng?

### Workflow boundary
AI hỗ trợ đoạn nào?

### Capability
AI phải làm gì?

### Duration
Test trong bao lâu?

### Evidence to collect
Đo gì?

### Success signal
Dấu hiệu nào cho thấy nên tiếp tục?

### Stop/reconsider signal
Điều gì cho thấy cần dừng, redesign hoặc thu hẹp scope?

---

## 7. Example — AI hỗ trợ viết unit test

### Opportunity
Sau mỗi feature, developer mất nhiều thời gian tạo unit test boilerplate và coverage thường không đồng đều.

### Known

- 10 frontend devs.
- 60 PRs/tháng.
- Team lead estimate 20–30 phút/PR cho initial unit test scaffolding.
- Existing CI có coverage report.

### Unknown

- AI-generated tests có meaningful assertions không?
- Có tạo brittle tests không?
- Review overhead có cao không?

### Readiness

- User group rõ.
- Owner rõ.
- Code access được phép trong approved environment.
- Có historical PRs để offline test.

### Judgment

**Test now** với scope nhỏ.

### Smallest useful test

- 3 developers.
- 20 PRs.
- AI chỉ tạo initial test draft.
- Human bắt buộc review.
- Đo:
  - time to first test draft,
  - reviewer edit time,
  - tests accepted without major rewrite,
  - coverage change,
  - failure/brittleness notes.

### Stop signal

Nếu reviewer edit time xấp xỉ hoặc lớn hơn manual creation time, cần reconsider workflow design.

---

## 8. Example — AI tự động quyết định refund

### Value
Có thể cao vì volume lớn.

### Nhưng complexity

- monetary decision,
- policy constraints,
- fraud risk,
- customer impact,
- need for auditability,
- edge cases.

### Judgment hợp lý ở giai đoạn đầu

Không nên nhảy ngay vào full automation.

Có thể **validate further** hoặc **sequence later** với scope:

> AI chỉ summarize case + retrieve policy + recommend action, human vẫn là decision maker.

Đây là ví dụ cho thấy judgment nên điều chỉnh **scope**, không chỉ yes/no.

---

## 9. Common failure modes

### Failure 1 — Solution-first thinking

> “Khách muốn agent nên mình tìm chỗ để gắn agent.”

Sửa bằng cách quay về workflow problem.

### Failure 2 — Mistaking enthusiasm for evidence

Stakeholder hào hứng không chứng minh value.

### Failure 3 — Calling something a quick win quá sớm

Nếu chưa rõ:

- approvals,
- data,
- owner,
- change effort,
- integration,

thì chưa nên gọi là quick win.

### Failure 4 — Ignoring hidden work

AI draft nhanh hơn nhưng human phải review 2x lâu hơn → value có thể biến mất.

### Failure 5 — Over-precise ROI

Không nên tạo con số ROI đẹp khi assumptions chưa validated.

### Failure 6 — Treating “not ready” as “bad opportunity”

Opportunity tốt có thể chỉ cần sequencing.

---

## 10. Opportunity judgment template

Bạn có thể dùng template sau khi học hoặc trong discovery workshop.

### Workflow problem
- Ai đang làm workflow?
- Họ muốn đạt kết quả gì?
- Điểm breakdown lớn nhất ở đâu?

### Strongest evidence of value
- Frequency:
- Reach:
- Friction:
- Rework/risk:
- Business relevance:

### Known / Inferred / Unknown
- Known:
- Inferred:
- Unknown:

### Readiness
- User group:
- Test group:
- Owner:
- Data/tools:
- Approvals:
- Measurable outcome:

### Complexity
- Process complexity:
- System dependencies:
- Cross-functional dependencies:
- Governance:
- Change effort:

### Recommendation
Chọn một:

- Test now
- Validate further
- Sequence later
- Avoid for now

### Smallest useful next step
- Owner:
- Participants:
- Scope:
- Question to answer:
- Evidence to collect:
- Success signal:
- Stop/reconsider signal:

---

## 11. Checklist section 04

- [ ] Recommendation có dựa trên evidence không?
- [ ] Có tách value khỏi readiness không?
- [ ] Có xét complexity/dependencies không?
- [ ] Có tránh assumption về ROI/feasibility không?
- [ ] Có xem AI có thực sự giải quyết root cause không?
- [ ] Nếu chưa đủ evidence, có nói rõ cần validate gì không?
- [ ] Recommendation có action cụ thể không?
- [ ] Next step có owner không?
- [ ] Nếu test, có success signal và stop signal không?
- [ ] Scope có đủ nhỏ để học nhanh không?

---

## 12. Vocabulary

| English | Nghĩa |
|---|---|
| Judgment | Phán đoán có căn cứ |
| Recommendation | Đề xuất hành động |
| Test now | Thử nghiệm ngay với scope giới hạn |
| Validate further | Kiểm chứng thêm |
| Sequence later | Để sau vì còn prerequisite/dependency |
| Avoid for now | Chưa nên theo đuổi ở hiện tại |
| Prerequisite | Điều kiện phải có trước |
| Lightweight test | Test nhỏ, nhanh, đủ để học |
| Success signal | Tín hiệu cho thấy nên tiếp tục |
| Stop signal | Tín hiệu cho thấy nên dừng/xem lại |
| Trade-off | Sự đánh đổi giữa các yếu tố |
| Root cause | Nguyên nhân gốc |

---

## Key takeaway

> **Good opportunity judgment không phải là cố chọn AI. Nó là dùng evidence để chọn đúng bước tiếp theo: test, validate, sequence hay tạm thời không làm — với scope nhỏ nhất đủ để giảm uncertainty.**
