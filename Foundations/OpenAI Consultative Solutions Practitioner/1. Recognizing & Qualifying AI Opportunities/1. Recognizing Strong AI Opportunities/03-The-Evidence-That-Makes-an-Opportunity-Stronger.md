# 03 — The Evidence That Makes an Opportunity Stronger

## 1. Vì sao evidence quan trọng?

Trong discovery, rất dễ nghe những câu như:

> “Team này chắc mất rất nhiều thời gian.”  
> “AI chắc sẽ giúp họ nhanh hơn 50%.”  
> “Mọi người sẽ thích tool này.”

Đó có thể là assumption, không phải evidence.

Một AI opportunity trở nên mạnh hơn khi recommendation dựa trên **evidence có thể kiểm tra**, không chỉ dựa trên enthusiasm hoặc intuition.

---

## 2. Known — Inferred — Unknown

Đây là mental model cực kỳ hữu ích.

### Known
Thông tin có bằng chứng trực tiếp.

Ví dụ:

- “Trong 4 tuần gần nhất có 1,200 support tickets.”
- “Median handling time là 11 phút.”
- “Support lead xác nhận routing là bước gây rework lớn nhất.”

Nguồn có thể là:

- logs,
- metrics,
- timestamps,
- workflow records,
- user interviews,
- direct observation,
- system data,
- quality reviews.

### Inferred
Suy luận hợp lý từ dữ liệu hiện có nhưng chưa được chứng minh hoàn toàn.

Ví dụ:

> “Nếu AI hỗ trợ classification, handling time có thể giảm.”

Đây là hypothesis hợp lý, nhưng vẫn cần test.

### Unknown
Thông tin chưa biết và có thể thay đổi recommendation.

Ví dụ:

- Model có classify tốt các edge case không?
- User có tin output không?
- Security có approve integration không?
- Cost có phù hợp khi scale không?

Một consultant tốt không che Unknown. Họ **làm cho Unknown rõ ràng**.

---

## 3. Evidence cho problem

Đầu tiên phải chứng minh **problem tồn tại**.

Các evidence signal mạnh:

### Frequency evidence

- số task/ngày,
- số ticket/tháng,
- số report/tuần,
- số lần workflow được thực hiện.

### Time evidence

- average handling time,
- cycle time,
- waiting time,
- preparation time.

### Rework evidence

- số lần phải sửa,
- re-route rate,
- rejection rate,
- duplicate work.

### Error/quality evidence

- error rate,
- defect count,
- QA score,
- missed information,
- inconsistent outputs.

### User evidence

- recurring complaints,
- support requests,
- interview quotes,
- observed workarounds,
- repeated requests for help.

Evidence càng cụ thể, opportunity càng dễ đánh giá.

---

## 4. Evidence cho value

Problem evidence nói:

> “Có vấn đề.”

Value evidence nói:

> “Giải quyết vấn đề này đáng để làm.”

Ví dụ:

- Workflow chiếm 500 giờ/tháng.
- Delay làm chậm customer onboarding 2 ngày.
- Rework ảnh hưởng 3 teams.
- Error dẫn đến escalation.
- Bottleneck giới hạn throughput.

Điểm quan trọng:

Không nên nhảy thẳng từ:

> “Task mất nhiều thời gian”

sang:

> “AI sẽ tiết kiệm X tiền mỗi năm”

nếu chưa có đủ validated data.

---

## 5. Baseline — Mốc trước khi có AI

Nếu không có baseline, rất khó chứng minh improvement.

Một baseline tốt nên trả lời:

- Hiện tại mất bao lâu?
- Output quality hiện tại ra sao?
- Có bao nhiêu lỗi?
- Có bao nhiêu handoff?
- Bao nhiêu người tham gia?
- Throughput hiện tại là bao nhiêu?

Ví dụ:

> “Trước test, preparation time trung bình là 90 phút/report.”

Sau test:

> “Trong 6 report, preparation time trung bình còn 42 phút; reviewer correction time tăng thêm 5 phút.”

Đây tốt hơn nhiều so với:

> “AI tiết kiệm rất nhiều thời gian.”

---

## 6. Quantitative + Qualitative evidence

### Quantitative
Dữ liệu dạng số.

Ví dụ:

- time,
- count,
- error rate,
- throughput,
- usage frequency,
- acceptance rate.

### Qualitative
Thông tin mô tả trải nghiệm và nguyên nhân.

Ví dụ:

- interview,
- direct observation,
- reviewer comments,
- structured feedback,
- reasons for override.

Hai loại evidence bổ sung cho nhau.

Số liệu cho biết **“cái gì đang xảy ra”**.

Qualitative feedback thường giúp hiểu **“tại sao nó xảy ra”**.

---

## 7. Evidence phù hợp với claim

Một nguyên tắc quan trọng:

> **Claim phải nhỏ hơn hoặc bằng sức mạnh của evidence.**

Ví dụ:

Nếu 3 user nói “demo khá hay”, bạn chưa thể claim:

> “Organization đã sẵn sàng adopt.”

Nếu 10 người dùng tool một lần, bạn chưa thể claim:

> “Workflow đã được adopted.”

Nếu task time giảm trong 5 examples, bạn chưa thể claim:

> “Company sẽ tiết kiệm hàng triệu USD mỗi năm.”

Hãy nói đúng mức evidence hỗ trợ.

---

## 8. Evidence theo từng giai đoạn

### Trước test
Cần evidence về:

- problem,
- frequency,
- reach,
- friction,
- current workflow,
- user demand,
- owner,
- readiness.

### Trong test
Cần evidence về:

- output quality,
- failure cases,
- human correction,
- task time,
- user behavior,
- technical reliability.

### Sau test
Cần evidence về:

- repeat usage,
- adoption,
- efficiency,
- quality,
- outcome impact,
- operational burden.

Evidence cần thay đổi theo maturity của opportunity.

---

## 9. Evidence về adoption

“Có người thử” khác với “được adopt”.

Adoption signal tốt hơn gồm:

- dùng trong real work,
- cùng người dùng lặp lại nhiều lần,
- thêm user mới sử dụng,
- shared workflow/template được reuse,
- team process bắt đầu thay đổi để incorporate workflow,
- usage xuất hiện theo cadence ổn định.

Các signal như:

- attendance,
- downloads,
- demo reactions,
- “tôi sẽ thử”

chỉ là **interest**, chưa phải adoption.

---

## 10. Evidence về efficiency

Có thể đo:

- time required,
- number of steps,
- manual handoffs,
- waiting time,
- rework,
- cycle time,
- throughput,
- capacity.

Khi báo cáo, giữ rõ:

- baseline,
- unit,
- period,
- measurement method.

Ví dụ tốt:

> “Average triage time giảm từ 8.2 phút xuống 5.1 phút trên 120 tickets trong 2 tuần.”

Ví dụ yếu:

> “AI giúp tiết kiệm khoảng 40% thời gian.”

---

## 11. Evidence về quality

Time saving chỉ có ý nghĩa nếu quality vẫn đạt yêu cầu.

Có thể đo:

- reviewer acceptance,
- correction rate,
- rubric score,
- factual accuracy,
- completeness,
- error severity,
- escalation rate.

Đây là lý do OpenAI nhấn mạnh **evals**: phải định nghĩa “good” trước khi đo model/workflow có đạt kỳ vọng hay không.

---

## 12. Đừng invent ROI

Nếu chưa đủ data, không nên tạo một con số ROI quá chính xác.

Ví dụ:

Bạn biết:

- 100 tasks/tháng,
- mỗi task 15 phút.

Nhưng bạn chưa biết:

- AI tiết kiệm được bao nhiêu,
- review overhead,
- tool cost,
- error cost,
- adoption rate.

→ Chưa nên claim ROI.

Bước tốt hơn là:

1. thiết lập baseline,
2. test 50–100 real tasks,
3. đo time + quality + correction,
4. sau đó estimate value có assumptions rõ ràng.

---

## 13. Example — Support response drafting

### Initial claim

> “AI sẽ giúp support trả lời nhanh hơn.”

### Evidence collected

Known:

- 600 tickets/tháng.
- 70% là các question pattern lặp lại.
- Average first-draft time: 6.5 phút.
- 8 agents xác nhận họ thường search 2–3 internal docs trước khi trả lời.

Inferred:

- Retrieval + draft generation có thể giảm preparation time.

Unknown:

- Output có giữ đúng policy không?
- Agents có phải sửa quá nhiều không?
- Retrieval có lấy đúng version của docs không?

### Next evidence to collect

- 100 historical tickets.
- Expert rubric về accuracy/completeness/tone.
- Human correction time.
- Acceptance rate.
- Failure cases theo category.

→ Opportunity trở nên mạnh hơn không phải vì “AI nghe có vẻ phù hợp”, mà vì uncertainty đang được giảm bằng evidence.

---

## 14. Evidence checklist

- [ ] Có số liệu về frequency không?
- [ ] Có baseline time/cost/quality không?
- [ ] Có direct observation hoặc user feedback không?
- [ ] Có evidence về rework/error/delay không?
- [ ] Known, Inferred, Unknown đã tách riêng chưa?
- [ ] Claim có vượt quá evidence không?
- [ ] Có real examples để test không?
- [ ] Có cách đánh giá quality không?
- [ ] Có đo human correction/review effort không?
- [ ] Có xác định evidence cần thu thập ở bước tiếp theo không?

---

## 15. Vocabulary

| English | Nghĩa |
|---|---|
| Evidence | Bằng chứng |
| Known | Điều đã biết/có xác nhận |
| Inferred | Điều suy luận nhưng chưa xác nhận hoàn toàn |
| Unknown | Điều chưa biết |
| Assumption | Giả định |
| Baseline | Mức hiện tại để so sánh |
| Direct observation | Quan sát trực tiếp |
| Quantitative | Định lượng — dạng số |
| Qualitative | Định tính — mô tả/feedback |
| Adoption | Việc workflow thật sự được đưa vào sử dụng |
| Throughput | Khối lượng công việc xử lý được trong một khoảng thời gian |
| Correction rate | Tỷ lệ output cần chỉnh sửa |
| Acceptance rate | Tỷ lệ output được chấp nhận |

---

## Key takeaway

> **Strong opportunities are evidence-backed. Hãy tách rõ điều đã biết, điều đang suy luận và điều chưa biết; sau đó dùng test nhỏ để thu thập evidence có khả năng thay đổi quyết định.**
