# 02 — Understanding What Training and Inference Mean in AI

> **Course:** OpenAI Foundational Knowledge  
> **Sub-course:** AI Infrastructure & Implementation  
> **Section:** Understanding what training and inference mean in AI

---

# 1. Section objective

Sau section này, bạn cần:

- hiểu training và inference khác nhau về purpose và infrastructure;
- biết pretraining, post-training, fine-tuning nằm ở đâu;
- hiểu tại sao enterprise application thường consume inference chứ không train frontier model;
- biết training compute và inference compute ảnh hưởng cost/architecture khác nhau;
- tránh nhầm prompting/RAG với training.

---

# 2. Big picture

Training:

```text
Data
+ objective
+ large compute
→ update model parameters
→ trained model
```

Inference:

```text
New input
+ trained model
→ output
```

Simplest distinction:

> **Training changes the model. Inference uses the model.**

---

# 3. Training

During training, system:

1. receives training examples/data;
2. makes predictions;
3. computes error/objective signal;
4. updates parameters;
5. repeats.

Result:

```text
Model parameters encode learned patterns
```

Training can require enormous compute for frontier foundation models.

---

# 4. Why training is infrastructure-heavy

Training often involves:

- many accelerators;
- distributed computing;
- high-bandwidth networking;
- large datasets;
- checkpoint storage;
- long-running jobs.

Challenges:

- hardware cost;
- power;
- reliability;
- orchestration;
- storage;
- data pipeline.

This is fundamentally different from building a normal web app.

---

# 5. Pretraining

Pretraining builds broad foundational capability.

Simplified:

```text
large broad dataset
↓
self-supervised/objective-driven learning
↓
general model capability
```

Pretraining frontier models is typically done by model providers/labs, not every enterprise customer.

---

# 6. Post-training

Post-training shapes model behavior after broad pretraining.

Can target:

- instruction following;
- safety;
- task behavior;
- preference alignment.

Partner should understand concept but not invent proprietary details.

---

# 7. Fine-tuning

Fine-tuning adapts an existing model with additional examples/data.

Potential goals:

- more consistent format;
- domain/task behavior;
- specialized style.

Infrastructure need is usually much smaller than training from scratch, but it is still model training.

---

# 8. Prompting is not training

Prompt:

```text
instruction/context
→ model
→ response
```

The model uses the input at inference time.

Its weights do not necessarily change.

So:

```text
Prompting ≠ training
```

---

# 9. RAG is not training

RAG:

```text
retrieve knowledge
→ place in context
→ inference
```

Again:

```text
RAG ≠ updating model weights
```

This distinction is critical for solution design.

---

# 10. Inference

Inference is when a trained model processes live/new input.

Example API flow:

```text
Application
→ model request
→ inference compute
→ output
→ application
```

This happens every time a user asks/does something with the model.

---

# 11. Inference infrastructure

Inference serving must handle:

- request queue;
- model loading;
- GPU/accelerator compute;
- memory;
- batching;
- response streaming;
- capacity.

Hosted providers manage most of this.

Customer still cares about:

- latency;
- rate limits;
- cost;
- throughput;
- reliability.

---

# 12. Training compute vs inference compute

Training:

```text
large upfront compute
```

Inference:

```text
compute per request/use
```

At enterprise scale, inference cost can become large because:

```text
small cost/request
× millions of requests
=
material operating cost
```

So cost optimization matters.

---

# 13. CAPEX vs OPEX intuition

Self-hosted training infrastructure often looks more like **capital-intensive** compute investment.

Hosted inference often behaves more like usage-based **operational expense**.

Exact accounting depends on organization.

Partner-level takeaway:

> Infrastructure economics differ between owning compute and consuming managed AI services.

---

# 14. Batch inference

Not all inference is realtime.

Batch inference:

```text
100,000 documents
→ process asynchronously
```

Priorities:

- throughput;
- cost;
- reliability.

Realtime inference:

```text
user asks
→ waits for answer
```

Priorities:

- latency;
- responsiveness.

Same model, different serving pattern.

---

# 15. Streaming inference

Instead of waiting for complete answer:

```text
Model generates tokens
→ application streams progressively
```

Benefit:

- better perceived latency;
- user sees response sooner.

Important:

> Streaming may improve perceived latency even if total completion time stays similar.

---

# 16. Context length affects inference

Longer input/context generally means:

- more tokens;
- more compute;
- more cost;
- potentially more latency.

Therefore:

```text
more context
≠ always better
```

Retrieval can help send only relevant context.

---

# 17. Output length affects inference

Longer outputs also:

- take more generation time;
- cost more;
- increase user waiting time.

Design should request only needed output.

---

# 18. Reasoning depth and compute

More complex reasoning tasks can require more inference work.

Trade-off:

```text
quality
↔ compute
↔ latency
↔ cost
```

This is why model/task routing can matter.

---

# 19. Model routing

A system may use different models for different tasks.

Example:

```text
simple classification
→ efficient model

complex reasoning
→ higher-capability model
```

This can optimize:

- cost;
- latency;
- quality.

But routing adds architecture/evaluation complexity.

---

# 20. Caching

Some repeated results/context can be cached.

Potential benefit:

- lower latency;
- lower cost;
- less duplicate work.

Examples:

- static reference data;
- repeated retrieval;
- stable computation.

Need caution around:

- user-specific data;
- permissions;
- stale content.

---

# 21. Inference concurrency

Concurrency = how many requests happen simultaneously.

A system serving 10 users differs from 100,000 users.

Need planning for:

- request bursts;
- rate limits;
- queues;
- backpressure;
- autoscaling.

---

# 22. Throughput

Throughput measures how much work can be processed per time.

Examples:

- requests/sec;
- documents/hour;
- tokens/sec.

Latency and throughput are related but not identical.

---

# 23. Cold start / warm start intuition

Some systems may have startup/load overhead before serving efficiently.

Terms:

- cold start;
- warm model/service.

Managed services may abstract much of this.

Still useful vocabulary in self-hosted inference discussions.

---

# 24. Fine-tuning vs RAG decision

A common enterprise misunderstanding:

> “We have company documents, so we need training.”

Often false.

If need current facts:

```text
RAG / tools
```

If need behavior/style adaptation:

```text
fine-tuning may help
```

If need both:

```text
fine-tuning + RAG
```

They solve different problems.

---

# 25. Training data vs runtime data

Training data:

```text
used to update weights
```

Runtime data:

```text
provided for current request
```

Examples runtime:

- user prompt;
- retrieved doc;
- CRM record;
- tool output.

Don't call all data “training data.”

---

# 26. Enterprise implementation perspective

Most enterprise AI projects focus on:

```text
Use pretrained foundation model
↓
Add instructions
↓
Connect data/tools
↓
Evaluate
↓
Deploy inference
```

Not:

```text
Train frontier model from scratch
```

This dramatically reduces infrastructure barrier.

---

# 27. Example — Support assistant

No training required initially.

```text
Pretrained model
+ support policies via RAG
+ customer data via tools
+ evals
→ support application
```

Only consider fine-tuning if repeated behavior problems remain.

---

# 28. Example — Invoice extraction

```text
Document
→ pretrained multimodal model
→ structured output
→ validation
```

Could potentially be solved entirely at inference.

No need to “train on every invoice” by default.

---

# 29. Developer mental model

Training resembles:

> building/compiling a learned artifact.

Inference resembles:

> calling that artifact at runtime.

Analogy is imperfect, but useful:

```text
TRAINING
creates model state

INFERENCE
uses model state
```

---

# 30. Partner discovery questions

1. Does customer actually need training?
2. Is problem knowledge or behavior?
3. Is data current/dynamic?
4. Is workload realtime or batch?
5. Expected request volume?
6. Required response latency?
7. Cost sensitivity?
8. Need specialized behavior?
9. Can prompt/RAG/tools solve before fine-tuning?

---

# 31. Common mistakes

1. Prompting = training.
2. RAG = training.
3. Every enterprise needs fine-tuning.
4. Fine-tuning = adding current facts.
5. Training and inference use same infrastructure economics.
6. Ignore inference scale/cost.
7. Assume all inference is realtime.
8. Ignore input/output token length.

---

# 32. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Training | Huấn luyện model |
| Inference | Chạy model để tạo output |
| Pretraining | Huấn luyện nền quy mô lớn |
| Post-training | Huấn luyện bổ sung sau pretraining |
| Fine-tuning | Adapt model bằng training thêm |
| Training data | Dữ liệu dùng update weights |
| Runtime data | Dữ liệu dùng ở inference |
| Batch inference | Inference theo lô |
| Realtime inference | Inference tương tác |
| Streaming | Trả output dần |
| Throughput | Khối lượng xử lý / thời gian |
| Concurrency | Số request đồng thời |
| Caching | Lưu kết quả/ngữ cảnh tái sử dụng |

---

# 33. Section recap

Remember:

```text
TRAINING
data + objective + compute
→ changes weights

INFERENCE
input + context + trained model
→ output
```

And:

```text
Prompt ≠ training
RAG ≠ training
Memory ≠ training
```

Enterprise default:

```text
pretrained model
+ context
+ retrieval
+ tools
+ evals
```

before considering custom training.

---

# 34. Self-check

1. Training và inference khác nhau thế nào?
2. Pretraining và fine-tuning khác gì?
3. Vì sao RAG không phải training?
4. Batch inference và realtime inference khác nhau?
5. Input/output length ảnh hưởng inference ra sao?
6. Tại sao enterprise thường không train frontier model từ scratch?
