# 01 — Understanding the OpenAI Portfolio

> **Course:** OpenAI Foundational Knowledge  
> **Course group:** Core AI Concepts & Solution Patterns  
> **Sub-course:** OpenAI Product Portfolio Overview  
> **Section:** Understanding the OpenAI Portfolio
>
> **Freshness note:** OpenAI product names and packaging evolve quickly. This guide was aligned with OpenAI public sources available on **21 September 2026**. Treat exact plan names, feature availability, model IDs and pricing as facts to re-check before a customer commitment.
>
> **PartnerU note:** We currently have the section title, not the internal PartnerU transcript. This is therefore an optimized study guide based on public OpenAI materials—not a verbatim PartnerU transcript.

---

# 1. Section objective

Sau section này, bạn cần:

- nhìn OpenAI portfolio như một **system of capabilities**, không phải danh sách product rời rạc;
- phân biệt end-user products, developer platform, model layer, agent layer và enterprise platform;
- hiểu product surface nào phù hợp với employee productivity, custom applications, coding, agents và enterprise operations;
- tránh nhầm ChatGPT subscription với API platform;
- biết exact names/features nào cần verify tại thời điểm solutioning.

---

# 2. Big picture

Một mental model tốt cho OpenAI portfolio:

```text
┌─────────────────────────────────────────────┐
│ USER / BUSINESS EXPERIENCES                 │
│ ChatGPT • ChatGPT Work • Codex • Workspace │
├─────────────────────────────────────────────┤
│ AGENT / WORKFLOW CAPABILITIES               │
│ Agents • tools • long-running execution     │
├─────────────────────────────────────────────┤
│ DEVELOPER PLATFORM                          │
│ API • Responses • Agents API/SDK • realtime │
├─────────────────────────────────────────────┤
│ MODEL & MEDIA CAPABILITIES                  │
│ reasoning • text • code • vision • audio    │
│ image • embeddings                          │
├─────────────────────────────────────────────┤
│ CONNECTION / BUSINESS CONTEXT               │
│ plugins • MCP • file/web/data connections   │
├─────────────────────────────────────────────┤
│ ENTERPRISE GOVERNANCE / OPERATIONS          │
│ identity • permissions • security • evals   │
│ audit • monitoring • enterprise platforms   │
└─────────────────────────────────────────────┘
```

OpenAI portfolio không nên học như:

> “Product A làm X, Product B làm Y.”

Nên học như:

> “Customer muốn **ai** làm **workflow nào**, cần **capability, context, tools, actions và governance** gì?”

---

# 3. Portfolio layer 1 — ChatGPT

ChatGPT là end-user AI experience.

User có thể tương tác trực tiếp với AI để:

- write;
- research;
- analyze;
- code;
- create;
- reason;
- work with files;
- use connected tools/capabilities.

Business value:

```text
Employee
→ direct AI access
→ productivity / capability expansion
```

ChatGPT phù hợp khi user cần **general-purpose AI workspace** mà không phải build một custom application từ đầu.

---

# 4. ChatGPT for organizations

Business/enterprise workspace adds organizational controls around user access and work.

Conceptually:

```text
Individual AI experience
+
workspace
+
admin controls
+
business data/privacy controls
+
shared capabilities
```

Current OpenAI public business materials position ChatGPT as a broad business AI environment across functions such as:

- finance;
- analytics;
- sales;
- marketing;
- operations;
- engineering;
- design;
- security.

Exact plan packaging should be verified at time of sale.

---

# 5. ChatGPT Work

Current OpenAI business materials describe **ChatGPT Work** as a work-oriented experience for substantial tasks such as:

- creating docs/decks/spreadsheets;
- working across files and tools;
- automating tasks;
- handling longer-running work.

Conceptual distinction:

```text
Chat
→ answer / collaborate

Work
→ carry substantial work through to completion
```

For PartnerU, the durable lesson is:

> OpenAI portfolio includes both **interactive assistance** and **work execution** surfaces.

---

# 6. Codex

Codex is OpenAI's coding-oriented capability/product experience.

Typical developer workflows:

```text
Understand codebase
→ implement
→ test
→ debug
→ review
→ document
```

Codex is relevant when the primary user/workflow is software engineering.

Important:

> Coding use case does not automatically mean “build a custom AI app.”

A developer-facing product like Codex may be the faster path if the workflow already fits it.

---

# 7. API Platform

OpenAI API Platform is for builders who need AI inside their own application or workflow.

Mental model:

```text
Your application
→ OpenAI API
→ model / tools / agent capability
→ your business logic
```

Use API when customer needs:

- custom UX;
- embedded AI feature;
- proprietary workflow;
- backend automation;
- custom data/tool integration;
- customer-facing AI product.

ChatGPT and API are separate product surfaces and may have separate commercial/billing models.

---

# 8. Model layer

The API platform exposes model capabilities.

At a durable level, think:

- general-purpose reasoning/text;
- coding;
- multimodal understanding;
- image generation;
- speech/audio/realtime;
- embeddings/retrieval-related models.

Exact model families change.

Rule:

> **Remember capability categories; verify exact model names.**

---

# 9. Responses / application API layer

OpenAI's platform includes APIs designed to combine model intelligence with tools and multi-step application behavior.

A builder may need:

```text
Input
+ model
+ tools
+ context
+ structured output
+ state
```

This sits between raw model access and fully built agent system.

---

# 10. Agents layer

OpenAI provides agent-oriented capabilities for workflows that require:

- multiple steps;
- tools;
- files;
- code execution;
- long-running tasks;
- controlled environments;
- state/context.

Current public portfolio includes agent APIs/SDK capabilities and workspace/product agent experiences.

Durable concept:

```text
Model call
→ one intelligent step

Agent system
→ coordinates intelligent work across steps/tools
```

---

# 11. Workspace agents

OpenAI public materials currently describe shared/workspace agents that organizations can configure for repeatable work across team knowledge and tools.

Value:

- package best practices;
- reuse workflows;
- share across teams;
- operate under organization controls.

This is a **configure/product path** rather than always building from scratch.

---

# 12. Plugins and business connections

OpenAI business portfolio includes ways to connect AI to business systems/data.

Current public materials describe **plugins** and connectivity approaches including MCP-based integrations.

Examples of connected systems can include:

- CRM;
- data warehouses;
- collaboration tools;
- developer tools;
- finance systems.

Core value:

```text
AI without company context
→ generic capability

AI + company systems
→ workflow-specific capability
```

---

# 13. MCP — conceptual role

**MCP (Model Context Protocol)** is an integration approach that can expose tools/context to AI systems using a common protocol.

Partner-level takeaway:

> MCP can reduce bespoke integration friction, but it does not remove the need for permissions, security and tool governance.

MCP is not itself an agent.

---

# 14. OpenAI Frontier

Current OpenAI public materials describe **OpenAI Frontier** as an enterprise platform for operating AI agents with:

- business context;
- enterprise system integration;
- agent execution;
- evaluation/optimization loops;
- security/governance;
- permissions/audit.

Conceptually, Frontier sits at:

```text
Enterprise agent operations layer
```

rather than simply “a model.”

---

# 15. OpenAI Presence

Current public materials describe **OpenAI Presence** as an enterprise product for production voice/chat agent workflows.

Durable portfolio lesson:

> Some solutions may be delivered as specialized managed enterprise agent products rather than customer-built API applications.

Availability and exact packaging should be verified.

---

# 16. Developer tools vs end-user products

This distinction is critical.

## End-user surface

Examples conceptually:

```text
ChatGPT / Work / Codex / workspace agents
```

Users work directly with AI.

## Builder surface

```text
API / Responses / Agents APIs/SDK / model endpoints
```

Developers create application behavior.

Customer may need one or both.

---

# 17. Portfolio as build-vs-configure spectrum

Think of portfolio as:

```text
CONFIGURE / USE
ChatGPT
Work
Codex
Workspace agents
      ↓
CUSTOMIZE / CONNECT
Plugins / MCP / business context
      ↓
BUILD
API
Responses
Agents APIs/SDK
      ↓
OPERATE AT ENTERPRISE SCALE
Enterprise agent platforms / governance
```

This is a study mental model—not a rigid product hierarchy.

---

# 18. One customer can use multiple portfolio surfaces

Example enterprise:

### Employees
Use ChatGPT.

### Developers
Use Codex.

### Product team
Builds embedded AI with API.

### Support
Uses an agent workflow.

### IT/security
Manages identity, permissions, governance.

Portfolio is complementary, not mutually exclusive.

---

# 19. Product surface vs underlying capability

Same model capability can appear in:

- ChatGPT;
- Codex;
- custom API app;
- workspace agent;
- enterprise agent workflow.

Therefore:

```text
Capability
≠
Product surface
```

Partner must know both layers.

---

# 20. Current-model names are not the portfolio

OpenAI may release new model families frequently.

A product portfolio overview should not collapse into:

> “Which GPT number exists today?”

Model name is one implementation detail.

More durable:

```text
What capability?
What product/workflow surface?
What integration?
What governance?
```

---

# 21. Business privacy / enterprise controls

Current public OpenAI business materials state that organization data across eligible business products/API is not used for training by default.

Exact:

- retention;
- residency;
- compliance;
- security;
- plan availability

must be verified for the specific product/customer requirement.

Do not transfer one product's controls to another without checking.

---

# 22. A portfolio selection mental model

Ask in order:

```text
1. Who is the user?
2. Is this direct AI usage or embedded AI?
3. Is workflow general or highly custom?
4. Does it need business data?
5. Does it need actions/tools?
6. Does it require multi-step agency?
7. What governance is needed?
8. Build, configure, or managed solution?
```

---

# 23. Example — Company-wide knowledge work

Need:

- broad employee use;
- writing/research/analysis;
- company controls.

Likely starting path:

```text
ChatGPT business/enterprise workspace
```

Then add:

- connections/plugins;
- shared/workspace agents;
- governance

as needed.

---

# 24. Example — AI feature in customer SaaS

Need:

- AI inside company's own product;
- custom UX;
- proprietary workflow.

Likely path:

```text
API platform
→ models
→ tools/data
→ app backend
→ evaluations
```

---

# 25. Example — Coding productivity

Need:

- developer workflow;
- repository work;
- code execution/testing.

Potential path:

```text
Codex / coding-oriented agent capability
```

rather than generic chat alone.

---

# 26. Example — Long-running enterprise agent

Need:

- multi-step work;
- business systems;
- durable context;
- audit/governance.

Potential path may involve:

- Agents API/SDK;
- workspace agents;
- enterprise agent platform;

depending on build-vs-buy and control requirements.

---

# 27. Partner lens

Do not ask:

> “Which OpenAI product can we sell?”

Ask:

> “What workflow is the customer trying to improve?”

Then map to portfolio.

Partner value:

```text
Customer problem
→ capability
→ product/technology path
→ deployment evidence
```

---

# 28. Common mistakes

1. ChatGPT = API.
2. Model = product.
3. Agent = model.
4. Codex = generic business assistant.
5. Every workflow needs custom API development.
6. Every workflow can be solved only inside ChatGPT.
7. Product plan features assumed from memory.
8. Exact model names learned as permanent portfolio architecture.
9. Enterprise platform controls assumed to exist identically across every surface.

---

# 29. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Portfolio | Danh mục sản phẩm/capability |
| Product surface | Bề mặt/trải nghiệm sản phẩm |
| End-user product | Product người dùng sử dụng trực tiếp |
| Developer platform | Nền tảng cho developer build |
| Model layer | Lớp model capability |
| Agent layer | Lớp agent/workflow execution |
| Business context | Context/dữ liệu doanh nghiệp |
| Plugin | Integration đóng gói |
| MCP | Model Context Protocol |
| Managed service | Dịch vụ được provider vận hành |
| Embedded AI | AI nhúng vào product |
| Workspace | Không gian làm việc tổ chức |
| Governance | Quản trị/kiểm soát |

---

# 30. Section recap

Portfolio mental model:

```text
People use AI
→ ChatGPT / Work / Codex

Teams configure reusable work
→ workspace agents / plugins

Developers build
→ API / agent APIs / SDKs

Systems connect
→ tools / MCP / enterprise data

Organizations operate at scale
→ governance / enterprise agent platform
```

Core rule:

> **Learn the portfolio as capability + workflow paths, not a list of brand names.**

---

# 31. Self-check

1. ChatGPT và API Platform khác nhau thế nào?
2. Product surface và model capability khác nhau ra sao?
3. Khi nào Codex có thể là better path than custom build?
4. Plugins/MCP đóng vai trò gì?
5. Workspace agent và custom API agent khác nhau về build path thế nào?
6. Tại sao exact plan/model names cần verify?
