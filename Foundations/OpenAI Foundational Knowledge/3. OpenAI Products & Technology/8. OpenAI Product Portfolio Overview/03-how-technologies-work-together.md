# 03 — How Technologies Work Together

> **Course:** OpenAI Foundational Knowledge  
> **Sub-course:** OpenAI Product Portfolio Overview  
> **Section:** How Technologies Work Together

---

# 1. Section objective

Sau section này, bạn cần:

- hiểu portfolio components có thể kết hợp thành solution;
- biết model, retrieval, tools, plugins, agents và enterprise controls đóng vai trò khác nhau;
- thiết kế solution theo layers;
- tránh suy nghĩ “một product giải quyết mọi thứ”.

---

# 2. Big picture

A production AI solution often looks like:

```text
User / workflow
↓
Product or custom application
↓
Model intelligence
├─ retrieval / knowledge
├─ tools / actions
├─ state / memory
└─ agent orchestration
↓
Enterprise systems
↓
Identity / security / evals / monitoring
```

Each component solves a different problem.

---

# 3. Model + prompt

Simplest composition:

```text
Prompt
+
Model
→ output
```

Good for:

- drafting;
- transformation;
- general reasoning.

Not enough for:

- private current data;
- business actions;
- durable workflow state.

---

# 4. Model + retrieval

Adds knowledge.

```text
Question
↓
Retrieve trusted sources
↓
Model
↓
Grounded answer
```

Use when system needs:

- private documents;
- source-backed answers;
- updated unstructured knowledge.

---

# 5. Model + tool

Adds live state/action.

```text
Question / goal
↓
Model decides tool needed
↓
API/tool
↓
result
↓
model
```

Examples:

- query CRM;
- create issue;
- update account.

---

# 6. Retrieval + tools

Many enterprise solutions need both.

Example support:

```text
Policy
→ retrieval

Customer account
→ tool/API
```

Agent uses both:

```text
“What should we do?”
→ policy

“What is true right now?”
→ account API
```

This distinction is extremely useful.

---

# 7. Model + structured output

If downstream software consumes output:

```text
Unstructured input
↓
Model
↓
JSON schema
↓
business logic
```

This creates a clean bridge between probabilistic AI and deterministic code.

---

# 8. Model + code

Use deterministic code for:

- math;
- validation;
- rules;
- transformations;
- control flow.

Model handles:

- interpretation;
- ambiguity;
- natural language.

Best solutions are hybrid.

---

# 9. Model + agent orchestration

Agent orchestration adds a loop:

```text
Goal
↓
Model decides next step
↓
Tool
↓
Observe
↓
Continue
```

Use when one model call is insufficient.

---

# 10. Agent + retrieval + tools

A common enterprise architecture:

```text
Agent
├─ retrieve policy
├─ query account
├─ execute action
└─ log result
```

This is the core pattern behind many agentic workflows.

---

# 11. ChatGPT + plugins/connections

For end-user work:

```text
User
↓
ChatGPT
↓
Plugin / connected business system
↓
data/action
```

This can deliver workflow integration without building full custom UI.

Use when ChatGPT is acceptable primary user surface.

---

# 12. ChatGPT + workspace agents

Organization may configure repeatable agents inside workspace.

Conceptually:

```text
Shared instructions
+ tools
+ business context
+ permissions
→ reusable team agent
```

This packages repeatable work.

---

# 13. API + MCP

Custom application can connect to external MCP servers/tools.

Conceptual:

```text
Custom app
→ OpenAI model/agent
→ MCP tool server
→ enterprise system
```

Benefits:

- standardized tool exposure;
- reusable integration.

Still requires auth/permissions.

---

# 14. API + agents SDK

A developer can use agent-oriented SDK to manage:

- tools;
- handoffs;
- orchestration;
- traces.

Application still owns:

- business logic;
- integration;
- security choices;
- deployment.

---

# 15. Agents API + cloud execution

Current OpenAI public platform includes a managed Agents API for cloud agent execution.

Conceptual value:

```text
Developer defines work
→ managed agent harness/execution
→ files/tools/subtasks
```

This can reduce infrastructure burden for long-running agents.

Exact beta/availability details should be checked when implementing.

---

# 16. Codex + repository/tool environment

Coding agent architecture:

```text
Issue/task
↓
Codex/coding agent
↓
repository
↓
commands/tests
↓
change
↓
review
```

The solution combines model intelligence with a controlled development environment.

---

# 17. ChatGPT + Codex

In current business portfolio, coding capabilities can be available within broader ChatGPT business experiences.

Portfolio lesson:

> Specialized capability can appear inside a broader product surface.

Do not assume products are isolated silos.

---

# 18. Enterprise platform + business context

Enterprise agent platforms can connect:

```text
CRM
data warehouse
internal apps
policies
```

into shared business context.

Agent execution then operates over that context with:

- permissions;
- governance;
- evaluation.

---

# 19. Enterprise platform + evaluation loops

Agent systems need continuous improvement.

Flow:

```text
Production execution
↓
trace/outcome
↓
evaluation
↓
identify failures
↓
optimize
↓
redeploy
```

This is how agent operation differs from a static chatbot demo.

---

# 20. Layer responsibility map

| Layer | Purpose |
|---|---|
| Model | intelligence |
| Prompt/instructions | task behavior |
| Retrieval | unstructured knowledge |
| Tool/API | live data/action |
| Structured output | integration |
| Agent loop | multi-step coordination |
| Product UI | user experience |
| Plugins/MCP | system connectivity |
| Evals | evidence |
| Governance | enterprise control |

No single layer replaces all others.

---

# 21. Example — Employee HR assistant

```text
Employee
↓
ChatGPT or internal app
↓
identity
↓
HR retrieval
↓
model
↓
answer + source
```

Add agent only if actions needed:

```text
submit leave request
update HR system
```

---

# 22. Example — Sales agent

```text
Sales request
↓
Agent
├─ CRM tool
├─ account research
├─ approved content retrieval
└─ email/calendar tool
↓
brief / action
```

Need:

- permissions;
- approval for outreach if appropriate;
- logging.

---

# 23. Example — Finance analysis

```text
User
↓
ChatGPT/custom app
↓
data connector/tool
↓
analysis
↓
structured table + explanation
```

No agent loop required if task is one-shot analysis.

---

# 24. Example — Coding

```text
Developer task
↓
Codex
↓
repo + terminal/test tools
↓
iterative coding loop
↓
human review
```

This is a specialized agentic workflow.

---

# 25. Technology composition principle

Ask for each requirement:

```text
Need knowledge?
→ retrieval

Need live state?
→ tool

Need action?
→ write tool + permissions

Need multiple adaptive steps?
→ agent

Need reusable end-user experience?
→ product/workspace

Need custom UX?
→ API

Need scale/governance?
→ enterprise controls/platform
```

---

# 26. Avoid technology stacking for its own sake

Bad architecture:

```text
RAG + agent + multi-agent + MCP
```

just because each sounds modern.

Better:

> Add each component only when it solves a defined requirement.

Complexity is a cost.

---

# 27. Partner lens

Good solution story:

```text
Workflow need
→ component role
→ integration
→ control
→ evidence
```

Not:

> “We will combine all OpenAI technologies.”

Customer should understand why each component exists.

---

# 28. Common mistakes

1. RAG when model already has enough context.
2. Agent when one tool call works.
3. Plugin when custom integration is required.
4. Custom API when workspace configuration is enough.
5. Forget identity across tool chain.
6. Assume business context = unrestricted data access.
7. No eval/monitoring layer.
8. Stack technologies without requirement.

---

# 29. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Composition | Kết hợp các công nghệ |
| Orchestration | Điều phối |
| Retrieval layer | Lớp lấy knowledge |
| Tool layer | Lớp action/API |
| Execution environment | Môi trường thực thi |
| Business context | Context doanh nghiệp |
| Trace | Dấu vết execution |
| Evaluation loop | Vòng đánh giá/cải tiến |
| Connectivity | Khả năng kết nối |
| Technology stack | Tập các công nghệ |

---

# 30. Section recap

Think in layers:

```text
MODEL
→ intelligence

RETRIEVAL
→ knowledge

TOOLS
→ live state/actions

AGENT
→ multi-step coordination

PRODUCT/API
→ user/builder surface

PLUGINS/MCP
→ connectivity

EVALS/GOVERNANCE
→ trust and operations
```

Core rule:

> **Compose technologies because the workflow requires them—not because the portfolio contains them.**

---

# 31. Self-check

1. Retrieval và tool khác nhau về information source thế nào?
2. Khi nào one model call đủ?
3. Agent orchestration thêm gì?
4. MCP/plugin đóng vai trò gì?
5. Hãy thiết kế stack cho support workflow.
6. Tại sao evals nên là một layer riêng?
