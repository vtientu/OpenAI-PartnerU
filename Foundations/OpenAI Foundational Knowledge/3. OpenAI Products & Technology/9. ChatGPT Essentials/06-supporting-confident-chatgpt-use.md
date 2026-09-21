# 06 — Supporting Confident ChatGPT Use

> **Course:** OpenAI Foundational Knowledge  
> **Course:** ChatGPT Essentials  
> **Section:** Supporting confident ChatGPT use

---

# 1. Section objective

Sau section này, bạn cần:

- giúp users sử dụng ChatGPT tự tin nhưng không overtrust;
- biết cách verify output;
- biết khi nào dùng source/tool/human review;
- hiểu workplace data discipline;
- biết adoption support cần training, examples và feedback loops.

---

# 2. Big picture

Confident use is not:

> “Trust ChatGPT.”

It is:

```text
Know what it can do
+
Know where it can fail
+
Use the right context/tool
+
Verify important outputs
+
Follow workplace policy
```

Confidence should come from **method**, not blind trust.

---

# 3. Confidence vs overconfidence

## Confidence

> “I know how to use this tool effectively and check its output.”

## Overconfidence

> “It sounds good, so it must be right.”

Goal:

```text
High capability
+
calibrated trust
```

---

# 4. Rule 1 — Match verification to consequence

Low-consequence:

- brainstorm names;
- rewrite tone.

Light review.

Higher-consequence:

- finance;
- legal;
- customer commitments;
- security;
- policy.

Stronger review.

```text
Higher impact
→ stronger verification
```

---

# 5. Rule 2 — Separate draft from fact

ChatGPT is excellent for drafting.

A draft may contain:

- assumptions;
- unsupported facts;
- outdated details.

So mark workflow:

```text
Draft
→ verify
→ approve
```

---

# 6. Rule 3 — Ask for sources when facts matter

For current/public claims:

- search;
- cite;
- open source;
- check date.

Do not use a citation only as decoration.

Ask:

> Does the source actually support the claim?

---

# 7. Rule 4 — Use trusted internal sources

If question is:

> “What is our company policy?”

Use:

- approved document;
- project source;
- authorized plugin.

Not general model knowledge.

Source of truth matters.

---

# 8. Rule 5 — Tell ChatGPT when not to guess

Useful instruction:

> If the provided material does not support an answer, say that the information is missing.

This is especially useful for:

- document analysis;
- policy Q&A;
- technical specs.

---

# 9. Rule 6 — Check numbers

For calculations:

- inspect formulas;
- verify units;
- reproduce critical totals;
- use data-analysis/code tools where appropriate.

Language fluency is not arithmetic evidence.

---

# 10. Rule 7 — Check names, dates and current product facts

Dynamic facts include:

- prices;
- plan limits;
- laws;
- product features;
- model names;
- company leadership;
- current events.

Verify current official source.

---

# 11. Rule 8 — Protect sensitive data

Before sharing:

Ask:

- Is this allowed?
- Which workspace?
- Is it confidential?
- Does company policy permit upload?
- Is plugin approved?

Do not make workplace data decisions based only on technical possibility.

---

# 12. Rule 9 — Respect permissions

Connected AI should not bypass existing access.

If user cannot access a CRM record normally, AI should not magically make it available.

Permissions are part of trust.

---

# 13. Rule 10 — Review actions, not just words

When AI can take actions:

- send;
- update;
- create;
- delete;

risk increases.

Use:

- confirmation;
- limits;
- human approval;
- logs.

---

# 14. Confidence ladder

A useful study model:

```text
Level 1 — Use
Can prompt.

Level 2 — Guide
Can add context/output requirements.

Level 3 — Verify
Can check evidence.

Level 4 — Integrate
Can use files/tools/projects.

Level 5 — Delegate safely
Can use Work/agent capabilities with controls.
```

Confident adoption grows progressively.

---

# 15. Teach workflows, not tips

Weak training:

> “Here are 50 prompts.”

Strong training:

```text
Workflow
→ prompt
→ tool
→ output
→ verification
```

Users remember job-related patterns better than random prompt tricks.

---

# 16. Use-role examples

## Sales
Account research → brief → verify → meeting.

## Marketing
Brief → draft → brand review → publish.

## Finance
Data → analysis → formula verification → report.

## Engineering
Issue → code suggestion → tests → review.

---

# 17. Build a safe experimentation culture

Users need space to try:

- prompts;
- workflows;
- tools.

But with boundaries:

- approved workspace;
- data rules;
- escalation path;
- examples of good use.

Fear-only guidance reduces adoption.

No-rules guidance increases risk.

---

# 18. Champion model

Organizations may benefit from internal champions who:

- share workflows;
- answer questions;
- collect use cases;
- surface issues;
- help teams learn.

This supports scalable adoption.

---

# 19. Usage guidelines

Good internal guide should explain:

- allowed data;
- prohibited data;
- approved workspace;
- verification expectations;
- sharing rules;
- connected-tool policy;
- incident/reporting path.

Make it concrete.

---

# 20. Encourage source-aware behavior

Users should learn to ask:

```text
What is your source?
Is it current?
Does it support this?
What are your assumptions?
```

This is more useful than generic “be careful.”

---

# 21. Encourage comparison

For important decision:

> Give two or three options and trade-offs.

This reduces single-answer anchoring.

Human chooses.

---

# 22. Encourage critique

Prompt:

> What could be wrong with this analysis?

Then review.

A second-pass critique can reveal:

- missing data;
- assumption;
- unsupported claim.

---

# 23. Encourage staged work

Instead of one giant prompt:

```text
Understand
↓
Plan
↓
Draft
↓
Check
↓
Finalize
```

Staged workflow gives more review opportunities.

---

# 24. Hallucination handling

If ChatGPT gives unsupported fact:

Don't simply retry with:

> “Are you sure?”

Better:

- ask for source;
- provide source;
- use search;
- constrain to document;
- independently verify.

---

# 25. When not to use ChatGPT alone

Do not rely on ChatGPT alone for decisions where:

- authoritative source is required;
- specialized professional judgment is required;
- irreversible action is high-risk;
- real-time data is unavailable;
- organizational policy requires human approval.

Use ChatGPT as part of controlled workflow.

---

# 26. Confidence for managers

Managers should ask:

- Which workflows?
- What evidence of value?
- What data?
- What review?
- What adoption?
- What controls?

Not only:

> “How many employees used ChatGPT?”

---

# 27. Confidence for partners

Partner should demonstrate:

1. useful workflow;
2. limitation;
3. verification step;
4. data/control consideration.

This builds credibility.

Avoid demo theater where everything looks perfect.

---

# 28. Value measurement

Measure:

- task time;
- quality;
- throughput;
- user adoption;
- business outcome.

Also monitor:

- error;
- escalation;
- misuse;
- unsupported outputs.

Value and trust together.

---

# 29. Confidence framework — TRUST

## T — Task
Is this a good AI task?

## R — Reference
What source/context is authoritative?

## U — User judgment
What must human decide/review?

## S — Security
What data/permissions matter?

## T — Test
How will we verify output?

This is a study mnemonic.

---

# 30. Example — Customer email

```text
Task:
Draft reply.

Reference:
Approved policy + account facts.

User judgment:
Support agent approves.

Security:
Use company workspace.

Test:
Check policy and customer details.
```

---

# 31. Example — Financial summary

```text
Task:
Summarize quarter.

Reference:
Approved financial dataset.

User judgment:
Finance owner interprets.

Security:
Approved business environment.

Test:
Reconcile totals + definitions.
```

---

# 32. Common mistakes

1. Trust fluency.
2. Avoid ChatGPT because it can be wrong.
3. No verification policy.
4. Give only prompt tips.
5. Ignore company data policy.
6. Assume citations always support claim.
7. Let connected tools exceed permissions.
8. Measure usage but not value.
9. Use AI as final decision-maker by default.

---

# 33. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Confident use | Sử dụng tự tin có kiểm chứng |
| Calibrated trust | Mức tin phù hợp với evidence |
| Verification | Kiểm chứng |
| Authoritative source | Nguồn có thẩm quyền/chuẩn |
| Human review | Con người kiểm tra |
| Adoption | Mức độ sử dụng |
| Champion | Người thúc đẩy sử dụng |
| Usage guideline | Hướng dẫn sử dụng |
| Unsupported claim | Claim không có evidence |
| Escalation | Chuyển cho người/process phù hợp |

---

# 34. Section recap

Confident ChatGPT use:

```text
Know capability
+ provide context
+ choose right tool
+ verify important output
+ protect data
+ follow permissions
+ keep human ownership
```

Use TRUST:

```text
Task
Reference
User judgment
Security
Test
```

Core rule:

> **Confidence should come from a repeatable verification workflow, not from how convincing the answer sounds.**

---

# 35. Self-check

1. Confidence và overconfidence khác nhau thế nào?
2. Tại sao verification cần theo consequence?
3. Khi nào cần authoritative source?
4. TRUST framework gồm gì?
5. How should a company teach ChatGPT usage beyond prompt tips?
6. Hãy áp dụng TRUST cho một customer-support workflow.
