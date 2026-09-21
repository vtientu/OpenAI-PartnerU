# 05 — Going Further With ChatGPT

> **Course:** OpenAI Foundational Knowledge  
> **Course:** ChatGPT Essentials  
> **Section:** Going further with ChatGPT
>
> **Freshness note:** Features and plan availability change. This guide describes capability patterns and references current OpenAI public features as of **21 September 2026**.

---

# 1. Section objective

Sau section này, bạn cần:

- biết cách vượt khỏi basic chat;
- hiểu Projects, files/data, search/research, plugins, Work và richer tool use;
- biết chọn capability theo task;
- hiểu connected/agentic use làm tăng cả value và responsibility.

---

# 2. Big picture

Progression:

```text
Basic chat
↓
Files / images
↓
Projects
↓
Web / research
↓
Data analysis
↓
Plugins / connected systems
↓
Work / agentic execution
```

Going further không có nghĩa dùng feature phức tạp nhất.

It means:

> Use the capability that removes the next workflow bottleneck.

---

# 3. Projects

Projects keep related:

- chats;
- files;
- instructions;
- context

together.

Good for ongoing work:

- course learning;
- client project;
- research;
- recurring report;
- content program.

---

# 4. Why Projects matter

Without project:

```text
new chat
→ repeat context
```

With project:

```text
shared ongoing context
→ continue work
```

This improves consistency and reduces repeated setup.

---

# 5. Project instructions

Project instructions can define:

- purpose;
- tone;
- terminology;
- output format;
- working rules.

Example:

> Always write executive summaries in concise English and list assumptions separately.

This is reusable context.

---

# 6. Files

Files allow ChatGPT to work directly with:

- documents;
- PDFs;
- spreadsheets;
- presentations;
- images.

Good tasks:

- summarize;
- extract;
- compare;
- analyze;
- transform.

---

# 7. File-based workflow

Strong pattern:

```text
Upload
↓
Ask ChatGPT to inspect first
↓
Confirm understanding/schema
↓
Perform task
↓
Verify source
```

Avoid:

> “Analyze everything” with no goal.

---

# 8. Web/search

Use when answer depends on:

- today;
- current;
- latest;
- recent changes;
- public sources.

Good workflow:

```text
Search
→ source selection
→ synthesis
→ citation
→ date check
```

---

# 9. Deep research / research workflows

For broader research tasks, advanced research capabilities can:

- gather many sources;
- synthesize;
- produce report;
- cite evidence.

Use when:

- question is multi-source;
- evidence matters;
- manual research is substantial.

Still review source quality and conclusion.

---

# 10. Data analysis

ChatGPT can work with files/data using analysis tools.

Use for:

- cleaning;
- exploration;
- calculations;
- charts;
- statistical summaries.

Better prompt:

> First inspect the dataset and identify data-quality issues. Do not begin conclusions until you explain the fields.

---

# 11. Image understanding and creation

Image input:

- analyze screenshot;
- inspect visual;
- extract information.

Image generation:

- create visuals;
- concept exploration;
- diagrams/creative assets.

For business output, verify:

- brand;
- factual labels;
- rights/policy requirements.

---

# 12. Voice

Voice can be useful for:

- hands-free brainstorming;
- practice;
- quick discussion;
- ideation.

For complex factual work, written output can be easier to verify.

Choose interaction mode based on task.

---

# 13. Plugins

Plugins connect ChatGPT to external tools/data.

Current OpenAI public business materials describe plugins for systems such as:

- CRM;
- cloud storage;
- data platforms;
- developer systems;
- collaboration tools.

Value:

```text
ChatGPT
+ authorized business context
→ less context switching
```

---

# 14. Plugin capabilities

Depending on plugin:

- retrieve data;
- analyze;
- search;
- possibly take action.

Different plugins have different permissions.

User/admin should review:

- access;
- scope;
- creator;
- actions.

---

# 15. Plugin vs upload

Upload:

```text
static snapshot
```

Plugin:

```text
connected live/authorized system
```

Use plugin when freshness/workflow connection matters.

---

# 16. ChatGPT Work

Current OpenAI materials describe Work as capable of longer-running work across files/apps and creating finished artifacts.

Examples:

- research and build a brief;
- analyze business data;
- create docs/decks/spreadsheets;
- automate repetitive work.

This is a shift from:

```text
assist me
```

toward:

```text
complete this work
```

---

# 17. When to use Work

Use when:

- task has multiple steps;
- there is a clear deliverable;
- task takes substantial effort;
- files/tools must be coordinated.

Don't use Work for:

> “Define latency.”

Chat is simpler.

---

# 18. Projects + Work

Project provides durable context.

Work performs substantial task.

Conceptually:

```text
Project
= ongoing context

Work
= execution
```

Together they support longer-term work patterns.

---

# 19. Plugins + Work

Connected systems can extend Work.

Example:

```text
Slack + Drive + Asana
↓
Work
↓
project status analysis
↓
finished weekly report
```

This can reduce manual context gathering.

---

# 20. Current Data plugin pattern

OpenAI currently describes a Data plugin usable in ChatGPT Work and Codex for connected business analysis.

Concept:

```text
business data
→ governed connection
→ analysis
→ dashboard/report
```

This illustrates how ChatGPT can move from generic AI to organization-specific work.

---

# 21. Memory / personalization

ChatGPT may use memory/personalization features depending on account/settings.

Conceptual value:

- remember preferences;
- reduce repeated context.

But:

```text
memory
≠ model training
```

And sensitive/workplace information should follow appropriate policy.

---

# 22. Model/reasoning choices

Some plans allow users to choose or invoke different reasoning levels/models.

General rule:

```text
Everyday task
→ fast/default

Hard planning/coding/analysis
→ stronger reasoning where available
```

Exact model names should not be memorized as permanent.

---

# 23. Tool-first thinking

Before prompting, ask:

> Which capability does this task need?

Examples:

```text
current facts → web
spreadsheet → data analysis
company CRM → plugin
ongoing context → project
large deliverable → Work
coding repo → Codex
```

This often matters more than perfect wording.

---

# 24. Capability stacking

Complex workflow may combine:

```text
Project
+ files
+ web
+ plugin
+ Work
```

But use only needed components.

More tools = more complexity.

---

# 25. Example — Competitive brief

```text
Project
→ company positioning docs

Web
→ current competitor facts

Research
→ gather evidence

Work
→ create finished brief
```

Human verifies conclusions.

---

# 26. Example — Operations weekly review

```text
Plugins
→ project/tool data

Data analysis
→ metrics

Work
→ status deck/report
```

This is a real productivity workflow beyond basic chat.

---

# 27. Example — Learning project

```text
Project
→ course materials
→ recurring explanations
→ study notes
→ quizzes
```

This is precisely the kind of context-preserving workflow Projects support.

---

# 28. Going further safely

As access expands:

```text
More context
→ more privacy responsibility

More tools
→ more permission responsibility

More action
→ more verification responsibility
```

Capability growth should be matched by discipline.

---

# 29. Advanced use does not mean maximum autonomy

Sometimes the best advanced workflow is:

```text
AI prepares
→ human approves
```

Not:

```text
AI executes everything
```

Choose based on risk.

---

# 30. Common mistakes

1. Use every tool because available.
2. Web search for stable simple concept.
3. Upload when live plugin is needed.
4. Plugin when static file is enough.
5. Work for trivial question.
6. No project organization for long-running work.
7. Trust connected data without verifying definitions.
8. Assume feature exists on every plan.

---

# 31. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Project | Không gian context dài hạn |
| Deep research | Nghiên cứu nhiều nguồn/chuyên sâu |
| Plugin | Integration với external system |
| Connected data | Dữ liệu từ hệ thống kết nối |
| ChatGPT Work | Chế độ/capability thực hiện task lớn |
| Memory | Context/preferences được lưu |
| Tool selection | Chọn công cụ phù hợp |
| Capability stacking | Kết hợp nhiều capability |
| Live data | Dữ liệu hiện tại |
| Static snapshot | Bản dữ liệu tại một thời điểm |

---

# 32. Section recap

Going further:

```text
Projects
Files
Web/research
Data analysis
Images
Voice
Plugins
Work
Memory/personalization
```

Core decision:

```text
Task need
→ right capability
```

Not:

```text
Use every advanced feature
```

---

# 33. Self-check

1. Project và Work khác nhau thế nào?
2. Plugin khác file upload ra sao?
3. Khi nào web/research cần thiết?
4. Khi nào Work phù hợp?
5. Tại sao more tools means more responsibility?
6. Hãy thiết kế capability stack cho weekly operations report.
