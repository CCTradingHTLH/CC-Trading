---
title: Core Engine
id: architecture-core-engine
version: 3.1
status: Freeze
author: HTLH
language: vi
created: 2026-07-12
last_updated: 2026-07-17
review_cycle: Monthly
confidence: 100%
tags:
  - architecture
  - core-engine
  - reasoning
---

🏠 [CC Trading](../README.md) › [Architecture](README.md) › Core Engine

# Core Engine

> Core Engine là bộ máy suy luận cốt lõi của CC Trading.

---

# Mục tiêu

Core Engine chuyển đổi dữ liệu quan sát thành một kết luận có thể giải thích.

Core Engine xây dựng kết luận từ các bằng chứng hiện có.

Mỗi kết luận phản ánh trạng thái hiểu biết của hệ thống tại thời điểm suy luận.

---

# Triết lý

Core Engine tổ chức quá trình suy luận nhằm từng bước giảm sự không chắc chắn.

Sau mỗi Layer:

- Hiểu biết tăng lên.
- Bằng chứng rõ ràng hơn.
- Mức độ tin cậy được cập nhật.

Decision được hình thành khi toàn bộ Pipeline hoàn tất.

---

# Reasoning Workflow

```text
Observe

↓

Auction

↓

Market Context

↓

Momentum

↓

Structure

↓

Quality

↓

Decision

↓

Signal Weight

↓

Scenario Space

↓

Execution Planner

↓

Reality Feedback

↓

Observe
```

Core Engine luôn vận hành theo trình tự này.

---

# Reasoning Principle

Core Engine suy luận thông qua một chuỗi câu hỏi.

```text
Q1

Mình đang quan sát điều gì?

↓

Q2

Thị trường đang đấu giá như thế nào?

↓

Q3

Hành vi này đang diễn ra trong bối cảnh nào?

↓

Q4

Lực đang thay đổi như thế nào?

↓

Q5

Thị trường đã phản ứng như thế nào?

↓

Q6

Toàn bộ Pipeline đáng tin đến mức nào?

↓

Q7

Kết luận hợp lý nhất tại thời điểm hiện tại là gì?

↓

Q8

Điều gì ảnh hưởng nhiều nhất đến kết luận?

↓

Q9

Những khả năng nào đang tồn tại?

↓

Q10

Nếu kịch bản này xảy ra, mình nên hành động như thế nào?

↓

Q11

Thực tế đã diễn ra như thế nào?
```

Mỗi câu hỏi kế thừa câu trả lời của câu hỏi trước.

---

# Layer Responsibility

| Layer | Câu hỏi |
|--------|----------|
| Observe | Mình đang quan sát điều gì? |
| Auction | Thị trường đang đấu giá như thế nào? |
| Market Context | Hành vi này đang diễn ra trong bối cảnh nào? |
| Momentum | Lực đang thay đổi như thế nào? |
| Structure | Thị trường đã phản ứng như thế nào trước sự thay đổi của lực? |
| Quality | Toàn bộ Pipeline đáng tin đến mức nào? |
| Decision | Kết luận hợp lý nhất tại thời điểm hiện tại là gì? |
| Signal Weight | Điều gì ảnh hưởng nhiều nhất đến kết luận? |
| Scenario Space | Những khả năng nào đang tồn tại? |
| Execution Planner | Nếu kịch bản này xảy ra, mình nên hành động như thế nào? |
| Reality Feedback | Thực tế đã diễn ra như thế nào? |

Mỗi Layer chịu trách nhiệm trả lời một câu hỏi.

---

# Decision

Decision là kết quả của toàn bộ Pipeline.

Decision mở đầu cho giai đoạn giải thích, xây dựng kịch bản và lập kế hoạch thực thi.

Decision trở thành đầu vào của:

- Signal Weight.
- Scenario Space.
- Execution Planner.

---

# Reality

Reality luôn có độ ưu tiên cao nhất.

Reality Feedback đánh giá mức độ phù hợp giữa suy luận và thực tế.

Kết quả của Reality Feedback được sử dụng để cập nhật toàn bộ Pipeline.

Một chu kỳ suy luận mới bắt đầu từ Reality.

---

# Quan hệ với Canon

Core Engine tổ chức quá trình suy luận.

Canon cung cấp tri thức cho từng Layer.

Core Engine kết nối các tri thức đó thành một chuỗi suy luận nhất quán.

---

# Quan hệ với Constitution

| Thành phần | Vai trò |
|------------|----------|
| **Constitution** | Định nghĩa các nguyên tắc nền tảng. |
| **Architecture** | Tổ chức quá trình suy luận. |
| **Canon** | Cung cấp tri thức cho từng Layer. |
| **Core Engine** | Điều phối toàn bộ Pipeline suy luận. |
| **Decision** | Kết quả của quá trình suy luận. |

---

# Thiết kế

Core Engine vận hành theo một vòng lặp học hỏi liên tục.

```text
Observe

↓

Reason

↓

Execute

↓

Reality

↓

Observe
```

Mỗi Layer kế thừa kết quả của Layer trước.

Workflow luôn tiến theo một chiều.

Reality khởi đầu cho chu kỳ suy luận tiếp theo.

---

# Tư tưởng cốt lõi

Core Engine hướng tới kết luận hợp lý nhất dựa trên bằng chứng hiện có.

Mỗi Layer giúp giảm thêm một phần sự không chắc chắn.

Reality là tiêu chuẩn cuối cùng để kiểm chứng mọi kết luận.

Quá trình học hỏi liên tục giúp hệ thống ngày càng đáng tin cậy hơn.

---

> Một Core Engine tốt tổ chức quá trình suy luận một cách nhất quán.
>
> Một Core Engine trưởng thành liên tục học hỏi từ thực tế.