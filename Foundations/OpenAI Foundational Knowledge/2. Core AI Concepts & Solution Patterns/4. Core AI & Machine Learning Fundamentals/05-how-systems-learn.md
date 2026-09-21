# 05 — How Systems Learn

> **Course:** OpenAI Foundational Knowledge  
> **Sub-course:** Core AI & Machine Learning Fundamentals  
> **Section:** How Systems Learn
>
> **Scope:** Giải thích machine learning training ở mức partner/developer foundation. Đây không phải tài liệu toán học chuyên sâu và không mô tả các chi tiết proprietary chưa được OpenAI công khai.

---

# 1. Section objective

Sau section này, bạn cần:

- hiểu “learning” trong ML nghĩa là gì;
- phân biệt rules programming với learning from data;
- hiểu training loop, loss/objective và parameter update ở mức intuition;
- hiểu supervised, unsupervised/self-supervised và reinforcement learning ở mức cơ bản;
- hiểu pretraining, post-training, fine-tuning và inference;
- phân biệt **learning during training** với **context/memory at runtime**.

---

# 2. Big picture

Traditional software:

```text
Human writes rules
+ Data
→ Output
```

Machine learning:

```text
Data/examples
+ Learning objective
+ Algorithm
→ Learned model
```

Sau training:

```text
New input
→ Trained model
→ Prediction/output
```

“Learn” ở đây nghĩa:

> **Model parameters được điều chỉnh để system thực hiện objective tốt hơn trên patterns trong data.**

---

# 3. A simple learning example

Task:

> Predict house price.

Training examples:

```text
size, rooms, location → actual price
```

Model bắt đầu với poor parameters.

Training loop:

```text
Input example
↓
Model predicts
↓
Compare with correct result
↓
Calculate error
↓
Adjust parameters
↓
Repeat
```

Sau nhiều examples:

Model học relationships hữu ích.

---

# 4. Training objective

Model cần biết:

> “Tốt hơn” nghĩa là gì?

Đó là role của **objective/loss**.

**Loss** là numerical signal thể hiện model output khác desired target như thế nào.

Simplified:

```text
small loss → better
large loss → worse
```

Training algorithm cố gắng giảm loss.

---

# 5. Gradient descent — intuition

Bạn có thể nghe:

> **gradient descent**

Không cần calculus để hiểu principle.

Analogy:

Bạn đứng trên đồi trong sương và muốn xuống thấp.

1. cảm nhận hướng dốc;
2. bước xuống;
3. đo lại;
4. lặp.

ML:

```text
current weights
↓
measure loss
↓
calculate direction to reduce loss
↓
update weights
↓
repeat
```

Đây là oversimplified intuition, nhưng đủ cho foundation.

---

# 6. Epoch / batch

### Batch

Một nhóm training examples được xử lý cùng.

### Epoch

Một pass qua training dataset theo definition của training process.

Trong large foundation-model training, implementation phức tạp hơn nhiều; partner không cần dùng term này trừ khi relevant.

---

# 7. Supervised learning

Training data có explicit target/label.

Example:

```text
Email → spam
Email → not spam
```

Hoặc:

```text
Input prompt
→ desired response
```

System learns mapping.

Use cases:

- classification;
- extraction;
- supervised fine-tuning.

---

# 8. Unsupervised learning

Broad category nơi data không có explicit labels như supervised learning.

Goal có thể là tìm:

- structure;
- clusters;
- representation.

Modern foundation model training often uses methods better described as **self-supervised** rather than simply unsupervised.

---

# 9. Self-supervised learning

System tạo learning signal từ data itself.

For language-model intuition:

```text
Text:
"Paris is the capital of ..."

Use surrounding sequence
to learn prediction objective.
```

Không cần human label mỗi token.

Đây là reason models có thể train trên broad text at huge scale.

---

# 10. Pretraining for language models

Simplified:

```text
Large corpus
↓
Tokenize
↓
Predict patterns/tokens
↓
Update parameters
↓
Repeat at scale
↓
Broad language/world-pattern capability
```

Important nuance:

Pretraining is not:

> “copy data into a database.”

It changes learned parameters.

---

# 11. What does a language model learn?

Not a neat list of facts.

It learns distributed statistical representations/patterns related to:

- language;
- syntax;
- concepts;
- relationships;
- code;
- formats;
- patterns in data.

This enables generalization.

But it also means:

- facts may be imperfect;
- outputs may be uncertain;
- model may generate plausible errors.

---

# 12. Generalization

**Generalization** = model can perform on new examples not exactly seen during training.

Example:

Train on many coding patterns.

Then model can help with a new codebase.

Generalization is one of the reasons ML is powerful.

But:

> Generalization quality varies by task/context.

---

# 13. Overfitting

**Overfitting** = model fits training examples too closely and performs poorly on new data.

Mental model:

```text
Memorizes training specifics
instead of learning useful general pattern
```

Hence evaluation uses data separate from training where possible.

---

# 14. Training / validation / test data

Typical ML concept:

## Training set
Used to learn.

## Validation set
Used to tune choices.

## Test set
Used for final/independent evaluation.

Exact practice varies.

Core lesson:

> Don't evaluate only on examples model learned from.

---

# 15. Post-training

After broad pretraining, models may undergo additional training processes to improve useful behavior.

Goals may include:

- instruction following;
- preferred response behavior;
- safety;
- specific capabilities.

Mental model:

```text
Pretraining
→ broad capability

Post-training
→ shape behavior/usefulness
```

---

# 16. Fine-tuning

Fine-tuning adapts model using additional training data/objectives.

Example:

A company needs consistent structured output style.

Training examples:

```text
Input A → desired format
Input B → desired format
...
```

Fine-tuning can improve recurring behavior.

But fine-tuning is not always necessary.

---

# 17. Prompting vs fine-tuning vs RAG

This is a critical table.

| Need | Candidate mechanism |
|---|---|
| Give instruction for current task | Prompt |
| Give private/current knowledge | RAG / tools / context |
| Change repeated behavior/style | Fine-tuning may help |
| Take action in system | Tools/agent |
| Measure quality | Evals |

Example:

Company policy changes weekly.

Don't fine-tune every week by default.

Better:

```text
Retrieve latest policy at runtime.
```

---

# 18. Reinforcement Learning — RL

RL learns from reward signals related to actions/behavior.

Basic loop:

```text
System takes action
↓
Receives reward/feedback
↓
Updates behavior
↓
Repeat
```

RL can be used in model post-training approaches.

Partner doesn't need proprietary pipeline details.

---

# 19. Feedback-based model improvement

You may hear terms like:

- human feedback;
- preference data;
- reward model;
- reinforcement learning.

High-level:

```text
Generate candidate behavior
↓
Evaluate/prefer behavior
↓
Use signal to improve model
```

Exact methodology evolves.

Do not claim a specific current model uses a training method unless official source supports it.

---

# 20. Training is compute-intensive

Large-model training requires:

- data;
- compute;
- distributed systems;
- optimization;
- engineering.

But enterprise customers usually do **not** train a frontier foundation model from scratch.

They consume model capability and adapt at application level.

Partner question should often be:

> “Do we need training at all?”

---

# 21. In-context learning

Foundation models can adapt behavior from examples placed in prompt/context.

Example:

```text
Example 1:
input → JSON output

Example 2:
input → JSON output

Now:
input C → ?
```

Model may follow pattern.

This is called **in-context learning**.

Important:

> It does not necessarily update model weights.

---

# 22. Few-shot / zero-shot

## Zero-shot

Give instruction, no examples.

```text
Classify sentiment: ...
```

## Few-shot

Give several examples.

```text
Example A → positive
Example B → negative
Now classify C
```

These happen at inference/context level.

Not full training.

---

# 23. Runtime context is not permanent learning

Suppose you tell AI:

> “Our internal project is called Phoenix.”

Within context, model can use that.

But:

```text
provided context
≠
weights permanently changed
```

This distinction helps understand:

- privacy;
- architecture;
- memory;
- RAG.

---

# 24. Product memory is also a separate concept

An application can store information then retrieve it later.

Conceptually:

```text
User info
→ storage
→ retrieve later
→ include in context
```

That is application-level memory.

Do not automatically call it “the model learned.”

---

# 25. Online learning

**Online learning** broadly refers to systems that update model from new data continuously or incrementally.

Do not assume hosted foundation models do this from each user interaction.

Whether/how data contributes to training is a product/data-policy question and should be verified from current official documentation.

---

# 26. Fine-tuning does not equal adding facts

This mistake is common.

If need current inventory:

```text
database/tool
```

If need latest HR policy:

```text
retrieval
```

If need specific response format/style:

```text
prompt / fine-tuning candidate
```

Choose mechanism based on problem.

---

# 27. Learning for agents

An agent may appear to “learn” because it:

- reads prior state;
- stores memory;
- retrieves history;
- uses tool results;
- adjusts plan.

But those can all occur without model weight updates.

Distinguish:

```text
Stateful adaptation
≠
model training
```

---

# 28. Model improvement vs system improvement

AI applications improve in many ways without training model:

```text
Better prompt
Better retrieval
Better tool
Better data
Better workflow
Better guardrail
Better eval
Better UI
```

This is crucial for partners.

Don't jump to:

> “We need to retrain/fine-tune.”

---

# 29. Evals close the learning/improvement loop

For customer application:

```text
Build
↓
Eval
↓
Find failure
↓
Change prompt/context/tool/model
↓
Eval again
```

This is application development learning, not necessarily model training.

---

# 30. Example — Customer support

Goal:

> Correct support responses.

Possible improvements:

### Problem: lacks current policy
Use RAG.

### Problem: output format inconsistent
Prompt/schema/fine-tune candidate.

### Problem: wrong account information
Use customer tool/API.

### Problem: quality unknown
Build evals.

### Problem: high-risk cases
Add escalation.

Only some problems require model training.

---

# 31. Example — Frontend coding assistant

AI generates React component.

Learning/training not required per project.

System can receive:

```text
Project conventions
Component examples
Design tokens
API types
```

through context/retrieval.

Then produce code.

If persistent repeated style issue exists, fine-tuning may become candidate—but only after eval evidence.

---

# 32. The full lifecycle

```text
DATA
  ↓
PRETRAINING
  ↓
BASE CAPABILITY
  ↓
POST-TRAINING
  ↓
RELEASED MODEL
  ↓
INFERENCE
  ↓
APPLICATION CONTEXT + TOOLS
  ↓
SYSTEM OUTPUT
  ↓
EVALUATION
  ↓
APPLICATION IMPROVEMENT
```

Fine-tuning can be an optional adaptation branch.

---

# 33. Partner lens

Customer says:

> “Can the AI learn our business?”

Clarify what “learn” means.

Could mean:

### A. Know our current documents
→ retrieval/context.

### B. Remember user preference
→ application memory.

### C. Follow our style
→ prompt/examples/fine-tuning.

### D. Access current systems
→ tools/APIs.

### E. Improve model weights
→ training/fine-tuning.

Same word “learn”, five different technical needs.

---

# 34. Questions partners should ask

1. Is information dynamic?
2. Does it need to be cited?
3. Is change about knowledge or behavior?
4. Does system need actions?
5. How often does data change?
6. What eval proves improvement?
7. Can prompting/retrieval solve it before training?

---

# 35. Common mistakes

## Mistake 1
Every new document requires training.

## Mistake 2
Prompt = training.

## Mistake 3
Memory = weights updated.

## Mistake 4
Fine-tuning = database.

## Mistake 5
Agent “learning” = model learning.

## Mistake 6
No held-out eval/test.

## Mistake 7
Fine-tune before defining problem/eval.

---

# 36. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| **Training** | Quá trình model học parameters |
| **Objective** | Mục tiêu training |
| **Loss** | Signal đo error |
| **Gradient descent** | Phương pháp cập nhật weights để giảm loss |
| **Batch** | Nhóm training examples |
| **Epoch** | Một lượt qua training dataset theo định nghĩa process |
| **Supervised learning** | Học từ labeled targets |
| **Self-supervised learning** | Tạo training signal từ chính data |
| **Reinforcement learning** | Học từ reward/feedback |
| **Pretraining** | Huấn luyện nền quy mô lớn |
| **Post-training** | Huấn luyện bổ sung để định hình behavior |
| **Fine-tuning** | Adapt model bằng training thêm |
| **Generalization** | Làm tốt trên examples mới |
| **Overfitting** | Fit training data quá mức |
| **Zero-shot** | Không đưa example vào prompt |
| **Few-shot** | Đưa một số examples vào prompt |
| **In-context learning** | Model thích nghi từ context mà không nhất thiết đổi weights |
| **Online learning** | Học/update liên tục từ data mới |

---

# 37. Section recap

Three layers to remember:

```text
MODEL LEARNING
pretraining / post-training / fine-tuning
→ changes learned parameters

RUNTIME ADAPTATION
prompt / context / few-shot / RAG / memory
→ usually does not change model weights

SYSTEM IMPROVEMENT
tools / workflows / evals / controls
→ improves solution without retraining model
```

Critical partner question:

> **When a customer says “learn,” what do they actually need?**

---

# 38. Self-check

1. ML “learning” nghĩa là gì?
2. Loss có vai trò gì?
3. Supervised và self-supervised learning khác nhau thế nào?
4. Pretraining và fine-tuning khác nhau gì?
5. In-context learning có nhất thiết đổi weights không?
6. Khi nào RAG phù hợp hơn fine-tuning?
7. Customer nói “AI cần học policy mới mỗi tuần” — bạn sẽ hỏi/đề xuất gì?
