# 03 — Model Vocabulary Partners May Hear

> **Course:** OpenAI Foundational Knowledge  
> **Sub-course:** Core AI & Machine Learning Fundamentals  
> **Section:** Model vocabulary partners may hear
>
> **Goal:** Đây là “partner vocabulary map” — không nhằm biến bạn thành ML researcher, mà giúp bạn nghe đúng, hỏi đúng và không dùng thuật ngữ sai trong customer conversation.

---

# 1. Section objective

Sau section này, bạn cần:

- nhận diện các từ model/AI phổ biến;
- hiểu chúng đủ sâu để trao đổi với technical stakeholder;
- biết term nào mô tả **model**, term nào mô tả **system**, term nào mô tả **measurement**;
- tránh dùng benchmark/model size/context window như proxy duy nhất cho solution quality.

---

# 2. Vocabulary map

Chia vocabulary thành 7 nhóm:

```text
A. Model family / capability
B. Input & representation
C. Training
D. Inference/runtime
E. System patterns
F. Performance
G. Evaluation
```

Học theo category sẽ dễ nhớ hơn thuộc từng từ riêng.

---

# 3. A — Foundation model

Model broad-purpose được train ở scale lớn và có thể support nhiều downstream tasks.

Examples of task types:

- writing;
- summarization;
- coding;
- analysis;
- extraction.

Partner translation:

> “Một model nền tảng có thể được reused across many business workflows.”

---

# 4. Large Language Model — LLM

Language-focused foundation model có scale lớn.

Partner should avoid:

> “LLM = all AI.”

Some AI tasks may use:

- embedding models;
- image models;
- speech models;
- classifiers;
- specialized models.

---

# 5. Multimodal model

Model hỗ trợ nhiều modality.

Examples:

```text
text + image
audio + text
```

Partner question:

> Which input/output modalities does this workflow actually need?

Không cần multimodal nếu use case chỉ text.

---

# 6. Reasoning model / reasoning capability

Capability dành cho multi-step problems.

Good business translation:

> “Better suited to complex analysis/planning/coding tasks.”

Avoid:

> “It thinks exactly like a human.”

Human-like metaphor dễ gây hiểu sai.

---

# 7. Specialized model

Model optimized cho narrower task/modalities.

Examples category:

- image generation;
- speech transcription;
- text-to-speech;
- embeddings.

Rule:

> General-purpose model is not automatically best for every specialized task.

---

# 8. B — Token

Token là unit mà text model processes.

Not always one word.

Why partner cares:

- context limits;
- input/output usage;
- cost in some API pricing models;
- latency.

Avoid manually converting:

> “1 token = 1 word.”

Không chính xác universally.

---

# 9. Context window

Lượng context model có thể process.

Includes potentially:

- prompt;
- history;
- documents;
- tool outputs.

Large context helpful but not magic.

```text
More context
can also mean
more irrelevant context
```

Need retrieval/context engineering.

---

# 10. Embedding

Vector numerical representation capturing useful semantic relationships.

Use cases:

- semantic search;
- retrieval;
- clustering;
- recommendation.

Example:

```text
"annual leave policy"
and
"vacation rules"
```

can be semantically close even if words differ.

---

# 11. Vector / vector database

**Vector** = list of numbers representing content.

**Vector database** = system optimized to store/search vectors.

Often used in RAG.

But:

> Vector DB is infrastructure, not intelligence by itself.

---

# 12. C — Pretraining

Large-scale initial training phase that builds broad model capability.

Mental model:

```text
broad data
→ learn general patterns
→ foundation capability
```

Do not equate with:

> “upload company docs.”

---

# 13. Post-training

Training steps after pretraining to shape usefulness/behavior.

May include methods focused on:

- instruction following;
- preference/alignment;
- safety;
- task behavior.

Exact pipeline can vary.

Partner should not invent internal training details not publicly documented.

---

# 14. Fine-tuning

**Fine-tuning** = additional training to adapt model behavior using task/example data.

Potential reasons:

- specific style/format;
- repeated behavior;
- specialized task performance.

Fine-tuning is **not automatically first solution**.

First consider:

```text
Prompt/instructions?
Retrieval?
Tools?
Workflow?
Evals?
```

Then fine-tune if evidence supports it.

---

# 15. Supervised fine-tuning — SFT

Fine-tuning using examples of desired input → output behavior.

Simplified:

```text
Example input
→ desired output
```

System learns to better reproduce desired pattern.

---

# 16. Reinforcement learning — RL

Broad ML family where behavior is improved based on reward/evaluation signals.

Partner-level intuition:

```text
Behavior
→ feedback/reward signal
→ learning
```

No need to explain advanced RL math unless audience requires it.

---

# 17. D — Inference

Using trained model to generate prediction/output.

API call time = inference/runtime.

Important because business concerns appear here:

- latency;
- cost;
- throughput;
- reliability.

---

# 18. Latency

Time from request to useful response/result.

For UI:

```text
User request
→ waiting
→ first/complete response
```

Low latency important for:

- interactive chat;
- realtime use.

Less critical for:

- overnight batch analysis.

---

# 19. Throughput

Amount of work processed per unit time.

Example:

```text
requests/minute
tokens/second
documents/hour
```

A system can have good latency for one request but insufficient throughput at enterprise scale.

---

# 20. Temperature / sampling

Some generative systems expose parameters controlling output variation.

Partner mental model:

```text
lower variation ↔ more variation
```

But do not oversimplify to:

> “temperature = creativity slider” in every model/API.

Model/runtime controls evolve.

Verify current documentation when tuning specific product/model.

---

# 21. Context engineering

Broad practice of deciding what information/instructions/tools are presented to model at runtime.

Can include:

- system/developer instructions;
- relevant documents;
- user history;
- tool definitions;
- structured state.

It is broader than prompt writing.

---

# 22. E — RAG

**Retrieval-Augmented Generation**

```text
query
→ retrieve relevant content
→ add to context
→ model generates
```

Use when model needs:

- private company data;
- current knowledge;
- citations/grounding.

---

# 23. Grounding

Make output rely on trusted/relevant source context.

Example:

> Answer HR question based on approved HR documents.

Grounding ≠ guarantee of correctness.

Need evals.

---

# 24. Tool calling / function calling

Model can choose/request a predefined tool.

Example:

```text
get_customer_order(order_id)
```

Tool performs actual operation.

Key security principle:

> Tool permissions are application responsibility.

---

# 25. Agent

System in which model can manage multiple steps toward a goal, often using tools.

Agent vocabulary often includes:

- planning;
- actions;
- observations;
- state;
- loop;
- termination;
- handoff.

Again:

> Agent is a system design pattern, not just a model name.

---

# 26. Orchestration

Code/system logic coordinating:

- models;
- tools;
- data;
- steps;
- retries;
- approvals.

Analogy:

```text
Model = intelligent worker
Orchestrator = workflow manager
Tools = systems worker can use
```

---

# 27. Guardrail

Control constraining or checking system behavior.

Examples:

- input/output checks;
- permission;
- policy checks;
- human approval.

Guardrail is not one universal feature.

---

# 28. F — Model size / parameter count

Parameter count can describe scale.

But partner should avoid:

> “More parameters = always better.”

Quality depends on:

- architecture;
- training;
- task;
- inference techniques;
- system design.

Modern model families may not expose/comparably use parameter counts.

Capability evaluation is usually more useful.

---

# 29. Quantization

Technique that reduces numerical precision of model weights/operations to improve efficiency.

Relevant mostly when:

- self-hosting/open models;
- edge deployment;
- infrastructure optimization.

Often not central to hosted OpenAI API customer conversations.

Know the word; don't force it into business discussion.

---

# 30. Knowledge cutoff

Model documentation may state a point after which broad pretraining knowledge is not guaranteed to include events.

But modern systems can use:

- web search;
- retrieval;
- tools;
- user-provided context.

Therefore:

```text
knowledge cutoff
≠
system can never access newer info
```

It depends on tools/context.

---

# 31. G — Benchmark

Standardized test/dataset for comparing capability.

Useful for:

- broad signal;
- research comparison.

Not sufficient for:

- customer-specific ROI;
- production reliability.

Partner phrase:

> “Benchmark is evidence about a benchmark, not proof of your workflow.”

---

# 32. Eval

**Evaluation / eval** measures model/system performance for a defined task/criterion.

Customer eval example:

```text
500 historical support cases
→ expected resolution
→ AI system output
→ score
```

Evals are closer to customer reality than generic benchmark.

---

# 33. Ground truth

Expected/accepted reference answer/label used to evaluate.

Can be:

- human-labeled;
- historical outcome;
- domain expert judgment.

Not all tasks have one exact ground truth.

Creative/writing tasks may require rubric.

---

# 34. Precision / recall

Common classification/retrieval metrics.

## Precision

Of items system said “positive”, how many were correct?

## Recall

Of all true positives, how many did system find?

Trade-off can matter.

Example fraud/security/search contexts may value them differently.

---

# 35. Accuracy

Proportion correct under a defined evaluation.

Warning:

> “95% accuracy” is meaningless without saying **on what task, dataset and definition**.

---

# 36. Hallucination / factuality

Hallucination: unsupported/generated information presented as if factual.

Factuality: degree output is supported/correct.

Grounding + source tools + evals can help.

No generic “hallucination percentage” should be assumed across tasks.

---

# 37. Model version / snapshot / alias

Important operational vocabulary.

A provider may offer:

- specific model IDs;
- aliases;
- versions/snapshots.

Names and availability can change.

Partner rule:

> If exact name affects architecture, pricing, availability or commitment, verify current official documentation.

---

# 38. Current OpenAI example — why verification matters

As of **21 September 2026**, OpenAI's public API model guide lists the GPT‑5.6 family including models positioned for different trade-offs, such as:

- GPT‑5.6 Sol;
- GPT‑5.6 Terra;
- GPT‑5.6 Luna;

alongside specialized image, realtime, speech and other models.

This is an **example of current naming**, not vocabulary to memorize permanently.

The lesson:

```text
Capability concepts are durable.
Product/model names change.
```

---

# 39. Vocabulary classification cheat sheet

| Term | Category |
|---|---|
| LLM | Model category |
| Multimodal | Model capability |
| Token | Representation/runtime |
| Embedding | Representation/model type |
| Pretraining | Training |
| Fine-tuning | Training/adaptation |
| Inference | Runtime |
| Context window | Runtime constraint |
| RAG | System pattern |
| Agent | System pattern |
| Tool calling | System capability |
| Latency | Performance |
| Benchmark | Evaluation |
| Eval | Evaluation |
| Guardrail | System control |

---

# 40. Partner conversation example

Customer:

> “Does this model have a million-token context and RLHF and RAG?”

Don't answer the vocabulary soup directly.

Clarify:

> “Which workflow are you trying to support? Is the requirement to process long documents, use private knowledge, or adapt response behavior?”

Then map:

```text
long documents → context/retrieval
private current knowledge → RAG/tools
repeated format/style → prompt/fine-tuning candidate
multi-step actions → agent/tooling
```

---

# 41. Common mistakes

1. Parameter count = intelligence.
2. Context window = usable knowledge.
3. RAG = training.
4. Benchmark = production performance.
5. Agent = model.
6. Fine-tuning = upload latest data.
7. Temperature = universal creativity setting.
8. Exact model name assumed from memory.

---

# 42. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Foundation model | Model nền tảng broad-purpose |
| LLM | Mô hình ngôn ngữ lớn |
| Multimodal | Đa phương thức |
| Token | Đơn vị model xử lý |
| Context window | Giới hạn context |
| Embedding | Vector representation |
| Pretraining | Huấn luyện nền quy mô lớn |
| Post-training | Huấn luyện sau pretraining |
| Fine-tuning | Huấn luyện thêm để thích nghi behavior |
| Inference | Chạy model |
| Latency | Độ trễ |
| Throughput | Khả năng xử lý theo thời gian |
| RAG | Retrieval-Augmented Generation |
| Tool calling | Model yêu cầu gọi công cụ |
| Agent | System làm nhiều bước hướng tới goal |
| Orchestration | Điều phối system |
| Benchmark | Bài test chuẩn hóa |
| Eval | Đánh giá model/system |
| Ground truth | Reference answer/label |
| Hallucination | Output không được support |

---

# 43. Section recap

Hãy nhớ:

```text
MODEL terms:
LLM, multimodal, reasoning

TRAINING terms:
pretraining, post-training, fine-tuning

RUNTIME terms:
token, context, inference, latency

SYSTEM terms:
RAG, agent, tool calling, orchestration

MEASUREMENT terms:
benchmark, eval, accuracy, precision/recall
```

Partner principle:

> **Translate jargon back into a requirement.**

---

# 44. Self-check

1. RAG và fine-tuning khác nhau thế nào?
2. Benchmark và eval khác nhau thế nào?
3. Context window lớn có đảm bảo answer tốt hơn không?
4. Agent thuộc model layer hay system layer?
5. Vì sao exact model names cần verify?
6. Accuracy claim cần đi kèm những context gì?
