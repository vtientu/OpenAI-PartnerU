# 04. Defining Success Signals

## 1. Mục tiêu của section

Sau khi đã:

1. **Translating discovery into use cases** – chuyển discovery thành các candidate use cases.
2. **Evaluating candidate use cases** – đánh giá từng candidate.
3. **Prioritizing use cases** – xác định use case nào nên làm trước.

Bước tiếp theo là:

> **Defining success signals – xác định những tín hiệu cho biết use case có thực sự tạo ra giá trị hay không.**

Nói ngắn gọn:

```text
Use case
→ Test
→ Observe evidence
→ Decide whether it is working
```

Nếu không định nghĩa success signal từ trước, sau khi pilot xong rất dễ rơi vào tình trạng:

```text
“It looked useful.”
“People seemed to like it.”
“The demo worked.”
```

Những câu này chưa đủ để chứng minh use case thành công.

---

# 2. Success signal là gì?

**Success signal** = một dấu hiệu có thể quan sát hoặc đo lường được, giúp trả lời:

> “Có evidence nào cho thấy workflow đã được cải thiện theo hướng chúng ta kỳ vọng?”

Ví dụ:

### Không tốt

```text
AI gives good answers.
```

Vấn đề:

- “good” nghĩa là gì?
- ai đánh giá?
- so với baseline nào?
- đo như thế nào?

### Tốt hơn

```text
Support agents complete responses with fewer manual edits.
```

Hoặc cụ thể hơn:

```text
Average number of manual revisions per response decreases.
```

---

# 3. Success signal phải bắt nguồn từ problem

Success signal không nên được nghĩ ra độc lập.

Nó phải quay lại discovery.

Ví dụ discovery:

```text
Problem:
Support agents spend too much time searching
across multiple internal documents.
```

Candidate use case:

```text
AI retrieves relevant information
and drafts a response.
```

Expected value:

```text
Reduce time spent finding information.
```

Success signal:

```text
Time to produce a first response decreases.
```

Flow đầy đủ:

```text
Problem
↓
Desired outcome
↓
Use case
↓
Success signal
↓
Evidence
```

---

# 4. Activity không giống Outcome

Đây là một distinction rất quan trọng.

## Activity signal

Cho biết mọi người **đang sử dụng** AI.

Ví dụ:

```text
100 prompts were sent.
50 employees tried the workflow.
```

Những số này hữu ích, nhưng chưa chứng minh business value.

---

## Outcome signal

Cho biết workflow **thực sự được cải thiện**.

Ví dụ:

```text
Time required for the task decreased by 30%.

Revisions decreased from 4 rounds to 2.

More tasks were completed on time.
```

Do đó:

```text
Usage ≠ Value
```

Một workflow có thể có usage cao nhưng không tạo ra improvement đáng kể.

---

# 5. Các nhóm Success Signals phổ biến

## 5.1 Speed / Time

AI có giúp công việc nhanh hơn không?

Ví dụ:

```text
Time to complete task ↓
Time to first draft ↓
Time to decision ↓
Number of workflow steps ↓
```

### Frontend example

Trước AI:

```text
Understand legacy component
→ 40 minutes
```

Sau AI:

```text
Understand legacy component
→ 15 minutes
```

Success signal:

```text
Average investigation time decreases.
```

---

## 5.2 Quality

AI có giúp output tốt hơn không?

Ví dụ:

```text
Fewer errors
Fewer missing fields
Better completeness
Higher reviewer acceptance
```

Frontend example:

```text
Use case:
AI generates initial unit tests.

Success signal:
Percentage of generated tests accepted
with minimal modification.
```

---

# 5.3 Consistency

AI có giúp output ổn định hơn không?

Ví dụ:

```text
Reports follow the same structure.
Responses follow policy more consistently.
Required information is less frequently omitted.
```

Đây đặc biệt quan trọng với workflow:

- support
- compliance
- reports
- documentation
- customer communication

---

# 5.4 Effort

Không chỉ đo thời gian.

Một workflow có thể vẫn mất 30 phút, nhưng mental effort giảm đáng kể.

Ví dụ:

Trước:

```text
Developer manually searches:
components
→ hooks
→ APIs
→ types
→ documentation
```

Sau:

```text
AI prepares the initial dependency explanation.
Developer verifies it.
```

Possible signal:

```text
Manual search steps required per task decrease.
```

---

# 5.5 Adoption / Repeat Use

Một signal rất hữu ích trong pilot là:

> Người dùng có quay lại sử dụng workflow không?

Ví dụ:

```text
Tried once
→ weak evidence
```

so với:

```text
Uses AI workflow every week
→ stronger evidence
```

Các signal:

```text
Repeat use
Active users
Reuse across teammates
Percentage of eligible workflows using AI
```

Repeat use thường cho thấy workflow có practical value tốt hơn việc chỉ thử một lần.

---

# 5.6 Reliability

AI workflow có tạo kết quả đủ ổn định để dựa vào không?

Ví dụ:

```text
Successful completion rate
Failure rate
Escalation rate
Required human correction
```

Với AI system, reliability rất quan trọng vì:

```text
Great demo
≠
Reliable workflow
```

---

# 6. Baseline – phải biết “trước AI” như thế nào

Muốn biết AI cải thiện gì, cần có **baseline**.

Baseline = trạng thái hiện tại trước khi áp dụng AI.

Ví dụ:

```text
Current workflow:
Draft report = 90 minutes
Average revisions = 4
```

Sau pilot:

```text
AI-assisted workflow:
Draft report = 45 minutes
Average revisions = 2
```

Bây giờ mới có evidence để so sánh.

Mental model:

```text
Before
vs
After
```

Nếu không có baseline:

```text
“AI saved time.”
```

sẽ rất khó chứng minh.

---

# 7. Leading signals và Lagging signals

Có thể chia success signals thành 2 nhóm.

## Leading signals

Xuất hiện sớm và giúp ta biết workflow có đang đi đúng hướng không.

Ví dụ:

```text
Users trying workflow
Repeat usage
Fewer edits
Reduced completion time
```

Rất hữu ích trong pilot ngắn.

---

## Lagging signals

Xuất hiện muộn hơn và thường gắn trực tiếp với business outcome.

Ví dụ:

```text
Customer satisfaction ↑
Support cost ↓
Revenue ↑
Retention ↑
Cycle time across organization ↓
```

Trong giai đoạn đầu, thường chưa đủ thời gian để thấy lagging signal.

Do đó:

```text
Early pilot
→ leading signals

Scaled deployment
→ stronger business outcome signals
```

---

# 8. Success signals nên ít và rõ

Một lỗi phổ biến:

```text
Track everything.
```

Nếu mỗi use case có 20 metrics:

- khó thu thập
- khó hiểu
- khó quyết định
- team mất focus

Thường nên hỏi:

> “Một hoặc hai signals nào sẽ giúp chúng ta biết use case này có đáng tiếp tục không?”

Ví dụ:

```text
Use case:
AI summarizes customer meetings.

Success signals:
1. Preparation/follow-up time decreases.
2. Fewer important action items are missed.
```

Hai signals này thường hữu ích hơn 15 vanity metrics.

---

# 9. Success criteria vs Success signal

Hai thuật ngữ khá gần nhau.

## Success signal

Evidence chúng ta quan sát.

Ví dụ:

```text
Average drafting time decreases.
```

## Success criteria

Ngưỡng hoặc điều kiện chúng ta dùng để quyết định “đủ tốt”.

Ví dụ:

```text
Average drafting time decreases by at least 25%
without reducing reviewer-rated quality.
```

Có thể nhớ:

```text
Signal
= What will we observe?

Criteria
= What level would count as success?
```

---

# 10. Guardrail Metrics

Không chỉ hỏi:

```text
What should improve?
```

Cũng phải hỏi:

```text
What must NOT get worse?
```

Ví dụ:

```text
Goal:
Reduce support response time.
```

Nếu AI giúp response nhanh hơn 50% nhưng accuracy giảm mạnh thì không phải outcome mong muốn.

Do đó:

```text
Primary signal:
Response time ↓

Guardrail:
Accuracy must remain acceptable.
```

Một số guardrails:

```text
Accuracy
Safety
Compliance
Customer experience
Error rate
Cost
Human review requirements
```

---

# 11. Example hoàn chỉnh – Customer Support

## Discovery

```text
Agents spend 15 minutes searching
multiple internal documents per case.
```

## Use case

```text
AI retrieves relevant approved information
and drafts an initial response.
```

## Expected outcome

```text
Agents answer customers faster.
```

## Baseline

```text
Average response preparation:
15 minutes
```

## Success signals

```text
1. Average response preparation time decreases.
2. Manual revision effort decreases.
3. Agents repeatedly use the workflow.
```

## Guardrails

```text
Accuracy must not degrade.
Responses must remain grounded in approved sources.
```

---

# 12. Example dành cho Frontend Developer

Giả sử vấn đề là:

```text
Developers spend significant time understanding
unfamiliar legacy React components.
```

Use case:

```text
AI analyzes a component and explains:
- responsibility
- props
- dependencies
- state
- hooks
- related APIs
```

## Baseline

```text
Average investigation time:
45 minutes
```

## Success signals

```text
Investigation time ↓

Number of manual searches ↓

Developers reuse the workflow
for other unfamiliar components.
```

## Quality guardrail

Developer vẫn phải xác minh:

```text
Explanation matches actual code behavior.
```

Nếu AI tiết kiệm thời gian nhưng thường xuyên giải thích sai dependency thì use case chưa thực sự thành công.

---

# 13. Example thứ hai – AI Test Generation

## Problem

```text
Developers postpone unit tests
because writing boilerplate takes time.
```

## Use case

```text
AI generates the first version
of unit tests for React components.
```

## Success signals

```text
Time to create tests ↓

Percentage of generated tests
accepted with small edits ↑

Test coverage for targeted components ↑
```

## Guardrails

```text
Tests must verify meaningful behavior.

Passing tests must not simply reflect
incorrect assumptions generated by AI.
```

---

# 14. Evidence mạnh và evidence yếu

### Weak

```text
“I liked it.”

“The demo looked impressive.”

“AI generated a response.”
```

### Stronger

```text
Task time:
60 min → 35 min

Revision rounds:
4 → 2

8/10 users reused the workflow
during the following week.

Reviewer acceptance:
70% → 88%
```

Rule:

```text
Opinion
< Observation
< Measured Evidence
```

Không phải mọi workflow đều cần số liệu cực kỳ chính xác, nhưng evidence càng concrete thì decision càng tốt.

---

# 15. Một success signal tốt thường có 5 đặc điểm

```text
Observable
Relevant
Measurable enough
Connected to business value
Practical to collect
```

Bạn có thể kiểm tra bằng câu hỏi:

```text
Can we actually observe this during the test?
```

Nếu câu trả lời là “không”, signal có thể đang quá abstract.

---

# 16. Template để định nghĩa Success Signals

```text
Use case:
[What workflow are we improving?]

Current problem:
[What is difficult today?]

Expected outcome:
[What should become better?]

Baseline:
[What happens today?]

Success signal #1:
[Observable change]

Success signal #2:
[Observable change]

Success criteria:
[What level would be encouraging enough to continue?]

Guardrail:
[What must not get worse?]

Evidence source:
[Where will the evidence come from?]
```

---

# 17. Câu hỏi Discovery hỗ trợ việc định nghĩa Success Signals

Khi nói chuyện với customer, có thể hỏi:

```text
How do you know this workflow is working well today?

How long does this task usually take?

How often does it happen?

Where do errors or revisions occur?

What would noticeably improve for the user?

What metric does the team already track?

What would make you say this test was worth continuing?

What must not get worse?
```

Những câu này biến một mục tiêu mơ hồ thành evidence có thể kiểm chứng.

---

# 18. Những lỗi phổ biến

## Error 1 – Chỉ đo adoption

```text
100 users tried AI.
```

Không chứng minh được value.

---

## Error 2 – Không có baseline

```text
AI saved a lot of time.
```

Không biết “a lot” là bao nhiêu.

---

## Error 3 – Signal quá abstract

```text
Improve productivity.
```

Productivity cụ thể là gì?

---

## Error 4 – Có metric nhưng không liên quan business problem

Ví dụ:

```text
Number of prompts ↑
```

trong khi problem ban đầu là:

```text
Customer response quality is inconsistent.
```

Hai thứ không trực tiếp liên kết.

---

## Error 5 – Chỉ tối ưu speed

```text
Faster
```

không đủ nếu:

```text
Quality ↓
Accuracy ↓
Risk ↑
```

---

# 19. Mental Model quan trọng

```text
DISCOVERY
↓
What hurts?

USE CASE
↓
How could AI help?

EXPECTED OUTCOME
↓
What should improve?

SUCCESS SIGNAL
↓
What evidence would show improvement?

SUCCESS CRITERIA
↓
How much improvement is enough?

GUARDRAIL
↓
What must not get worse?
```

---

# 20. Liên kết với các section trước

```text
1. Translating discovery into use cases
   ↓
   Create candidate use cases

2. Evaluating candidate use cases
   ↓
   Assess value, complexity, readiness

3. Prioritizing use cases
   ↓
   Decide what to test first

4. Defining success signals
   ↓
   Decide what evidence will tell us
   whether the test is working
```

Sau bước này, một use case bắt đầu trở nên **testable**.

---

# 21. Những câu cần nhớ

```text
Usage ≠ Value
```

```text
Demo success ≠ Workflow success
```

```text
No baseline
→ weak evidence
```

```text
A success signal should be observable.
```

```text
Measure what matters to the workflow,
not what is easiest to count.
```

Và mental model quan trọng nhất:

```text
Problem
→ Outcome
→ Signal
→ Evidence
→ Decision
```

---

# 22. Vocabulary

| English | Nghĩa dễ hiểu |
|---|---|
| Success signal | Tín hiệu cho thấy use case đang tạo giá trị |
| Success criteria | Tiêu chí/ngưỡng để xem là đạt |
| Baseline | Trạng thái/số liệu trước khi áp dụng AI |
| Outcome | Kết quả thực tế mong muốn |
| Activity | Hoạt động được thực hiện |
| Adoption | Mức độ người dùng bắt đầu sử dụng |
| Repeat use | Người dùng quay lại sử dụng |
| Leading signal | Tín hiệu xuất hiện sớm |
| Lagging signal | Kết quả xuất hiện muộn hơn |
| Guardrail | Chỉ số/điều kiện không được xấu đi |
| Evidence | Bằng chứng |
| Reliability | Độ ổn định/tin cậy |
| Revision | Chỉnh sửa lại |
| Acceptance rate | Tỷ lệ output được chấp nhận |
| Pilot | Thử nghiệm có giới hạn |

---

# 23. Cheat Sheet

```text
Defining Success Signals

1. Start from the problem
2. Define the desired outcome
3. Establish a baseline
4. Choose 1–2 observable signals
5. Define success criteria when useful
6. Add guardrails
7. Decide how evidence will be collected
8. Test
9. Compare evidence with expectations
10. Continue, adjust, or stop
```

## Một câu tóm tắt

> **A strong AI use case is not only clear about what AI will do; it is also clear about what evidence would show that the workflow became meaningfully better.**
