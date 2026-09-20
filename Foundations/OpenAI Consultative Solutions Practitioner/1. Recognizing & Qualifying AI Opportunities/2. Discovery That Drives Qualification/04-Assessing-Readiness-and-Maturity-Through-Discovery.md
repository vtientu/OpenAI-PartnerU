# 04 — Assessing Readiness and Maturity Through Discovery

> **Module:** Discovery That Drives Qualification  
> **Loại tài liệu:** Study Notes / Teaching Notes  
> **Lưu ý:** Đây là ghi chú giảng lại để dễ học và ôn tập, không phải transcript nguyên văn của OpenAI PartnerU.

---

# 1. Definition — Là gì?

### Readiness
**Readiness** = khách hàng có thể bắt đầu use case này bây giờ chưa?

### Maturity
**Maturity** = tổ chức đã phát triển capability, process và governance cho AI đến mức nào?

Hai khái niệm liên quan nhưng không giống nhau.

---

# 2. Key idea

Một use case có problem rất rõ vẫn có thể **chưa ready**.

Ví dụ:

✓ Pain rõ  
✓ Volume lớn  
✓ Sponsor quan tâm

Nhưng:

? Data access chưa rõ  
? Security chưa review  
? Không có success metric  
? Không có human escalation process

→ Opportunity có value nhưng chưa đủ điều kiện triển khai ngay.

---

# 3. Readiness mental model

## 3.1 Problem
- Problem đã rõ chưa?
- Có evidence support không?
- Business impact có đủ meaningful không?

## 3.2 Data
- Data/knowledge có tồn tại?
- Có access được?
- Chất lượng có đủ tốt?
- Ai owns data?

## 3.3 People
- Có business owner?
- Có technical owner?
- Có sponsor?
- Có end users tham gia?

## 3.4 Process
- Workflow hiện tại rõ?
- Có exception cases?
- Có human handoff?

## 3.5 Technology
- Systems/integrations nào liên quan?
- Có API/dependency?
- Có technical constraints?

## 3.6 Governance
- Security?
- Privacy?
- Compliance?
- Access control?
- Human review?

## 3.7 Measurement
- Có baseline?
- Có success metric?
- Có evaluation method?

## 3.8 Adoption
- Người dùng có sẵn sàng?
- Workflow mới sẽ được áp dụng thế nào?
- Có change management không?

---

# 4. Example — AI Support Agent

Evidence:

- 8,000 tickets/month
- 40% repetitive
- ~6 minutes/ticket

Problem có vẻ mạnh.

Discovery tiếp:

> “Knowledge ở đâu?”

“Zendesk, Confluence, Google Docs.”

> “Ai maintain knowledge?”

“Không rõ.”

> “AI có được access customer account không?”

“Security chưa review.”

> “Nếu AI không chắc thì sao?”

“Chưa xác định.”

> “Pilot success đo bằng gì?”

“AI hoạt động tốt.”

Kết luận:

> **Problem validated hơn readiness.**

---

# 5. Readiness ≠ Maturity

## Example A
Tổ chức ít kinh nghiệm AI nhưng:

- problem rõ;
- owner rõ;
- data sẵn;
- pilot nhỏ;
- metric rõ.

→ **Maturity thấp nhưng có thể ready cho pilot.**

## Example B
Tổ chức đã thử nhiều AI tools nhưng:

- use case không có owner;
- governance unclear;
- metric không rõ.

→ **Maturity có vẻ cao nhưng use case cụ thể chưa ready.**

---

# 6. Readiness signals

## Positive signals
- clear business owner;
- accessible data;
- narrow use case;
- measurable KPI;
- involved technical team;
- governance stakeholders engaged;
- willingness to pilot.

## Warning signals
- “We just want AI.”
- no clear owner;
- unclear data source;
- no baseline;
- security involved too late;
- success defined vaguely;
- no user adoption plan.

---

# 7. Developer analogy

Một feature có business value cao nhưng:

- API chưa tồn tại;
- backend owner chưa xác định;
- security chưa approve;
- staging chưa sẵn sàng;
- acceptance criteria chưa rõ.

Bạn không nói:

> “Feature này không có value.”

Bạn nói:

> “Feature có value nhưng chưa ready để build.”

AI opportunity cũng vậy.

---

# 8. Common mistakes

## Nhầm value với readiness
Problem lớn không đồng nghĩa có thể triển khai ngay.

## Dùng maturity như điểm số tuyệt đối
Maturity phụ thuộc context và use case.

## Chỉ nhìn technical readiness
AI còn cần business, governance, people, adoption.

## Bỏ qua measurement
Không có baseline/KPI thì khó chứng minh success.

---

# 9. Checklist

- [ ] Problem đã validated?
- [ ] Data/knowledge available?
- [ ] Data access possible?
- [ ] Owner/sponsor rõ?
- [ ] Workflow hiểu đủ sâu?
- [ ] Technical dependencies rõ?
- [ ] Security/privacy/compliance được xem xét?
- [ ] Human oversight/escalation rõ?
- [ ] Success metric đo được?
- [ ] Người dùng có khả năng adopt?

---

# 10. Mental model

> **Is the problem real?**

Nếu yes:

> **Can this organization realistically act on it now?**

Nếu chưa:

> **What readiness gap needs to be resolved next?**

---

# 11. One-line takeaway

> **A valuable use case is not automatically a ready use case.**

Hiểu đơn giản:

**Use case có giá trị chưa chắc đã sẵn sàng để triển khai.**

---

# 12. Vocabulary

| English | Hiểu đơn giản |
|---|---|
| Readiness | Mức độ sẵn sàng |
| Maturity | Mức độ trưởng thành |
| Capability | Năng lực |
| Governance | Quản trị/kiểm soát |
| Constraint | Ràng buộc |
| Dependency | Phụ thuộc |
| Human oversight | Con người giám sát |
| Escalation | Chuyển lên người/nhóm xử lý |
| Adoption | Mức độ tiếp nhận/sử dụng |
| Success metric | Chỉ số thành công |
| Evaluation | Đánh giá |

---

# Cheat Sheet — 30 giây

### 3 điều phải nhớ

1. **Value ≠ Readiness**
2. **Readiness ≠ Maturity**
3. **AI readiness is more than technology**

### 8 nhóm cần kiểm tra

**Problem → Data → People → Process → Technology → Governance → Measurement → Adoption**

### Output cần có

**Readiness signals + gaps + risks**
