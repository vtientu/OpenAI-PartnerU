# 03. Building an Evidence-Based Value Hypothesis

> **Mục tiêu:** Biết cách xây một **value hypothesis** có logic, có evidence và đủ rõ để kiểm chứng trong pilot.

---

## 1. Value Hypothesis là gì?

**Value hypothesis** = giả thuyết có cấu trúc về cách một use case có thể tạo ra business value.

Nó **không phải lời hứa**.

Nó là một câu trả lời có căn cứ cho câu hỏi:

> “Nếu chúng ta thay đổi workflow này bằng AI, kết quả nào có khả năng cải thiện và dựa trên evidence nào?”

---

## 2. Template dễ nhớ

```text
If [user/team]
uses AI to [change a specific workflow],
then [operational metric] may improve,
which could contribute to [business outcome],
because [evidence].
```

Phiên bản tiếng Việt:

```text
Nếu [đối tượng]
dùng AI để [thay đổi workflow cụ thể],
thì [metric vận hành] có thể được cải thiện,
từ đó có thể đóng góp vào [business outcome],
vì [evidence hiện có].
```

---

## 3. Một hypothesis tốt cần 5 phần

### 1. User / stakeholder

Ai đang làm workflow?

### 2. Workflow

Công việc nào được thay đổi?

### 3. Mechanism

AI giúp bằng cách nào?

### 4. Measurable outcome

Metric nào dự kiến thay đổi?

### 5. Evidence

Tại sao ta tin thay đổi đó có khả năng xảy ra?

---

## 4. Evidence cần thu thập

Không phải evidence nào cũng là “financial data”.

### Workflow evidence

- Số task/ngày hoặc tháng.
- Thời gian trung bình mỗi task.
- Số bước thủ công.
- Tỷ lệ lỗi.
- Backlog.
- Tần suất rework.

### User evidence

- Người dùng nói bước nào đau nhất.
- Team nào đang bị ảnh hưởng.
- Tần suất pain xảy ra.
- Mức adoption dự kiến.

### Business evidence

- KPI hiện tại.
- SLA.
- Capacity constraint.
- Business priority.
- Cost hoặc revenue driver có liên quan.

### Technical / operational evidence

- Dữ liệu có sẵn không?
- Quy trình có đủ ổn định để hỗ trợ AI không?
- Cần human review ở đâu?
- Có constraint về privacy, quality hoặc compliance không?

---

## 5. Phân biệt Evidence và Assumption

Ví dụ:

> “Support agent mất trung bình 12 phút/ticket.”

Nếu được đo từ hệ thống → **Evidence**.

Nếu một manager ước lượng → có thể là **Assumption** hoặc directional evidence.

> “AI sẽ giảm 50% thời gian xử lý.”

Trước pilot, đây thường là **Assumption cần validate**.

Một value hypothesis tốt phải biết rõ:

```text
What we know
vs
What we assume
vs
What we need to test
```

---

## 6. Example — Customer Support

### Evidence hiện tại

- 2,000 ticket/tuần.
- Agent mất trung bình 10 phút/ticket.
- Khoảng 40% thời gian là đọc context và tạo first draft.
- Team đang có backlog cao.

### Value hypothesis

> Nếu support agents dùng AI để tóm tắt lịch sử ticket và tạo first draft, thời gian xử lý trung bình có thể giảm. Điều này có thể tăng team capacity và giảm backlog, bởi vì phần đọc context và drafting hiện đang chiếm một tỷ lệ đáng kể trong handling time.

### Cần validate trong pilot

- AI thực sự tiết kiệm bao nhiêu phút/ticket?
- Draft acceptance rate là bao nhiêu?
- Quality có giữ nguyên hoặc tốt hơn không?
- Agent có sử dụng tính năng thường xuyên không?

Đây là **evidence-based hypothesis**, không phải lời cam kết ROI.

---

## 7. Confidence Ladder đơn giản

Bạn có thể tự đánh dấu mức chắc chắn của từng claim:

### Low confidence

- Chủ yếu là assumption.
- Chưa có baseline.
- Chưa rõ adoption.

### Medium confidence

- Có baseline và workflow evidence.
- Có feedback từ user.
- Chưa pilot thực tế.

### Higher confidence

- Có pilot data.
- Có actual usage.
- Có measured outcome.

> Mục tiêu không phải làm mọi claim trông chắc chắn. Mục tiêu là **biết claim nào đã có evidence và claim nào cần kiểm chứng**.

---

## 8. Hypothesis phải falsifiable

Một hypothesis tốt phải có khả năng bị chứng minh là **không đúng**.

Không tốt:

> “AI sẽ giúp team làm việc tốt hơn.”

Khó đo, khó bác bỏ.

Tốt hơn:

> “AI-assisted drafting có thể giảm average preparation time cho một ticket đủ điều kiện mà không làm giảm quality score.”

Có thể đo được:

- preparation time.
- quality score.
- eligible ticket population.

---

## 9. Evidence Map

Dùng bảng sau cho mỗi use case:

| Thành phần | Hiện có | Cần validate |
|---|---|---|
| Workflow volume | 2,000 tickets/week | Confirm seasonality |
| Time/task | 10 min | Measure by ticket type |
| Pain point | Reading + drafting | Quantify % time |
| AI effect | Expected faster drafting | Pilot actual time saved |
| Quality | Current score known | Compare AI vs baseline |
| Adoption | Unknown | Measure active usage |
| Business outcome | Backlog is priority | Observe backlog trend |

Bảng này giúp tránh “kể câu chuyện value” bằng assumption.

---

## 10. Các câu hỏi discovery để xây value hypothesis

- Workflow nào đang chiếm nhiều thời gian nhất?
- Bao nhiêu người đang làm workflow này?
- Bao nhiêu lần mỗi ngày/tuần/tháng?
- Hiện mất bao lâu mỗi lần?
- Có baseline metric không?
- Chất lượng được đo bằng gì?
- Bước nào có khả năng AI hỗ trợ nhất?
- Nếu bước này tốt hơn, KPI nào có thể thay đổi?
- Điều gì cần đúng để value thực sự xảy ra?

---

## 11. Common mistakes

### 1. Treating assumptions as facts

Dùng con số ước lượng như dữ liệu đã được chứng minh.

### 2. Chỉ có upside

Không đưa quality, adoption, risk hoặc human review vào hypothesis.

### 3. Hypothesis quá rộng

> “AI sẽ transform toàn bộ company.”

Quá rộng để validate.

### 4. Không có baseline

Không biết “before” thì rất khó chứng minh “after”.

---

## 12. Vocabulary

| English | Hiểu đơn giản |
|---|---|
| Value hypothesis | Giả thuyết về giá trị |
| Assumption | Giả định chưa được chứng minh |
| Evidence-based | Dựa trên bằng chứng/dữ liệu |
| Baseline | Giá trị hiện tại để so sánh |
| Falsifiable | Có thể kiểm chứng đúng/sai |
| Pilot | Thử nghiệm phạm vi nhỏ |
| Adoption | Mức độ người dùng thực sự sử dụng |
| Constraint | Điều kiện/ràng buộc |

---

## 13. Cheat sheet

```text
A good value hypothesis =
Specific workflow
+ measurable outcome
+ business relevance
+ existing evidence
+ assumptions to test
```

### Câu template nên nhớ

> **If** we change this workflow with AI, **then** this metric may improve, **because** current evidence shows this is where time/cost/error/friction exists. We will **validate** the remaining assumptions through measurement.
