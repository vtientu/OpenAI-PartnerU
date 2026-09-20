# 01 — What Makes an AI Opportunity Worth Pursuing?

## 1. Ý chính của section

Một AI opportunity đáng theo đuổi **không được đánh giá chỉ vì AI có thể làm được việc đó**.

Câu hỏi quan trọng hơn là:

> **Nếu workflow này được cải thiện, nó có tạo ra giá trị đủ lớn và đủ thực tế để đáng đầu tư thời gian hay không?**

Vì vậy, cần bắt đầu từ **workflow problem**, không bắt đầu từ technology.

---

## 2. AI idea khác AI opportunity như thế nào?

### AI idea
Ví dụ:

> “Chúng ta nên build một AI agent cho team support.”

Đây chỉ nói về solution.

Nó chưa trả lời:

- Agent giải quyết vấn đề nào?
- Ai đang gặp vấn đề?
- Vấn đề xảy ra bao nhiêu lần?
- Hiện tại mất bao nhiêu thời gian?
- Kết quả tốt hơn là gì?
- Có ai chịu trách nhiệm cho workflow không?

### AI opportunity
Ví dụ:

> “Support team nhận khoảng 400 ticket/tháng. Mỗi ticket mất trung bình 8 phút để phân loại và route. Khoảng 15% bị route sai. Nếu AI có thể đề xuất category và destination team trước khi agent xác nhận, chúng ta có thể giảm thời gian xử lý và rework.”

Đây là một opportunity rõ hơn vì có:

- workflow,
- current pain,
- frequency,
- evidence,
- user,
- outcome có thể đo.

---

## 3. Strong opportunity bắt đầu từ observable problem

Một cơ hội mạnh phải dựa trên **vấn đề có thể quan sát được**.

Các dấu hiệu đáng chú ý:

- Công việc xảy ra lặp lại thường xuyên.
- Nhiều người/team cùng gặp vấn đề.
- Có nhiều manual handoff.
- Có thời gian chờ đáng kể.
- Người dùng phải tạo workaround thủ công.
- Có rework hoặc lỗi lặp lại.
- Output thiếu nhất quán.
- Mọi người thường xuyên phải hỏi nhau cách hoàn thành task.
- Workflow khiến team phản ứng với thông tin quá chậm.

Các câu như:

> “AI chắc sẽ tiết kiệm thời gian.”  
> “Demo này trông rất hay.”

chưa đủ để chứng minh opportunity mạnh.

---

## 4. Potential value — Giá trị tiềm năng

OpenAI Academy gợi ý nhìn potential value qua các chiều sau.

### 4.1 Frequency — Tần suất

> Workflow xảy ra bao nhiêu lần?

Một task 100 lần/ngày thường có potential value cao hơn một task 2 lần/năm, nếu các yếu tố khác tương đương.

Ví dụ:

- Viết release note mỗi quý → frequency thấp.
- Triage support ticket mỗi ngày → frequency cao.

Frequency cao có thể khuếch đại một cải thiện nhỏ thành giá trị lớn.

---

### 4.2 Reach — Phạm vi ảnh hưởng

> Bao nhiêu người, team hoặc customer bị ảnh hưởng?

Một workflow chỉ làm phiền 1 người có thể ít ưu tiên hơn workflow làm chậm 200 nhân viên.

Reach không chỉ là số user trực tiếp. Nó có thể bao gồm:

- downstream teams,
- customers,
- managers,
- reviewers,
- operations.

---

### 4.3 Friction — Mức độ đau của workflow hiện tại

Friction có thể là:

- time spent,
- delay,
- waiting,
- duplicated work,
- rework,
- inconsistency,
- error,
- risk,
- poor user/customer experience.

Câu hỏi tốt:

> “Điều gì làm workflow này tốn kém hoặc khó chịu ở hiện tại?”

Càng mô tả được friction cụ thể, càng dễ đánh giá opportunity.

---

### 4.4 Repeatability — Khả năng tái sử dụng

> Nếu giải pháp hoạt động với nhóm đầu tiên, có thể reuse cho nhóm khác không?

Ví dụ:

Một workflow tóm tắt customer feedback nếu có pattern chuẩn có thể mở rộng từ Product Team sang Sales, Support hoặc Customer Success.

Repeatability làm tăng giá trị dài hạn.

---

### 4.5 Relevance — Liên hệ với priority thật

> Cải thiện workflow này có hỗ trợ một mục tiêu quan trọng của team/business không?

Ví dụ:

- giảm response time,
- tăng conversion,
- tăng developer throughput,
- giảm operational cost,
- giảm risk,
- cải thiện customer experience.

Một workflow có thể rất “cool” nhưng nếu không gắn với priority thực, nó có thể vẫn là low-value opportunity.

---

## 5. Value không đủ — phải xét Complexity & Effort

Một opportunity có potential value cao vẫn chưa chắc nên làm ngay.

Cần xem các yếu tố như:

### Process complexity
Workflow có rõ ràng và ổn định không?

Nếu mỗi người làm một kiểu khác nhau, có thể cần chuẩn hóa quy trình trước.

### System dependencies
Có cần truy cập:

- database,
- API,
- CRM,
- ticketing system,
- internal docs,
- source code,
- permissions?

### Governance and approvals
Có cần involvement từ:

- security,
- legal,
- compliance,
- privacy,
- IT,
- functional owner?

### Cross-functional dependencies
Có bao nhiêu team phải phối hợp?

### Change effort
User có phải thay đổi behavior nhiều không?

Một solution technically tốt nhưng không ai dùng vẫn không tạo value.

---

## 6. Hidden workflow complexity

Một trong những lỗi phổ biến là chỉ nhìn “happy path”.

Hãy tìm:

- upstream dependencies,
- downstream dependencies,
- handoffs,
- approval bottlenecks,
- manual workarounds,
- duplicated steps,
- unclear ownership,
- exception cases.

Đôi khi AI chỉ **che đi một process problem**, chứ không giải quyết nó.

Ví dụ:

> Công ty muốn dùng AI để tự động tổng hợp dữ liệu từ 6 spreadsheet.

Nhưng root cause thực tế là 6 team đang sử dụng 6 format dữ liệu khác nhau và không có owner cho schema.

Trong trường hợp này, chuẩn hóa data/process có thể là bước cần làm trước.

---

## 7. Value vs. Effort

Có thể dùng mental model 2 chiều:

| | Effort thấp | Effort cao |
|---|---|---|
| **Value cao** | Candidate tốt để test sớm | Strategic opportunity, cần sequence cẩn thận |
| **Value thấp** | Có thể thử nếu rất rẻ và giúp học | Thường nên deprioritize |

Đây không phải công thức cứng.

Nó giúp tránh hai lỗi:

1. Chọn idea rất visible nhưng value thấp.
2. Bỏ qua workflow nhỏ nhưng xảy ra thường xuyên và dễ tạo momentum.

---

## 8. Không phải mọi problem đều nên giải bằng AI

Luôn hỏi:

> “Nếu bỏ từ AI ra khỏi câu, cách đơn giản nhất để cải thiện workflow này là gì?”

Có thể solution tốt hơn là:

- sửa process,
- thêm validation rule,
- tạo form chuẩn,
- cải thiện search,
- viết automation deterministic,
- thay đổi ownership,
- tích hợp hai hệ thống.

AI phù hợp hơn khi workflow cần xử lý các công việc như:

- language,
- unstructured information,
- classification,
- extraction,
- summarization,
- generation,
- reasoning over context,
- flexible decision support.

Nhưng capability fit vẫn phải được test, không được assumption.

---

## 9. Example — Frontend bug triage

### Problem
Bug reports đến từ nhiều channel và format khác nhau.

### Current friction
Developer phải:

1. đọc report,
2. tìm component liên quan,
3. hỏi lại thiếu thông tin,
4. gắn severity,
5. route cho squad phù hợp.

### Evidence

- 250 bug reports/tháng.
- 6 phút/report cho bước triage.
- 20% thiếu reproduction steps.
- 12% phải re-route.

### Potential value

- Frequency: cao.
- Reach: Support + QA + Engineering.
- Friction: time + rework + delay.
- Repeatability: có thể dùng cho nhiều product team.
- Relevance: hỗ trợ giảm bug resolution time.

### Nhưng cần kiểm tra thêm

- AI có truy cập đúng product docs không?
- Có dữ liệu lịch sử đủ tốt không?
- Severity có yêu cầu human approval không?
- Có owner cho triage process không?

→ Opportunity có vẻ có giá trị, nhưng judgment cuối cùng còn phụ thuộc readiness và evidence.

---

## 10. Checklist section 01

Trước khi nói “đây là strong AI opportunity”, hãy trả lời:

- [ ] Workflow cụ thể là gì?
- [ ] Ai thực hiện workflow?
- [ ] Pain/friction hiện tại là gì?
- [ ] Workflow xảy ra bao nhiêu lần?
- [ ] Bao nhiêu người/team/customer bị ảnh hưởng?
- [ ] Có rework, delay, error hoặc risk không?
- [ ] Nếu cải thiện, outcome nào trở nên tốt hơn?
- [ ] Outcome đó có liên quan business/team priority không?
- [ ] Nếu solution thành công, có reuse được không?
- [ ] Có dependency hoặc approval lớn nào không?
- [ ] AI có thực sự cần thiết hay process/software thường là đủ?

---

## 11. Vocabulary

| English | Nghĩa |
|---|---|
| Worth pursuing | Đáng để tiếp tục đầu tư/tìm hiểu |
| Observable problem | Vấn đề có thể quan sát/chứng minh |
| Potential value | Giá trị tiềm năng |
| Frequency | Tần suất |
| Reach | Phạm vi ảnh hưởng |
| Friction | Ma sát/điểm gây tốn công, chậm, lỗi |
| Repeatability | Khả năng lặp lại/tái sử dụng |
| Relevance | Mức độ liên quan tới priority |
| Effort | Công sức/chi phí triển khai |
| Hidden complexity | Độ phức tạp ẩn |
| Workaround | Cách làm tạm để né một vấn đề trong quy trình |
| Deprioritize | Hạ mức ưu tiên |

---

## Key takeaway

> **Đừng hỏi “AI làm được gì ở đây?” trước. Hãy hỏi “workflow nào đang có vấn đề, giá trị của việc cải thiện nó là gì, và điều gì chứng minh rằng vấn đề này đáng theo đuổi?”**
