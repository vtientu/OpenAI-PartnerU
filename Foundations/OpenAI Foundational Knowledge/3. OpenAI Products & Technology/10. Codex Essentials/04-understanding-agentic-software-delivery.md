# 04 — Understanding Agentic Software Delivery

> **Course:** OpenAI Foundational Knowledge  
> **Course:** Codex Essentials  
> **Section:** Understanding agentic software delivery
>
> **Source note:** This section synthesizes current OpenAI Codex engineering guidance, including the Codex agent loop, long-running work, and AI-native engineering practices.

---

# 1. Section objective

Sau section này, bạn cần:

- hiểu “agentic software delivery” là gì;
- biết unit of work dịch chuyển từ code suggestion sang delegated task;
- hiểu human-agent division of labor;
- biết role của feedback loops, environment, parallelism và review;
- hiểu organization/process changes needed to benefit.

---

# 2. Big picture

Traditional AI-assisted coding:

```text
Engineer writes
+ AI suggests
```

Agentic software delivery:

```text
Engineer specifies intent
↓
Agent executes scoped task
↓
Environment provides feedback
↓
Agent iterates
↓
Engineer reviews/steers
↓
Ship
```

OpenAI has summarized this pattern in engineering guidance as:

> Humans steer; agents execute.

The durable idea matters more than the phrase itself.

---

# 3. Unit of work changes

Autocomplete unit:

```text
token / line
```

Chat coding unit:

```text
snippet / function
```

Agent unit:

```text
issue / feature / refactor / migration / investigation
```

This changes:

- prompting;
- planning;
- review;
- team capacity.

---

# 4. Intent becomes an engineering artifact

When agent writes more implementation, human value shifts toward:

- defining intent;
- acceptance criteria;
- constraints;
- architecture;
- feedback loops.

A vague ticket that a human engineer could clarify informally may cause agent drift.

Therefore:

> Specification quality becomes execution quality.

---

# 5. Agent loop as delivery engine

Agentic delivery loop:

```text
Understand
↓
Plan
↓
Act
↓
Run/check
↓
Observe
↓
Revise
↓
Complete
```

Software has rich feedback:

- compiler;
- tests;
- linter;
- runtime;
- browser;
- CI.

These make agent loops practical.

---

# 6. Environment engineering

Agent performance depends on environment.

A strong environment includes:

- easy setup;
- deterministic commands;
- test suite;
- good docs;
- clear repo structure;
- useful error messages.

This leads to an important idea:

> Improving developer infrastructure can improve agent effectiveness too.

---

# 7. Agent-readable repository

If repo has:

- flaky tests;
- undocumented setup;
- confusing scripts;
- hidden conventions;

humans struggle.

Agents also struggle.

Therefore AI-native engineering can reward:

- cleaner interfaces;
- better tests;
- better docs;
- consistent tooling.

---

# 8. Feedback loops

Agent needs objective signals.

Good:

```text
change
→ test
→ failure
→ fix
```

Weak:

```text
change
→ no validation
→ declare success
```

More verifiable task = safer delegation.

---

# 9. Human role shifts

Traditional:

```text
Human implements most steps.
```

Agentic:

```text
Human:
- scope
- architecture
- prioritization
- review
- escalation

Agent:
- exploration
- implementation
- repetitive execution
- testing
```

This is a redistribution, not disappearance of engineering work.

---

# 10. Human attention becomes scarce resource

Parallel agents can create many outputs.

Then bottleneck becomes:

- review;
- judgment;
- task specification;
- integration.

This means simply running more agents can create review overload.

---

# 11. Parallelism

Agentic delivery allows parallel execution:

```text
Feature work
Migration
Test cleanup
Documentation
```

running simultaneously.

Value:

- higher throughput.

Risk:

- merge conflict;
- duplicated work;
- review backlog;
- inconsistent design.

Coordination becomes important.

---

# 12. Work decomposition

A large project should be decomposed.

Bad:

> “Rewrite the platform.”

Better:

```text
1. inventory
2. define migration boundary
3. pilot one module
4. validate
5. split remaining work
6. parallelize
7. integrate
```

Agentic delivery still needs engineering planning.

---

# 13. Deterministic vs agentic steps

Keep deterministic tasks deterministic.

Example:

```text
Release gate
→ code/policy

Implementation reasoning
→ agent

Merge approval
→ human/process
```

AI-native does not mean AI-controlled everything.

---

# 14. Long-running work

Current Codex guidance emphasizes persistent tasks beyond one prompt.

Long-running work requires:

- clear state;
- intermediate artifacts;
- checkpoints;
- verification;
- ability to steer.

This is closer to managing work than chatting.

---

# 15. Steering

Humans may intervene:

- clarify intent;
- change direction;
- comment on artifact;
- reject approach;
- add constraint.

Good agentic workflow supports steering without discarding all progress.

---

# 16. Artifacts as shared context

In long-running work, shared artifacts can be:

- code;
- diff;
- test output;
- plan;
- issue;
- PR;
- design.

Human and agent coordinate around artifacts.

This is more effective than only conversational text.

---

# 17. Agentic code review

More agent-generated code means stronger review systems matter.

Review may include:

- automated tests;
- static analysis;
- AI review;
- human review.

Layered verification becomes more important, not less.

---

# 18. Merge philosophy changes

If agents can generate many PRs, team must decide:

- review depth;
- batch size;
- ownership;
- merge criteria.

Throughput without quality can increase entropy/technical debt.

---

# 19. Quality compounding

Good environment + tests + standards can make agent output more reliable.

Pattern:

```text
better test suite
→ better agent feedback
→ better changes
→ more delegation possible
```

This creates a positive loop.

---

# 20. Bad environment can compound failure

Pattern:

```text
flaky tests
→ agent misreads signal
→ poor changes
→ more complexity
```

Agentic scale amplifies both good and bad engineering practices.

---

# 21. Agentic delivery maturity

A useful study ladder:

```text
Level 1 — Ask for code
Level 2 — Agent edits repo
Level 3 — Agent runs tests
Level 4 — Agent owns scoped issue
Level 5 — Multiple agents work in parallel
Level 6 — Team redesigns SDLC around agents
```

Not an official OpenAI maturity model.

---

# 22. Engineer as orchestrator

At higher maturity, engineer increasingly:

- creates tasks;
- sets constraints;
- delegates;
- monitors;
- reviews;
- integrates.

This resembles orchestration.

But hands-on coding still remains important depending on task.

---

# 23. Agent-first does not mean code-free engineer

Engineering fundamentals remain necessary:

- architecture;
- debugging;
- security;
- systems thinking;
- testing.

Without them, user cannot effectively review agent work.

---

# 24. Agentic delivery and junior learning

Organizations should consider skill development.

If agents do all basic tasks, newer engineers may get fewer opportunities to build foundational skills.

Adoption should consider:

- mentorship;
- review;
- learning workflows;
- intentional hands-on work.

This is an organizational design issue.

---

# 25. Security boundary

Agentic software delivery raises questions:

- repo access;
- secret access;
- network access;
- terminal commands;
- deployment rights.

Use least privilege.

A coding agent should not have more access than needed for task.

---

# 26. Production deployment

Good default:

```text
Agent prepares
↓
tests
↓
review
↓
controlled CI/CD
```

Not:

```text
Agent changes production freely
```

Autonomy level should match risk/evidence.

---

# 27. Evaluation

Evaluate agentic software delivery using:

## Task
- completion rate.

## Quality
- defects;
- test outcomes.

## Speed
- cycle time.

## Human effort
- review time;
- intervention.

## Operations
- failures;
- retries.

## Business
- roadmap capacity;
- incident reduction.

---

# 28. Productivity paradox

If Codex generates more code but engineers spend more time fixing/reviewing it, productivity may not improve.

So:

```text
Output volume
≠
productivity
```

Measure end-to-end outcome.

---

# 29. Agentic delivery framework — STEER

## S — Specify
Define intent.

## T — Tools
Give the right environment/tools.

## E — Evaluate
Provide tests/checks.

## E — Escalate
Know when human must intervene.

## R — Review
Human owns final judgment.

This is a study mnemonic.

---

# 30. Example — Migration program

```text
Human:
architecture + migration rules

Agent:
inventory usages
pilot one package
run tests
generate migration PRs

Human:
review pilot
adjust rules

Agents:
parallelize remaining packages

CI + humans:
validate and merge
```

This is agentic delivery, not a single prompt.

---

# 31. Example — Incident

```text
Human:
sets incident priority and business context

Codex:
traces failure path
inspects relevant code
proposes fix
adds regression test

Human:
reviews risk

CI:
validates

Human:
owns deployment
```

---

# 32. Common mistakes

1. Agentic = full autonomy.
2. More agents = more productivity.
3. Specification quality doesn't matter.
4. Existing flaky tests are fine.
5. Engineers no longer need coding skill.
6. Agent can deploy freely.
7. Measure code volume instead of outcomes.
8. Ignore review capacity.

---

# 33. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Agentic software delivery | Delivery software với agent thực thi nhiều bước |
| Intent | Ý định/mục tiêu kỹ thuật |
| Feedback loop | Vòng phản hồi |
| Environment engineering | Thiết kế môi trường cho agent/dev |
| Work decomposition | Chia nhỏ công việc |
| Orchestration | Điều phối |
| Review capacity | Năng lực review |
| Merge criteria | Tiêu chí merge |
| Engineering entropy | Sự xuống cấp/khó kiểm soát của codebase |
| Least privilege | Quyền tối thiểu |
| Human steering | Con người định hướng |

---

# 34. Section recap

Agentic software delivery is:

```text
Human intent
↓
Agent execution
↓
Environment feedback
↓
Iteration
↓
Evidence
↓
Human review
```

At scale:

```text
multiple agents
+ good repo/test infrastructure
+ strong review
+ clear ownership
```

Core rule:

> **Agentic delivery scales engineering execution only when specification, feedback and review scale with it.**

---

# 35. Self-check

1. Unit of work thay đổi thế nào với agents?
2. Tại sao environment engineering quan trọng?
3. Parallel agents tạo bottleneck mới gì?
4. STEER framework gồm gì?
5. Vì sao code volume không phải productivity?
6. Hãy thiết kế agentic workflow cho một migration.
