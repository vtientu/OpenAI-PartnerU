# 01 — Discovering the Customer Problem and Workflow Pain

> **Module:** Discovery That Drives Qualification  
> **Loại tài liệu:** Study Notes / Teaching Notes  
> **Lưu ý:** Đây là ghi chú giảng lại để dễ học và ôn tập, không phải transcript nguyên văn của OpenAI PartnerU.

---

# 1. Definition — Là gì?

### Customer Problem
**Customer problem** là vấn đề business/nghiệp vụ mà khách hàng đang thực sự gặp.

### Workflow Pain
**Workflow pain** là điểm gây:
- chậm;
- tốn công;
- lặp lại;
- dễ lỗi;
- rủi ro;
- trải nghiệm kém

trong cách công việc đang được thực hiện hiện tại.

---

# 2. Key idea

Khách hàng thường mô tả nhu cầu bằng **solution language**:

> “We want an AI chatbot.”

> “We need an agent.”

> “We want to automate this.”

Nhưng người làm consultative discovery cần quay về:

> **Current workflow → Pain → Cause → Impact**

Không nên bắt đầu bằng:

> “Khách hàng muốn AI gì?”

Mà nên bắt đầu bằng:

> “Công việc đang diễn ra thế nào và chỗ nào đang gây vấn đề?”

---

# 3. Problem-first vs Solution-first

## Solution-first

Customer:

> “We need an AI agent.”

Response:

> “Great, let's design an agent.”

Rủi ro:
- chưa hiểu workflow;
- chưa biết pain thật;
- chưa biết AI có phù hợp;
- dễ build sai thứ.

## Problem-first

Customer:

> “We need an AI agent.”

Discovery:

- Workflow hiện tại là gì?
- Ai thực hiện?
- Bước nào khó nhất?
- Pain xảy ra khi nào?
- Có workaround không?
- Impact là gì?

Sau đó mới nghĩ:

> “AI có phải cách phù hợp để cải thiện workflow này không?”

---

# 4. Example — Customer Support

Customer:

> “We want an AI agent for customer support.”

Discovery:

### Current workflow
Support request vào Zendesk.

Agent:
1. đọc ticket;
2. tìm thông tin trong Confluence;
3. kiểm tra CRM;
4. hỏi Slack nếu thiếu context;
5. trả lời khách.

### Workflow pain
- phải chuyển giữa nhiều hệ thống;
- nhiều câu hỏi lặp lại;
- knowledge khó tìm;
- response time tăng khi volume cao.

### Problem statement tốt hơn
Không phải:

> “Customer needs an AI agent.”

Mà là:

> “Support agents spend significant time handling repetitive questions and searching fragmented knowledge across multiple systems.”

---

# 5. Discovery questions hữu ích

## Understand the workflow
- “Can you walk me through how this works today?”
- “What happens first?”
- “What happens next?”
- “Who is involved?”

## Find the pain
- “Where does the process slow down?”
- “Which step is the most manual?”
- “Which part causes the most frustration?”
- “Where do errors happen?”

## Understand workarounds
- “What do people do when the process fails?”
- “What tools or manual steps are used today?”

## Understand impact
- “What happens when this takes too long?”
- “Who is affected?”
- “How does this affect the business?”

---

# 6. Developer analogy

Bug report:

> “Website chậm.”

Developer tốt không lập tức:

> “Đổi framework.”

Bạn investigate:

**User action → Network → API → Rendering → Root cause**

Consultative discovery cũng vậy:

**Workflow → Pain → Cause → Impact → Possible solution**

Một example:

> “Website slow” = problem statement ban đầu.

Sau investigation:

> “Checkout page chậm vì API `/checkout` mất 4.8s.”

Bây giờ problem rõ hơn nhiều.

---

# 7. Common mistakes

## Mistake 1 — Bắt đầu từ product
Nghe “AI agent” và lập tức nói về model, API, architecture.

## Mistake 2 — Chấp nhận problem quá chung
Ví dụ:

> “Our process is inefficient.”

Cần hỏi sâu hơn.

## Mistake 3 — Chỉ hỏi pain, không hỏi workflow
Nếu không hiểu workflow, bạn có thể hiểu sai nguyên nhân.

## Mistake 4 — Nhầm symptom với root problem
Ví dụ:

> “Response time chậm.”

Có thể symptom này đến từ:
- fragmented knowledge;
- manual approval;
- missing integration;
- staffing;
- process design.

---

# 8. Checklist

Sau discovery, bạn cần trả lời được:

- [ ] Workflow hiện tại là gì?
- [ ] Ai thực hiện workflow?
- [ ] Pain nằm ở bước nào?
- [ ] Pain xảy ra thường xuyên không?
- [ ] Workaround hiện tại là gì?
- [ ] Pain tạo ra business impact gì?
- [ ] Root cause có rõ chưa?
- [ ] Ta đang mô tả problem hay đã nhảy sang solution?

---

# 9. Mental model

> **How does the work happen today?**

↓

> **Where is the pain?**

↓

> **Why does it happen?**

↓

> **Why does it matter?**

↓

> **Only then consider AI.**

---

# 10. One-line takeaway

> **Understand how the work happens today before deciding how AI should change it.**

Hiểu đơn giản:

**Hiểu workflow và pain trước khi nghĩ đến AI solution.**

---

# 11. Vocabulary

| English | Hiểu đơn giản |
|---|---|
| Customer problem | Vấn đề business/nghiệp vụ |
| Workflow | Quy trình công việc |
| Pain point | Điểm gây khó khăn |
| Root cause | Nguyên nhân gốc |
| Workaround | Cách xử lý tạm/thủ công |
| Bottleneck | Điểm nghẽn |
| Manual step | Bước làm thủ công |
| Repetitive | Lặp đi lặp lại |
| Impact | Ảnh hưởng |
| Current state | Trạng thái hiện tại |
| Future state | Trạng thái mong muốn |

---

# Cheat Sheet — 30 giây

### 3 điều phải nhớ

1. **Problem ≠ requested solution**
2. **Understand the workflow first**
3. **Find pain + cause + impact**

### Câu hỏi quan trọng nhất

> **“Can you walk me through how this works today?”**

### Output cần có

**Clear problem + current workflow + workflow pain**
