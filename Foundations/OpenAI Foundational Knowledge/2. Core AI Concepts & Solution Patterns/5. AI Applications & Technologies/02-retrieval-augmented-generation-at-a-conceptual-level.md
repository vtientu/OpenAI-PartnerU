# 02 — Retrieval-Augmented Generation at a Conceptual Level

> **Course:** OpenAI Foundational Knowledge  
> **Sub-course:** AI Applications & Technologies  
> **Section:** Retrieval-augmented generation at a conceptual level
>
> **Scope:** Phần này tập trung vào concept và solution reasoning, không khóa vào một implementation/vendor cụ thể. Product/API names có thể thay đổi; concept RAG bền hơn.

---

# 1. Section objective

Sau section này, bạn cần:

- giải thích **RAG** bằng ngôn ngữ đơn giản;
- hiểu tại sao RAG tồn tại;
- nắm pipeline **ingest → index → retrieve → augment → generate**;
- hiểu embeddings, chunking, metadata, retrieval ở mức concept;
- phân biệt RAG với fine-tuning, search, long context và tool/API lookup;
- hiểu failure modes, security và evaluation cơ bản của RAG.

---

# 2. RAG là gì?

**RAG = Retrieval-Augmented Generation.**

Một definition dễ nhớ:

> Trước khi model tạo answer, application **tìm thông tin liên quan từ một nguồn bên ngoài** rồi đưa thông tin đó vào context để model sử dụng.

```text
Question
↓
Retrieve relevant knowledge
↓
Add knowledge to context
↓
Model generates answer
```

---

# 3. Why RAG exists

Foundation model có thể không có:

- private company data;
- latest policy;
- customer-specific documents;
- recently changed product information;
- live internal knowledge.

RAG giải quyết bằng cách đưa knowledge vào runtime.

Example:

```text
Employee:
"Parental leave của công ty là bao nhiêu ngày?"
↓
Retrieve approved HR policy
↓
Model answers from source
```

Điểm quan trọng:

> RAG không yêu cầu model phải “học thuộc” mọi document vào weights.

---

# 4. Core mental model

RAG tách hai thứ:

```text
Model capability
=
understand + reason + synthesize

Knowledge source
=
current/private/approved information
```

Khi kết hợp:

```text
Reasoning model
+
trusted external context
=
knowledge-grounded application
```

---

# 5. The conceptual pipeline

```text
1. INGEST
   documents enter the system

2. PREPARE / INDEX
   split + represent + store

3. RETRIEVE
   find relevant pieces for query

4. AUGMENT
   place retrieved content into model context

5. GENERATE
   model creates answer

6. VERIFY / CITE / EVALUATE
   show evidence and measure quality
```

---

# 6. Step 1 — Ingest

Knowledge sources may include:

- PDFs;
- policies;
- wiki pages;
- technical docs;
- support articles;
- contracts;
- manuals;
- CRM notes;
- product documentation.

RAG quality begins with source quality.

```text
Bad / stale source
→ bad retrieval
→ potentially bad answer
```

This is a **data governance** issue, not only an AI issue.

---

# 7. Source-of-truth thinking

Partner should ask:

- Which repository is authoritative?
- Who owns content?
- How often is it updated?
- Which versions are active?
- Which documents are obsolete?
- Who may access which source?

Before architecture, clarify truth source.

---

# 8. Step 2 — Chunking

Large documents are often split into smaller retrieval units called **chunks**.

```text
100-page handbook
↓
sections / paragraphs / semantic chunks
```

Why?

Because user question usually relates to only a small part.

We want:

> relevant context, not all context.

---

# 9. Good chunking

A good chunk should:

- contain enough information to make sense;
- preserve relevant context;
- avoid too much irrelevant material;
- ideally align with document structure.

Possible boundaries:

- heading;
- section;
- paragraph;
- semantic unit.

No universal “best chunk size.”

It must be evaluated.

---

# 10. Embeddings

A common retrieval method uses **embeddings**.

An embedding maps content to a numerical vector.

```text
"vacation policy"
→ [0.14, -0.32, ...]
```

Semantically similar content can be close in vector space.

Example:

```text
"annual leave allowance"
```

may be close to:

```text
"vacation entitlement"
```

even though keywords differ.

---

# 11. Vector search

Conceptual flow:

```text
User query
↓
Create query embedding
↓
Compare with document embeddings
↓
Return semantically related chunks
```

Storage may be:

- vector index;
- vector database;
- managed retrieval system.

Important:

> **RAG ≠ vector database.**

Vector search is only one retrieval technique.

---

# 12. Retrieval can use multiple techniques

Possible approaches:

- keyword search;
- vector search;
- hybrid search;
- metadata filtering;
- database query;
- API lookup;
- reranking.

A strong retrieval system may combine them.

---

# 13. Metadata

Metadata helps filter/restrict results.

Examples:

```text
department = HR
region = Vietnam
document_type = policy
effective_date = 2026-07-01
status = active
```

This helps:

- relevance;
- freshness;
- permissions;
- version selection.

---

# 14. Step 3 — Retrieval

At runtime:

```text
Question
↓
Retriever
↓
Relevant chunks
```

The core question is:

> **Did we retrieve the evidence needed to answer correctly?**

A strong model cannot use evidence it never received.

---

# 15. Retrieval failure vs generation failure

RAG can fail in at least two different places.

## Retrieval failure

Correct source exists, but system does not retrieve it.

## Generation failure

Correct source is retrieved, but model:

- misreads it;
- ignores it;
- synthesizes incorrectly.

These require different fixes and different evals.

---

# 16. Step 4 — Augmentation

Retrieved content is added to the model's context.

Conceptually:

```text
Instruction:
Answer using approved sources.

Question:
...

Retrieved context:
Source A...
Source B...
```

The model now has external evidence at inference time.

---

# 17. Step 5 — Generation

The model can then:

- answer;
- summarize;
- compare;
- explain;
- extract;
- synthesize.

A well-designed system may instruct the model to:

- cite source;
- say when evidence is missing;
- avoid unsupported claims;
- identify conflicting sources.

---

# 18. Grounding

**Grounding** means connecting output to trusted/relevant evidence.

RAG is commonly used to ground responses.

But:

```text
RAG ≠ guaranteed correctness
```

Why?

- wrong document may be retrieved;
- source may be stale;
- model may misunderstand;
- question may be ambiguous;
- source may conflict.

Therefore RAG still needs evals.

---

# 19. Citations

A knowledge assistant can return:

```text
Answer
+
source reference
```

Citations help:

- verification;
- user trust;
- debugging;
- auditability.

But:

> A citation is useful only if it actually supports the claim.

---

# 20. RAG vs plain model

## Plain model

```text
Question
→ model
→ answer
```

Useful for:

- general drafting;
- broad reasoning;
- general knowledge.

## RAG

```text
Question
→ retrieve source
→ model
→ grounded answer
```

Useful when private/current/approved knowledge matters.

---

# 21. RAG vs long context

Could we put all documents directly into context?

Sometimes yes.

But there are trade-offs:

- tokens;
- cost;
- latency;
- irrelevant information;
- context limits;
- harder permission handling.

Mental model:

```text
Long context
= bring a lot of data to model

RAG
= find likely relevant data first
```

They can be combined.

---

# 22. RAG vs fine-tuning

This distinction is critical.

## RAG

Problem:

> model needs **knowledge** at runtime.

Examples:

- latest policy;
- private product docs;
- customer information.

## Fine-tuning

Problem is more like:

> model needs different **behavior/style/task consistency**.

Examples:

- consistent response format;
- task-specific behavior;
- repeated classification pattern.

Strong default:

```text
Knowledge problem
→ retrieval/context first

Behavior problem
→ prompt/evals/fine-tuning candidate
```

---

# 23. RAG vs search

Search:

```text
query
→ documents/results
```

RAG:

```text
query
→ documents
→ model synthesis
→ answer
```

A good user experience may expose both answer and sources.

---

# 24. RAG vs tool/API lookup

If question asks structured live state:

> “Where is order 123?”

An API is often better:

```text
getOrderStatus(123)
```

For unstructured knowledge:

> “What does our returns policy say?”

RAG may fit better.

Simple rule:

```text
Unstructured knowledge
→ retrieval

Live structured state/action
→ tool/API
```

Often they are combined.

---

# 25. Permission-aware retrieval

Enterprise RAG must respect user access.

```text
User identity
↓
Access policy
↓
Eligible documents
↓
Retrieval
↓
Model
```

Avoid architecture:

```text
retrieve everything
→ ask model not to reveal it
```

Access control should happen before/at retrieval.

---

# 26. Freshness

Knowledge changes.

Need lifecycle:

```text
Source changes
↓
index updates
↓
old version removed/deprioritized
↓
retrieval reflects active truth
```

Partner should ask:

- update frequency;
- owner;
- SLA;
- versioning.

---

# 27. Conflicting sources

Example:

Old policy:
> 15 days.

New policy:
> 18 days.

Without metadata/versioning, both may retrieve.

System may need:

- active-version filter;
- effective date;
- conflict handling;
- escalation.

This is why RAG is partly a knowledge-management problem.

---

# 28. Query rewriting

Sometimes user wording is poor for retrieval.

User:

> “What happens when a baby arrives?”

System may rewrite/search for:

```text
parental leave
maternity leave
paternity leave
```

This can improve retrieval.

---

# 29. Reranking

Initial retrieval may return many candidates.

```text
retrieve 20
↓
rerank
↓
use top 5
```

Reranking improves relevance before context reaches the model.

---

# 30. No-answer behavior

A strong RAG application should sometimes say:

> “I don't have enough evidence to answer.”

Flow:

```text
No reliable source
↓
abstain / ask clarification / escalate
```

This is often better than a confident unsupported answer.

---

# 31. Evaluation — retrieval layer

Questions:

- Did system retrieve correct document?
- Did relevant chunk appear in top results?
- Did metadata filter correctly?
- Did permission filter correctly?

Possible metrics:

- recall;
- precision;
- ranking quality.

---

# 32. Evaluation — answer layer

Questions:

- Is answer correct?
- Is it supported by source?
- Is it complete?
- Is citation correct?
- Does system abstain when evidence missing?

Both layers matter.

---

# 33. Build representative evaluation cases

For a knowledge assistant:

```text
Question
Expected source
Expected answer/rubric
```

Include:

- common cases;
- edge cases;
- ambiguous cases;
- no-answer cases;
- conflicting-source cases;
- permission-sensitive cases.

---

# 34. Example — HR knowledge assistant

```text
Employee
↓
SSO identity
↓
Question
↓
Permission + metadata filter
↓
Retrieve active HR policies
↓
Model
↓
Answer + sources
↓
No evidence? → HR escalation
```

Metrics:

- grounded answer quality;
- retrieval success;
- HR ticket reduction;
- user satisfaction.

---

# 35. Example — Developer documentation assistant

Sources:

- API docs;
- architecture docs;
- repository documentation.

Flow:

```text
Question
→ retrieve relevant code/docs context
→ model
→ explanation
```

Can later combine with code search/tools.

---

# 36. When RAG is not the right pattern

RAG may be unnecessary when:

### Pure drafting
No external knowledge required.

### Live structured data
Use API/tool.

### Tiny static knowledge
Direct context may be simpler.

### Behavior adaptation
Prompt/fine-tuning may be more relevant.

### Deterministic calculation
Use code/tool.

---

# 37. Developer mental model

Think of RAG as:

```text
Search layer
+
Context builder
+
LLM synthesizer/reasoner
```

Not:

```text
"Upload documents into the model's brain"
```

---

# 38. Partner discovery questions

1. What are the sources?
2. Who owns them?
3. How often do they change?
4. Who can access what?
5. What query types?
6. Do users need citations?
7. What happens when nothing relevant is found?
8. Is data unstructured or structured/live?
9. How will retrieval quality be tested?
10. How will answer quality be tested?

---

# 39. Common mistakes

1. RAG = vector DB.
2. RAG = fine-tuning.
3. More retrieved context is always better.
4. Ignore source governance.
5. Ignore permissions.
6. Evaluate answer but not retrieval.
7. Assume citation guarantees correctness.
8. Use RAG for live structured data that should come from an API.

---

# 40. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| RAG | Retrieval-Augmented Generation |
| Retrieval | Tìm/lấy knowledge liên quan |
| Grounding | Neo answer vào evidence |
| Chunk | Đoạn dữ liệu dùng làm retrieval unit |
| Embedding | Vector representation |
| Vector search | Search theo semantic similarity |
| Hybrid search | Kết hợp nhiều search technique |
| Metadata | Dữ liệu mô tả source/chunk |
| Index | Cấu trúc phục vụ tìm kiếm |
| Reranking | Xếp hạng lại kết quả |
| Citation | Tham chiếu nguồn |
| Freshness | Độ cập nhật |
| Abstain | Không trả lời khi thiếu evidence |
| Permission-aware retrieval | Retrieval có kiểm tra quyền |

---

# 41. Section recap

Pipeline:

```text
Source
↓
Ingest
↓
Chunk / index
↓
Retrieve
↓
Augment
↓
Generate
↓
Cite / evaluate
```

Critical distinctions:

```text
RAG ≠ fine-tuning
RAG ≠ vector DB
RAG ≠ search only
RAG ≠ guaranteed truth
RAG ≠ API/tool lookup
```

Core rule:

> **Use retrieval when the system needs external/private/current unstructured knowledge at runtime.**

---

# 42. Self-check

1. RAG giải quyết problem gì?
2. Chunking và embeddings có vai trò gì?
3. RAG khác fine-tuning thế nào?
4. Khi nào API/tool tốt hơn RAG?
5. Vì sao permission-aware retrieval quan trọng?
6. Retrieval eval và answer eval khác nhau thế nào?
7. Hãy vẽ RAG flow cho HR assistant.
