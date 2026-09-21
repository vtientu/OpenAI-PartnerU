# 03 — Latency in AI

> **Course:** OpenAI Foundational Knowledge  
> **Sub-course:** AI Infrastructure & Implementation  
> **Section:** Latency in AI

---

# 1. Section objective

Sau section này, bạn cần:

- hiểu latency là gì;
- phân biệt **time to first token** và **time to completion** ở mức concept;
- biết các nguồn latency trong AI system;
- hiểu latency vs quality vs cost trade-off;
- biết cách latency ảnh hưởng UX và feasibility.

---

# 2. Big picture

Latency = thời gian user/system chờ result.

AI latency không chỉ đến từ model.

```text
User
↓
Network
↓
App backend
↓
Retrieval/tools
↓
Model inference
↓
Post-processing
↓
Response
```

Total latency = tổng thời gian across chain.

---

# 3. Why latency matters

A 5-second wait can be fine for:

- complex report;
- deep analysis.

But bad for:

- realtime voice;
- autocomplete;
- interactive support.

Therefore:

> **Acceptable latency depends on workflow.**

---

# 4. Latency vs response time

In many conversations, latency and response time are used similarly.

For deeper thinking, split:

```text
Request starts
↓
First useful output appears
↓
Full output completes
```

Users may perceive these differently.

---

# 5. Time to First Token — TTFT

For streaming text applications:

> TTFT = time before first generated token appears.

Important for chat UX.

Lower TTFT makes system feel responsive.

Even if total answer takes longer.

---

# 6. Time to completion

Time until full response/task completes.

Important for:

- batch workflows;
- long generation;
- downstream processing.

A system can have:

- low TTFT;
- high total completion time.

---

# 7. Perceived latency

User perception depends on UX.

Example:

### Non-streaming

```text
wait 8 sec
→ entire answer appears
```

### Streaming

```text
wait 1 sec
→ text begins
→ completes at 8 sec
```

Same total time; second often feels faster.

---

# 8. Sources of latency

Total AI latency can include:

```text
1. Client/network
2. Authentication
3. Backend processing
4. Retrieval/search
5. Tool/API calls
6. Model queueing
7. Model inference
8. Output generation
9. Post-processing
10. Rendering
```

Optimization must identify actual bottleneck.

---

# 9. Network latency

Factors:

- physical distance;
- region;
- network quality;
- TLS/connection overhead;
- proxies/gateways.

Realtime workloads care more.

---

# 10. Retrieval latency

RAG adds steps:

```text
question
→ embedding/search
→ retrieval
→ reranking
→ model
```

Better grounding may add some latency.

Trade-off:

```text
accuracy/context
↔ latency
```

Need measure, not assume.

---

# 11. Tool latency

Agent/tool workflow:

```text
Model
→ tool A
→ model
→ tool B
→ model
```

Each step adds:

- network time;
- API processing;
- model reasoning.

Multi-step agent can be much slower than simple generation.

---

# 12. Model size/capability and latency

More capable/heavier reasoning may require more compute.

Potentially:

```text
higher capability
→ higher latency/cost
```

But exact relationship depends on implementation/model.

Partner should evaluate actual candidates rather than use generic assumptions.

---

# 13. Input length

Longer prompts/context can increase processing time.

Examples:

- 100 tokens;
- 100,000 tokens.

Larger context also costs more.

RAG can reduce input by selecting relevant chunks.

---

# 14. Output length

Generating 2 sentences vs 5,000 words has different latency.

If workflow only needs:

```text
category + confidence
```

don't request an essay.

Output design is performance design.

---

# 15. Reasoning depth

Complex tasks may use more internal reasoning/inference work.

Useful for:

- complex coding;
- planning;
- analysis.

Not always necessary for:

- simple classification;
- formatting.

Task routing can help.

---

# 16. Sequential vs parallel execution

Sequential:

```text
A → B → C
```

Total time roughly adds.

Parallel:

```text
A
├→ B
└→ C
```

If independent operations run in parallel, latency may reduce.

Architecture design matters.

---

# 17. Agent loops

Agent:

```text
reason
→ tool
→ observe
→ reason
→ tool
...
```

Powerful but latency can accumulate.

Partner must ask:

> Is flexibility worth the latency?

Sometimes deterministic orchestration is faster.

---

# 18. Latency budget

A useful design technique:

```text
Total acceptable latency: 3 sec

Network: 0.2
Retrieval: 0.3
Model: 2.0
Post-process: 0.2
Buffer: 0.3
```

Numbers vary.

Concept:

> Treat latency as a budget allocated across system components.

---

# 19. Latency vs quality

A common trade-off:

```text
fast/simple model
→ lower latency
→ potentially lower quality on hard tasks

deeper reasoning
→ better hard-task quality
→ potentially higher latency
```

Optimal choice depends on business need.

---

# 20. Latency vs cost

Performance optimization can affect cost.

Examples:

- more compute;
- bigger model;
- more replicas;
- less batching.

Sometimes lower latency costs more.

Need explicit priority.

---

# 21. Latency vs throughput

Latency:

> how long one request waits.

Throughput:

> how many requests processed per time.

A batch system can optimize throughput even if individual latency is high.

Realtime systems optimize per-request responsiveness.

---

# 22. UX patterns for slow operations

If operation takes longer:

- streaming;
- progress indicators;
- background job;
- notification when done;
- partial results;
- asynchronous workflow.

Don't force synchronous UX for long-running tasks.

---

# 23. Realtime AI

Voice/interactive applications need:

- low round-trip delay;
- streaming audio;
- fast turn-taking.

Latency can determine whether experience feels natural.

---

# 24. Coding agent latency

A coding agent may take longer because it can:

- inspect repo;
- edit files;
- run tests;
- debug;
- retry.

User may accept minutes if task replaces substantial manual work.

Again:

> acceptable latency depends on value.

---

# 25. Batch latency

For nightly document processing:

A 10-minute completion may be fine.

Important metrics:

- throughput;
- deadline;
- cost;
- success rate.

Latency should be defined in business terms.

---

# 26. Caching

Caching can reduce repeated work.

Examples:

- static retrieved data;
- repeated tool result;
- common prompts/context.

But beware:

- stale data;
- access control;
- user-specific content.

---

# 27. Precomputation

Some outputs can be prepared before user asks.

Example:

- nightly document embeddings;
- account summary generated daily.

Then user interaction becomes faster.

Trade-off:

- freshness;
- storage;
- background cost.

---

# 28. Model routing

Use efficient model for simple task.

Use stronger model for complex cases.

```text
easy case
→ fast model

hard case
→ stronger model
```

Potential benefit:

- better latency/cost mix.

Need routing evals.

---

# 29. Tool timeout and fallback

External tools fail or run slowly.

Need:

- timeout;
- retry;
- fallback;
- error handling.

Without this, one slow dependency can block whole AI workflow.

---

# 30. Observability

Measure latency by component.

Don't only measure total.

Useful breakdown:

```text
network
retrieval
model
tools
post-process
```

This identifies bottleneck.

---

# 31. Example — Support chat

Target:

> interactive.

Need:

- low TTFT;
- fast retrieval;
- limited tool calls;
- streaming.

Could route complex cases to slower flow or human.

---

# 32. Example — Contract analysis

Target:

> quality over instant response.

Could accept:

- larger context;
- deeper reasoning;
- longer runtime.

UX:

```text
submit job
→ background analysis
→ notify user
```

Better than keeping browser waiting.

---

# 33. Developer mental model

Frontend performance already teaches:

```text
TTFB
rendering
API latency
network waterfall
```

AI apps add:

```text
model inference
retrieval
tool chains
generation length
```

Same performance mindset, more components.

---

# 34. Partner discovery questions

1. Is user waiting?
2. What response time is acceptable?
3. Need first partial result quickly?
4. Realtime or async?
5. How many tool calls?
6. Long context?
7. High reasoning requirement?
8. Peak concurrency?
9. Is faster worth more cost?
10. What business metric suffers if response is slow?

---

# 35. Common mistakes

1. Latency = model only.
2. Bigger/faster always better.
3. Use synchronous UI for long job.
4. Ignore tool/API latency.
5. Ignore output length.
6. Optimize before measuring.
7. Confuse latency with throughput.
8. Ignore perceived latency.

---

# 36. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Latency | Độ trễ |
| TTFT | Time to First Token |
| Time to completion | Thời gian hoàn tất |
| Perceived latency | Độ trễ cảm nhận |
| Streaming | Trả output dần |
| Throughput | Khối lượng xử lý |
| Concurrency | Số request đồng thời |
| Timeout | Giới hạn chờ |
| Retry | Thử lại |
| Precompute | Tính trước |
| Latency budget | Ngân sách thời gian cho các bước |
| Bottleneck | Điểm nghẽn |

---

# 37. Section recap

Total AI latency includes:

```text
Network
+ backend
+ retrieval
+ tools
+ model
+ generation
+ post-processing
```

Key rules:

1. Acceptable latency depends on workflow.
2. TTFT and completion time differ.
3. Streaming improves perceived responsiveness.
4. Agent/tool chains add latency.
5. More context/output generally increases work.
6. Latency, quality and cost trade off.
7. Measure component-level latency before optimizing.

---

# 38. Self-check

1. TTFT và total completion time khác gì?
2. Tại sao RAG có thể tăng latency?
3. Agent loops ảnh hưởng latency thế nào?
4. Latency và throughput khác nhau?
5. Khi nào async UX tốt hơn synchronous?
6. Hãy tạo latency budget cho support assistant.
