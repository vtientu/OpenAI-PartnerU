# 02 — What Makes Codex Different

> **Course:** OpenAI Foundational Knowledge  
> **Course:** Codex Essentials  
> **Section:** What makes Codex different
>
> **Freshness note:** Product surfaces/capabilities reflect OpenAI public materials available on **21 September 2026**.

---

# 1. Section objective

Sau section này, bạn cần:

- hiểu điều gì biến Codex từ code assistant thành coding agent;
- hiểu role của environment, tools, agent loop và verification;
- phân biệt interactive pairing với asynchronous delegation;
- hiểu parallelism và persistent/long-running work;
- biết khi nào Codex phù hợp hơn general-purpose chat.

---

# 2. Big picture

What makes Codex different is not only:

> “It writes better code.”

The deeper difference is:

```text
Code intelligence
+
environment access
+
tool execution
+
agent loop
+
task persistence
+
verification
+
developer workflow integration
```

---

# 3. Difference 1 — Codex works against a real codebase

Generic chat can reason over pasted code.

Codex can work against repository context.

That enables:

- cross-file changes;
- dependency awareness;
- tests;
- configuration;
- conventions.

Real engineering work is repository-level.

---

# 4. Difference 2 — It can execute

Codex can use tools/commands in an environment.

Examples:

```text
npm test
npm run lint
pytest
tsc
build scripts
repo search
```

This lets Codex observe whether its work succeeds.

Execution creates feedback.

---

# 5. Difference 3 — It has an agent loop

OpenAI engineering materials describe the Codex agent loop conceptually as repeated model inference + tool execution.

Simplified:

```text
Read task
↓
inspect repo
↓
decide action
↓
run command/edit
↓
observe
↓
decide again
↓
finish
```

This is the core agentic pattern.

---

# 6. Difference 4 — Verification is built into the workflow

Instead of only producing code:

```text
generate
→ test
→ inspect
→ fix
```

Codex can use:

- tests;
- type checks;
- linters;
- build output;
- screenshots/browser in supported workflows.

This can raise confidence.

But:

> Passing tests ≠ proof of all correctness.

Human review remains necessary.

---

# 7. Difference 5 — Interactive + asynchronous modes

Traditional assistant:

```text
developer asks
→ waits
→ receives answer
```

Codex can support both:

### Interactive pairing
Work together in IDE/CLI.

### Asynchronous delegation
Assign task and review later.

This matters because not all work requires continuous human attention.

---

# 8. Interactive pairing

Best for:

- quick iteration;
- exploration;
- debugging;
- design conversation;
- targeted edits.

The developer remains closely involved.

---

# 9. Asynchronous delegation

Best for:

- well-scoped tasks;
- test generation;
- migrations;
- refactors;
- background investigation.

Pattern:

```text
Delegate
↓
agent works
↓
engineer does something else
↓
review result
```

This can change developer throughput.

---

# 10. Difference 6 — Parallel work

Current Codex positioning emphasizes multiple agents/worktrees in parallel.

Concept:

```text
Engineer
├─ Agent 1: bug
├─ Agent 2: tests
├─ Agent 3: refactor
└─ Agent 4: research
```

This changes the bottleneck.

The bottleneck may shift from:

> typing code

to:

> specifying, reviewing and coordinating work.

---

# 11. Worktrees / isolated work

Parallel agents need isolated changes so they do not constantly conflict.

Current Codex product materials reference built-in worktree/cloud environments.

Partner-level takeaway:

> Parallel agent work requires isolated execution contexts and a merge/review process.

You don't need to memorize implementation internals.

---

# 12. Difference 7 — Long-running work

Codex can be used for work beyond a single prompt.

OpenAI's 2026 Codex materials emphasize persistent/long-running tasks.

Examples:

- migration;
- large refactor;
- issue investigation;
- multi-stage artifact.

This changes prompt design.

---

# 13. Prompt becomes task specification

For one-turn chatbot:

> “Write a function.”

For coding agent:

> “Implement the seat-selection bug fix. Reproduce the issue, identify root cause, make the smallest change, update tests, and run the relevant suite. Do not change unrelated behavior.”

This resembles a good engineering ticket.

---

# 14. Difference 8 — It lives where developers work

Current Codex surfaces include:

- ChatGPT;
- editor;
- terminal;
- cloud workflows.

This reduces friction between AI and existing engineering tools.

Good AI adoption often happens inside current workflow.

---

# 15. Difference 9 — It can prepare reviewable artifacts

Useful output may be:

- code diff;
- PR;
- test results;
- explanation;
- screenshots;
- logs.

A coding agent should produce evidence, not just assertions.

---

# 16. Difference 10 — Code review

Current Codex positioning includes code review as an important workflow.

Code review agent can:

- inspect diff;
- identify bugs;
- flag edge cases;
- suggest tests;
- reason across code.

Human reviewers still own the merge decision.

---

# 17. Difference 11 — Skills / team conventions

Current Codex product positioning includes reusable Skills to teach team standards/workflows.

Conceptually:

```text
Team conventions
+ reusable instructions/workflows
→ more consistent agent behavior
```

This helps move from individual prompting to organizational capability.

---

# 18. Difference 12 — Background/scheduled work

Current Codex materials position always-on/background work for tasks such as:

- issue triage;
- monitoring;
- CI/CD-related work.

This shifts Codex from reactive assistant toward continuous engineering support.

Exact feature availability should be verified.

---

# 19. Codex vs ChatGPT

ChatGPT is general-purpose.

Codex is optimized around software delivery.

Compare:

| Area | ChatGPT | Codex |
|---|---|---|
| General research/writing | Strong fit | Not primary |
| Small code explanation | Strong | Strong |
| Repository execution | Limited/general | Core workflow |
| Run tests/commands | Context-dependent | Core agent pattern |
| Long-running coding task | Less specialized | Core |
| Parallel engineering agents | Not generic default | Core Codex positioning |

This is a conceptual comparison, not a benchmark ranking.

---

# 20. Codex vs static code generation

Static generation:

```text
Prompt
→ code
```

Codex:

```text
Task
→ inspect
→ code
→ execute
→ test
→ revise
→ deliver
```

Feedback loop is the differentiator.

---

# 21. Codex vs deterministic automation

Codex is useful where software task contains ambiguity.

Traditional automation still better for fixed steps.

Example:

```text
Release script
→ deterministic code

Investigate why release failed
→ Codex can help
```

---

# 22. Codex and human engineering judgment

Codex is strong at execution.

Humans remain critical for:

- ambiguous product intent;
- architecture;
- trade-offs;
- risk;
- prioritization;
- review.

OpenAI's AI-native engineering guide explicitly notes that code ownership, especially for new/ambiguous problems, remains with engineers.

---

# 23. Developer mental model

Think of Codex as:

```text
Junior/senior-capability agent?
```

Better avoid human seniority metaphor.

A more precise mental model:

```text
LLM reasoning node
+
repo-aware execution environment
+
developer tools
+
feedback loop
```

This avoids anthropomorphizing.

---

# 24. Example — Small code edit

If change is one line:

- IDE interaction may be fastest.

No need to send every task to cloud.

---

# 25. Example — Large migration

Task spans 70 files.

Codex can:

- map usages;
- apply pattern;
- run tests;
- fix errors.

This is where agent-level persistence matters.

---

# 26. Example — Code review

Codex:

- reads PR diff;
- checks related code;
- reasons about behavior;
- flags issue.

Engineer:

- judges relevance;
- asks follow-up;
- decides action.

---

# 27. Partner lens

When explaining differentiation, don't say:

> “Codex is smarter than every coding tool.”

Say:

> “Codex is designed around agentic software work: repository context, tool execution, iterative testing, delegation and review.”

This is descriptive and defensible.

---

# 28. Common mistakes

1. Difference = model benchmark only.
2. Async is always better than interactive.
3. More parallel agents = more productivity automatically.
4. Passing tests = safe merge.
5. Environment access = unrestricted access.
6. Codex replaces architecture/design judgment.
7. Long-running task needs vague prompt.

---

# 29. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Agent loop | Vòng reasoning → action → observation |
| Interactive pairing | Làm việc tương tác trực tiếp |
| Asynchronous delegation | Giao task chạy nền |
| Parallel agents | Nhiều agent chạy song song |
| Worktree | Working tree Git riêng biệt |
| Execution environment | Môi trường chạy code |
| Verification loop | Vòng kiểm chứng |
| Code review | Review code |
| Skill | Instruction/workflow tái sử dụng |
| Task specification | Mô tả task chi tiết |

---

# 30. Section recap

What makes Codex different:

```text
repository awareness
+ execution
+ agent loop
+ tests
+ interactive + async
+ parallelism
+ long-running work
+ developer-tool integration
+ reviewable evidence
```

Core idea:

> **Codex is designed around completing software tasks, not merely generating code.**

---

# 31. Self-check

1. Agent loop thay đổi coding assistance thế nào?
2. Interactive và async modes dùng khi nào?
3. Tại sao parallel agents thay đổi engineering bottleneck?
4. Why do tests matter but not prove everything?
5. Codex Skills giải quyết vấn đề gì?
6. Hãy chuyển một vague request thành Codex task specification.
