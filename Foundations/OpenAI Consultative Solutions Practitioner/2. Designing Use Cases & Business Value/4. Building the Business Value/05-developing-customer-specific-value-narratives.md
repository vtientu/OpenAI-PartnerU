# 05. Developing Customer-Specific Value Narratives

> **Mục tiêu:** Biết cách biến discovery + use case + evidence thành một câu chuyện value **cụ thể cho từng khách hàng**, thay vì dùng thông điệp AI chung chung.

---

## 1. Value Narrative là gì?

**Value narrative** = cách kể một câu chuyện ngắn, logic và có evidence về:

1. Khách hàng đang gặp vấn đề gì.
2. Workflow nào có thể thay đổi.
3. AI hỗ trợ ở đâu.
4. Outcome nào có thể cải thiện.
5. Vì sao outcome đó quan trọng với business.
6. Cách sẽ đo hoặc validate value.

> **Câu nhớ nhanh:** `Their problem → Their workflow → Their evidence → Their outcome`

---

## 2. Generic narrative vs Customer-specific narrative

### Generic

> “AI có thể giúp nhân viên tăng productivity và giảm chi phí.”

Vấn đề:

- Không nói về khách hàng cụ thể.
- Không nói workflow nào.
- Không có evidence.
- Không biết đo bằng gì.

### Customer-specific

> “Team support của bạn đang xử lý khoảng 2,000 ticket/tuần và phần đọc context + drafting chiếm nhiều thời gian. Nếu AI hỗ trợ hai bước này, hypothesis là handling time có thể giảm mà vẫn giữ quality. Pilot có thể đo time-per-ticket, draft acceptance và quality score để xem capacity thực tế được unlock bao nhiêu.”

Khác biệt lớn nhất: câu chuyện thứ hai sử dụng **customer evidence**.

---

## 3. Structure 7 phần

### 1. Context

Doanh nghiệp/team đang cố đạt điều gì?

### 2. Pain

Workflow hiện tại đang cản trở như thế nào?

### 3. Evidence

Ta biết pain này tồn tại dựa trên dữ liệu nào?

### 4. AI-enabled change

AI sẽ thay đổi bước nào?

### 5. Operational outcome

Metric nào có thể cải thiện?

### 6. Business relevance

Tại sao outcome đó quan trọng?

### 7. Measurement / next step

Ta sẽ validate bằng cách nào?

---

## 4. Narrative template

```text
Today, [team] handles [workflow / volume].
The main friction is [pain point], supported by [evidence].

If AI assists with [specific workflow step],
we expect [operational metric] to improve.

That matters because [business priority / outcome].

We would validate this by measuring
[baseline + pilot metrics + quality/adoption].
```

Phiên bản tiếng Việt:

```text
Hiện tại [team] đang thực hiện [workflow / volume].
Pain chính nằm ở [bước cụ thể], được thể hiện qua [evidence].

Nếu AI hỗ trợ [bước cụ thể],
chúng ta kỳ vọng [metric] có thể cải thiện.

Điều này quan trọng vì [business priority].

Pilot sẽ kiểm chứng bằng [metrics].
```

---

## 5. Cùng một use case, kể khác nhau theo stakeholder

### Với end user

Tập trung vào:

- Ít repetitive work.
- Ít context switching.
- Draft nhanh hơn.
- Dễ tìm thông tin hơn.

### Với functional leader

Tập trung vào:

- Throughput.
- Backlog.
- Quality.
- Team capacity.
- SLA.

### Với executive

Tập trung vào:

- Strategic priority.
- Scale.
- Business impact.
- Risk.
- Evidence để ra quyết định đầu tư.

> **Không phải thay đổi sự thật.** Chỉ thay đổi trọng tâm theo điều mỗi stakeholder cần biết.

---

## 6. Example — Software Engineering

### Discovery evidence

- Team đang có code review bottleneck.
- PR thường chờ review lâu.
- Reviewer mất nhiều thời gian hiểu context.
- Engineering leadership muốn rút ngắn delivery cycle nhưng không muốn giảm code quality.

### Value narrative

> Hiện tại code review đang là một điểm nghẽn trong delivery flow. Reviewers phải dành nhiều thời gian đọc context và kiểm tra các pattern lặp lại. Một AI assistant có thể hỗ trợ tóm tắt PR, highlight thay đổi đáng chú ý và gợi ý review checklist. Hypothesis là review preparation time có thể giảm trong khi vẫn giữ quality controls. Pilot nên đo review cycle time, reviewer acceptance, defect-related signals và adoption trước khi ước lượng impact ở quy mô toàn team.

Narrative này mạnh vì:

- Bắt đầu từ customer problem.
- Không hứa quá mức.
- Có hypothesis.
- Có metric để validate.

---

## 7. Customer language > AI language

Nếu khách hàng dùng các từ:

- “backlog”
- “SLA”
- “release velocity”
- “review burden”
- “customer wait time”

hãy dùng lại đúng vocabulary đó.

Tránh ép mọi câu chuyện thành:

- LLM.
- tokens.
- parameters.
- context window.
- benchmark.

Trừ khi technical detail thực sự quan trọng với quyết định.

> Business narrative nên nói ngôn ngữ của **workflow và outcome**, không phải chỉ ngôn ngữ của model.

---

## 8. Value Narrative phải chứa uncertainty hợp lý

Tốt:

> “Pilot sẽ giúp xác định mức time saving thực tế và liệu quality có được duy trì không.”

Không tốt:

> “Giải pháp này chắc chắn sẽ giảm 40% chi phí.”

Khi chưa có evidence, dùng các cụm:

- “we hypothesize…”
- “could improve…”
- “directionally…”
- “we would validate…”
- “based on current evidence…”

Đây không phải nói yếu. Đây là **evidence discipline**.

---

## 9. 30-second Value Narrative

Có thể dùng mẫu cực ngắn:

```text
You told us [pain + evidence].
We see an opportunity to use AI to [workflow change].
If successful, that should move [operational metric],
which matters because [business priority].
We would validate it by measuring [metrics].
```

---

## 10. 2-minute Value Narrative

Thêm 3 thành phần:

- Baseline hiện tại.
- Assumptions còn chưa chắc.
- Directional benefit nếu pilot thành công.

Flow:

```text
Business priority
→ Workflow pain
→ Current evidence
→ AI-enabled change
→ Value hypothesis
→ Measurement plan
→ Directional scale
→ Next step
```

---

## 11. Narrative Quality Checklist

Trước khi trình bày, tự hỏi:

- Đây có phải vấn đề **của khách hàng này** không?
- Có workflow cụ thể không?
- Có evidence từ discovery không?
- Có metric đo được không?
- Có business outcome rõ không?
- Có overclaim không?
- Có nói assumptions nào cần validate không?
- Có phù hợp với stakeholder đang nghe không?

Nếu 2–3 câu đầu có thể copy-paste cho bất kỳ công ty nào, narrative chưa đủ customer-specific.

---

## 12. Common mistakes

### 1. Open with product features

Khách hàng quan tâm outcome trước, feature sau.

### 2. Copy-paste value statement

“Boost productivity” quá chung chung.

### 3. Không dùng discovery evidence

Đã hỏi customer rất nhiều nhưng narrative lại không phản ánh điều họ nói.

### 4. Overload bằng technical detail

Technical detail chỉ nên xuất hiện khi nó hỗ trợ quyết định.

### 5. Không có next step

Một narrative tốt nên kết thúc bằng cách **validate** chứ không chỉ mô tả tiềm năng.

---

## 13. Vocabulary

| English | Hiểu đơn giản |
|---|---|
| Value narrative | Câu chuyện giải thích giá trị |
| Customer-specific | Cụ thể cho khách hàng đó |
| Business priority | Ưu tiên business |
| Stakeholder | Người/nhóm có liên quan |
| Value proposition | Đề xuất giá trị |
| Evidence discipline | Kỷ luật chỉ nói điều có bằng chứng hoặc nêu rõ assumption |
| Directional | Mang tính định hướng/quy mô tương đối |
| Validate | Kiểm chứng bằng dữ liệu thực tế |

---

## 14. Cheat sheet cuối module

```text
A strong customer-specific value narrative:

1. Starts with THEIR business priority
2. Uses THEIR workflow
3. Uses THEIR evidence
4. States a clear value hypothesis
5. Connects to THEIR outcome
6. Explains how value will be measured
7. Separates evidence from assumptions
```

### Công thức tổng hợp toàn bộ “Building the Business Value”

```text
Discovery Evidence
      ↓
Workflow Change
      ↓
Operational Outcome
      ↓
Business Outcome
      ↓
Value Hypothesis
      ↓
Measurement
      ↓
Customer-Specific Narrative
```

Nếu nhớ được chuỗi này, bạn đã nắm được phần cốt lõi của module.
