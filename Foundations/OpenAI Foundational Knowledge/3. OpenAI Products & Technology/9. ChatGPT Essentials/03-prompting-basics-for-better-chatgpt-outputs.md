# 03 — Prompting Basics for Better ChatGPT Outputs

> **Course:** OpenAI Foundational Knowledge  
> **Course:** ChatGPT Essentials  
> **Section:** Prompting basics for better ChatGPT outputs
>
> **Source note:** OpenAI Academy's current prompting guidance emphasizes clear task instructions, useful context, desired output and iteration. There is no single perfect prompt.

---

# 1. Section objective

Sau section này, bạn cần:

- hiểu prompt là gì;
- biết framework đơn giản để viết prompt tốt;
- biết cung cấp context, constraints, audience và output format;
- biết dùng examples/files;
- hiểu prompting là iterative conversation, không phải magic formula.

---

# 2. What is a prompt?

A prompt is the input/instruction you give ChatGPT.

It may include:

- text;
- image;
- audio;
- file.

Prompt tells ChatGPT:

> “What do I need from you in this context?”

---

# 3. Big picture

OpenAI Academy uses a simple pattern:

```text
TASK
+
CONTEXT
+
OUTPUT
```

A stronger practical extension:

```text
Task
+ Context
+ Audience
+ Constraints
+ Output format
+ Source/reference material
```

Not every prompt needs all fields.

Use what improves clarity.

---

# 4. Step 1 — State the task

Weak:

> Help with this.

Better:

> Summarize this document.

Stronger:

> Summarize this document into five key decisions and three open questions.

Use an action verb:

- summarize;
- compare;
- draft;
- analyze;
- explain;
- rewrite;
- classify;
- extract.

---

# 5. Step 2 — Give context

Context helps ChatGPT understand:

- why;
- who;
- background;
- domain;
- current situation.

Example:

> I am preparing a five-minute update for a product leadership meeting.

Now the model can tailor output.

---

# 6. Step 3 — Specify audience

Same information changes by audience.

Example:

```text
Explain RAG
for:
- developer
- CFO
- new employee
```

Different terminology and detail are appropriate.

---

# 7. Step 4 — Specify output

Examples:

- five bullets;
- Markdown table;
- executive summary;
- email draft;
- JSON;
- checklist.

If you know the desired shape, say it.

---

# 8. Step 5 — Add constraints

Useful constraints:

- length;
- tone;
- language;
- must include;
- must avoid;
- source limitations.

Example:

> Keep it under 200 words and avoid technical jargon.

Constraints reduce ambiguity.

---

# 9. Step 6 — Provide source material

If task depends on specific facts:

- upload file;
- paste content;
- provide project context;
- ask ChatGPT to use connected source.

Say explicitly:

> Base the answer only on the attached file.

This reduces silent generalization.

---

# 10. Step 7 — Define uncertainty behavior

For important work:

> If the source does not support a claim, say so instead of guessing.

This is a powerful reliability instruction.

---

# 11. A reusable prompt template

```text
Task:
[What should ChatGPT do?]

Context:
[What should it know?]

Audience:
[Who is this for?]

Requirements:
[Must include / avoid / constraints]

Output:
[Format / length / structure]

Sources:
[Use these files/data if applicable]
```

---

# 12. Example — Weak vs strong

Weak:

> Write a project update.

Better:

```text
Draft a weekly project update for senior leadership.

Context:
The migration is one week behind because vendor access was delayed.
Testing is now 70% complete.
No budget impact so far.

Include:
- overall status;
- progress;
- top risk;
- next steps.

Use a concise professional tone.
Max 180 words.
```

---

# 13. Prompting is not one-shot

OpenAI Academy emphasizes iteration.

First answer not ideal?

Follow up:

- make shorter;
- add examples;
- compare alternatives;
- explain assumption;
- change tone;
- use a table;
- verify claim.

Conversation itself is part of prompting.

---

# 14. Use critique/refinement

Pattern:

```text
Draft
↓
Critique
↓
Improve
```

Example:

> Review this draft for unclear claims, then rewrite it.

This is useful for writing and analysis.

---

# 15. Ask for options

Instead of:

> Give me the answer.

Try:

> Give me three approaches with trade-offs.

Useful when decision is ambiguous.

---

# 16. Ask ChatGPT to ask questions

When context is missing:

> Before drafting, ask me up to three questions needed to produce a strong result.

Good for:

- strategy;
- planning;
- complex writing.

But don't use unnecessarily for simple tasks.

---

# 17. Examples / few-shot prompting

Show desired pattern.

```text
Example input:
...

Desired output:
...

Now do the same for:
...
```

Useful for:

- style;
- format;
- classification;
- structured extraction.

---

# 18. Role prompting — use carefully

A role can clarify perspective:

> Act as a technical reviewer.

But role alone is weak.

Better:

```text
Role
+ exact task
+ criteria
+ context
```

Don't rely on dramatic persona prompts.

---

# 19. Prompt with success criteria

Example:

> A good answer should identify the root cause, list evidence, and distinguish fact from hypothesis.

This makes quality expectations explicit.

---

# 20. Prompt with comparison criteria

Instead of:

> Compare A and B.

Use:

> Compare A and B on cost, implementation effort, security and time-to-value.

Now comparison is targeted.

---

# 21. Prompting with files

Good pattern:

```text
Use the attached report.

1. Extract all KPIs.
2. Identify changes >10%.
3. Cite the section/page if available.
4. Do not add outside facts.
```

This is much stronger than:

> Analyze this.

---

# 22. Prompting for current information

For time-sensitive work:

> Search for current information and cite sources.

Then verify:

- date;
- source authority;
- context.

Current facts should not rely only on static model knowledge.

---

# 23. Prompting for data analysis

Specify:

- question;
- definitions;
- expected output;
- checks.

Example:

> Analyze the uploaded CSV. First summarize columns and missing values, then compare monthly revenue by region. Flag any assumptions.

---

# 24. Prompting for code

Include:

- language/framework;
- existing code;
- constraints;
- desired behavior;
- error;
- test expectation.

Weak:

> Fix my React app.

Strong:

> In this React component, the modal closes immediately after submit. Identify the cause, propose the smallest fix, and include a test case.

---

# 25. Prompting for brainstorming

Give decision space.

Example:

> Generate 10 ideas, grouped into low-effort, medium-effort and experimental. Avoid ideas requiring new headcount.

Constraints improve usefulness.

---

# 26. Avoid prompt superstition

No magic phrase guarantees correctness.

Examples of bad beliefs:

- “Act as a genius” makes model factual.
- caps lock improves intelligence.
- one huge persona replaces context.
- “be 100% accurate” guarantees accuracy.

Reliability comes from:

```text
clear task
+ evidence
+ tools
+ verification
```

---

# 27. Long prompt vs short prompt

Use enough detail to remove relevant ambiguity.

Do not add irrelevant instructions.

```text
Clarity > length
```

Modern models can handle complex instructions, but unnecessary complexity can still confuse task intent.

---

# 28. Prompt hierarchy intuition

In products/APIs, behavior can be influenced by different instruction/context layers.

As a normal ChatGPT user, focus on:

- clear request;
- relevant context;
- explicit output requirements.

You don't need to learn internal prompt hierarchy to be productive.

---

# 29. Prompting framework — TACO

Easy memory:

## T — Task
What do you want done?

## A — Audience
Who is output for?

## C — Context & constraints
What should ChatGPT know and obey?

## O — Output
What format/result?

TACO is a study mnemonic, not official OpenAI terminology.

---

# 30. Add EVIDENCE for important work

```text
TACO
+
Evidence
```

Ask:

- What sources?
- What assumptions?
- What needs verification?

This separates good prompting from overtrust.

---

# 31. Common mistakes

1. Vague task.
2. No audience.
3. No output requirement.
4. Too much irrelevant context.
5. No source grounding.
6. Treat first answer as final.
7. Ask for “100% accuracy” instead of evidence.
8. Over-engineer prompts.
9. Use persona instead of requirements.

---

# 32. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Prompt | Yêu cầu/input đưa cho ChatGPT |
| Context | Bối cảnh |
| Constraint | Ràng buộc |
| Audience | Đối tượng đọc |
| Output format | Dạng output |
| Few-shot | Đưa ví dụ mẫu |
| Iteration | Lặp/chỉnh dần |
| Refinement | Tinh chỉnh |
| Success criteria | Tiêu chí output tốt |
| Grounding | Bám vào nguồn |
| Assumption | Giả định |

---

# 33. Section recap

Prompting basics:

```text
TASK
+ CONTEXT
+ OUTPUT
```

Practical mnemonic:

```text
TACO

Task
Audience
Context & constraints
Output
```

For important work:

```text
TACO + evidence + verification
```

Core rule:

> **A good prompt reduces ambiguity; a good workflow also verifies the result.**

---

# 34. Self-check

1. Task, context và output khác nhau thế nào?
2. Khi nào cần audience?
3. Few-shot prompting dùng khi nào?
4. Tại sao iteration quan trọng?
5. “Be 100% accurate” có đủ không?
6. Viết lại một prompt yếu bằng TACO.
