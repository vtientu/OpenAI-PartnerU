# 01 — How Core AI Terms Relate

> **Course:** OpenAI Foundational Knowledge  
> **Course group:** Core AI Concepts & Solution Patterns  
> **Sub-course:** Core AI & Machine Learning Fundamentals  
> **Section:** How core AI terms relate
>
> **Purpose:** Section này giúp bạn xây một “bản đồ thuật ngữ” trước khi học sâu. Đây là study guide tổng hợp, không phải transcript nguyên văn của PartnerU.

---

# 1. Section objective

Sau section này, bạn cần có thể:

- phân biệt **AI, Machine Learning, Deep Learning, Generative AI và LLM**;
- hiểu những thuật ngữ này **lồng vào nhau** như thế nào;
- không dùng “AI”, “model”, “LLM”, “ChatGPT” như từ đồng nghĩa;
- hiểu **model**, **application** và **AI system** khác nhau;
- giải thích các khái niệm cho customer mà không cần quá nhiều toán.

---

# 2. Big picture

Hãy bắt đầu bằng bản đồ này:

```text
Artificial Intelligence (AI)
│
├── Rule-based / symbolic approaches
│
└── Machine Learning (ML)
    │
    └── Deep Learning
        │
        ├── Computer vision models
        ├── Speech/audio models
        ├── Other neural models
        │
        └── Generative AI
            │
            ├── Text
            ├── Image
            ├── Audio
            ├── Video
            └── Large Language Models (LLMs)
```

Đây là **mental model đơn giản hóa** để học.

Điểm quan trọng:

> **AI là khái niệm rộng nhất. LLM chỉ là một loại model trong thế giới AI.**

---

# 3. Artificial Intelligence — AI

## 3.1. AI là gì?

**Artificial Intelligence** là thuật ngữ rộng chỉ các hệ thống máy tính thực hiện những task mà ta thường liên hệ với “intelligence”, ví dụ:

- nhận diện pattern;
- hiểu/ngôn ngữ;
- lập kế hoạch;
- dự đoán;
- reasoning;
- ra recommendation;
- tạo nội dung;
- thực hiện task.

AI không nhất thiết phải “học” từ data theo cách Machine Learning.

Ví dụ lịch sử:

```text
IF condition A
THEN action B
```

Một rule-based expert system vẫn có thể được gọi là AI, dù không train neural network.

---

# 4. Machine Learning — ML

## 4.1. ML là gì?

**Machine Learning** là một nhánh của AI trong đó hệ thống học pattern từ data thay vì người lập trình viết mọi rule cụ thể.

Traditional programming:

```text
Rules + Data
    ↓
Output
```

Machine learning:

```text
Data + Desired examples/objective
        ↓
Learning algorithm
        ↓
Model
        ↓
New input → prediction/output
```

---

## 4.2. Ví dụ đơn giản

Muốn phân loại email spam.

### Rule-based

Developer viết:

```text
if contains("FREE MONEY"):
    spam = true
```

Problem:

- rule cứng;
- khó cover tất cả variation;
- attacker/user language thay đổi.

### Machine learning

Cho system nhiều email có label:

```text
Email A → spam
Email B → not spam
Email C → spam
...
```

Model học statistical patterns rồi dự đoán email mới.

---

# 5. Deep Learning

## 5.1. Deep learning là gì?

**Deep Learning** là một nhánh của Machine Learning sử dụng **neural networks có nhiều layer**.

Mental model:

```text
AI
└── ML
    └── Deep Learning
```

Deep learning đặc biệt thành công với:

- language;
- image;
- speech;
- audio;
- complex pattern recognition.

---

# 6. Neural network

Bạn không cần học toán sâu ở section này.

Có thể hiểu:

> Neural network là một mô hình toán học gồm nhiều đơn vị/layer liên kết, với rất nhiều numerical parameters được điều chỉnh trong quá trình training để học pattern.

Simplified:

```text
Input
↓
Layer
↓
Layer
↓
Layer
↓
Output
```

“Deep” nghĩa là có nhiều layer xử lý nối tiếp.

---

# 7. Generative AI

## 7.1. Generative AI là gì?

Generative AI là AI có khả năng tạo ra nội dung mới, ví dụ:

- text;
- code;
- image;
- audio;
- video;
- structured data.

Khác với model chỉ phân loại:

```text
Input image
→ cat / dog
```

Generative model có thể:

```text
Prompt
→ new text/image/code/audio
```

---

# 8. Generative vs predictive AI

Không nên hiểu rằng generative AI “không dự đoán”.

Ở mức technical, generation thường dựa vào prediction.

Nhưng business vocabulary thường tách:

### Predictive AI

Dự đoán category/value/outcome.

Examples:

- fraud score;
- demand forecast;
- churn likelihood.

### Generative AI

Tạo artifact/output.

Examples:

- email;
- report;
- code;
- image.

Trong modern AI systems, hai kiểu capability có thể coexist.

---

# 9. Large Language Model — LLM

## 9.1. LLM là gì?

**Large Language Model** là một model được train trên lượng lớn data để học các pattern liên quan đến language và có thể thực hiện nhiều language-related tasks.

Một intuition quan trọng:

> LLM không phải “database chứa câu trả lời”.

Nó là model đã học statistical/semantic patterns trong data.

Nó có thể:

- generate;
- summarize;
- translate;
- classify;
- extract;
- answer;
- reason;
- write code;
- use tools khi application cho phép.

---

# 10. Vì sao gọi là “Large”?

“Large” thường liên quan đến scale của:

- model parameters;
- training data;
- compute.

Nhưng:

> “Large” không phải business metric.

Customer quan tâm hơn:

- capability;
- quality;
- latency;
- cost;
- reliability;
- fit for task.

---

# 11. Transformer

Bạn có thể nghe từ:

> **Transformer**

Transformer là một neural-network architecture rất quan trọng trong modern language models.

Không cần học full mathematics để làm partner.

Hãy nhớ:

```text
Transformer
=
architecture family
```

Trong khi:

```text
LLM
=
a language model category
```

Một LLM có thể được xây dựa trên transformer architecture.

---

# 12. Foundation model

**Foundation model** = model được train ở quy mô lớn trên broad data/capabilities và có thể làm nền tảng cho nhiều downstream tasks.

Thay vì:

```text
one model
→ one narrow task
```

foundation model có thể:

```text
one broad model
→ summarization
→ extraction
→ coding
→ analysis
→ conversation
→ tool-use workflows
```

Nó trở thành “foundation” để xây applications.

---

# 13. Multimodal AI

**Multimodal** nghĩa là hệ thống/model có thể làm việc với nhiều modality.

Modalities có thể gồm:

- text;
- image;
- audio;
- video.

Ví dụ:

```text
Image + text instruction
→ text analysis
```

Hoặc:

```text
Audio
→ transcription / understanding
```

Multimodal ≠ multi-model.

Hai thuật ngữ khác nhau.

---

# 14. Reasoning

Bạn sẽ nghe:

> “reasoning model” hoặc “reasoning capability”.

Trong partner context, reasoning thường mô tả khả năng xử lý các task cần:

- multi-step thinking;
- planning;
- constraint handling;
- analysis;
- problem solving.

Điều quan trọng:

> Đừng biến “reasoning” thành một magic word.

Hãy chuyển nó thành task cụ thể:

- analyze contract differences;
- debug code;
- plan workflow;
- solve multi-step business problem.

---

# 15. Model vs application vs system

Đây là distinction cực quan trọng.

## Model

Core learned capability.

```text
Input → model → output
```

## Application

Software sử dụng model.

Ví dụ:

```text
UI
+ backend
+ model API
```

## AI system

Rộng hơn:

```text
Model
+ prompts/instructions
+ data
+ retrieval
+ tools
+ permissions
+ business logic
+ human review
+ monitoring
```

Customer outcome thường đến từ **system**, không phải model alone.

---

# 16. ChatGPT ≠ LLM

Một lỗi rất phổ biến.

**LLM** = loại model.

**ChatGPT** = product/application experience có thể sử dụng nhiều models/capabilities/tools.

Analogy:

```text
Engine
≠
Car
```

Model giống “engine” theo một mức abstraction.

Product là toàn bộ trải nghiệm/hệ thống.

Analogy không hoàn hảo, nhưng dễ nhớ.

---

# 17. AI agent nằm ở đâu?

**Agent** thường không phải chỉ một model.

Một agentic system có thể gồm:

```text
Model
+ Goal
+ Instructions
+ Tools
+ State/context
+ Control loop
+ Permissions
+ Evaluation
```

Agent có thể:

1. hiểu goal;
2. quyết định next step;
3. gọi tool;
4. quan sát result;
5. tiếp tục;
6. complete hoặc escalate.

Do đó:

> Agent là **system pattern**, không nên đồng nhất với LLM.

---

# 18. Retrieval-Augmented Generation — RAG

Bạn có thể nghe:

> RAG.

RAG là pattern trong đó application tìm/retrieve relevant information rồi cung cấp nó làm context cho model trước khi model tạo output.

Simplified:

```text
User asks
↓
Search company knowledge
↓
Retrieve relevant documents
↓
Give context to model
↓
Generate grounded response
```

RAG không “train lại” model mỗi lần.

Đây là distinction rất quan trọng.

---

# 19. Embeddings nằm ở đâu?

**Embedding** là numerical representation của content.

Có thể hiểu:

```text
Text/image
→ vector of numbers
```

Các content có ý nghĩa gần nhau có thể có vector relationship hữu ích cho:

- semantic search;
- retrieval;
- clustering;
- recommendation.

Embedding model ≠ chat model.

---

# 20. Taxonomy summary

```text
AI
│
├── ML
│   └── Deep Learning
│       └── Foundation / Generative models
│           └── LLMs
│
└── Applications / systems built using models
    ├── Chat experiences
    ├── RAG applications
    ├── Agents
    ├── Coding tools
    └── Enterprise workflows
```

---

# 21. Developer mental model

Nếu bạn là Frontend Developer:

```text
React
≠
Web application
```

Một web app còn có:

- backend;
- DB;
- auth;
- APIs;
- business logic.

Tương tự:

```text
LLM
≠
AI solution
```

AI solution còn có:

- orchestration;
- context;
- tools;
- evals;
- controls;
- UI;
- human workflow.

---

# 22. Partner lens

Customer nói:

> “Chúng tôi cần một LLM.”

Không nên assume họ thực sự cần “LLM” như requirement.

Hỏi:

- task gì?
- input gì?
- output gì?
- data gì?
- action gì?
- latency?
- risk?
- success metric?

Có thể họ cần:

- retrieval;
- classification;
- speech;
- vision;
- workflow automation;
- combination.

Partner nên map **business need → capability**, không map buzzword → product.

---

# 23. Common confusions

## AI = ML?

Không hoàn toàn.

ML là subset của AI.

## ML = Deep Learning?

Không.

Deep learning là subset của ML.

## Generative AI = LLM?

Không.

LLM là một loại generative model; generative AI còn có image/audio/video models.

## LLM = ChatGPT?

Không.

LLM là model category; ChatGPT là product.

## Model = agent?

Không.

Agent thường là system sử dụng model + tools + loop.

## RAG = fine-tuning?

Không.

RAG cung cấp context at runtime; fine-tuning thay đổi model behavior/weights through training.

---

# 24. English–Vietnamese glossary

| Term | Nghĩa dễ hiểu |
|---|---|
| **Artificial Intelligence (AI)** | Trí tuệ nhân tạo — umbrella term rộng |
| **Machine Learning (ML)** | Máy học — học pattern từ data |
| **Deep Learning** | ML dùng neural networks nhiều layer |
| **Neural network** | Mô hình mạng nơ-ron |
| **Generative AI** | AI tạo nội dung mới |
| **LLM** | Large Language Model |
| **Transformer** | Kiến trúc neural network quan trọng |
| **Foundation model** | Model nền tảng broad-purpose |
| **Multimodal** | Xử lý nhiều loại dữ liệu/modality |
| **Reasoning** | Khả năng xử lý vấn đề nhiều bước |
| **Agent** | System thực hiện nhiều bước/tool hướng tới goal |
| **RAG** | Retrieval-Augmented Generation |
| **Embedding** | Biểu diễn content dưới dạng vector số |
| **Application** | Ứng dụng sử dụng model |
| **AI system** | Toàn hệ thống model + data + tools + controls |

---

# 25. Section recap

Hãy nhớ bản đồ:

```text
AI
└─ ML
   └─ Deep Learning
      └─ Generative / Foundation Models
         └─ LLMs
```

Và ba distinction quan trọng:

```text
LLM ≠ ChatGPT
Model ≠ AI system
Agent ≠ just a model
```

Business rule:

> **Start from the customer task, not from the buzzword.**

---

# 26. Self-check

1. AI, ML và Deep Learning quan hệ với nhau thế nào?
2. Generative AI và LLM khác nhau gì?
3. ChatGPT và LLM khác nhau gì?
4. RAG có train lại model không?
5. Tại sao agent nên được coi là system pattern?
6. Hãy giải thích “foundation model” bằng lời của bạn.
