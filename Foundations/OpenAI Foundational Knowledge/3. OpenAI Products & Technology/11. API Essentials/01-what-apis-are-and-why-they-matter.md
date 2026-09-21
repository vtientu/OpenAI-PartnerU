# 01 — What APIs Are and Why They Matter

> **Course:** OpenAI Foundational Knowledge  
> **Course:** API Essentials  
> **Section:** What APIs are and why they matter
>
> **PartnerU note:** Đây là optimized study guide dựa trên section title. Không phải transcript nguyên văn của PartnerU.

---

# 1. Section objective

Sau section này, bạn cần:

- giải thích API bằng ngôn ngữ đơn giản;
- hiểu API giúp software systems giao tiếp như thế nào;
- hiểu request/response, endpoint, authentication và JSON;
- phân biệt API với UI;
- hiểu tại sao APIs rất quan trọng với AI implementation.

---

# 2. API là gì?

**API = Application Programming Interface.**

Definition dễ nhớ:

> API là một giao diện cho phép một phần mềm yêu cầu dữ liệu hoặc capability từ một phần mềm/service khác theo một contract đã định nghĩa.

Ví dụ:

```text
Weather application
→ weather API
→ current weather data
```

Hoặc:

```text
E-commerce backend
→ payment API
→ charge/payment result
```

API cho phép software-to-software interaction.

---

# 3. UI vs API

## User Interface — UI

Cho con người sử dụng.

```text
Human
→ buttons/forms
→ application
```

## API

Cho software sử dụng.

```text
Application
→ programmatic request
→ service
```

Ví dụ:

```text
ChatGPT
= user-facing product

OpenAI API
= developer-facing interface
```

Hai thứ có thể dùng related AI capabilities nhưng phục vụ different interaction models.

---

# 4. Frontend developer analogy

Bạn là Frontend Developer nên concept này rất gần.

React app thường:

```text
Browser
↓
fetch("/api/products")
↓
Backend API
↓
JSON response
↓
UI renders data
```

OpenAI integration tương tự:

```text
Browser
↓
Your backend
↓
OpenAI API
↓
AI result
↓
Backend
↓
UI
```

AI không làm API concept trở thành thứ hoàn toàn mới.

---

# 5. Request

**Request** = message/application call gửi tới API.

Request thường chứa:

- endpoint;
- method;
- authentication;
- parameters;
- body/payload.

Conceptual example:

```http
POST /something
Authorization: Bearer ...
Content-Type: application/json

{
  "input": "Summarize this text..."
}
```

Bạn không cần học exact OpenAI endpoint ở section này.

Quan trọng là mental model.

---

# 6. Response

API trả về **response**.

Conceptually:

```json
{
  "result": "..."
}
```

Response may include:

- output;
- metadata;
- usage information;
- status/error details.

Application decides what to do next.

---

# 7. Endpoint

**Endpoint** = specific API location/functionality.

Think:

```text
API
├─ endpoint A
├─ endpoint B
└─ endpoint C
```

Different endpoints/resources may support different operations.

Modern API platforms may also consolidate multiple capabilities behind broader endpoints.

---

# 8. HTTP methods — concept only

Common web API methods:

- `GET` — retrieve;
- `POST` — send/create/process;
- `PUT/PATCH` — update;
- `DELETE` — remove.

AI model inference calls commonly involve sending input via a request.

You do not need to memorize HTTP details to understand API solutioning.

---

# 9. JSON

**JSON = JavaScript Object Notation.**

Common format for API payloads.

Example:

```json
{
  "name": "Alice",
  "priority": "high"
}
```

For a JavaScript developer, this should feel natural.

Benefits:

- machine-readable;
- structured;
- easy to parse.

---

# 10. Authentication

APIs need to know:

> Who is allowed to make this request?

Common pattern:

```text
application
+ secret/API credential
→ authenticated request
```

For server-based AI applications, credentials should generally be protected on a trusted backend rather than exposed to public browser code.

---

# 11. Why credentials matter

If secret key is placed in public frontend bundle:

```text
browser
→ user can inspect secret
```

Risk:

- unauthorized usage;
- cost;
- abuse;
- account compromise.

Therefore common architecture:

```text
Frontend
→ Your backend
→ External API
```

Backend owns secret.

---

# 12. API contract

An API defines expectations:

```text
Input shape
↓
Service behavior
↓
Output shape
```

This is a **contract**.

Developers build against documented contract rather than service internals.

---

# 13. Abstraction

API hides implementation complexity.

When calling a weather API, you don't operate satellites.

When calling an AI API, you don't operate frontier-model training/inference infrastructure yourself.

This is an important value:

> **API exposes capability without requiring customer to build the underlying service.**

---

# 14. Why APIs matter for modern software

APIs allow companies to compose systems.

Example product:

```text
Own application
├─ payment API
├─ email API
├─ maps API
├─ identity API
└─ AI API
```

Companies can focus on differentiated application value.

---

# 15. API as integration boundary

APIs connect:

```text
Service A
↔
Service B
```

In enterprise workflows:

```text
AI app
→ CRM API
→ ERP API
→ OpenAI API
```

This makes APIs central to AI agents and automation.

---

# 16. Synchronous request

Simplified:

```text
send request
→ wait
→ response
```

Useful for interactive tasks.

Example:

- classify text;
- generate short response.

---

# 17. Asynchronous work

Some tasks take longer.

Pattern:

```text
submit job
↓
work runs
↓
check/result later
```

Good for:

- batch processing;
- long-running workflows;
- agents.

Implementation pattern depends on use case.

---

# 18. Errors

APIs do not always succeed.

Errors may come from:

- invalid request;
- authentication;
- rate limit;
- service availability;
- timeout.

Good software handles errors.

```text
request
↓
success? ── yes → continue
  │
  no
  ↓
retry/fallback/error state
```

---

# 19. Rate limits

Services usually limit how much workload can be sent over a period.

Reasons include:

- capacity;
- reliability;
- abuse prevention.

Application needs:

- retries;
- backoff;
- queueing;
- capacity planning.

Exact OpenAI rate-limit details depend on account/model and should be verified from current documentation.

---

# 20. API versioning/evolution

APIs change.

Good provider tries to maintain clear documentation/migration paths.

Developer should:

- track changes;
- test;
- avoid assumptions from old docs.

This mirrors the PartnerU principle:

> capability concepts are durable; exact implementation details need verification.

---

# 21. API vs SDK

## API

The service interface/protocol.

## SDK

A library that makes API use easier in a programming language.

Example mental model:

```text
API
= capability contract

SDK
= convenient client library
```

SDK can handle:

- request creation;
- types;
- parsing;
- common helpers.

---

# 22. API vs webhook

API:

```text
your app asks service
```

Webhook:

```text
service notifies your app when event occurs
```

Both are integration patterns.

Useful distinction for automation.

---

# 23. API vs database

Database stores/manages data.

API exposes operations/capabilities.

An API may read/write a database internally, but API itself is not the DB.

---

# 24. API vs model

Model is intelligence component.

API exposes programmable access to model/service capability.

```text
Model
↓
serving infrastructure
↓
API
↓
developer application
```

Important distinction:

```text
API ≠ model
```

---

# 25. Why APIs matter for AI

Without API, AI may remain a standalone product.

With API:

```text
AI capability
→ embedded into customer product/workflow
```

That enables:

- AI-powered features;
- automation;
- agents;
- customer-facing experiences;
- back-office processing.

---

# 26. Example — Support application

```text
Customer
↓
Company support UI
↓
Company backend
↓
AI API
↓
Draft/analysis
↓
Support workflow
```

User never needs to open ChatGPT.

AI is embedded.

---

# 27. Example — Document processing

```text
New document event
↓
Backend
↓
AI API
↓
structured extraction
↓
validation
↓
database
```

No interactive UI required.

This is a backend API workflow.

---

# 28. Example — Agent

```text
Goal
↓
Agent application
├─ OpenAI API
├─ CRM API
├─ email API
└─ internal tools
↓
business outcome
```

Agents depend heavily on APIs because agents need tools.

---

# 29. Partner lens

When customer says:

> “We need an API.”

Don't stop there.

Ask:

- What application?
- Who is user?
- What workflow?
- What data?
- What action?
- What scale?
- What custom behavior?

API is implementation path—not business requirement by itself.

---

# 30. Common mistakes

1. API = UI.
2. API = database.
3. API = model.
4. API key belongs in public frontend.
5. Every API request always succeeds.
6. API eliminates application logic.
7. API means no security responsibility.
8. Customer says “API” so no discovery needed.

---

# 31. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| API | Giao diện cho software giao tiếp |
| Request | Yêu cầu gửi tới API |
| Response | Kết quả API trả về |
| Endpoint | Điểm/chức năng API |
| Payload | Dữ liệu request/response |
| JSON | Format dữ liệu có cấu trúc |
| Authentication | Xác thực |
| API key | Credential truy cập API |
| SDK | Thư viện hỗ trợ dùng API |
| Rate limit | Giới hạn request/usage |
| Timeout | Hết thời gian chờ |
| Retry | Thử lại |
| Webhook | Service chủ động gửi event tới app |

---

# 32. Section recap

Basic API model:

```text
Application
↓ request
API service
↓ response
Application
```

For AI:

```text
Your app
→ backend
→ OpenAI API
→ model/capability
→ result
→ your workflow
```

Core rule:

> **An API turns a service capability into a programmable building block that another application can use.**

---

# 33. Self-check

1. API và UI khác nhau thế nào?
2. Request/response là gì?
3. Tại sao API credentials không nên đặt trong public frontend?
4. API và SDK khác nhau thế nào?
5. API và model khác nhau ra sao?
6. Hãy vẽ API flow cho document extraction.
