# 02. Map the Workflow to a User or Product Surface

> Course: **OpenAI Consultative Solutions Practitioner – Foundations**  
> Sub-course: **Mapping Solutions & Advancing the Opportunity**  
> Section: **Map the workflow to a user or product surface**

---

## 1. Mục tiêu của section

Section này dạy cách chọn **surface** dựa trên cách công việc thực sự diễn ra.

Câu hỏi trung tâm:

> **Where should AI show up so the workflow becomes better?**

Không phải:

> “Product nào mạnh nhất?”

Mà là:

> “Interaction model nào phù hợp nhất với user và workflow?”

---

# 2. Surface là gì?

**User/product surface** = nơi người dùng hoặc workflow tương tác với AI.

Trong Knowledge Checks, các surface quan trọng gồm:

- **ChatGPT Chat**
- **ChatGPT Work**
- **Codex**
- **An application or process built with the API**
- **Combined solution using more than one surface**

Có thể có Workspace Agents trong routing rộng hơn, nhưng section này tập trung vào việc match workflow với trải nghiệm/surface mạnh nhất.

---

# 3. Mental model: interaction pattern → surface

```text
Interactive exploration
→ ChatGPT Chat

Delegated multi-step knowledge work
→ ChatGPT Work

Software engineering workflow
→ Codex

AI embedded into product/process
→ API-built application/process

Multiple user groups / interaction models
→ Combined solution
```

---

# 4. ChatGPT Chat — khi nào phù hợp?

Chat phù hợp khi user:

- chủ động hỏi;
- khám phá;
- iterate;
- draft;
- refine;
- reason together with AI;
- muốn kiểm soát từng vòng tương tác.

Pattern:

```text
Ask
→ inspect
→ clarify
→ refine
→ draft
→ revise
```

### Knowledge Check example

> Employees need to explore policy documents and iteratively draft reviewed responses.

Clue:

```text
explore
iteratively
draft
review
```

→ **ChatGPT Chat**

### Vì sao?

Đây là **interactive knowledge work**, không phải một workflow cần AI tự hoàn thành end-to-end.

---

# 5. ChatGPT Work — khi nào phù hợp?

Work phù hợp khi user muốn **delegate** một task nhiều bước và nhận finished deliverable.

Pattern:

```text
Goal
→ gather context
→ plan
→ execute multiple steps
→ create finished output
→ user reviews
```

### Knowledge Check example

> A finance team wants to delegate source gathering, analysis, and creation of a review-ready weekly performance pack.

Clue:

```text
delegate
source gathering
analysis
creation
review-ready pack
```

→ **ChatGPT Work**

### Distinction với Chat

```text
Chat:
"Help me work through this."

Work:
"Take this goal and carry the work through."
```

---

# 6. Codex — khi nào phù hợp?

Codex phù hợp với software-engineering workflow.

Clues:

```text
code review
testing
bug fixing
refactoring
modernization
migration
PR preparation
repository work
```

### Knowledge Check example

> An engineering team wants to reduce code review, testing, and modernization bottlenecks.

→ **Codex**

Mental model:

```text
Issue / codebase
→ investigate
→ change code
→ test
→ review-ready output
```

---

# 7. API-built application/process — khi nào phù hợp?

API route phù hợp khi AI phải được:

- embedded inside a product;
- integrated into a business process;
- given custom UX;
- connected to app state/data;
- triggered programmatically;
- made part of a customer-facing experience.

### Knowledge Check example

> A customer-facing onboarding flow needs personalized guidance embedded inside the product.

Key clue:

```text
customer-facing
embedded inside the product
```

→ **An application or process built with the API**

### Vì sao không Chat?

Vì user cần trải nghiệm **inside the product**, không phải rời app để mở ChatGPT.

---

# 8. Combined solution — khi nào cần nhiều surface?

Một customer có thể có nhiều user group hoặc workflow khác nhau.

### Knowledge Check example

> Employees need a workspace, and the customer-facing product also needs embedded intelligence.

Ở đây có:

```text
Employees
→ internal workspace

Customers
→ embedded product intelligence
```

Một surface không giải quyết cả hai tốt.

→ **Combined solution using more than one surface**

---

# 9. Decision tree

```text
Is this primarily software engineering?
├─ Yes → Codex
└─ No
   ↓
Does the user want to delegate a multi-step knowledge task
and receive a finished artifact?
├─ Yes → ChatGPT Work
└─ No
   ↓
Is the AI experience embedded inside a customer/product process?
├─ Yes → API-built application/process
└─ No
   ↓
Is the user iteratively exploring, drafting, refining?
├─ Yes → ChatGPT Chat
└─ No
   ↓
Do multiple workflow/user groups require different interaction models?
├─ Yes → Combined solution
└─ Continue routing / discovery
```

---

# 10. Surface selection is not just feature matching

Một task có thể technically làm được ở nhiều surfaces.

Ví dụ:

> Draft a customer response.

Có thể làm bằng:

- Chat;
- Work;
- API;
- Agent.

Câu hỏi không phải:

```text
"Can this surface draft?"
```

Mà là:

```text
"Which interaction model best fits this workflow?"
```

---

# 11. Workflow signals cần đọc

## Human-led vs delegated

```text
Human-led:
User stays in the loop throughout
→ Chat

Delegated:
User gives goal, AI carries out multiple steps
→ Work
```

## Engineering vs general knowledge work

```text
Repository/code workflow
→ Codex
```

## Internal vs customer-facing

```text
Internal employee work
→ Chat / Work / Codex / Agent depending on workflow

Customer-facing embedded experience
→ API
```

## One surface vs combined

```text
One user group + one interaction model
→ likely one surface

Internal + external
or distinct workflow modes
→ combined solution
```

---

# 12. Surface vs architecture

Đừng nhầm:

```text
Surface = WHERE user experiences AI
Architecture = HOW systems/data/models connect
```

Ví dụ:

```text
Surface:
API-built onboarding assistant

Architecture:
App state + customer profile + model + business rules + backend systems
```

Surface là top-level interaction choice, chưa phải full technical design.

---

# 13. Ví dụ hoàn chỉnh — Sales research

### Context

Account team spends hours preparing research and follow-up drafts.

### Option A: Chat

User asks questions one by one.

Good if:

```text
work is exploratory
human wants to steer every step
```

### Option B: Work

User delegates:

```text
Gather account context
Analyze recent activity
Prepare a meeting brief
Draft follow-up
```

Good if:

```text
goal is multi-step
deliverable is review-ready
```

### Option C: API

Good if this must appear directly inside CRM with account context auto-loaded.

Point:

> Same business problem can produce different surface choices based on workflow design.

---

# 14. Example — Frontend Developer

### Task 1

> “Giải thích component này và cùng tôi refactor từng bước.”

Could be interactive, but repository-aware engineering work strongly points to **Codex**.

### Task 2

> “Tạo weekly engineering summary từ tickets, PRs, docs và xuất report.”

→ **ChatGPT Work**

### Task 3

> “Thêm AI onboarding assistant ngay trong SaaS app.”

→ **API**

### Task 4

> “Nhân viên đọc policy và iteratively draft response.”

→ **ChatGPT Chat**

---

# 15. Common mistakes

## ❌ “Chat is default for everything”

Chat is only one interaction model.

## ❌ “Work = longer Chat”

No.

Work represents **delegated execution toward a deliverable**, not merely a long conversation.

## ❌ “API because we are developers”

Do not choose API because it is technically interesting.

Choose it when:

```text
embedded UX
custom process
programmatic orchestration
integration
```

requires it.

## ❌ “One customer = one surface”

Large customers often need combined routes.

---

# 16. Knowledge Check mapping

```text
Customer-facing onboarding embedded in product
→ API-built application/process

Engineering code review/testing/modernization
→ Codex

Finance delegates source gathering + analysis + pack creation
→ ChatGPT Work

Employees explore policies + iterative drafting
→ ChatGPT Chat
```

And:

```text
Employees need workspace
+
Customer-facing product needs embedded intelligence
→ Combined solution
```

---

# 17. Cheat Sheet

```text
CHAT
= Interact

WORK
= Delegate

CODEX
= Engineer

API
= Embed / Build

COMBINED
= Multiple interaction models
```

Another version:

```text
Explore/refine → Chat
Goal-to-deliverable → Work
Codebase workflow → Codex
Embedded customer/product workflow → API
More than one → Combined
```

---

# 18. Vocabulary

| Term | Nghĩa dễ hiểu |
|---|---|
| Surface | Nơi AI được sử dụng |
| Interactive | User chủ động trao đổi từng bước |
| Delegated work | Giao mục tiêu để AI thực hiện nhiều bước |
| Embedded | AI nằm trực tiếp trong app/process |
| Customer-facing | Hướng tới end customer |
| Internal workspace | Workspace cho employee |
| Combined solution | Dùng nhiều surface cho các workflow khác nhau |
| Programmatic | Được gọi/điều khiển bằng code/API |
| Review-ready | Gần hoàn thiện để con người review |

---

# 19. Self-check

1. Điểm khác nhau bản chất giữa Chat và Work?
2. Khi nào API mạnh hơn Chat?
3. Vì sao code review/testing/modernization route sang Codex?
4. Khi nào cần combined solution?
5. Surface khác architecture thế nào?
6. Nếu một task có thể chạy ở cả Chat và API, bạn dùng tiêu chí gì để chọn?

---

## Nguồn và mức độ grounding

### Từ Knowledge Checks bạn cung cấp
- ChatGPT Chat ↔ iterative policy exploration/drafting.
- ChatGPT Work ↔ delegated finance performance pack.
- Codex ↔ code review/testing/modernization.
- API ↔ embedded customer onboarding.
- Combined surface ↔ employee workspace + customer embedded intelligence.

### OpenAI public docs để đối chiếu sản phẩm
- ChatGPT Work: https://openai.com/chatgpt-work/
- Codex / Engineering: https://openai.com/business/solutions/engineering/
- API Platform: https://openai.com/api/
- ChatGPT Work vs Codex: https://help.openai.com/en/articles/20001275/

> Đây là study synthesis, không phải transcript PartnerU.
