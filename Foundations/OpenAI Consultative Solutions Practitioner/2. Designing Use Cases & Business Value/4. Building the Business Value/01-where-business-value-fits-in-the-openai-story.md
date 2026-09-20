# 01. Where Business Value Fits in the OpenAI Story

> **Mục tiêu:** Hiểu **Business Value** nằm ở đâu trong câu chuyện tư vấn OpenAI và vì sao không nên bắt đầu bằng tính năng/model.

---

## 1. Ý chính cần nhớ

**OpenAI capability không tự động tạo ra business value.**

Giá trị chỉ xuất hiện khi khả năng AI **thay đổi một workflow thực tế** và thay đổi đó **tạo ra kết quả có ý nghĩa cho doanh nghiệp**.

```text
AI capability
    ↓
Workflow change
    ↓
Operational outcome
    ↓
Business outcome
    ↓
Evidence / measurement
```

> **Câu nhớ nhanh:** `Capability → Workflow → Outcome → Value`

---

## 2. Business Value là gì?

**Business Value** = lợi ích có ý nghĩa đối với tổ chức khi một workflow được cải thiện.

Nó có thể xuất hiện dưới nhiều dạng:

- Tiết kiệm thời gian.
- Tăng năng suất hoặc throughput.
- Giảm lỗi / giảm rework.
- Cải thiện chất lượng hoặc consistency.
- Rút ngắn thời gian phản hồi khách hàng.
- Tăng khả năng phục vụ cùng một khối lượng công việc.
- Giúp nhân viên tập trung vào công việc có giá trị cao hơn.
- Hỗ trợ tăng doanh thu, giảm chi phí hoặc giảm rủi ro **nếu có đủ bằng chứng để nối tới outcome đó**.

Điểm quan trọng: **không được nhảy từ “AI làm được X” sang “doanh nghiệp sẽ kiếm thêm Y tiền” nếu chưa có dữ liệu và logic chứng minh.**

---

## 3. Business Value nằm ở đâu trong consultative story?

Một flow tư vấn tốt thường đi theo trình tự:

1. **Discovery** — hiểu vấn đề, workflow, người liên quan và evidence.
2. **Use Case Design** — chuyển pain point thành use case cụ thể.
3. **Prioritization** — chọn use case đáng thử trước.
4. **Business Value** — giải thích vì sao thay đổi workflow này có ý nghĩa với business.
5. **Measurement** — xác định cách chứng minh impact.
6. **Next step** — pilot, validate hoặc mở rộng.

Business Value vì vậy **không phải slide ROI được thêm vào cuối cuộc nói chuyện**. Nó phải được xây từ evidence có được trong discovery.

---

## 4. Phân biệt 3 tầng rất dễ nhầm

### Tầng 1 — Capability

AI có thể làm gì?

Ví dụ:

- Tóm tắt văn bản.
- Phân loại nội dung.
- Sinh draft.
- Trích xuất thông tin.
- Reasoning trên nhiều bước.

### Tầng 2 — Workflow outcome

Công việc thay đổi như thế nào?

Ví dụ:

- Nhân viên support đọc ticket nhanh hơn.
- Developer giảm thời gian viết test boilerplate.
- Sales rep chuẩn bị account brief nhanh hơn.

### Tầng 3 — Business outcome

Tại sao thay đổi đó quan trọng với doanh nghiệp?

Ví dụ:

- Tăng số ticket xử lý mỗi ngày.
- Giảm backlog.
- Rút ngắn release cycle.
- Tăng thời gian nhân viên dành cho công việc giá trị cao.
- Cải thiện customer response time.

> **Sai lầm phổ biến:** Capability được trình bày như thể chính nó đã là Business Value.

---

## 5. Ví dụ đơn giản

### Ví dụ: Customer Support

**Capability:** AI tóm tắt ticket và gợi ý draft response.

**Workflow change:** Agent không phải đọc toàn bộ lịch sử hội thoại và viết phản hồi từ đầu.

**Operational outcome:** Average handling time giảm.

**Business outcome có thể liên quan:**

- Tăng capacity của team.
- Giảm backlog.
- Cải thiện response time.

**Evidence cần có:**

- Bao nhiêu ticket/ngày?
- Hiện mất bao nhiêu phút/ticket?
- Phần nào của workflow AI có thể hỗ trợ?
- Tỷ lệ ticket nào phù hợp?
- Chất lượng phản hồi có giữ được không?

Không có các dữ liệu trên, ta mới chỉ có **potential value**, chưa phải proven value.

---

## 6. Cách nói chuyện với khách hàng

Thay vì hỏi:

> “Anh/chị muốn dùng GPT để làm gì?”

Hãy hướng cuộc trao đổi về workflow:

- Công việc nào đang tốn nhiều thời gian nhất?
- Bước nào lặp lại nhiều?
- Chỗ nào tạo backlog hoặc delay?
- Ai đang chịu ảnh hưởng?
- Hiện tại team đo hiệu quả bằng metric nào?
- Nếu bước này nhanh hơn hoặc tốt hơn thì business sẽ được lợi gì?

---

## 7. Framework ghi nhớ

### `Problem → Change → Outcome → Evidence`

| Thành phần | Câu hỏi |
|---|---|
| Problem | Workflow hiện tại đau ở đâu? |
| Change | AI sẽ thay đổi bước nào? |
| Outcome | Điều gì tốt hơn sau thay đổi? |
| Evidence | Dữ liệu nào chứng minh điều đó? |

Nếu thiếu **Evidence**, câu chuyện business value vẫn chỉ là giả thuyết.

---

## 8. Common mistakes

### 1. Feature-first

> “Model mới có context lớn hơn nên rất có giá trị.”

Chưa đủ. Context lớn hơn chỉ có ý nghĩa khi nó giải quyết một workflow cụ thể.

### 2. ROI-first

Cố tính ROI trước khi hiểu workflow thường tạo ra con số đẹp nhưng yếu.

### 3. Generic value

> “AI giúp tăng productivity.”

Đúng nhưng quá chung chung. Cần nói rõ:

- Productivity của ai?
- Trong workflow nào?
- Ở bước nào?
- Đo bằng metric nào?

### 4. Overclaim

Không nên biến “time saved” thành “cost saved” nếu doanh nghiệp chưa thực sự giảm chi phí hoặc tái phân bổ nguồn lực.

---

## 9. Vocabulary — từ chuyên ngành cần nhớ

| English | Hiểu đơn giản |
|---|---|
| Business value | Giá trị mà doanh nghiệp nhận được |
| Capability | Khả năng của AI |
| Workflow | Quy trình/cách công việc được thực hiện |
| Operational outcome | Kết quả ở cấp vận hành |
| Business outcome | Kết quả có ý nghĩa với doanh nghiệp |
| Evidence | Bằng chứng/dữ liệu hỗ trợ |
| Baseline | Mốc hiện tại trước khi thay đổi |
| Impact | Tác động tạo ra |
| Value hypothesis | Giả thuyết về giá trị có thể tạo ra |

---

## 10. Cheat sheet

```text
Đừng bắt đầu bằng:
“AI có thể làm gì?”

Hãy bắt đầu bằng:
“Workflow nào cần thay đổi?”

Sau đó nối:
Workflow change
→ operational outcome
→ business outcome
→ evidence
```

### 3 điều cần nhớ

1. **AI capability ≠ Business Value.**
2. Business Value phải gắn với **workflow thực tế**.
3. Một value story tốt luôn có **evidence hoặc kế hoạch đo lường**.
