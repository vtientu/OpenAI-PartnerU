# 04. Measuring Impact and Estimating Directional Benefit

> **Mục tiêu:** Biết cách đo impact và ước lượng lợi ích theo hướng **directional** — đủ để hỗ trợ quyết định nhưng không tạo cảm giác chính xác giả.

---

## 1. Ý chính cần nhớ

Trước khi có pilot data, ta thường **không biết chính xác ROI**.

Điều ta có thể làm là:

1. Xác định baseline.
2. Chọn metric phù hợp.
3. Ước lượng directional benefit.
4. Ghi rõ assumptions.
5. Validate bằng pilot.

> **Câu nhớ nhanh:** `Baseline → Measure → Estimate → Validate`

---

## 2. Baseline trước, impact sau

Muốn biết AI tạo impact bao nhiêu, cần biết hiện tại đang ở đâu.

Ví dụ cần baseline:

- 10 phút/ticket.
- 500 ticket/ngày.
- 8% error rate.
- 3 ngày review cycle.
- 40 giờ/tuần dành cho một workflow.

Sau pilot mới so sánh:

```text
Impact = After - Before
```

Hoặc với metric cần giảm:

```text
Improvement % = (Baseline - New value) / Baseline × 100
```

---

## 3. Các nhóm metric nên đo

### Efficiency

- Time per task.
- Cycle time.
- Throughput.
- Number of tasks completed.

### Quality

- Error rate.
- Rework rate.
- Review score.
- Acceptance rate.

### Adoption

- Active users.
- Usage frequency.
- % eligible tasks using AI.

### Business outcome

- Backlog.
- SLA compliance.
- Customer response time.
- Cost per task.
- Revenue-related metrics nếu có causal link đủ mạnh.

> Không nên chỉ đo “time saved”. Nếu output nhanh hơn nhưng quality kém hoặc adoption thấp, value có thể không materialize.

---

## 4. Directional Benefit là gì?

**Directional benefit** = ước lượng quy mô và hướng tác động để xem use case có đáng tiếp tục validate hay không.

Nó không nhất thiết là một business case tài chính hoàn chỉnh.

Ví dụ:

> “Nếu pilot cho thấy tiết kiệm khoảng 2–3 phút trên nhóm ticket phù hợp, quy mô hiện tại cho thấy team có thể unlock hàng chục giờ capacity mỗi tuần.”

Điều này hữu ích hơn một con số ROI rất chính xác nhưng dựa trên assumptions yếu.

---

## 5. Công thức 1 — Time Saved

```text
Time Saved
= Eligible Volume
× Adoption Rate
× Time Saved per Task
```

Ví dụ:

- 1,000 task/tuần.
- 60% phù hợp cho use case.
- 70% adoption trong nhóm phù hợp.
- Tiết kiệm 3 phút/task.

```text
1,000 × 60% × 70% × 3 phút
= 1,260 phút
= 21 giờ/tuần
```

Điểm hay của công thức này: không giả định 100% task đều phù hợp và 100% user đều dùng AI.

---

## 6. Công thức 2 — Capacity Unlocked

```text
Capacity Unlocked
= Total Time Saved
÷ Productive Hours per Person
```

Nhưng cần cẩn thận:

**Capacity unlocked ≠ headcount reduction.**

21 giờ/tuần có thể được dùng để:

- Xử lý backlog.
- Nhận thêm task.
- Làm quality review.
- Tăng customer-facing time.
- Làm công việc có giá trị cao hơn.

Vì vậy cách diễn đạt an toàn hơn là **capacity unlocked** hoặc **hours redirected**.

---

## 7. Công thức 3 — Cost-Equivalent Estimate

Nếu khách hàng có loaded labor cost:

```text
Cost-equivalent capacity
= Hours Saved × Cost per Hour
```

Nhưng đây thường là **economic equivalent**, không mặc định là actual cash saving.

Ví dụ:

```text
20 giờ/tuần × $50/giờ = $1,000/tuần equivalent capacity
```

Chỉ gọi là “cost savings” nếu tổ chức thực sự giảm chi tiêu/cost base tương ứng.

---

## 8. Công thức 4 — Error / Rework Reduction

```text
Avoided Rework
= Task Volume
× Reduction in Error Rate
× Rework Time per Error
```

Ví dụ:

- 5,000 task/tháng.
- Error rate từ 6% xuống 4%.
- Mỗi lỗi mất 15 phút sửa.

```text
5,000 × 2% × 15 phút
= 1,500 phút
= 25 giờ rework avoided / tháng
```

---

## 9. Dùng range thay vì fake precision

Nếu assumptions chưa chắc chắn, nên estimate theo range.

Ví dụ:

```text
Low case: 1 phút/task
Expected case: 2 phút/task
High case: 3 phút/task
```

Hoặc:

```text
Adoption range: 40%–70%
Eligible volume: 50%–65%
```

Range giúp:

- Thể hiện uncertainty.
- Cho thấy assumption nào ảnh hưởng lớn nhất.
- Tránh “chính xác tới từng đồng” khi chưa có dữ liệu.

---

## 10. Pilot Measurement Design

Một pilot tốt nên trả lời 4 câu hỏi:

### 1. Did people use it?

Adoption.

### 2. Did the workflow change?

Time, cycle time, throughput.

### 3. Was quality maintained or improved?

Quality score, error rate, human review.

### 4. Did the change matter operationally?

Backlog, capacity, SLA hoặc metric business liên quan.

---

## 11. Example — Before vs After

| Metric | Baseline | Pilot | Change |
|---|---:|---:|---:|
| Avg task time | 12 min | 9 min | -3 min |
| Quality score | 92% | 93% | +1 pp |
| Adoption | — | 65% | New |
| Eligible tasks | — | 70% | New |

Từ đây mới bắt đầu scale estimate:

```text
Total volume
× eligible rate
× adoption
× measured time saved
```

---

## 12. Sensitivity thinking

Hãy hỏi:

> “Nếu assumption này sai thì estimate thay đổi nhiều không?”

Ví dụ value phụ thuộc mạnh vào adoption:

```text
20% adoption → small impact
60% adoption → meaningful impact
90% adoption → large impact
```

Vậy adoption là **critical assumption** cần đo trong pilot.

---

## 13. Common mistakes

### 1. 100% adoption assumption

Không thực tế trong hầu hết use case.

### 2. Time saved = cash saved

Không phải lúc nào cũng đúng.

### 3. Không đo quality

Faster nhưng output kém hơn có thể phá value.

### 4. Không phân biệt eligible workload

Không phải mọi task đều phù hợp với AI.

### 5. Fake precision

Ví dụ: “ROI = 237.42%” khi dữ liệu đầu vào chỉ là rough estimates.

---

## 14. Vocabulary

| English | Hiểu đơn giản |
|---|---|
| Directional benefit | Ước lượng hướng/quy mô lợi ích |
| Baseline | Mốc hiện tại |
| Eligible volume | Khối lượng công việc phù hợp với use case |
| Adoption rate | Tỷ lệ thực sự sử dụng |
| Capacity unlocked | Năng lực/thời gian được giải phóng |
| Sensitivity | Mức estimate thay đổi khi assumption thay đổi |
| Actual savings | Khoản tiết kiệm chi phí thực sự |
| Cost equivalent | Giá trị quy đổi tương đương về chi phí |

---

## 15. Cheat sheet

```text
Directional Value
= Volume
× Eligible %
× Adoption %
× Improvement per task
```

Nhưng luôn kiểm tra thêm:

```text
Quality maintained?
User actually adopts?
Value is realized in the workflow?
```

### 4 điều cần nhớ

1. Luôn có **baseline**.
2. Đo cả **efficiency + quality + adoption**.
3. Dùng **range** khi uncertainty cao.
4. Estimate là để **hỗ trợ quyết định**, không phải để giả vờ chắc chắn.
