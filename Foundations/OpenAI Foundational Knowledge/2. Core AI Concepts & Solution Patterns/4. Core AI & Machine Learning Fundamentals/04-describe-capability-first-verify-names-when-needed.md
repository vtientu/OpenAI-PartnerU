# 04 — Describe Capability First, Verify Names When Needed

> **Course:** OpenAI Foundational Knowledge  
> **Sub-course:** Core AI & Machine Learning Fundamentals  
> **Section:** Describe capability first, verify names when needed
>
> **Source note:** Model catalogs thay đổi nhanh. File này tập trung vào communication discipline. Khi cần exact OpenAI model/product facts, dùng documentation chính thức hiện hành.

---

# 1. Section objective

Sau section này, bạn cần:

- biết tại sao customer conversation nên bắt đầu từ **capability**, không phải model name;
- mô tả solution requirement theo task/capability;
- biết khi nào exact model name thực sự quan trọng;
- biết workflow xác minh model name/version;
- tránh “model-name selling” và stale claims.

---

# 2. Big picture

Một pattern kém:

```text
Customer problem
↓
"We should use Model X"
```

Pattern tốt hơn:

```text
Customer problem
↓
Task
↓
Required capability
↓
Constraints
↓
Evaluation
↓
Candidate model/system
```

Điểm cốt lõi:

> **Capability is durable. Model names are implementation details that can change.**

---

# 3. Capability-first nghĩa là gì?

Thay vì nói:

> “Use GPT-X.”

Hãy nói:

> “Workflow cần strong document reasoning, image understanding và tool use với low latency.”

Đây là capability statement.

Sau đó mới select model.

---

# 4. Why model-first is risky

## 4.1. Names change

Models:

- release;
- update;
- deprecate;
- receive aliases;
- gain/lose availability by product/endpoint.

Notes hard-coded to a name can become stale.

---

## 4.2. Same model may not fit all tasks

Task A may need:

- highest reasoning quality.

Task B:

- low cost at high volume.

Task C:

- realtime audio.

Task D:

- image generation.

“Best model” depends on requirement.

---

## 4.3. Customer buys outcome

Business leader rarely cares about exact model ID.

They care:

- does it work?
- how fast?
- how reliable?
- how much?
- can it integrate?
- is it trusted?

Model name is supporting detail.

---

# 5. Capability categories

Describe needs in terms like:

```text
Text understanding
Reasoning
Coding
Image understanding
Image generation
Speech/audio
Realtime interaction
Embedding/search
Tool use
Long-context processing
Structured output
```

These are more stable than product names.

---

# 6. Add non-functional requirements

Capability alone is not enough.

Also define:

```text
Quality
Latency
Cost
Volume
Context size
Region/availability
Tool support
Security/data requirements
Operational reliability
```

This forms a model-selection profile.

---

# 7. Model selection matrix

Example:

| Requirement | Importance |
|---|---|
| Complex reasoning | High |
| Image input | Required |
| Realtime response | Medium |
| Cost | Medium |
| High volume | High |
| Tool use | Required |
| Long context | Medium |

Then evaluate candidates.

Do not start with favorite model.

---

# 8. Capability statement vs product statement

## Capability statement

> “We need a model that can analyze code and reason over repository context.”

Durable.

## Product statement

> “We will use model ID X.”

Implementation-specific.

Both can be needed, but at different stage.

---

# 9. When exact model name matters

Exact name is important when discussing:

- API implementation;
- endpoint compatibility;
- tool support;
- pricing;
- context limits;
- quotas;
- availability;
- deprecation;
- latency;
- model-specific evaluation;
- deployment commitment.

At that point:

> verify documentation.

---

# 10. When exact model name does not matter

Early discovery:

Customer:

> “Can AI analyze our contracts?”

No need to immediately say exact model.

First define:

- document formats;
- length;
- extraction/reasoning tasks;
- accuracy criteria;
- volume;
- security;
- integration.

---

# 11. Verification workflow

Use this sequence:

```text
1. Define capability requirement
2. Identify candidate model family
3. Open current official model docs
4. Confirm exact model ID/alias
5. Confirm modalities/tools/context
6. Confirm availability/pricing if relevant
7. Run customer-specific eval
8. Record date/version in recommendation
```

---

# 12. Why record the date?

Because statement:

> “Model X supports Y”

can become stale.

Better documentation:

```text
Verified:
21 Sep 2026

Source:
OpenAI Models documentation

Requirement:
text + image input, tool use

Candidate:
[current model]
```

Now future reviewers understand context.

---

# 13. Current OpenAI example

As of **21 September 2026**, OpenAI's public API model guide recommends the GPT‑5.6 family for general-purpose work, with current variants positioned for different intelligence/cost trade-offs, and also lists specialized models for image, realtime speech and other tasks.

Do **not** turn that into:

> “GPT‑5.6 Sol is always the right choice.”

The correct takeaway:

```text
Need complex task?
→ evaluate high-capability candidate

Need cost-sensitive scale?
→ evaluate cost-optimized candidate

Need specialized modality?
→ evaluate specialized model
```

Then measure on your task.

---

# 14. Names vs aliases vs model IDs

You may encounter:

## Friendly/product name

Easy to say.

## Model ID

Used in API.

## Alias

Pointer/name that may represent a recommended/current variant.

Partner should not assume these behave identically over time.

For technical implementation, verify exact docs.

---

# 15. Avoid naming from memory

Bad:

> “I'm pretty sure this model has X context and supports Y.”

Better:

> “The workflow requires X and Y. I'll verify the current model documentation before treating those as implementation facts.”

This is professional, not weakness.

---

# 16. Capability-first discovery

Customer:

> “Which OpenAI model should we use?”

Good response structure:

### Step 1 — Task
What exactly must system do?

### Step 2 — Inputs
Text/image/audio/code?

### Step 3 — Output/action
Generate? classify? tool call?

### Step 4 — Quality
How is correctness measured?

### Step 5 — Constraints
Latency/cost/volume?

### Step 6 — Trust
Risk/controls?

### Step 7 — Candidate + eval
Test models.

---

# 17. Model selection is empirical

Do not decide purely from:

- marketing description;
- benchmark;
- parameter count.

Run eval:

```text
Representative cases
× Candidate A
× Candidate B
× Candidate C
↓
Quality / latency / cost
↓
Decision
```

Model selection should be evidence-based.

---

# 18. Capability-first improves architecture

Suppose you hard-code:

> “Use Model X because it is the best.”

Architecture may couple logic to name.

Capability-first encourages abstraction:

```text
Task interface
↓
Model adapter
↓
Current selected model
```

Future model upgrade becomes easier.

---

# 19. Developer analogy

Frontend:

Bad requirement:

> “Use library X.”

Better requirement:

> “We need accessible data table with virtualization and server pagination.”

Then compare libraries.

AI is similar.

Implementation choice should follow requirements.

---

# 20. Avoid model-brand competition in discovery

Customer may ask:

> “Is model A better than model B?”

Partner should ask:

> “Better for which task and metric?”

Potential dimensions:

- reasoning;
- coding;
- latency;
- cost;
- tool use;
- modality.

No universal “better” required.

---

# 21. Model upgrade process

AI systems should expect model evolution.

Good practice:

```text
New model available
↓
Run eval suite
↓
Compare quality
↓
Compare latency/cost
↓
Regression checks
↓
Pilot
↓
Update if justified
```

Do not migrate just because model is newer.

---

# 22. Separate model upgrade from product commitment

Customer contract/solution design should ideally describe:

- service capability;
- performance expectations;
- evaluation criteria.

Hard-binding to exact model names can be unnecessary unless required.

Implementation details still need tracking internally.

---

# 23. How to communicate capability

Good:

> “The solution needs multimodal document understanding and structured extraction.”

Good:

> “The agent needs reliable tool use for three approved operations.”

Good:

> “We need low-latency speech interaction.”

Less useful:

> “We need the newest model.”

---

# 24. Capability → solution pattern

Example:

### Requirement
Answer employee policy questions.

### Capabilities
- language understanding;
- retrieval;
- grounded generation.

### System
```text
User question
→ search approved knowledge
→ model answers with source
→ escalate when no evidence
```

Model name selected later.

---

# 25. Capability → model is not one-to-one

One solution may use multiple models:

```text
Speech model
↓
Reasoning/text model
↓
Embedding/search
↓
Text-to-speech model
```

Therefore “which model?” may need answer:

> “Which part of the system?”

---

# 26. Source hierarchy for exact facts

When exact fact matters:

```text
Official current model docs
↓
Official API/product docs
↓
Model-specific system/release docs
↓
Older guides/slides
↓
Memory
```

Memory should be last.

---

# 27. Partner communication templates

## Early discovery

> “Before choosing a model, let's define the task, data, latency, quality and integration requirements.”

## Technical design

> “These capabilities point to two candidate models. We'll verify current tool/context support and evaluate both.”

## Customer asks newest model

> “We can test the newest suitable model, but the decision should be based on your evals rather than release date alone.”

## Unverified fact

> “I want to verify the current documentation before treating that model detail as a commitment.”

---

# 28. Common mistakes

## Mistake 1
Use latest = best.

## Mistake 2
Memorize product names instead of capability.

## Mistake 3
Quote stale context/pricing.

## Mistake 4
Use benchmark winner as task winner.

## Mistake 5
Select model before defining eval.

## Mistake 6
Assume one model serves entire system.

---

# 29. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| **Capability-first** | Bắt đầu từ khả năng cần thiết |
| **Model selection** | Lựa chọn model |
| **Model family** | Nhóm model liên quan |
| **Model ID** | Tên định danh dùng kỹ thuật/API |
| **Alias** | Tên trỏ tới model/version |
| **Deprecation** | Ngừng hỗ trợ dần |
| **Candidate model** | Model ứng viên |
| **Trade-off** | Sự đánh đổi giữa các mục tiêu |
| **Non-functional requirement** | Yêu cầu như latency/cost/scale |
| **Regression** | Chất lượng bị giảm so với baseline |
| **Eval suite** | Bộ bài đánh giá |
| **Implementation detail** | Chi tiết triển khai |

---

# 30. Section recap

Core rule:

```text
Problem
→ Task
→ Capability
→ Constraints
→ Eval
→ Model
```

Not:

```text
Model name
→ Find a problem
```

Remember:

1. Capability language is durable.
2. Exact names change.
3. Verify names when implementation/commitment depends on them.
4. Selection should be empirical.
5. Newer does not automatically mean better for a workflow.
6. One AI system may use several model types.

---

# 31. Self-check

1. Tại sao capability-first tốt hơn model-first?
2. Khi nào exact model name cần verify?
3. “Newest model” có phải automatically best không?
4. Model selection matrix nên có những dimension nào?
5. Hãy chuyển câu “We need GPT-X” thành capability-based requirement.
6. Tại sao model upgrade cần eval suite?
