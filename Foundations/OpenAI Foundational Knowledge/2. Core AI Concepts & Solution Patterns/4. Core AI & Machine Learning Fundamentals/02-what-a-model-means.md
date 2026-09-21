# 02 — What “a Model” Means

> **Course:** OpenAI Foundational Knowledge  
> **Sub-course:** Core AI & Machine Learning Fundamentals  
> **Section:** What “a model” means

---

# 1. Section objective

Sau section này, bạn cần:

- hiểu “model” nghĩa là gì trong Machine Learning;
- hiểu model khác code/database/rule engine như thế nào;
- hiểu **parameters/weights**, training và inference ở mức intuition;
- biết vì sao model output có thể không deterministic;
- hiểu model là một component, không phải toàn bộ AI solution.

---

# 2. Big picture

Một definition dễ nhớ:

> **Model là một mathematical system đã học patterns từ data và dùng các learned parameters để chuyển input thành prediction/output.**

Simplified:

```text
Input
  ↓
Model
  ↓
Output
```

Model behavior đến từ:

- architecture;
- learned parameters;
- training;
- runtime input/context.

---

# 3. Model trong software truyền thống

Trong programming truyền thống:

```js
function calculateVAT(price, rate) {
  return price * rate;
}
```

Developer viết explicit logic.

Nếu input giống nhau:

```text
same input
→ same deterministic calculation
```

---

# 4. Model trong Machine Learning

Trong ML, developer không viết từng rule của behavior.

Thay vào đó:

```text
Training data
+ Objective
+ Learning process
        ↓
Learned parameters
        ↓
Model
```

Model học relation/pattern.

Ví dụ image classifier:

```text
Image
→ model
→ probability(cat), probability(dog)
```

---

# 5. Model is not a database

Đây là misconception cực phổ biến.

Database:

```text
key/query
→ stored data
```

Model:

```text
input
→ learned computation
→ generated/predicted output
```

LLM không hoạt động như:

> “Tìm đúng câu trả lời đã lưu trong bảng.”

Nó tạo output dựa trên learned patterns + context hiện tại.

Do đó model có thể:

- generalize;
- combine patterns;
- generate novel output;
- sometimes produce incorrect/unsupported output.

---

# 6. Parameters / weights

Bạn sẽ nghe:

> parameters / weights.

Có thể hiểu mỗi parameter là một numerical value bên trong model.

Training điều chỉnh rất nhiều values này.

Simplified:

```text
Before training:
weights ≈ unhelpful values

Training:
compare prediction with objective
→ update weights
→ repeat

After training:
weights encode learned patterns
```

Không nên nói:

> “Parameter là một fact model nhớ.”

Một parameter riêng lẻ thường không tương ứng với một fact đơn giản.

Knowledge/behavior được distributed across model representation.

---

# 7. Architecture vs weights

Hai model concepts:

## Architecture

Blueprint/cấu trúc computation.

Analogy:

```text
architecture = thiết kế của engine
```

## Weights

Learned numerical settings.

Analogy:

```text
weights = configuration learned through training
```

Hai model có thể dùng architecture tương tự nhưng weights/training khác.

---

# 8. Model checkpoint

Bạn có thể nghe:

> **checkpoint**

Checkpoint là snapshot của model parameters tại một thời điểm trong training/development.

Một released model thường xuất phát từ một trained checkpoint + additional post-training/safety/system work.

Partner không cần sử dụng term này thường xuyên với business customer.

---

# 9. Base model

**Base model** thường chỉ model sau broad pretraining trước một số bước post-training chuyên để model follow instruction/safety preferences.

Mental model:

```text
Large-scale pretraining
→ base capability
→ post-training
→ more useful/aligned behavior
```

Exact development pipeline có thể khác theo model/provider.

Đừng giả định mọi model dùng cùng process.

---

# 10. Model input

Model nhận một representation của input.

Trong language models, text được xử lý thành **tokens**.

Ví dụ conceptually:

```text
"OpenAI is useful"
↓
tokens
↓
model computation
```

Token không nhất thiết = word.

Một word có thể:

- là một token;
- chia thành nhiều token;
- punctuation có thể là token.

---

# 11. Model output

LLM thường tạo output token-by-token.

Simplified:

```text
Context
↓
Predict next token distribution
↓
Choose token
↓
Add to context
↓
Predict next
↓
...
```

Đây là intuition quan trọng.

Nó giải thích một phần vì sao generation:

- flexible;
- context-sensitive;
- probabilistic.

---

# 12. Probability distribution

Model không nhất thiết nói:

> “Câu trả lời duy nhất là X.”

Thay vào đó, ở mỗi bước nó có distribution:

```text
Token A → probability
Token B → probability
Token C → probability
...
```

Generation process chọn token dựa trên distribution và decoding/settings.

Do đó variation có thể xuất hiện.

---

# 13. Deterministic vs probabilistic

Traditional deterministic function:

```text
2 + 2 → 4
```

Generative model:

```text
"Write a product headline"
→ many acceptable outputs
```

Điều này không có nghĩa model “random hoàn toàn”.

Output được strongly conditioned bởi:

- model;
- prompt;
- system/developer instruction;
- context;
- sampling settings;
- tool results.

---

# 14. Inference

**Inference** = dùng model đã train để xử lý input mới và tạo prediction/output.

Training:

```text
learn parameters
```

Inference:

```text
use parameters
```

Developer gọi OpenAI API để model trả response = inference.

---

# 15. Model vs prompt

Prompt không phải model.

Prompt = runtime input/instruction.

```text
Model
+
Prompt
=
Specific behavior in this interaction
```

Cùng model:

```text
Prompt A → summarize
Prompt B → classify
Prompt C → code
```

Đây là sức mạnh của foundation models.

---

# 16. Model vs context

Context là information model có trong một request/session.

Có thể gồm:

- instructions;
- conversation;
- documents;
- tool outputs;
- images.

Model weights không tự thay đổi chỉ vì bạn cung cấp context.

Important:

```text
Context at inference
≠
training model weights
```

---

# 17. Context window

**Context window** = lượng input/context mà model có thể consider trong một request/workflow, thường được đo bằng tokens.

Nếu context window lớn:

- có thể đưa nhiều documents/history hơn.

Nhưng:

> larger context ≠ automatically better answer.

Cần:

- relevant context;
- clear instructions;
- retrieval strategy;
- evals.

---

# 18. Model vs memory

Product/application “memory” có thể là system feature lưu/retrieve user context.

Đừng assume:

> model weights update mỗi khi product remembers something.

Application memory và model training là hai khái niệm khác.

---

# 19. Model vs tool

Model có thể decide/request tool use.

Tool có thể:

- query DB;
- call API;
- search;
- execute code;
- update system.

But:

```text
Model
≠
Tool
```

System orchestrates relationship.

Example:

```text
User: What's my order status?
↓
Model recognizes need
↓
Tool call: getOrder(id)
↓
Backend returns current status
↓
Model explains result
```

Current order status không cần “nằm trong model.”

---

# 20. Model vs knowledge source

Nếu business data thay đổi mỗi ngày:

Không nên cố “teach” mọi thay đổi vào model weights.

Có thể dùng:

- retrieval;
- database;
- API;
- tool.

This leads to critical architecture rule:

> **Use the right mechanism for the right kind of knowledge.**

---

# 21. Model capability vs system capability

Model có thể có capability:

> reason about text.

System capability có thể là:

> resolve a support case.

System cần:

```text
Model
+ customer data
+ policy
+ tools
+ permissions
+ workflow
+ evals
```

Không claim system outcome từ model capability alone.

---

# 22. Model quality is multidimensional

Không có một metric “model good”.

Có thể evaluate:

- reasoning quality;
- coding;
- instruction following;
- factuality;
- latency;
- cost;
- tool use;
- modality;
- safety behavior.

Model selection = trade-offs.

---

# 23. Developer mental model

Nếu frontend:

### Library

React gives capability.

### Application

Your product adds:

- state;
- backend;
- auth;
- UX;
- data.

Tương tự:

### Model

Gives intelligence capability.

### AI application

Adds:

- context;
- integration;
- workflow;
- controls.

---

# 24. Example — Support

Model alone:

```text
Prompt:
"How do I reset password?"
```

Could answer generally.

Enterprise system:

```text
User identity
↓
Approved company policy
↓
Account state
↓
Model reasoning
↓
Reset tool
↓
Permissions
↓
Audit log
```

The business capability comes from the entire system.

---

# 25. Common misconceptions

## “Model knows everything.”

No.

Models have limitations, training cutoffs/context constraints, and may lack current/private data.

## “Model is internet search.”

No.

Search can be a tool.

## “If I paste data, model learns it permanently.”

Not equivalent to training.

## “A bigger model is always better.”

Not necessarily for cost/latency/task fit.

## “Same model = same application behavior.”

No.

System prompt, tools, context, safety controls and orchestration matter.

---

# 26. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| **Model** | Mô hình học pattern và tạo prediction/output |
| **Parameter / weight** | Giá trị số được học trong model |
| **Architecture** | Cấu trúc tính toán của model |
| **Checkpoint** | Snapshot parameters của model |
| **Base model** | Model nền sau broad training trước một số post-training |
| **Token** | Đơn vị representation của text cho model |
| **Inference** | Dùng model đã train để xử lý input |
| **Context** | Information model được cung cấp ở runtime |
| **Context window** | Giới hạn context model có thể xử lý |
| **Prompt** | Input/instruction gửi tới model |
| **Probability distribution** | Phân phối xác suất các output candidate |
| **Deterministic** | Cùng input → behavior cố định |
| **Probabilistic** | Output được tạo dựa trên xác suất/model distribution |

---

# 27. Section recap

1. Model là learned mathematical system.
2. ML model behavior đến từ parameters learned during training.
3. Model không phải database.
4. Prompt/context không phải model weights.
5. Training ≠ inference.
6. Model ≠ application/system.
7. Tool access mở rộng system capability mà không cần knowledge nằm trong model.
8. Business outcome phải đánh giá ở system level.

Mental model:

```text
TRAINING
data → learned parameters

INFERENCE
input + context → model → output

SOLUTION
model + data + tools + workflow + controls → outcome
```

---

# 28. Self-check

1. Model khác database như thế nào?
2. Parameter/weight là gì?
3. Training và inference khác gì?
4. Context window là gì?
5. Tại sao prompt không “train model”?
6. Hãy giải thích model capability vs system capability.
