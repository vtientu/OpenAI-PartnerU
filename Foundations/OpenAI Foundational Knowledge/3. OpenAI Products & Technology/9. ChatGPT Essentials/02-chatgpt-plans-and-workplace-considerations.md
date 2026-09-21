# 02 — ChatGPT Plans and Workplace Considerations

> **Course:** OpenAI Foundational Knowledge  
> **Course:** ChatGPT Essentials  
> **Section:** ChatGPT plans and workplace considerations
>
> **Freshness snapshot:** **21 September 2026**. Plans, model access, usage limits, seat packaging and pricing can change quickly. Verify current OpenAI pricing/help pages before quoting them to a customer.

---

# 1. Section objective

Sau section này, bạn cần:

- hiểu plan categories ở mức concept;
- phân biệt personal plans với organization workspaces;
- hiểu Business vs Enterprise considerations;
- biết workplace questions về privacy, workspace, admin, sharing và policy;
- tránh tư vấn plan dựa trên feature/pricing cũ.

---

# 2. Big picture

Plan selection is not only:

> “How much does it cost?”

For workplace use:

```text
User needs
+ usage
+ collaboration
+ admin
+ security
+ governance
+ support
=
plan fit
```

---

# 3. Current plan landscape — durable view

Current ChatGPT plan families include personal/user-oriented plans such as:

- Free;
- Go;
- Plus;
- Pro;

and organization-oriented plans such as:

- Business;
- Enterprise;

plus education/specialized organizational offerings in eligible contexts.

Exact packaging can change.

---

# 4. Personal plans

Personal plans are generally optimized for individual usage.

Typical progression:

```text
Free
→ everyday access

Go
→ expanded access at lower-cost paid tier

Plus
→ broader/higher model and tool access

Pro
→ highest individual access for complex/heavy usage
```

Do not memorize exact limits.

Limits can change by:

- model;
- tool;
- rollout;
- plan.

---

# 5. Free

Current public Help Center materials describe Free as giving access to core ChatGPT capabilities with usage limits that can differ by tool.

Examples currently include access to capabilities such as:

- web search;
- file/image upload;
- data analysis;
- image creation;
- GPT usage.

Limits are stricter than paid plans.

---

# 6. Go

Go is a lower-cost paid plan designed for expanded access to popular ChatGPT features.

It generally provides more usage than Free across eligible features.

OpenAI states Go is available in supported ChatGPT countries.

Exact local price can vary.

---

# 7. Plus

Plus is an enhanced individual subscription.

Current OpenAI materials describe:

- broader model/tool access than Free;
- higher limits;
- advanced reasoning access;
- faster/priority experience.

Exact model availability should be checked in-product.

---

# 8. Pro

Pro is intended for users relying on AI heavily for complex work.

Current Pro packaging is particularly dynamic in September 2026.

Therefore:

> Do not quote plan tiers/availability from memory.

Verify the current Help Center before making purchase guidance.

Durable concept:

```text
Pro
→ higher individual capacity / advanced access
```

---

# 9. Business

ChatGPT Business is a self-serve organization workspace.

Current public OpenAI materials describe capabilities including:

- shared organization workspace;
- centralized administration/billing;
- business privacy commitments;
- workspace controls;
- ChatGPT/Work/Codex access under current seat packaging;
- connected tools/plugins;
- workspace agents.

Business is not merely “Plus for teams.”

It changes organizational control and data handling.

---

# 10. Enterprise

ChatGPT Enterprise is for organizations needing stronger scale/security/governance/support.

Current public materials include additional enterprise capabilities such as:

- SCIM;
- role-based access controls;
- enterprise key management in supported configurations;
- advanced analytics/administration;
- data residency options;
- retention controls;
- enterprise support/legal options.

Exact controls depend on contract/product setup.

---

# 11. Business vs Enterprise — mental model

## Business

```text
self-serve team workspace
+ admin
+ business privacy
+ shared organization usage
```

## Enterprise

```text
Business capabilities
+ deeper identity/governance
+ enterprise-scale controls/support
```

Do not reduce the difference only to user count.

---

# 12. ChatGPT and API billing are separate

A common misconception:

> “We bought ChatGPT Business, so API usage is included.”

Current OpenAI Help Center explicitly separates ChatGPT Business and API platform billing.

This matters in solution design.

```text
Employee productivity
→ ChatGPT plan

Custom application
→ API platform

May need both
```

---

# 13. Workplace consideration 1 — Business data

OpenAI currently states it does **not train models on organization data by default** for ChatGPT Business, Enterprise, Edu and API platform.

This is an important business privacy distinction from consumer/personal usage contexts.

But partner should still verify:

- exact product;
- current terms;
- customer requirements.

---

# 14. Workplace consideration 2 — Personal vs company workspace

A user may have:

- personal workspace;
- organization workspace.

These should be treated as distinct contexts.

Questions:

- Where should work data be used?
- Which workspace does company policy require?
- Is content allowed in personal workspace?
- Who owns/administers workspace?

---

# 15. Workplace consideration 3 — Company policy

Even if a tool technically supports upload:

> Company policy may prohibit uploading certain data.

Users need to understand:

- confidential data rules;
- customer data rules;
- regulated data;
- intellectual property;
- security classifications.

Product capability does not override workplace policy.

---

# 16. Workplace consideration 4 — Sharing

ChatGPT work can include:

- chats;
- project sharing;
- workspace content;
- generated artifacts.

Before sharing:

- check audience;
- remove sensitive info;
- verify factual content;
- confirm permissions.

---

# 17. Workplace consideration 5 — Projects

Projects can keep:

- chats;
- files;
- instructions;
- related context

together.

This is useful for ongoing work.

But users should organize projects with:

- appropriate access;
- clear purpose;
- approved content.

---

# 18. Workplace consideration 6 — Plugins

Plugins can connect ChatGPT to business systems.

This means workplace use expands from:

```text
uploaded context
```

to:

```text
live connected context/actions
```

Admin controls and permissions become important.

---

# 19. Permission principle

A plugin should only expose data/actions the user is authorized to access.

Good enterprise model:

```text
User identity
↓
authorized plugin access
↓
business system
```

Not:

```text
ChatGPT gets unrestricted organization access
```

---

# 20. Workplace consideration 7 — Admin controls

Organization workspaces may allow admins to control:

- users;
- roles;
- feature access;
- plugins;
- workspace agents;
- identity settings;
- analytics;
- spend/usage.

This is a major reason organizations use business plans rather than unmanaged personal accounts.

---

# 21. Workplace consideration 8 — Retention / residency

Some organizations have requirements around:

- retention;
- data residency;
- encryption;
- identity;
- audit.

Enterprise/product-specific options exist, but exact eligibility must be verified.

Never promise a control because “OpenAI supports it somewhere.”

---

# 22. Workplace consideration 9 — Adoption

Selecting plan is not enough.

Need:

- training;
- use cases;
- policy;
- champions;
- measurement;
- support.

A workspace with low adoption creates little value.

---

# 23. Plan-selection questions

Ask:

1. Individual or organization?
2. Number/type of users?
3. Usage intensity?
4. Need shared workspace?
5. Admin/SSO?
6. SCIM/RBAC?
7. Data residency/retention?
8. Plugins/connections?
9. Work/Codex/workspace agents?
10. Support/contract requirements?

---

# 24. Avoid exact-feature memory

Feature availability changes.

Examples:

- models;
- usage limits;
- plan tools;
- seat packaging.

Rule:

```text
Concept from memory
+
exact detail from current official source
```

---

# 25. Current plan table — study view

| Plan | Main lens |
|---|---|
| Free | Entry/everyday access |
| Go | Lower-cost expanded individual access |
| Plus | Broader individual access |
| Pro | Heavy/complex individual usage |
| Business | Managed organization workspace |
| Enterprise | Enterprise-scale security/governance/support |

This table intentionally avoids volatile usage limits.

---

# 26. Partner recommendation discipline

Bad:

> “You definitely need Enterprise.”

Better:

> “Your requirements include SCIM, RBAC, retention controls and enterprise support, so we should validate Enterprise against those requirements.”

Recommendation should follow requirements.

---

# 27. Common mistakes

1. Business = Plus with more users.
2. Enterprise = only “bigger Business”.
3. ChatGPT subscription includes API usage.
4. All plans have same privacy/admin behavior.
5. Exact limits remembered from old docs.
6. Company data uploaded to personal workspace without policy check.
7. Plugin connection assumed to grant unlimited access.
8. Plan purchase mistaken for adoption strategy.

---

# 28. English–Vietnamese glossary

| Term | Nghĩa |
|---|---|
| Plan | Gói sử dụng |
| Workspace | Không gian làm việc |
| Business plan | Gói cho tổ chức/team |
| Enterprise | Gói doanh nghiệp quy mô lớn |
| SSO | Single Sign-On |
| SCIM | Tự động provisioning user |
| RBAC | Role-Based Access Control |
| Retention | Thời gian lưu dữ liệu |
| Data residency | Khu vực lưu dữ liệu |
| Admin control | Kiểm soát quản trị |
| Seat | Quyền/người dùng trả phí trong workspace |
| Usage limit | Giới hạn sử dụng |

---

# 29. Section recap

Plan fit:

```text
Individual need
→ Free / Go / Plus / Pro

Organization need
→ Business / Enterprise
```

Workplace fit:

```text
Plan
+ privacy
+ admin
+ company policy
+ permissions
+ adoption
```

Core rule:

> **Choose a ChatGPT plan based on user, governance and workflow requirements—not only model access or price.**

---

# 30. Self-check

1. Personal plans và organization plans khác nhau về gì?
2. Business khác personal subscription ở điểm nào?
3. ChatGPT Business có bao gồm API billing không?
4. Tại sao workplace policy vẫn quan trọng dù product hỗ trợ file upload?
5. Khi nào Enterprise requirements xuất hiện?
6. Tại sao exact plan limits phải verify?
