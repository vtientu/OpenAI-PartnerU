# 02 — OpenAI’s Evolution and Operating Posture

> **Course:** Foundation — OpenAI Foundational Knowledge  
> **Step:** Introduction to OpenAI  
> **Section:** OpenAI’s evolution and operating posture

---

## 1. Section objective

Sau section này, bạn cần hiểu:

- OpenAI đã tiến hóa như thế nào từ research organization đến research + deployment organization;
- vì sao deployment quan trọng bên cạnh research;
- **operating posture** nghĩa là gì;
- iterative deployment hoạt động như thế nào;
- vì sao partner nên áp dụng tư duy test → evaluate → deploy → improve.

---

# 2. Evolution là gì?

**Evolution** = quá trình một tổ chức thay đổi theo thời gian.

Trong bài này, không nên học timeline chỉ để nhớ năm.

Điều cần hiểu là:

> OpenAI đã thay đổi cách tổ chức và cách đưa AI ra thế giới khi capability, compute requirement và quy mô deployment tăng lên.

Mental model:

```text
Research
   ↓
Frontier capability
   ↓
Products / APIs
   ↓
Real-world deployment
   ↓
Feedback + evidence
   ↓
Better systems
```

---

# 3. Giai đoạn đầu — Research focus

OpenAI được thành lập năm 2015 dưới dạng nonprofit.

Trọng tâm ban đầu:

- AI research;
- frontier capabilities;
- long-term safety;
- mission alignment.

Ở giai đoạn này, mental model đơn giản là:

```text
Understand AI
→ advance AI
→ study safety
```

Nhưng frontier AI cần tài nguyên ngày càng lớn.

---

# 4. Vì sao organizational model phải thay đổi?

Frontier AI cần:

- large-scale compute;
- engineering talent;
- infrastructure;
- capital;
- product development;
- deployment capability.

Điều này tạo ra bài toán:

```text
Mission
+
Research ambition
+
Massive resource requirements
```

OpenAI vì thế phát triển thêm cấu trúc thương mại để có thể huy động và triển khai tài nguyên ở quy mô lớn hơn.

Điểm cần nhớ:

> Sự phát triển commercial capability là một phần của việc scale research và deployment.

---

# 5. Research → Platform → Product → Deployment

Khi model trở nên hữu ích hơn, OpenAI không chỉ nghiên cứu.

Capability được đưa tới:

- developers;
- consumers;
- startups;
- enterprises;
- partners.

Các hình thức deployment bao gồm:

```text
Models
API / platform
ChatGPT / products
Enterprise workflows
Partner-built solutions
```

Đây là một bước chuyển rất quan trọng.

---

# 6. Research and deployment company

OpenAI tự mô tả mình là một:

> **AI research and deployment company**

Hai từ cần hiểu riêng.

## Research

Mục tiêu:

- tạo capability mới;
- hiểu model behavior;
- cải thiện reasoning;
- multimodality;
- coding;
- safety;
- agentic capability.

## Deployment

Mục tiêu:

- đưa capability vào real-world use;
- học từ user behavior;
- phát hiện limitations;
- cải thiện product;
- thu evidence;
- xây safety practices.

Hai hoạt động tạo vòng lặp:

```text
Research
   ↓
Deployment
   ↓
Real-world feedback
   ↓
Evaluation
   ↓
Improvement
   ↓
Research
```

---

# 7. Operating posture là gì?

**Operating posture** không phải tên của một tính năng.

Nó có nghĩa gần như:

> **Cách OpenAI lựa chọn để vận hành và đưa AI vào thực tế.**

Nó thể hiện qua các pattern lặp lại như:

- iterative deployment;
- evaluation;
- safety;
- human control;
- learning from evidence;
- adaptation.

---

# 8. Operating posture #1 — Iterative deployment

**Iterative deployment** = không chờ tới khi hệ thống “hoàn hảo” mới học từ thực tế.

Thay vào đó:

```text
Build
↓
Test
↓
Deploy in controlled way
↓
Observe
↓
Evaluate
↓
Improve
↓
Expand
```

Đây rất giống software development, nhưng AI cần evaluation behavior nhiều hơn.

---

# 9. So sánh với frontend development

Bạn có thể liên hệ với workflow quen thuộc:

### Traditional frontend

```text
Requirement
→ implementation
→ unit/integration test
→ deploy
→ analytics
→ iterate
```

### AI application

```text
Business problem
→ workflow design
→ prototype
→ eval dataset
→ test system behavior
→ pilot
→ monitor
→ improve
```

Khác biệt:

Traditional code phần lớn deterministic.

AI behavior mang tính probabilistic hơn.

Do đó test không chỉ là:

```text
input A → exact output B
```

Mà còn là:

- output quality;
- correctness;
- grounding;
- tool choice;
- policy compliance;
- escalation behavior.

---

# 10. Operating posture #2 — Capability + safety

Một cách hiểu sai:

```text
Build capability
→ finish product
→ add safety later
```

Tư duy tốt hơn:

```text
Capability development
        +
Safety / evaluation / controls
```

Safety phải xuất hiện ở nhiều layer:

- model;
- prompt/instruction;
- tools;
- permissions;
- data;
- app logic;
- monitoring;
- human review.

---

# 11. Operating posture #3 — Human control

AI system không nhất thiết phải fully autonomous.

Trong nhiều workflow:

```text
AI proposes
↓
System checks
↓
Human approves
↓
Action executes
```

Hoặc:

```text
AI handles normal cases
↓
Exception detected
↓
Human escalation
```

Điểm quan trọng:

> **Autonomy là design choice, không phải success metric.**

Success metric phải là outcome.

---

# 12. Operating posture #4 — Learn from evidence

OpenAI hoạt động trong lĩnh vực thay đổi nhanh.

Do đó quyết định cần cập nhật khi có:

- capability mới;
- evaluation mới;
- deployment evidence;
- incidents;
- new risk;
- customer feedback.

Partner cũng nên áp dụng tư duy:

> Không dùng một architecture pattern cho mọi customer mãi mãi.

---

# 13. Operating posture #5 — Controlled scaling

Không nên triển khai:

```text
Idea
→ full enterprise rollout
```

Tốt hơn:

```text
Opportunity
→ narrow use case
→ evaluation
→ pilot
→ production
→ expand
```

Điều này giúp giảm risk và tạo evidence.

---

# 14. Cấu trúc tổ chức hiện nay

Từ cấu trúc được OpenAI công bố năm 2025:

- **OpenAI Foundation** là nonprofit;
- **OpenAI Group PBC** là public benefit corporation;
- Foundation tiếp tục giữ vai trò kiểm soát.

## PBC là gì?

**Public Benefit Corporation** là loại hình công ty có thể theo đuổi cả:

- commercial success;
- public benefit;
- stakeholder interests.

Điểm cần nhớ trong bài:

> Commercial scale và mission orientation được thiết kế để cùng tồn tại.

---

# 15. Vì sao evolution này quan trọng với partner?

Partner cần hiểu rằng OpenAI không chỉ là:

```text
Model vendor
```

Mà là một organization hoạt động theo chuỗi:

```text
Research
→ capability
→ platform/products
→ deployment
→ ecosystem
```

Điều này ảnh hưởng tới cách partner làm việc:

- không chỉ bán license/API;
- cần understand deployment;
- cần validate use case;
- cần evaluate;
- cần drive adoption;
- cần feedback loop.

---

# 16. Partner implementation pattern

Một pattern phù hợp:

```text
1. Discover problem
2. Define workflow
3. Select candidate use case
4. Prototype
5. Build evaluation set
6. Test
7. Pilot
8. Add controls
9. Production deployment
10. Monitor and improve
```

---

# 17. Common mistakes

## Mistake 1
“Model mới ra → phải migrate ngay.”

Không nhất thiết.

Cần evaluate trên task thật.

## Mistake 2
“Pilot chạy được → production-ready.”

Sai.

Production còn cần:

- security;
- monitoring;
- scalability;
- permissions;
- reliability;
- support;
- governance.

## Mistake 3
“Human review chứng minh AI chưa tốt.”

Sai.

Human review có thể là deliberate control.

## Mistake 4
“Deploy xong là kết thúc.”

Sai.

AI system cần continuous evaluation và improvement.

---

# 18. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| **Evolution** | Quá trình phát triển/thay đổi |
| **Operating posture** | Cách tổ chức vận hành và hành động |
| **Deployment** | Đưa hệ thống vào sử dụng |
| **Iterative deployment** | Triển khai theo vòng lặp |
| **Controlled deployment** | Triển khai có kiểm soát |
| **Feedback loop** | Vòng phản hồi |
| **Human control** | Kiểm soát của con người |
| **Autonomy** | Mức độ tự chủ |
| **Evidence** | Bằng chứng |
| **Pilot** | Triển khai thử phạm vi giới hạn |
| **Scale** | Mở rộng quy mô |
| **PBC** | Public Benefit Corporation |

---

# 19. Section recap

1. OpenAI tiến hóa từ research-focused organization sang **research + deployment company**.
2. Deployment giúp tạo real-world evidence.
3. Research và deployment tạo feedback loop.
4. Operating posture gồm iterative deployment, safety, human control và adaptation.
5. AI nên scale dựa trên evidence.
6. Pilot không đồng nghĩa production-ready.
7. Partner nên dùng workflow **discover → test → evaluate → deploy → improve**.

---

# 20. Self-check

1. “Research and deployment” có nghĩa gì?
2. Tại sao real-world deployment có ích cho research?
3. Iterative deployment khác big-bang deployment thế nào?
4. Vì sao human review có thể là design tốt?
5. Tại sao model mới không nên được adopt chỉ vì benchmark cao?
