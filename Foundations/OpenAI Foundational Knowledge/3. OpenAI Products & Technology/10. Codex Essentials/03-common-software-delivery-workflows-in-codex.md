# 03 — Common Software Delivery Workflows in Codex

> **Course:** OpenAI Foundational Knowledge  
> **Course:** Codex Essentials  
> **Section:** Common software delivery workflows in Codex
>
> **Source note:** Workflow categories are grounded in current OpenAI Codex/engineering materials. Exact UI steps are intentionally omitted because the product evolves quickly.

---

# 1. Section objective

Sau section này, bạn cần:

- biết Codex use cases across SDLC;
- hiểu workflow từ code understanding tới review;
- biết task nào nên interactive vs delegated;
- biết verification step cho từng workflow;
- dùng Codex theo software-delivery outcome, không phải “generate more code”.

---

# 2. Big picture

Software delivery lifecycle:

```text
Understand
↓
Plan
↓
Build
↓
Test
↓
Debug
↓
Review
↓
Ship
↓
Operate / maintain
```

Codex can support multiple stages.

---

# 3. Workflow 1 — Codebase understanding

OpenAI describes this as a major internal Codex use case.

Typical task:

> “Where is authentication handled and how does a request flow through the service?”

Codex can:

- search repo;
- identify files;
- trace calls;
- summarize architecture;
- find relevant tests.

---

# 4. Why code understanding matters

Developers spend significant time reading code.

Use cases:

- onboarding;
- unfamiliar service;
- ownership handoff;
- incident investigation;
- legacy code.

Value:

```text
less search time
+ faster context acquisition
```

---

# 5. Good code-understanding prompt

```text
Trace the request flow for /checkout from route entrypoint to payment provider.

Include:
- key files/functions;
- validation;
- persistence;
- failure handling.

Do not modify files.
```

This defines scope and read-only intent.

---

# 6. Workflow 2 — Feature implementation

Current Codex engineering positioning describes issue-to-tested-code workflows.

Flow:

```text
Feature spec
↓
inspect architecture
↓
plan
↓
implement
↓
tests
↓
validate
↓
review
```

Good when acceptance criteria are clear.

---

# 7. Feature task specification

Include:

- user behavior;
- affected area;
- acceptance criteria;
- constraints;
- tests;
- non-goals.

Example:

> Add keyboard navigation to the dropdown, preserving current mouse behavior and public API. Update unit tests and run the component test suite.

---

# 8. Workflow 3 — Bug investigation

Flow:

```text
Bug report
↓
reproduce
↓
trace
↓
root cause
↓
smallest fix
↓
regression test
↓
verify
```

Agentic execution is valuable because diagnosis changes based on what Codex observes.

---

# 9. Bug-fix discipline

Ask Codex to:

- reproduce before changing;
- explain root cause;
- keep change scoped;
- add regression test;
- run relevant checks.

This avoids “random change until test passes.”

---

# 10. Workflow 4 — Test generation

Tasks:

- add missing unit tests;
- increase edge-case coverage;
- create regression test;
- update fixtures.

Codex can inspect existing test patterns.

Quality check:

- tests should verify behavior;
- avoid trivial tests that only mirror implementation.

---

# 11. Workflow 5 — Refactoring

Examples:

- split large component/module;
- remove duplication;
- improve abstractions;
- modernize pattern.

Important constraint:

> preserve external behavior.

Good task:

```text
Refactor X without changing its public API.
Run existing tests.
Add tests only where current behavior is uncovered.
```

---

# 12. Workflow 6 — Large-scale migration

OpenAI describes migrations/refactors as a common Codex workflow.

Examples:

- framework version;
- deprecated API;
- design-system component;
- dependency;
- naming convention.

Agent can:

```text
find
→ classify usages
→ update
→ test
→ fix failures
```

---

# 13. Migration strategy

For large change:

```text
inventory
↓
plan
↓
small pilot subset
↓
validate
↓
scale
```

Don't blindly delegate entire migration before proving pattern.

---

# 14. Workflow 7 — Code review

Codex can review:

- PR diff;
- related modules;
- behavior;
- tests.

Ask for:

- correctness bugs;
- regressions;
- security-relevant concerns;
- missing tests;
- API compatibility.

Avoid asking only:

> “Is this good?”

---

# 15. Code review verification

AI review is a second set of eyes.

It does not remove:

- human ownership;
- CI;
- security tools;
- domain review.

Treat it as additive quality capacity.

---

# 16. Workflow 8 — Documentation

Codex can generate/update:

- README;
- API docs;
- code comments;
- migration guide;
- architecture notes.

Because it can inspect code, docs may be more grounded than generic generation.

Still verify technical accuracy.

---

# 17. Workflow 9 — Incident investigation

OpenAI internal-use guide describes Codex assisting incident response.

Possible flow:

```text
symptom
↓
inspect logs/code/context
↓
trace failure path
↓
identify candidates
↓
propose fix
```

High-pressure environments require strong human ownership.

---

# 18. Workflow 10 — Technical debt cleanup

Examples:

- remove dead code;
- feature flag cleanup;
- dependency upgrades;
- repetitive maintenance.

These are attractive delegation tasks because:

- bounded;
- low novelty;
- easy to verify.

---

# 19. Workflow 11 — Prototyping

Product request:

> “Try this UX idea.”

Codex can:

- scaffold;
- wire components;
- create first working version.

Value:

> shorten idea-to-artifact cycle.

Prototype is not production proof.

---

# 20. Workflow 12 — CI/CD and automation support

Codex may help:

- write scripts;
- update CI config;
- investigate failures;
- create telemetry/config.

Current product materials also position background/scheduled workflows for routine engineering work.

Use carefully because CI/deploy permissions can be sensitive.

---

# 21. Workflow 13 — Frontend visual iteration

Modern coding-agent workflows can use:

- screenshot/design input;
- browser execution;
- visual inspection.

Flow:

```text
Design/spec
↓
implement
↓
run app
↓
inspect UI
↓
iterate
```

Useful for frontend work.

---

# 22. Workflow 14 — Cross-repo / unfamiliar ownership

Task:

> Update integration across another team's code.

Codex can reduce time to understand unfamiliar repo.

But team ownership/review requirements still apply.

---

# 23. Workflow 15 — Background task queue

Developer can maintain tasks that are good candidates for delegation:

- test gaps;
- cleanup;
- migration;
- docs;
- small bugs.

Then:

```text
delegate multiple
→ review results in batches
```

This is an agentic productivity pattern.

---

# 24. Interactive vs delegated routing

## Interactive

Choose when:

- requirements evolving;
- need fast back-and-forth;
- small scoped edit;
- exploration.

## Delegated/background

Choose when:

- task well-defined;
- verification exists;
- can run independently;
- meaningful work duration.

---

# 25. Task-fit matrix

| Workflow | Codex fit signal | Verification |
|---|---|---|
| Code understanding | Large/unfamiliar repo | file references/explanation |
| Feature | Clear acceptance criteria | tests + review |
| Bug | Reproducible behavior | regression test |
| Refactor | Preserve behavior | existing tests |
| Migration | Repeated cross-file change | build/test |
| Review | Diff + context | human review |
| Docs | Code-backed facts | engineer check |
| Incident | complex code tracing | operator review |

---

# 26. Prompting Codex vs prompting ChatGPT

Codex prompt should often look like a ticket.

Good structure:

```text
Goal
Context
Acceptance criteria
Constraints
Validation
Non-goals
```

Example:

```text
Goal:
Fix duplicate API requests when filter changes.

Constraints:
Do not change API contracts.

Validation:
Add regression test and run existing dashboard tests.

Non-goal:
Do not refactor unrelated state management.
```

---

# 27. Workflow framework — CODE

## C — Context
Where in repo/system?

## O — Outcome
What behavior/result?

## D — Definition of done
What tests/checks prove completion?

## E — Exclusions
What should not change?

This is a study mnemonic.

---

# 28. Review framework — TEST

## T — Tests
Did relevant tests run?

## E — Evidence
What files/logs/diff support result?

## S — Scope
Did agent stay within task?

## T — Technical judgment
Does engineer agree with design?

---

# 29. Example — React bug

Task:

> Modal closes immediately after submit.

CODE:

```text
Context:
Checkout modal.

Outcome:
Stay open until API success.

Definition of done:
Regression test + existing suite passes.

Exclusions:
No API redesign.
```

Codex:

```text
reproduce
→ inspect state
→ patch
→ test
→ report
```

---

# 30. Metrics for Codex workflows

Possible engineering metrics:

- issue cycle time;
- PR throughput;
- review turnaround;
- test coverage;
- defect rate;
- time to understand code;
- migration completion;
- developer satisfaction.

Do not measure only generated lines.

---

# 31. Common mistakes

1. Delegate vague task.
2. No definition of done.
3. Ask for huge migration before pilot.
4. Skip regression test.
5. Use agent-generated code without review.
6. Treat code review as only style review.
7. Use lines generated as productivity metric.
8. Give production/deploy authority before controls.

---

# 32. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| SDLC | Software Development Lifecycle |
| Codebase understanding | Hiểu codebase |
| Acceptance criteria | Tiêu chí chấp nhận |
| Regression test | Test chống tái xuất hiện bug |
| Refactor | Cải tổ code không đổi behavior |
| Migration | Chuyển đổi công nghệ/pattern |
| Technical debt | Nợ kỹ thuật |
| CI/CD | Continuous Integration/Delivery |
| Definition of done | Tiêu chí hoàn thành |
| Non-goal | Việc không thuộc phạm vi |
| PR | Pull Request |

---

# 33. Section recap

Common workflows:

```text
Understand code
Build feature
Fix bug
Generate tests
Refactor
Migrate
Review
Document
Investigate incident
Clean technical debt
Prototype
Support CI/CD
```

For each task define:

```text
CODE
Context
Outcome
Definition of done
Exclusions
```

Then review with:

```text
TEST
Tests
Evidence
Scope
Technical judgment
```

---

# 34. Self-check

1. Bug-fix workflow nên bắt đầu bằng gì?
2. Why is Definition of Done important for Codex?
3. Interactive vs async task khác nhau thế nào?
4. Migration nên pilot ra sao?
5. CODE framework gồm gì?
6. Hãy viết task spec cho một frontend feature.
