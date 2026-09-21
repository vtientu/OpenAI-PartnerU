# 02 — What the OpenAI API Is

> **Course:** OpenAI Foundational Knowledge  
> **Course:** API Essentials  
> **Section:** What the OpenAI API is
>
> **Freshness note:** Aligned with official OpenAI public materials available on **21 September 2026**. Exact model names, prices, endpoints and features can change.
>
> **PartnerU note:** Optimized study guide; not a verbatim transcript.

---

# 1. Section objective

Sau section này, bạn cần:

- định nghĩa OpenAI API;
- hiểu OpenAI API khác ChatGPT như thế nào;
- hiểu model + tools + agents capabilities ở API platform;
- biết conceptual request flow;
- hiểu pricing/usage/security ở mức solution fundamentals;
- biết facts nào phải verify before customer commitment.

---

# 2. Official high-level definition

OpenAI Academy currently describes the OpenAI API as:

> programmable access to OpenAI models for developers building custom applications, workflows and systems.

The API can support applications that:

- generate text/images;
- analyze content;
- work with code;
- reason through problems;
- interact with tools.

Mental model:

```text
OpenAI intelligence
↓
API
↓
Developer-defined application
```

---

# 3. ChatGPT vs OpenAI API

This distinction is foundational.

## ChatGPT

```text
User
→ OpenAI product
→ AI work
```

OpenAI owns the product UI/experience.

## OpenAI API

```text
User/event
→ customer's application
→ customer's backend
→ OpenAI API
→ AI capability
```

Customer/partner owns more application design.

---

# 4. Why API exists

A company may want AI:

- inside its mobile app;
- inside its website;
- inside support backend;
- in automated document pipeline;
- inside business process;
- inside agent.

Users may never see an OpenAI UI.

API makes this possible.

---

# 5. Platform mental model

Current OpenAI API public page describes the platform around:

```text
MODELS
advanced intelligence + multimodal capability

BUILD
Responses API / Agents SDK / realtime

GROUND
web search / file search / MCP context

ACT
connections to business systems
```

This means modern API usage extends beyond:

> “send prompt, get text.”

---

# 6. Model capability layer

At the durable level, OpenAI API offers categories such as:

- general-purpose reasoning/text;
- multimodal understanding;
- coding;
- image;
- realtime/audio;
- embeddings.

Exact names change.

Partner rule:

```text
Capability first
→ exact model second
```

---

# 7. Responses API — conceptual role

Current OpenAI platform positions the Responses API as a primary building block for model/tool workflows.

At a conceptual level, it can support:

```text
Input
+ model
+ instructions
+ tools/context
→ response
```

Do not memorize exact parameters in an Essentials course.

Understand its role:

> one programmable surface for building model-driven applications.

---

# 8. Agent workflows

Current OpenAI API platform supports building agent workflows with agent-oriented SDK/API capabilities.

Agent architecture:

```text
Goal
↓
model
↓
tools
↓
state/context
↓
actions
↓
completion
```

The API is the builder path.

ChatGPT workspace agents are a configured product path.

---

# 9. Built-in tools

Current API platform publicly highlights tools such as:

- web search;
- file search;
- remote MCP servers.

Conceptual purpose:

```text
Model alone
→ learned/general capability

Model + tools
→ external/current/private context or actions
```

Exact supported tool set should be verified in current docs.

---

# 10. Tool calling

A custom application can expose functions/tools.

Example:

```text
get_order_status(order_id)
```

Flow:

```text
User asks
↓
model identifies tool
↓
your application executes tool
↓
tool result
↓
model continues
```

This is how AI interacts with business systems.

---

# 11. Grounding

If application needs organization knowledge:

```text
Question
→ file search/retrieval
→ trusted context
→ model
→ answer
```

The API can therefore support RAG/grounded applications.

---

# 12. Realtime / voice

Current OpenAI platform also supports realtime/voice experiences.

Concept:

```text
Audio
↔
AI
```

Use cases:

- voice assistant;
- customer service;
- realtime interaction.

Latency becomes important.

---

# 13. Image/media applications

API can support image-related workflows.

Examples:

- image creation;
- visual understanding depending on model/capability.

A custom product can embed this capability directly.

---

# 14. Embeddings / semantic applications

Embedding models support numerical representations useful for:

- semantic search;
- retrieval;
- clustering;
- recommendation.

This is another API use path beyond chat generation.

---

# 15. Authentication

Application needs API credentials.

Architecture:

```text
Frontend
↓
customer backend
↓
OpenAI API
```

Backend protects key and applies:

- auth;
- business rules;
- logging;
- limits.

Do not expose server API secret in public client code.

---

# 16. API project/organization management

Current OpenAI API platform includes project/organization controls for:

- access;
- usage;
- spend;
- administration.

At enterprise scale, AI API usage becomes operational infrastructure.

---

# 17. Usage-based economics

API is typically usage-based.

Cost depends on factors such as:

- model;
- amount of input;
- amount of output;
- tool/service usage;
- processing mode.

Exact pricing changes and must be checked on official pricing pages.

Do not hard-code old price in solution notes.

---

# 18. Tokens — conceptual reminder

Text-model usage is often measured in tokens.

Token is not exactly a word.

Longer:

- prompts;
- documents;
- responses

can affect cost and latency.

---

# 19. Context

API request may contain:

- instructions;
- user input;
- history;
- retrieved documents;
- tool results.

Context helps model perform task.

But:

```text
more context
≠ automatically better
```

Use relevant context.

---

# 20. Structured output

For application integration:

```text
Model
→ structured object/schema
→ deterministic software
```

This is often better than parsing free-form prose.

Example:

```json
{
  "category": "billing",
  "priority": "high",
  "needs_human": false
}
```

---

# 21. Streaming

Interactive products may stream output as it is generated.

Benefits:

- faster perceived response;
- better chat UX.

Batch/automation workflows may not need streaming.

---

# 22. Batch processing

Some workloads do not need realtime response.

Examples:

- classify 100,000 records;
- summarize archives;
- offline evaluation.

A batch processing path may improve cost/throughput depending on current platform options.

Verify current support/details.

---

# 23. Reliability concerns

Production API application needs:

- error handling;
- timeout;
- retry;
- rate-limit handling;
- observability;
- fallback.

Model/API call is one dependency inside your product.

---

# 24. API output is probabilistic

Traditional API:

```text
GET customer 123
→ exact record
```

Generative AI API:

```text
instruction
→ probabilistic model output
```

Therefore application also needs:

- evals;
- validation;
- guardrails.

This is a key difference from many traditional APIs.

---

# 25. API + deterministic software

Best architecture often combines:

```text
AI
→ interpretation/reasoning

Code
→ hard rules/calculation/control
```

Example:

```text
AI classifies expense description
↓
code checks maximum amount
↓
API writes approved record
```

Don't make model enforce every business rule.

---

# 26. Business data privacy

OpenAI currently states that data from the API platform is **not used to train models by default**.

Current business-data materials also describe enterprise/API security controls such as:

- encryption;
- retention controls for qualifying organizations;
- data residency options;
- access/admin controls.

Exact eligibility/configuration must be verified for customer requirements.

---

# 27. Data retention

Never assume one retention setting applies to all customers/endpoints.

Ask:

- product;
- endpoint;
- organization eligibility;
- required retention posture.

Then verify official documentation.

---

# 28. Regional processing

Some customers may require:

- data residency;
- in-region processing.

Current OpenAI business materials describe regional options for eligible API customers on supported endpoints.

Again:

> verify exact current availability.

---

# 29. Current OpenAI API positioning

As of **21 September 2026**, the public API page emphasizes:

```text
Build
Ground
Act
```

This is useful because it captures the platform's evolution:

```text
Generate text
↓
Build AI applications
↓
Ground them in context
↓
Connect them to systems/actions
↓
Build agents
```

---

# 30. Example — Product assistant

```text
Customer app
↓
backend
↓
OpenAI API
├─ model
├─ file search
└─ business tool
↓
answer/action
```

Customer experiences AI inside brand/product.

---

# 31. Example — Document automation

```text
Uploaded invoice
↓
backend
↓
OpenAI API
↓
structured extraction
↓
validation
↓
ERP API
```

The API becomes a processing component.

---

# 32. Example — Agent

```text
Goal
↓
custom agent
├─ OpenAI API reasoning
├─ company knowledge
├─ CRM tool
└─ email tool
↓
completed workflow
```

API is one foundation for custom agent development.

---

# 33. Partner lens

OpenAI API solution means customer owns more decisions around:

- UX;
- application logic;
- integration;
- tool permissions;
- evaluation;
- monitoring.

This provides flexibility but increases implementation responsibility.

---

# 34. Common mistakes

1. API = ChatGPT.
2. ChatGPT plan includes API usage automatically.
3. One API call = complete production solution.
4. API output behaves like deterministic database API.
5. Model knows customer's private/live data automatically.
6. API key in frontend.
7. API data controls assumed without checking.
8. Exact model/pricing facts quoted from memory.

---

# 35. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| OpenAI API | Developer platform truy cập OpenAI capability |
| Responses API | API surface cho model/tool responses |
| Agent workflow | Workflow nhiều bước có AI điều phối |
| Built-in tool | Tool platform cung cấp |
| Tool calling | Model yêu cầu gọi function/tool |
| Grounding | Neo output vào source/context |
| Realtime | Tương tác thời gian gần thực |
| Embedding | Vector representation |
| Structured output | Output theo schema |
| Streaming | Trả output dần |
| Token | Đơn vị model xử lý/usage |
| Project | Scope quản lý access/usage API |

---

# 36. Section recap

OpenAI API is:

```text
programmable access
to
models + tools + agent capabilities
for
custom products/workflows
```

Distinguish:

```text
ChatGPT
→ OpenAI-built end-user product

API
→ developer building block
```

Core rule:

> **Use the API when AI capability needs to become part of a customer-owned application, system or automated workflow.**

---

# 37. Self-check

1. OpenAI API khác ChatGPT thế nào?
2. Responses API đóng conceptual role gì?
3. Built-in tools giúp gì?
4. Structured output useful khi nào?
5. Tại sao AI API needs evals more than a deterministic lookup API?
6. What API data facts must be verified for an enterprise customer?
