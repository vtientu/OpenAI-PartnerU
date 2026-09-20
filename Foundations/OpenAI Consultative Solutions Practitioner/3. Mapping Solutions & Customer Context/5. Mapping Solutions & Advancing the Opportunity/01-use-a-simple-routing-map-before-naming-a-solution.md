# 01. Use a Simple Routing Map Before Naming a Solution

> Course: **OpenAI Consultative Solutions Practitioner – Foundations**  
> Sub-course: **Mapping Solutions & Advancing the Opportunity**  
> Section: **Use a simple routing map before naming a solution**

---

## 1. Mục tiêu của section

Sau các bước discovery, use-case design và business value, ta đã biết khá nhiều về:

- workflow hiện tại;
- pain / friction;
- user và stakeholder;
- candidate use case;
- expected business outcome;
- evidence và assumption;
- mức độ readiness.

Bước tiếp theo **không phải** là nhìn vào catalog sản phẩm rồi chọn ngay một cái tên.

Mục tiêu của section này là học cách:

1. **định tuyến (route)** từ customer context đến hướng solution hợp lý;
2. tách các quyết định thành những **decision layer** khác nhau;
3. tránh product-first thinking;
4. chỉ “name a solution” sau khi đã hiểu workflow, user, capability, architecture và operating requirements;
5. xác định khi nào route còn quá sớm và cần discovery/validation thêm.

Mental model cốt lõi:

```text
Customer context
      ↓
Workflow + user
      ↓
What must change?
      ↓
Where should AI show up?
      ↓
What must the solution do/connect to?
      ↓
How must it run/be controlled?
      ↓
What uncertainty remains?
      ↓
Credible route
      ↓
Next step
```

> **Problem first → Route second → Product last**

---

## 2. “Routing” là gì?

Trong course này, **routing** có thể hiểu là:

> Dùng evidence từ discovery để quyết định hướng solution và bước tiếp theo phù hợp nhất, thay vì nhảy ngay vào một product name.

Routing không phải full architecture design.

Nó cũng không phải final implementation plan.

Routing là một **decision framework** giúp ta trả lời:

```text
What kind of solution path is credible here?
```

Ví dụ customer nói:

> “Đội finance mất hàng giờ chuẩn bị weekly performance pack.”

Một phản ứng product-first:

```text
→ "Hãy dùng Product X."
```

Routing tốt hơn:

```text
Workflow:
Source gathering → analysis → synthesis → produce review-ready pack

User:
Finance knowledge workers

Interaction model:
Customer wants to delegate a multi-step knowledge task

Required capabilities:
Gather context + analyze + produce finished artifact

Operating needs:
Human review before final use

Likely surface:
A delegated knowledge-work surface

Next question:
Can representative source access, output quality, and review workflow be validated?
```

Chỉ sau đó mới map sang một product surface phù hợp.

---

# 3. Vì sao “name a solution” quá sớm là nguy hiểm?

## 3.1 Product-first bias

Ta dễ nhìn thấy một feature rồi cố ép problem vào feature đó.

Ví dụ:

```text
Customer says "search is slow"
→ immediately recommend chat
```

Nhưng workflow thực tế có thể cần:

- embedded search trong application;
- automated backend retrieval;
- a workspace agent;
- custom API-based solution;
- human review;
- integration với systems.

Cùng một pain “search is slow” có nhiều route.

---

## 3.2 Capability fit không đồng nghĩa solution fit

Một model có thể:

```text
summarize
draft
classify
retrieve
reason
```

nhưng route vẫn có thể không credible nếu:

```text
data inaccessible
integration impossible
approval unclear
users will not adopt
latency unacceptable
security path unknown
business value too weak
```

Do đó:

```text
Model capability
≠
Deployable solution
```

---

## 3.3 Demo-fit khác workflow-fit

Một demo có thể rất ấn tượng.

Nhưng customer cần solution hoạt động trong:

- process thật;
- permissions thật;
- systems thật;
- data thật;
- quality bar thật;
- review path thật.

Tư duy consultative không hỏi:

> “AI có demo được không?”

mà hỏi:

> “Route này có credible trong customer context không?”

---

# 4. Bốn decision layer quan trọng

Knowledge checks trong sub-course cho thấy routing cần phân biệt ít nhất bốn lớp quyết định.

## Layer 1 — User or product surface

Câu hỏi:

> **WHERE does the user interact with AI?**

Ví dụ:

- ChatGPT Chat;
- ChatGPT Work;
- Codex;
- application/process built with API;
- nhiều surface kết hợp.

Đây là quyết định về **nơi AI xuất hiện đối với user/workflow**.

---

## Layer 2 — Capability or architecture

Câu hỏi:

> **WHAT must the solution be able to do, and what must it connect to?**

Ví dụ:

```text
retrieve information
take actions
call tools
use apps
draft
classify
escalate
ask for approval
integrate with business systems
access permissioned data
```

Một Workspace Agent có apps, actions, schedules, approvals là ví dụ của route được định hình mạnh bởi **capability/architecture**.

---

## Layer 3 — Deployment and operating model

Câu hỏi:

> **HOW / WHERE will the solution run, and WHO operates or controls it?**

Ví dụ:

```text
hosted
customer-managed
open-weight
approval checkpoints
human-in-the-loop
operational ownership
monitoring
```

Nếu customer yêu cầu **self-managed execution và tự vận hành model**, đây là dấu hiệu rõ của deployment/operating model.

---

## Layer 4 — Progression motion

Câu hỏi:

> **WHAT should happen next to advance the opportunity credibly?**

Ví dụ:

- more discovery;
- validation session;
- technical validation;
- migration discovery;
- technical handoff;
- deployment handoff;
- structured handoff.

Đây không phải product decision.

Nó là **opportunity progression decision**.

---

# 5. Simple Routing Map

Một routing map thực dụng:

```text
1. WORKFLOW
   What is happening today?

2. USER
   Who performs / owns / receives the work?

3. SURFACE
   Where should AI appear?

4. CAPABILITY
   What must AI do?

5. ARCHITECTURE
   What data, tools, systems, identity, permissions are required?

6. OPERATING MODEL
   How will review, approval, governance and ownership work?

7. READINESS / CREDIBILITY
   What is known? What is still uncertain?

8. PROGRESSION
   What is the next credible action?
```

---

# 6. Dùng routing map theo từng bước

## Step 1 — Start from evidence, not product names

Viết ra evidence:

```text
Known:
- Finance team creates a weekly performance pack.
- Work involves source gathering, analysis, and drafting.
- Final pack needs review.

Unknown:
- Which systems hold sources?
- How much time is spent?
- Which review standards matter?
```

---

## Step 2 — Identify the workflow shape

Workflow có thể là:

```text
Human-led interactive
Delegated multi-step knowledge work
Software engineering
Embedded customer experience
Repeatable agent workflow
Backend automation
```

Workflow shape là clue quan trọng cho route.

---

## Step 3 — Identify constraints

Ví dụ:

```text
Near-real-time?
Sensitive data?
Customer-managed execution?
Integration?
Approvals?
Existing system replacement?
```

Constraint có thể thay đổi route hoàn toàn.

---

## Step 4 — Select a route category

Không cần chọn implementation detail.

Ví dụ:

```text
User-facing chat
Delegated work surface
Engineering surface
Embedded API solution
Workspace agent
Customer-managed/open-weight route
Combined solution
```

---

## Step 5 — Name assumptions

Ví dụ:

```text
Assumption:
The required source systems can be connected.

Assumption:
Users will accept an AI-assisted review flow.

Assumption:
The required latency can be achieved.
```

---

## Step 6 — Choose the next action

Nếu uncertainty lớn nhất là:

```text
workflow unclear
→ continue discovery

requirements unclear
→ validation session

integration/security material
→ technical validation / technical owner

existing tool replacement
→ migration discovery

route sufficiently clear
→ structured handoff
```

---

# 7. Ví dụ hoàn chỉnh — Customer Support

Customer nói:

> “Agents mất thời gian tìm policy, trả lời chậm, và đôi lúc phải escalations.”

### Discovery evidence

```text
Pain:
Search + interpretation delays response.

User:
Support agents.

Business outcome:
Response speed and customer experience matter.
```

### Route analysis

```text
Surface?
Could be Chat, embedded support experience, or agent.

Capability?
Retrieve approved policy + draft response + flag uncertainty.

Architecture?
Policy sources + ticket context + identity/permissions.

Operating?
Agent review + escalation + governance.

Readiness?
Need representative queries and source access.

Progression?
Run validation before committing to rollout.
```

Điểm quan trọng:

> Chưa cần name product ngay ở bước đầu.

---

# 8. Example — Frontend Developer analogy

Giả sử team nói:

> “Muốn AI giúp người dùng tạo form nhanh hơn.”

Product-first thinking:

```text
Let's add a chatbot.
```

Routing:

```text
Workflow:
User configures a form inside our app.

User:
Product end user.

Surface:
Needs guidance embedded inside the product.

Capability:
Understand config state, suggest fields, maybe generate schema.

Architecture:
Must access app state and write structured form config.

Operating:
User reviews before save.

Route:
Embedded API-powered experience.

Next step:
Prototype with representative form tasks and validate UX + quality.
```

Điểm học được:

```text
Need "AI"
≠
Need "chat"
```

---

# 9. Knowledge Check signals

Các clue quan trọng từ bài tập:

```text
"ChatGPT Work for delegated knowledge work"
→ User/product surface

"customer-managed open-weight model"
→ Deployment & operating model

"Workspace Agent with apps/actions/schedules/approvals"
→ Capability/architecture

"migration discovery"
→ Progression motion
```

Một cheat signal:

```text
WHERE user works?
→ Surface

WHAT solution does/connects?
→ Capability / architecture

HOW/WHERE it runs and is controlled?
→ Deployment / operating model

WHAT happens next?
→ Progression
```

---

# 10. Evidence vs Assumption trong routing

Một route credible phải phân biệt:

## Evidence

```text
Customer uses three internal systems.
Agents need approvals for certain actions.
The current tool is being replaced.
```

## Assumption

```text
All systems have usable APIs.
Identity mapping will be simple.
Users will accept the new interaction model.
```

Nguyên tắc:

```text
Evidence supports the route.
Assumptions define the next validation step.
```

---

# 11. Common mistakes

## ❌ Start with product catalog

```text
"What can I sell?"
```

Thay bằng:

```text
"What route best fits the workflow?"
```

## ❌ Treat all AI work as chat

Some workflows are better suited to:

- Work;
- Codex;
- API;
- agents;
- combined surfaces.

## ❌ Ignore deployment

Hosted vs customer-managed may be a first-order requirement.

## ❌ Ignore progression

Sometimes the right recommendation is not a product.

It is:

```text
more discovery
validation
migration discovery
technical handoff
```

## ❌ Hide uncertainty

A credible consultant says:

```text
"This route appears plausible, but X still needs validation."
```

---

# 12. Relationship với các section trước

Before:

```text
Discovery
→ Understand pain and evidence
```

Then:

```text
Use-case design
→ Define candidate workflow changes
```

Then:

```text
Business value
→ Connect workflow change to outcomes
```

Now:

```text
Routing
→ Determine the solution path and next action
```

---

# 13. Cheat Sheet

```text
ROUTING MAP

Workflow
↓
User
↓
Surface
↓
Capability
↓
Architecture
↓
Operating model
↓
Credibility
↓
Progression
```

One sentence:

> **Route from customer evidence to a solution path; do not reverse-engineer the customer into a product.**

---

# 14. Vocabulary

| Term | Nghĩa dễ hiểu |
|---|---|
| Routing | Định tuyến từ customer context đến solution path |
| Decision layer | Lớp quyết định |
| Surface | Nơi user tương tác với AI |
| Capability | AI/solution phải làm được gì |
| Architecture | Data/system/integration structure |
| Deployment model | Cách/nơi solution được triển khai |
| Operating model | Cách solution được vận hành/kiểm soát |
| Progression motion | Bước tiếp theo để advance opportunity |
| Validation | Kiểm chứng assumption |
| Customer-managed | Customer tự vận hành hạ tầng/model |
| Open-weight | Model có weights có thể chạy trên hạ tầng do customer kiểm soát |
| Handoff | Chuyển evidence/context cho owner tiếp theo |

---

# 15. Self-check

Bạn đã hiểu section nếu có thể trả lời:

1. Vì sao không nên name product ngay sau discovery?
2. Surface khác capability/architecture thế nào?
3. Customer-managed requirement thuộc layer nào?
4. “Migration discovery” là solution hay progression motion?
5. Evidence và assumption ảnh hưởng next step thế nào?
6. Khi nào “more discovery” tốt hơn “technical handoff”?

---

## Nguồn và mức độ grounding

### Từ course context / Knowledge Checks bạn đã cung cấp
- 4 decision layers: surface, capability/architecture, deployment/operating model, progression motion.
- Examples: Workspace Agent, customer-managed open-weight model, migration discovery, ChatGPT Work.

### Tài liệu OpenAI công khai dùng để đối chiếu thuật ngữ sản phẩm
- OpenAI Workspace Agents: https://openai.com/business/workspace-agents/
- OpenAI Help – Workspace Agents: https://help.openai.com/en/articles/20001143
- OpenAI open-weight models: https://help.openai.com/en/articles/11870455
- OpenAI API Platform: https://openai.com/api/

> Đây là **study synthesis**, không phải transcript nguyên văn của PartnerU.
