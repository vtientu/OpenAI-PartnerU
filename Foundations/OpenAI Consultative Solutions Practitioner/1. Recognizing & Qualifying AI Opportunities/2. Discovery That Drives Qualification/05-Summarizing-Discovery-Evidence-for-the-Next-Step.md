# 05 — Summarizing Discovery Evidence for the Next Step

> **Module:** Discovery That Drives Qualification  
> **Loại tài liệu:** Study Notes / Teaching Notes  
> **Lưu ý:** Đây là ghi chú giảng lại để dễ học và ôn tập, không phải transcript nguyên văn của OpenAI PartnerU.

---

# 1. Definition — Là gì?

Sau discovery, cần biến nhiều thông tin thành một summary trả lời:

> **“Dựa trên những gì ta thực sự biết, bước tiếp theo hợp lý là gì?”**

Discovery summary không chỉ là meeting notes.

---

# 2. Key idea

Một summary tốt phải phân biệt:

- **What we know**
- **What we think**
- **What we still need to prove**

Sau đó dùng **gaps/uncertainties** để xác định next step.

---

# 3. Framework

> **Problem → Evidence → Impact → Readiness → Gaps → Next step**

## Problem
Vấn đề đã xác định là gì?

## Evidence
Bằng chứng nào support problem?

## Impact
Tại sao problem đáng giải quyết?

## Readiness
Điều gì cho thấy customer có thể tiến lên?

## Gaps
Điều gì chưa biết/chưa validate?

## Next step
Bước nào giải quyết uncertainty quan trọng tiếp theo?

---

# 4. Summary ≠ Meeting Notes

Meeting notes có thể chứa:

- ai nói gì;
- nhiều chi tiết;
- nhiều topic;
- nhiều open questions.

Discovery summary phải giúp người đọc biết:

> “Opportunity này đang ở đâu và cần làm gì tiếp theo?”

---

# 5. Evidence ≠ Interpretation

### Evidence
> “40% of tickets are repetitive.”

### Interpretation
> “This may be a good area for AI assistance.”

### Unsupported conclusion
> “40% of tickets can be automated.”

Không nên biến interpretation thành fact.

---

# 6. Example — AI Support

## Problem
Support agents dành nhiều thời gian xử lý câu hỏi lặp lại về orders, refunds và account settings.

## Evidence
- ~8,000 tickets/month
- ~40% repetitive
- ~6 minutes/ticket

## Impact
Khi volume tăng, backlog và response time tăng.

## Readiness
- historical ticket data exists;
- Head of Support sẵn sàng sponsor pilot.

## Gaps
- Security chưa validate customer-data access;
- knowledge phân tán;
- chưa có escalation policy;
- chưa có success metrics.

## Next step
Làm việc với Support Operations + Security để:
1. validate data access;
2. chọn safe pilot scope;
3. định nghĩa success metrics.

---

# 7. Next step tốt vs yếu

## Yếu
> “Schedule another meeting.”

Không rõ:
- meeting với ai;
- để giải quyết gì;
- output là gì.

## Tốt
> “Meet with Security and Support Operations to validate customer-data access and define a safe pilot scope.”

Có:
- **Who**
- **Why**
- **Expected outcome**

---

# 8. Nguyên tắc chọn next step

Next step nên:

- giải quyết gap quan trọng nhất;
- giảm uncertainty;
- tạo thêm evidence;
- có owner;
- có expected output;
- đủ cụ thể để hành động.

Không nên chọn next step chỉ vì:

> “Mình muốn đẩy deal đi tiếp.”

---

# 9. Developer analogy

Sau khi investigate bug:

> Checkout latency chủ yếu đến từ `/checkout` API (~4.8s), frontend rendering ~300ms.

Summary tốt:

> Backend latency là phần lớn bottleneck; logs đã sẵn sàng; backend team owns endpoint.

Next step:

> Backend team profile database queries của `/checkout`.

Không phải:

> “Rewrite frontend.”

AI discovery cũng vậy:

> **Summary evidence → identify gap → define next action.**

---

# 10. Common mistakes

## Viết summary quá chung
> “Customer is interested in AI.”

Không đủ giá trị.

## Trộn fact với assumption
Cần ghi rõ đâu là evidence, đâu là hypothesis.

## Không ghi readiness gaps
Làm opportunity trông “ready” hơn thực tế.

## Next step không gắn với discovery
Ví dụ meeting tiếp nhưng không biết nhằm validate gì.

---

# 11. Checklist

- [ ] Problem có được diễn đạt rõ?
- [ ] Evidence và assumption được tách riêng?
- [ ] Impact có rõ?
- [ ] Readiness signals có rõ?
- [ ] Gaps/risks có được ghi lại?
- [ ] Next step giải quyết gap quan trọng?
- [ ] Có owner cho next step?
- [ ] Next step có output/decision rõ?

---

# 12. Mental model

> **What do we know?**

↓

> **What do we think?**

↓

> **What do we still need to prove?**

↓

> **What is the smallest useful next step?**

---

# 13. One-line takeaway

> **The next step should follow from the evidence, not from the desire to sell a solution.**

Hiểu đơn giản:

**Bước tiếp theo phải xuất phát từ evidence và gaps, không phải từ mong muốn đẩy solution đi tiếp.**

---

# 14. Vocabulary

| English | Hiểu đơn giản |
|---|---|
| Summary | Tóm tắt |
| Evidence | Bằng chứng |
| Interpretation | Diễn giải |
| Gap | Điều còn thiếu/chưa rõ |
| Risk | Rủi ro |
| Uncertainty | Điều chưa chắc chắn |
| Next step | Bước tiếp theo |
| Expected outcome | Kết quả mong đợi |
| Scope | Phạm vi |
| Pilot | Thử nghiệm quy mô nhỏ |
| Validation | Xác thực |

---

# Cheat Sheet — 30 giây

### Framework

> **Problem → Evidence → Impact → Readiness → Gaps → Next step**

### 3 điều phải nhớ

1. **Summary ≠ meeting notes**
2. **Evidence ≠ interpretation**
3. **Next step must reduce uncertainty**

### Output cần có

**Clear discovery summary + concrete next step**
