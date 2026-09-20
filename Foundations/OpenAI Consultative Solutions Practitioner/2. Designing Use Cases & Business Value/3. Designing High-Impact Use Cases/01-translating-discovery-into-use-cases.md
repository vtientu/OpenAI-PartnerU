# Designing High-Impact Use Cases
## Section 01 — Translating discovery into use cases

> **Mục tiêu:** Biết cách biến những gì thu thập được trong quá trình **discovery** thành một **AI use case** rõ ràng, có giá trị kinh doanh và đủ cụ thể để tiếp tục đánh giá, thiết kế hoặc thử nghiệm.

---

## 1. Ý tưởng cốt lõi

Trong discovery, chúng ta tìm hiểu:

- Khách hàng đang gặp vấn đề gì?
- Workflow hiện tại diễn ra như thế nào?
- Ai tham gia vào workflow?
- Bước nào chậm, lặp lại, tốn công hoặc dễ sai?
- Dữ liệu nào đang được sử dụng?
- Kết quả kinh doanh nào quan trọng?
- Có bằng chứng nào cho thấy vấn đề đủ đáng để giải quyết?

Nhưng những thông tin trên **chưa phải là một use case**.

Bước tiếp theo là chuyển bằng chứng discovery thành một mô tả đủ cụ thể về cách AI có thể hỗ trợ một phần của workflow.

Có thể hình dung như sau:

```text
Discovery evidence
      ↓
Customer problem / workflow pain
      ↓
Specific task or workflow step
      ↓
AI capability
      ↓
Desired output
      ↓
Business benefit
      ↓
Measurable success criteria
      ↓
AI use case
```

### Câu cần nhớ

> **Discovery tells us where the problem is. Use-case design defines where and how AI may create value.**

Nói đơn giản:

- **Discovery** = hiểu vấn đề.
- **Use case** = mô tả cách AI có thể giải quyết một phần cụ thể của vấn đề đó.

---

## 2. Đừng bắt đầu từ công nghệ

Một lỗi phổ biến là bắt đầu bằng câu:

> “Khách hàng muốn dùng AI / ChatGPT / agent.”

Đây chưa phải use case.

AI là **capability** hoặc công nghệ được sử dụng để giải quyết vấn đề. Nó không phải bản thân vấn đề kinh doanh.

Thay vì hỏi:

> “Chúng ta có thể dùng AI ở đâu?”

Nên bắt đầu từ:

> “Trong workflow hiện tại, bước nào tạo ra nhiều friction hoặc business impact nhất, và AI có khả năng hỗ trợ bước đó không?”

### Ví dụ

**Quá rộng:**

```text
Use AI to improve customer support.
```

Vấn đề: chưa biết ai dùng, AI làm gì, đầu vào là gì, kết quả mong muốn là gì.

**Cụ thể hơn:**

```text
Customer-support agents use AI to search internal product documentation
and generate a grounded draft response to customer questions,
reducing the time required to find and compose an answer.
```

Bây giờ ta đã thấy:

- **User:** customer-support agent
- **Task:** trả lời câu hỏi khách hàng
- **Pain:** mất thời gian tìm tài liệu và soạn câu trả lời
- **AI capability:** search/research + generation
- **Output:** draft response dựa trên tài liệu nội bộ
- **Benefit:** giảm thời gian xử lý

---

## 3. Discovery evidence được chuyển thành use case như thế nào?

Một use case tốt thường không xuất hiện từ một câu nói đơn lẻ của khách hàng.

Nó được tạo ra bằng cách kết nối nhiều evidence thu được trong discovery.

### Ví dụ discovery

Khách hàng nói:

```text
Support agents spend 10–15 minutes searching several internal systems
before they can answer many product questions.
```

Ta có thể phân tích:

| Discovery evidence | Ý nghĩa |
|---|---|
| Support agents | Người thực hiện workflow |
| Answer product questions | Công việc cần hoàn thành |
| Search several systems | Bước gây friction |
| 10–15 minutes | Evidence về mức độ pain |
| Internal systems | Data / knowledge source |

Từ đây, ta có thể xây dựng use case:

```text
Help support agents retrieve relevant product knowledge and draft
an answer using information from approved internal sources.
```

Điểm quan trọng là use case phải **traceable back to discovery evidence** — tức là ta có thể giải thích vì sao use case này tồn tại bằng những gì khách hàng đã cung cấp.

---

## 4. Cấu trúc cơ bản của một AI use case

Một format rất hữu ích là:

```text
As a [role],
I use AI to [task]
using [capability / information]
so that [business benefit].
```

OpenAI cũng sử dụng cách diễn đạt tương tự khi hướng dẫn tổ chức mô tả use case nhất quán.

### Ví dụ

```text
As a customer-support agent,
I use AI to find relevant product information and draft responses
using approved internal documentation,
so that I can answer customer questions faster and more consistently.
```

### 4 thành phần quan trọng

#### 1. Role — Ai sử dụng?

Ví dụ:

- Support agent
- Sales representative
- Marketing analyst
- Software engineer
- Finance analyst

Không nên chỉ viết “the company” hoặc “users” nếu có thể xác định rõ người thực hiện workflow.

#### 2. Task — Công việc cụ thể là gì?

Ví dụ:

- tìm thông tin
- tóm tắt tài liệu
- phân loại ticket
- soạn phản hồi
- phân tích dữ liệu
- tạo test cases
- review code

Task càng cụ thể thì use case càng dễ đánh giá.

#### 3. AI capability — AI hỗ trợ bằng khả năng gì?

Một số nhóm capability thường gặp:

- **Content creation** — tạo nội dung
- **Research / information retrieval** — tìm và tổng hợp thông tin
- **Coding** — hỗ trợ phát triển phần mềm
- **Data analysis** — phân tích dữ liệu
- **Ideation / strategy** — hỗ trợ suy nghĩ và xây dựng phương án
- **Task automation** — tự động hóa các bước công việc

Không nhất thiết một use case chỉ dùng một capability.

#### 4. Benefit — Giá trị mang lại là gì?

Ví dụ:

- giảm thời gian xử lý
- tăng throughput
- tăng chất lượng hoặc tính nhất quán
- giảm manual work
- tăng khả năng truy cập knowledge
- rút ngắn time-to-market

Benefit nên liên hệ trực tiếp với pain đã tìm thấy trong discovery.

---

## 5. Từ problem statement đến use case

Một cách làm thực tế là đi qua 5 bước.

### Step 1 — Xác định problem statement

Ví dụ:

```text
Support agents spend too much time searching multiple systems
for product information before answering customers.
```

### Step 2 — Xác định workflow step gây pain

Workflow có thể là:

```text
Customer asks question
      ↓
Agent understands the question
      ↓
Agent searches multiple systems   ← pain
      ↓
Agent identifies relevant information
      ↓
Agent writes response             ← pain
      ↓
Agent sends response
```

AI không nhất thiết phải thay thế cả workflow.

Ta nên tìm **bước cụ thể** mà AI có khả năng cải thiện.

### Step 3 — Xác định AI capability phù hợp

Trong ví dụ này:

```text
Search / retrieval
+
Summarization
+
Response generation
```

### Step 4 — Xác định desired outcome

Ví dụ:

```text
Agents can get a relevant, grounded draft answer from approved sources.
```

### Step 5 — Gắn với business value

Ví dụ:

```text
Reduce average response-preparation time.
```

Kết quả:

```text
AI-assisted support response preparation
```

Use case:

```text
Support agents use AI to retrieve relevant information from approved
internal sources and generate a draft response, reducing the time
required to prepare answers to customer questions.
```

---

## 6. Một discovery problem có thể tạo ra nhiều use cases

Không nên giả định:

```text
1 problem = 1 use case
```

Một workflow có thể chứa nhiều điểm AI có thể hỗ trợ.

Ví dụ workflow support:

```text
Incoming ticket
      ↓
Understand request
      ↓
Categorize ticket
      ↓
Find relevant knowledge
      ↓
Draft response
      ↓
Review response
      ↓
Update system
```

Có thể tạo ra nhiều use cases:

1. **Ticket classification**  
   AI phân loại ticket và đề xuất routing.

2. **Knowledge retrieval**  
   AI tìm thông tin liên quan từ knowledge base.

3. **Response drafting**  
   AI tạo draft trả lời.

4. **Conversation summarization**  
   AI tóm tắt cuộc trao đổi để cập nhật CRM/support system.

Điều quan trọng là không gom tất cả thành một use case quá lớn như:

```text
Automate customer service with AI.
```

Use case càng rõ ràng thì càng dễ:

- đánh giá feasibility,
- xác định data requirement,
- thiết kế prototype,
- đo impact,
- xác định risk,
- và quyết định ưu tiên.

---

## 7. Phân biệt Problem, Solution và Use Case

Đây là phần rất dễ nhầm.

### Problem

```text
Agents spend too much time finding product information.
```

Đây là **business/workflow problem**.

### Solution

```text
Build a RAG application connected to the knowledge base.
```

Đây là một **technical solution**.

### Use case

```text
Support agents retrieve relevant product information from approved
internal sources while responding to customer questions.
```

Đây là **cách AI được sử dụng trong workflow để tạo ra value**.

### Câu cần nhớ

```text
Problem = What is wrong?
Use case = Where/how could AI create value?
Solution = How will we technically build it?
```

Trong giai đoạn use-case design, không nên nhảy quá sớm sang kiến trúc hoặc implementation.

---

## 8. Ví dụ gần với Frontend Developer

Giả sử discovery với một engineering team cho thấy:

- Developer phải đọc nhiều file để hiểu một component cũ.
- Viết unit test mất khá nhiều thời gian.
- Pull request thường bị chậm vì reviewer phải tìm context.

### Không nên viết

```text
Use AI for software development.
```

Quá rộng.

### Use case 1 — Code understanding

```text
As a developer,
I use AI to explain unfamiliar components and trace related code,
so that I can understand an existing codebase faster.
```

### Use case 2 — Test generation

```text
As a frontend developer,
I use AI to generate initial unit-test cases from component behavior
and acceptance criteria,
so that I can reduce repetitive test-writing work.
```

### Use case 3 — Pull-request review support

```text
As a reviewer,
I use AI to summarize a pull request and highlight important changes,
so that I can understand the change context faster before reviewing it.
```

Một discovery problem của engineering team có thể trở thành nhiều use cases độc lập như vậy.

---

## 9. Một use case tốt cần đủ cụ thể nhưng không quá kỹ thuật

Hãy xem ba mức độ sau.

### Quá rộng

```text
Improve engineering productivity with AI.
```

Khó đánh giá và khó đo.

### Phù hợp

```text
Frontend developers use AI to generate initial unit tests from component
behavior and acceptance criteria, reducing repetitive test-writing time.
```

Có:

- actor,
- task,
- capability,
- outcome,
- value.

### Quá kỹ thuật quá sớm

```text
Create a Node.js service using model X, embeddings, vector database Y,
and framework Z to generate Jest tests.
```

Đây đã là **solution architecture**, không còn là use-case definition.

---

## 10. Gắn use case với measurable impact

Một use case mạnh nên dẫn tới câu hỏi:

> **How will we know this is working?**

Ví dụ use case:

```text
AI-assisted support response drafting
```

Có thể đo bằng:

- average response-preparation time,
- tickets handled per agent,
- first-response time,
- acceptance/edit rate của AI-generated drafts,
- answer quality hoặc consistency,
- customer satisfaction nếu có liên hệ trực tiếp.

Không phải lúc nào discovery ban đầu cũng đã có target chính xác.

Nhưng ít nhất ta nên biết **metric nào sẽ phản ánh value**.

---

## 11. Không biến mọi pain point thành AI use case

Discovery có thể tìm thấy nhiều vấn đề, nhưng AI không phải lúc nào cũng là giải pháp phù hợp.

Ví dụ:

```text
A form has 20 unnecessary fields and users find it annoying.
```

Giải pháp tốt nhất có thể đơn giản là:

```text
Remove unnecessary fields.
```

Không cần AI.

Vì vậy khi translate discovery → use case, cần hỏi:

1. Đây có phải vấn đề thật không?
2. Có đủ evidence cho thấy nó đáng giải quyết không?
3. AI có capability phù hợp với task không?
4. AI có tạo ra improvement đáng kể so với cách đơn giản hơn không?

---

## 12. Checklist chuyển discovery thành use case

Trước khi coi một use case là đủ rõ, hãy kiểm tra:

- [ ] Tôi biết **ai** thực hiện workflow này.
- [ ] Tôi biết **task hoặc workflow step** cụ thể cần cải thiện.
- [ ] Tôi biết **pain/friction** hiện tại là gì.
- [ ] Pain có **discovery evidence** hỗ trợ.
- [ ] Tôi biết AI sẽ dùng **capability** nào.
- [ ] Tôi biết **input / information source** quan trọng là gì.
- [ ] Tôi hình dung được **output** mong muốn.
- [ ] Tôi biết **business benefit** là gì.
- [ ] Tôi biết **metric** nào có thể dùng để đánh giá impact.
- [ ] Tôi chưa nhảy quá sớm vào technical architecture.

Nếu thiếu nhiều mục trong checklist, có thể cần quay lại discovery để hỏi thêm.

---

## 13. Công thức ghi nhớ nhanh

### Discovery

```text
WHO
+ WORKFLOW
+ PAIN
+ EVIDENCE
+ BUSINESS OUTCOME
```

### Use case

```text
WHO
+ TASK
+ AI CAPABILITY
+ OUTPUT
+ VALUE
+ SUCCESS METRIC
```

### Bridge

```text
Discovery evidence
→ identify painful workflow step
→ identify AI-suitable task
→ define expected output
→ connect to business value
→ define how success could be measured
```

---

## 14. Mini example hoàn chỉnh

### Discovery evidence

```text
Sales representatives spend around 30 minutes before customer meetings
reading CRM notes, previous emails, and account documents.
```

### Problem

```text
Meeting preparation requires manually gathering information from
multiple sources.
```

### Workflow step

```text
Gather and synthesize account context before a meeting.
```

### AI capability

```text
Research + summarization.
```

### Use case

```text
As a sales representative,
I use AI to summarize relevant CRM notes, account documents,
and prior interactions before a customer meeting,
so that I can prepare faster while retaining the important account context.
```

### Potential success metrics

```text
- Preparation time per meeting
- Percentage of generated briefs considered useful
- Number of sources manually opened by the seller
```

Đây chính là quá trình **translating discovery into a use case**.

---

## 15. Key takeaways

1. **Discovery evidence là nguyên liệu đầu vào của use-case design.**
2. Đừng bắt đầu bằng “chúng ta muốn dùng AI”; hãy bắt đầu từ workflow và pain.
3. Tìm **task hoặc workflow step cụ thể** mà AI có thể cải thiện.
4. Một use case nên làm rõ **role + task + capability + benefit**.
5. Use case phải liên kết được với **business value** và ideally có **success metric**.
6. Một problem có thể tạo ra nhiều use cases.
7. Không nên nhảy từ problem thẳng sang architecture.
8. Không phải mọi pain point đều cần AI.

---

## 16. Vocabulary — từ vựng cần nhớ

| Term | Nghĩa dễ hiểu |
|---|---|
| Discovery | Quá trình tìm hiểu vấn đề, workflow, stakeholder và evidence |
| Use case | Một cách sử dụng AI cụ thể để hỗ trợ task/workflow và tạo value |
| Workflow | Chuỗi các bước để hoàn thành một công việc |
| Pain point | Điểm gây khó khăn, chậm, tốn công hoặc lỗi |
| Friction | Sự cản trở / bất tiện trong workflow |
| Evidence | Bằng chứng cho thấy problem thực sự tồn tại và đáng quan tâm |
| Actor / Role | Người thực hiện hoặc sử dụng use case |
| Task | Công việc cụ thể cần hoàn thành |
| Capability | Khả năng của AI được áp dụng cho task |
| Outcome | Kết quả mong muốn |
| Business value | Giá trị mang lại cho tổ chức |
| Success metric | Chỉ số dùng để đánh giá use case có hiệu quả hay không |
| Grounded | Câu trả lời dựa trên nguồn dữ liệu/thông tin được cung cấp |
| Feasibility | Mức độ khả thi |
| Traceable | Có thể truy ngược lại nguồn/bằng chứng ban đầu |

---

## 17. One-line summary

> **Translating discovery into use cases means turning validated workflow pain into a specific AI-enabled task with a clear user, outcome, business value, and way to measure success.**

---

## Nguồn tham khảo

Phần ghi chú này là bản diễn giải phục vụ học tập, không phải transcript nguyên văn của PartnerU. Nội dung được xây dựng theo tên section và các nguyên tắc use-case design được OpenAI công khai:

- OpenAI Academy — *Empowering and supporting your team*: https://academy.openai.com/en/public/clubs/admins-6o6xf/resources/empowering-and-supporting-your-team
- OpenAI customer story — *The Estée Lauder Companies*: https://openai.com/index/estee-lauder/

