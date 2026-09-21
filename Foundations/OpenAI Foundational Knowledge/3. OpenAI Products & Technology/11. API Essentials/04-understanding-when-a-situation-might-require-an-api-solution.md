# 04 — Understanding When a Situation Might Require an API Solution

> **Course:** OpenAI Foundational Knowledge  
> **Course:** API Essentials  
> **Section:** Understanding when a situation might require an API solution
>
> **Goal:** Section này là decision/qualification guide: khi nào nên route opportunity sang API/custom build, và khi nào ChatGPT/Codex/product-native path đơn giản hơn.

---

# 1. Section objective

Sau section này, bạn cần:

- nhận diện signals cho thấy API solution phù hợp;
- biết khi nào product-native solution có thể phù hợp hơn;
- phân biệt custom UX, integration, automation và scale requirements;
- dùng framework để route use case;
- biết technical/readiness questions trước khi recommend API.

---

# 2. Big picture

Don't start with:

> “Does customer want API?”

Start with:

```text
Where should AI live?
What workflow?
What data?
What action?
What customization?
What scale?
```

Then decide.

---

# 3. Strong signal 1 — AI must live inside customer's product

Example:

```text
Customer-facing SaaS
→ embedded AI assistant
```

User should stay inside company product.

This strongly points to:

```text
API solution
```

because customer controls:

- UI;
- branding;
- auth;
- workflow.

---

# 4. Strong signal 2 — Custom user experience

Need:

- custom component;
- product-specific interaction;
- branded experience;
- unique workflow UI.

ChatGPT's standard interface may not fit.

API allows custom frontend/backend.

---

# 5. Strong signal 3 — Backend automation

No human is opening ChatGPT.

Example:

```text
Invoice uploaded
↓
automatically extract
↓
validate
↓
route
```

A backend API solution is natural.

---

# 6. Strong signal 4 — Event-driven workflow

Examples:

```text
new email
new ticket
new document
new order
```

trigger AI automatically.

This requires programmable integration.

---

# 7. Strong signal 5 — High-volume processing

Example:

```text
100,000 records
```

Need repeatable programmatic processing.

Manual ChatGPT usage is not appropriate.

API/batch architecture likely required.

---

# 8. Strong signal 6 — Live business-system integration

Need:

- CRM;
- ERP;
- order system;
- proprietary database.

If company wants deeply custom orchestration:

```text
AI
↔
business systems
```

API/custom agent may be needed.

But first check whether an approved ChatGPT plugin/native integration already covers workflow.

---

# 9. Strong signal 7 — AI takes custom actions

Example:

- create ticket;
- update record;
- initiate workflow.

Need:

- tools/functions;
- permissions;
- deterministic controls.

Custom API can implement exact business actions.

---

# 10. Strong signal 8 — Proprietary application logic

Workflow includes:

- internal rules;
- custom state machine;
- proprietary algorithm;
- unique decision path.

API lets AI live inside custom business logic.

---

# 11. Strong signal 9 — Machine-readable output

Downstream application expects:

```json
{
  "decision": "...",
  "fields": {}
}
```

API + structured output can integrate directly.

---

# 12. Strong signal 10 — Programmatic scale/control

Need:

- retries;
- queues;
- observability;
- custom caching;
- per-user logic;
- dynamic routing;
- A/B testing.

API gives engineering team this control.

---

# 13. Strong signal 11 — Customer-facing identity

Application already has:

- accounts;
- roles;
- permissions.

Need AI to operate within that existing identity model.

Custom API solution integrates with customer auth.

---

# 14. Strong signal 12 — Custom agent

Need agent that:

- uses proprietary tools;
- has custom workflow;
- persists custom state;
- runs in customer's product/backend.

API/agent SDK path likely relevant.

---

# 15. When API may NOT be needed — Employee productivity

Need:

- write;
- analyze;
- research;
- general knowledge work.

Users can work directly in ChatGPT.

Better first route may be:

```text
ChatGPT Business / Enterprise
```

Custom API may add unnecessary build cost.

---

# 16. When API may NOT be needed — Coding productivity

If developers need:

- repo coding;
- bug fixes;
- refactors.

A product like Codex may be faster than building your own coding agent.

---

# 17. When API may NOT be needed — Standard connected workflow

If ChatGPT plugin/workspace capability already connects needed business system and fits user workflow, configuration may be enough.

Rule:

> **Configure before custom-build when fit is strong.**

---

# 18. When API may NOT be needed — One-off task

Example:

> “Summarize these three PDFs once.”

ChatGPT/file workflow is simpler.

No need to build an API app.

---

# 19. When API may NOT be needed — Low-volume manual task

If only one employee performs task twice per month:

A manual workflow may be economically better.

API development has cost.

---

# 20. Build vs configure spectrum

```text
USE
ChatGPT / Codex
        ↓
CONFIGURE
Projects / plugins / workspace agents
        ↓
BUILD
API/custom application
```

Move downward only when requirements justify more control.

---

# 21. API solution adds responsibility

API gives flexibility.

But customer/partner now owns more:

```text
UX
backend
authentication
business logic
tool permissions
logging
evals
monitoring
error handling
deployment
```

So API is not “better”; it is “more programmable.”

---

# 22. Decision dimension 1 — Surface

Ask:

> Where must user experience live?

### ChatGPT acceptable
→ product path.

### Customer-owned product
→ API signal.

---

# 23. Decision dimension 2 — Trigger

### Human manually starts work
Product may work.

### System event starts work
API likely.

---

# 24. Decision dimension 3 — Integration depth

### Basic file/context
Product may work.

### Deep proprietary business-system flow
API signal.

---

# 25. Decision dimension 4 — Output destination

### Human reads output
Product may fit.

### Software consumes result
API strongly fits.

---

# 26. Decision dimension 5 — Scale

### Individual/team manual usage
Product.

### High-volume programmatic workload
API.

---

# 27. Decision dimension 6 — Custom control

Need:

- custom tool policies;
- custom state;
- custom fallback;
- model routing;
- custom observability.

API/custom build.

---

# 28. Decision dimension 7 — Time-to-value

A custom build may take longer.

If an existing product can solve 80% immediately, product path may create value faster.

Do not optimize only for customization.

---

# 29. Decision framework — API

Simple mnemonic:

## A — Application-owned experience
Does AI need to live in customer's app/backend?

## P — Programmatic workflow
Is it triggered/scaled by software?

## I — Integration depth
Does it need custom data/tools/business logic?

If all three are strong:

> API is likely a strong candidate.

---

# 30. Add READY

Before recommendation:

## R — Requirements
Clear task/success?

## E — Engineering
Team can build/operate?

## A — Access
Data/tools/APIs available?

## D — Data/security
Controls understood?

## Y — Yardstick
Eval/metric exists?

So:

```text
API + READY
```

---

# 31. Example — Internal policy Q&A

Need:

- employees;
- HR docs;
- no custom external UX.

Possible:

```text
ChatGPT workspace + connected knowledge
```

Don't jump to API.

---

# 32. Example — SaaS product assistant

Need:

- customer sees AI in SaaS;
- account permissions;
- product docs;
- subscription data;
- actions.

Strong API case:

```text
SaaS UI
↓
backend
↓
OpenAI API
├─ retrieval
└─ company tools
```

---

# 33. Example — Nightly report automation

Need:

```text
Every night
→ analyze warehouse export
→ generate summary
→ post to internal system
```

This is programmatic/event-driven.

API workflow fits.

---

# 34. Example — Coding team

Need:

> engineers want help implementing issues.

Before building custom API coding assistant:

Evaluate:

```text
Codex
```

Existing specialized product may be more efficient.

---

# 35. Example — Support automation

If need only agent drafting:

Could use product-native support/plugin path depending environment.

If need:

- custom customer portal;
- proprietary CRM;
- automated refunds;
- exact business logic;

API/custom agent becomes stronger candidate.

---

# 36. Technical discovery questions

1. Who triggers the request?
2. Where does UI live?
3. What data?
4. What APIs/tools?
5. Read or write actions?
6. Expected volume?
7. Latency?
8. Required output schema?
9. Error/fallback?
10. Who operates system?

---

# 37. Business discovery questions

1. What workflow pain?
2. Current baseline?
3. Why custom build?
4. What business value?
5. Who owns outcome?
6. What happens if wrong?
7. What pilot proves value?

API fit is not only technical.

---

# 38. Feasibility checklist

```text
Business owner ✓
Workflow defined ✓
Data accessible ✓
Integration available ✓
Security path ✓
Engineering capacity ✓
Eval cases ✓
Operational owner ✓
```

If several are missing, opportunity may be premature even if API is technically possible.

---

# 39. API decision tree

```text
Need AI?
↓
Can standard OpenAI product solve workflow?
├─ yes → start product/configure
└─ no
   ↓
Need custom app / automation / integration?
├─ no → reassess
└─ yes
   ↓
Need programmable model capability?
├─ yes → API candidate
└─ no → other technology path
```

---

# 40. Proof before scale

API solution progression:

```text
Prototype
↓
Eval
↓
Integration test
↓
Pilot
↓
Load/cost/security validation
↓
Production
```

Don't infer production feasibility from one demo request.

---

# 41. What to verify before commitment

Current facts:

- model availability;
- tool support;
- pricing;
- context limits;
- rate limits;
- regions;
- retention;
- residency;
- security/compliance controls.

Use official OpenAI docs.

---

# 42. Partner recommendation pattern

Good recommendation:

> “Because the experience needs to live inside the customer's SaaS product, use existing customer identity, access live account state and generate machine-readable actions at high volume, an API-based solution is the appropriate path to validate. The next step is a scoped prototype and eval using representative customer workflows.”

This connects requirement → technology → evidence.

---

# 43. Common mistakes

1. “Custom” automatically means API is best.
2. API because customer has developers.
3. Build something ChatGPT/Codex already solves.
4. Ignore maintenance/ops cost.
5. No eval plan.
6. No security/integration readiness.
7. Confuse API feasibility with business value.
8. Prototype success = production ready.

---

# 44. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| API solution | Solution xây bằng programmable API |
| Custom UX | Trải nghiệm người dùng riêng |
| Event-driven | Được trigger bởi event |
| Programmatic | Do software điều khiển |
| Integration depth | Mức tích hợp sâu |
| Machine-readable | Software đọc được |
| Build vs configure | Xây mới vs cấu hình |
| Technical feasibility | Khả thi kỹ thuật |
| Operational ownership | Chủ thể vận hành |
| Production readiness | Sẵn sàng production |

---

# 45. Section recap

Strong API signals:

```text
Custom product UI
Programmatic trigger
High-volume processing
Deep business integrations
Machine-readable output
Custom actions
Proprietary logic
Custom agents
```

But first ask:

```text
Can ChatGPT / Codex / product-native capability solve it?
```

Use:

```text
API

A — Application-owned experience
P — Programmatic workflow
I — Integration depth
```

Then:

```text
READY

Requirements
Engineering
Access
Data/security
Yardstick/eval
```

Core rule:

> **Use the API when the workflow needs programmable integration and custom control—not simply because an API is available.**

---

# 46. Self-check

1. What are three strong API signals?
2. When might ChatGPT be better than custom API?
3. When might Codex be better than building a coding API solution?
4. API + READY framework gồm gì?
5. Tại sao API adds operational responsibility?
6. Route a nightly document-processing workflow to the right technology path.
