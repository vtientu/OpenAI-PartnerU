# 02. Connecting Workflow Change to Business Outcomes

> **Mục tiêu:** Biết cách nối một thay đổi nhỏ trong workflow với một outcome có ý nghĩa đối với business mà không overclaim.

---

## 1. Ý chính cần nhớ

Một use case mạnh không dừng ở:

> “AI giúp người dùng làm task nhanh hơn.”

Ta cần trả lời tiếp:

> “Nhanh hơn thì **điều gì thay đổi trong vận hành**, và điều đó **quan trọng với business như thế nào**?”

Chuỗi suy luận:

```text
Current workflow
    ↓
AI-enabled change
    ↓
Operational metric changes
    ↓
Business outcome
```

> **Câu nhớ nhanh:** `Workflow change phải có một đường nối hợp lý tới Business outcome.`

---

## 2. Bắt đầu từ workflow hiện tại

Trước khi nói về value, cần hiểu:

- Ai đang thực hiện công việc?
- Task nào?
- Tần suất bao nhiêu?
- Mất bao lâu?
- Bước nào lặp lại?
- Bước nào hay lỗi?
- Bước nào tạo delay?
- Outcome hiện tại được đo bằng metric nào?

Nếu không hiểu current workflow thì rất khó chứng minh AI thực sự tạo ra thay đổi gì.

---

## 3. Xác định chính xác AI thay đổi bước nào

Không nói chung chung:

> “Dùng AI cho customer support.”

Hãy cụ thể:

> “Dùng AI để tóm tắt lịch sử hội thoại và tạo first draft cho agent trước khi agent review.”

Một workflow change tốt phải chỉ ra:

```text
Before: Người dùng làm gì?
After: AI hỗ trợ phần nào?
Human: Con người vẫn chịu trách nhiệm phần nào?
```

---

## 4. Từ workflow change → operational outcome

Đây thường là bước dễ đo nhất.

Các operational outcomes phổ biến:

- Time per task ↓
- Throughput ↑
- Backlog ↓
- Rework ↓
- Error rate ↓
- Response time ↓
- Consistency ↑
- Coverage ↑

Ví dụ:

```text
AI tạo first draft
→ agent viết ít hơn
→ handling time giảm
```

Đây là mối quan hệ khá trực tiếp.

---

## 5. Từ operational outcome → business outcome

Đây là nơi cần cẩn thận hơn.

Ví dụ:

```text
Handling time giảm
→ team có thêm capacity
→ có thể xử lý backlog nhanh hơn
→ customer response time có thể được cải thiện
```

Nhưng không nên tự động viết:

```text
Handling time giảm
→ doanh thu tăng 20%
```

Trừ khi có evidence cho mối quan hệ đó.

---

## 6. Framework: Outcome Chain

Dùng 5 câu hỏi:

1. **What changes?** — Bước nào của workflow thay đổi?
2. **For whom?** — Ai được hưởng lợi?
3. **How is work different?** — Nhanh hơn, ít lỗi hơn hay dễ hơn?
4. **What metric moves?** — Metric vận hành nào thay đổi?
5. **Why does the business care?** — Tại sao metric đó quan trọng?

---

## 7. Ví dụ 1 — Software Engineering

### Current workflow

Developer phải đọc ticket, codebase context và tự viết test case từ đầu.

### AI-enabled change

AI hỗ trợ:

- Tóm tắt ticket.
- Giải thích đoạn code liên quan.
- Đề xuất test cases ban đầu.

### Operational outcomes

Có thể đo:

- Thời gian chuẩn bị trước khi coding.
- Thời gian tạo test cases.
- Số lần rework.
- PR cycle time.

### Business outcomes có thể liên quan

- Rút ngắn delivery cycle.
- Tăng capacity của engineering team.
- Cho phép developer dành nhiều thời gian hơn cho design, debugging hoặc product work.

> Lưu ý: “Developer tiết kiệm 1 giờ” chưa chắc = “công ty tiết kiệm đúng 1 giờ lương”. Cần xem thời gian được tái sử dụng ra sao.

---

## 8. Ví dụ 2 — Sales

```text
Pain:
Sales rep mất nhiều thời gian tìm thông tin account.

Workflow change:
AI tổng hợp CRM notes + tài liệu liên quan thành account brief.

Operational outcome:
Preparation time giảm.

Possible business outcome:
Rep có thêm thời gian cho customer conversations.

Evidence cần:
- số account/reps
- thời gian chuẩn bị hiện tại
- tần suất sử dụng
- chất lượng brief
- liệu thời gian tiết kiệm có thực sự chuyển sang selling activity không
```

---

## 9. Dùng “because” test để kiểm tra logic

Mỗi bước trong value chain nên nối được bằng từ **because**.

Ví dụ:

> Response time có thể giảm **because** agent xử lý ticket nhanh hơn.

> Agent xử lý nhanh hơn **because** AI giúp tóm tắt lịch sử và tạo draft.

Nếu không thể giải thích “because” một cách rõ ràng, value chain có thể đang bị nhảy bước.

---

## 10. Leading vs Lagging outcomes

### Leading indicators

Thay đổi gần workflow, dễ thấy sớm:

- Time per task.
- Adoption rate.
- Draft acceptance rate.
- Cycle time.
- Number of tasks completed.

### Lagging outcomes

Thường xuất hiện sau và chịu ảnh hưởng của nhiều yếu tố:

- Revenue.
- Retention.
- CSAT.
- Cost reduction.
- Time-to-market.

> Khi pilot, thường nên đo **leading indicators trước**, sau đó quan sát xem chúng có đóng góp tới lagging outcomes hay không.

---

## 11. Common mistakes

### Mistake 1 — Nhảy thẳng đến money

```text
AI saves time → company saves millions
```

Thiếu adoption, scale, realization và business context.

### Mistake 2 — Không xác định người hưởng lợi

Value của developer, manager và CFO không giống nhau.

### Mistake 3 — Không có metric trung gian

Nếu chỉ có “AI feature → revenue”, chuỗi logic quá yếu.

### Mistake 4 — Không tính quality

Nhanh hơn nhưng lỗi nhiều hơn chưa chắc là value.

---

## 12. Vocabulary

| English | Hiểu đơn giản |
|---|---|
| Workflow change | Thay đổi trong cách làm việc |
| Operational metric | Chỉ số vận hành |
| Business outcome | Kết quả business |
| Throughput | Khối lượng công việc xử lý trong một khoảng thời gian |
| Backlog | Công việc tồn đọng |
| Rework | Làm lại do lỗi/chưa đạt |
| Leading indicator | Chỉ số xuất hiện sớm, gần workflow |
| Lagging indicator | Chỉ số business thường xuất hiện muộn hơn |
| Causal link | Mối liên hệ nguyên nhân-kết quả |

---

## 13. Cheat sheet

```text
Workflow pain
→ AI changes one or more steps
→ operational metric moves
→ business cares because...
```

### Tự kiểm tra

Trước khi gọi một use case là “high value”, hãy trả lời được:

- Workflow nào thay đổi?
- Metric nào thay đổi?
- Business outcome nào liên quan?
- Mối liên hệ có logic không?
- Evidence nào đã có, evidence nào vẫn cần validate?
