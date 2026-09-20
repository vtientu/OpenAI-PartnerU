# 03. Identify Capability, Architecture, and Operating Requirements

> Course: **OpenAI Consultative Solutions Practitioner – Foundations**  
> Sub-course: **Mapping Solutions & Advancing the Opportunity**  
> Section: **Identify capability, architecture, and operating requirements**

---

## 1. Mục tiêu

Sau khi đã chọn được một **likely surface**, ta phải hỏi:

> “Solution cần những điều kiện gì để thực sự hoạt động?”

Section này phân tách ba lớp:

```text
CAPABILITY
What must it do?

ARCHITECTURE
What must it connect to / depend on?

OPERATING MODEL
How must it run, be controlled, reviewed and owned?
```

Mục tiêu không phải design full system.

Mục tiêu là **identify requirements strong enough to test credibility**.

---

# 2. Capability requirements

Capability = solution phải có khả năng gì.

Ví dụ:

```text
retrieve information
reason over context
summarize
draft
classify
extract structured data
use tools
take actions
check system status
escalate
request approval
schedule work
```

### Knowledge Check example

> AI needs to check order status, draft a reply, escalate exceptions, and ask for approval.

Đây là strong clue cho:

→ **Capability or architecture requirement**

Vì câu hỏi đang mô tả **what the solution must do**.

---

# 3. Architecture requirements

Architecture = solution cần kết nối với gì và data/system flow ra sao.

Questions:

```text
Where does context live?
How is it retrieved?
What identity is used?
What permissions apply?
What systems must be called?
Where is output written?
Is access real-time?
What APIs/connectors exist?
```

Key elements:

```text
Data sources
Systems
Integrations
Identity
Permissions
Tools/actions
State
Latency
Output destination
```

---

# 4. Operating requirements

Operating requirements = solution sẽ được vận hành và kiểm soát như thế nào.

Examples:

```text
human review
approval checkpoints
escalation
monitoring
governance
auditability
ownership
quality evaluation
access controls
incident handling
change management
```

Question:

> “Even if it technically works, can the organization operate it responsibly and reliably?”

---

# 5. Deployment vs capability

Một distinction rất quan trọng:

```text
Capability:
What can it do?

Deployment:
Where/how is it run and who operates it?
```

### Knowledge Check example

> After hosted controls are evaluated, the customer requires self-managed execution and will operate the model.

Clues:

```text
self-managed
customer operates the model
```

→ **Deployment and operating model; open-weight consideration**

Không phải capability.

---

# 6. Open-weight consideration

OpenAI public docs describe open-weight models as models that can run on infrastructure the customer controls or via hosting providers.

Trong routing logic, open-weight có thể trở nên relevant khi customer requirement mạnh về:

```text
self-managed execution
on-prem/private infrastructure
data residency/control
custom operational ownership
```

Nhưng principle quan trọng là:

> **Evaluate hosted options and actual requirements first; do not assume self-managed is automatically better.**

Knowledge Check wording itself emphasizes:

```text
after hosted controls are evaluated
```

Nghĩa là route phải driven by requirement, không bởi preference mơ hồ.

---

# 7. Workspace Agent as capability/architecture pattern

Knowledge Check:

> A Workspace Agent that uses apps, actions, schedules, and approvals

Clues:

```text
apps
actions
schedules
approvals
```

Trong decision-layer exercise, đây được route mạnh nhất vào:

→ **Capability or architecture**

Vì nó mô tả solution composition:

```text
trigger
process
tools/systems
actions
controls
```

OpenAI public docs similarly describe workspace agents around repeatable workflows, tools/apps, schedules, write actions and approvals.

---

# 8. Capability ↔ Architecture ↔ Operating Model

Một solution mạnh cần cả ba.

Example: Order support agent

### Capability

```text
Check order status
Draft response
Detect exception
Escalate
Ask for approval
```

### Architecture

```text
Ticketing system
Order system
Customer identity
Permissioned data
Tool/action interfaces
```

### Operating

```text
Approval for sensitive write action
Escalation owner
Monitoring
Audit log
Quality review
```

Nếu thiếu một lớp:

```text
Capability works
+ Architecture works
- Operating owner
→ route still incomplete
```

---

# 9. Technical requirements vs business requirements

Do not let requirements become purely technical.

Example:

```text
Need low latency
```

Why?

Maybe:

```text
Technician needs near-real-time guidance from live equipment data.
```

Business/workflow reason drives technical requirement.

Better requirement chain:

```text
Workflow need
→ Technical requirement
→ Validation method
```

Example:

```text
Near-real-time operational decision
→ Latency + live integration requirement
→ Technical validation
```

---

# 10. Data requirements

Data readiness often determines route credibility.

Ask:

```text
What data is needed?
Is it authoritative?
Is it permissioned?
Is it current?
Is it structured/unstructured?
Can the model access it?
Who is allowed to see it?
Can outputs cite/trace sources when needed?
```

For sensitive data:

```text
data
+ governance
+ review
```

must be considered together.

---

# 11. Identity and permissions

A system can be technically connected yet unusable if identity is wrong.

Example:

> Proposed solution depends on ticketing integration, permissioned data, and customer identity rules.

This is a strong reason for:

→ **Technical handoff**

because architecture now depends on:

```text
who is the user?
what can they read?
what can they write?
which system identity acts?
```

---

# 12. Latency and live-system integration

Some workflows tolerate asynchronous work.

Others do not.

Example:

> Near-real-time guidance from live equipment data.

This creates a technical question:

```text
Can required data be accessed in time?
Can solution respond within workflow latency?
```

→ may require **technical validation**

Latency is not just performance optimization.

It can be **workflow feasibility**.

---

# 13. Approval and review requirements

Approval can be:

- capability (system can ask for approval);
- operating control (who must approve);
- governance requirement (when approval is mandatory).

Thus context matters.

Example:

```text
"AI must ask for approval before a write action."
```

Capability side:

```text
can request approval
```

Operating side:

```text
which actions require it?
who approves?
how logged?
```

---

# 14. Requirement discovery framework

```text
1. TASK
   What must AI do?

2. CONTEXT
   What data does it need?

3. SYSTEMS
   What must it connect to?

4. IDENTITY
   Who/what acts?

5. PERMISSIONS
   What can be read/written?

6. LATENCY
   How fast must it respond?

7. CONTROL
   What requires review/approval?

8. OWNERSHIP
   Who operates and monitors?

9. DEPLOYMENT
   Hosted or customer-managed?

10. VALIDATION
   What must be tested before progression?
```

---

# 15. Example — Manufacturing handoff

Workflow:

```text
Technicians create shift handoff notes.
```

### Capability

```text
summarize equipment events
draft handoff
flag anomalies
```

### Architecture

```text
live equipment data
maintenance logs
identity
permissioned source access
```

### Operating

```text
technician review
escalation for high-risk anomaly
approved source list
```

### Technical validation trigger

If notes need near-real-time live data:

```text
latency + integration
→ validate technically
```

---

# 16. Frontend Developer analogy

Feature:

> AI fills parts of a checkout flow.

Capability:

```text
Generate recommendation
Read current cart
Suggest action
```

Architecture:

```text
Frontend state
Backend inventory
User identity
Permissions
API calls
```

Operating:

```text
User confirms purchase
High-risk actions require explicit confirmation
Logs/monitoring
```

Lesson:

> “The model can generate text” is only a tiny part of the solution.

---

# 17. Knowledge Check signals

```text
self-managed execution
customer operates model
→ deployment/operating model

check order + draft + escalate + approval
→ capability/architecture

apps + actions + schedules + approvals
→ capability/architecture

live integration + security review
→ technical validation

permissioned data + identity rules
→ technical handoff
```

---

# 18. Common mistakes

## ❌ Treat “model choice” as architecture

Architecture is broader than model.

## ❌ Assume data access

If source access is unknown, say so.

## ❌ Ignore permissions

“API available” does not mean every user can access every datum/action.

## ❌ Overdesign

At routing stage, identify critical requirements, not every component.

## ❌ Forget operating model

A technically good solution with no owner/review path is not deployment-ready.

---

# 19. Cheat Sheet

```text
CAPABILITY
= Do what?

ARCHITECTURE
= Connect to what, with what data/identity/permissions?

OPERATING
= Run/review/control by whom and how?

DEPLOYMENT
= Hosted vs customer-managed?

VALIDATION
= What must be proven before advancing?
```

---

# 20. Vocabulary

| Term | Nghĩa dễ hiểu |
|---|---|
| Capability | Khả năng solution phải có |
| Architecture | Cấu trúc kết nối data/system |
| Integration | Kết nối hệ thống |
| Identity | Danh tính dùng khi truy cập/hành động |
| Permission | Quyền read/write/action |
| Latency | Độ trễ |
| Operating model | Cách vận hành solution |
| Deployment model | Cách/nơi triển khai |
| Human-in-the-loop | Con người tham gia review/decision |
| Approval checkpoint | Điểm cần phê duyệt |
| Open-weight | Model chạy được trên hạ tầng do customer kiểm soát |
| Hosted | Được cung cấp như managed service |

---

# 21. Self-check

1. Capability khác architecture thế nào?
2. “Self-managed execution” thuộc layer nào?
3. Vì sao identity/permissions là architecture concern?
4. Approval có thể vừa là capability vừa là operating requirement như thế nào?
5. Khi nào latency trở thành validation blocker?
6. Vì sao model capability không đủ để prove deployability?

---

## Nguồn và grounding

### Từ Knowledge Checks bạn cung cấp
- Workspace Agent → capability/architecture.
- Customer-managed open-weight → deployment/operating model.
- Order status + draft + escalate + approval → capability/architecture.
- Live integration/security → technical validation.
- Permissioned data/identity → technical handoff.

### OpenAI public docs
- Workspace Agents: https://openai.com/business/workspace-agents/
- Workspace Agents Help: https://help.openai.com/en/articles/20001143
- Open-weight models: https://help.openai.com/en/articles/11870455
- API Platform: https://openai.com/api/

> Study synthesis, không phải transcript PartnerU.
