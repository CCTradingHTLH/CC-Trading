---
title: Core Engine
id: architecture-core-engine
version: 3.0
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

# Core Engine

> Core Engine là bộ máy suy luận cốt lõi của CC Trading.

---

# Mục tiêu

Core Engine chuyển đổi dữ liệu quan sát thành một kết luận có thể giải thích.

Core Engine không dự đoán thị trường.

Core Engine không tạo ra sự thật.

Core Engine suy luận dựa trên bằng chứng hiện có.

---

# Triết lý

Core Engine không cố tìm tín hiệu.

Core Engine tổ chức quá trình suy luận nhằm giảm sự không chắc chắn.

Sau mỗi Layer.

- Hiểu biết tăng lên.
- Bằng chứng rõ ràng hơn.
- Mức độ tin cậy được cập nhật.

Decision chỉ xuất hiện khi toàn bộ Pipeline đã hoàn thành.

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

Core Engine luôn tuân theo trình tự này.

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

Kết luận hợp lý nhất là gì?

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

Một câu hỏi chỉ được trả lời sau khi câu hỏi trước đã hoàn thành.

---

# Layer Responsibility

| Layer | Câu hỏi |
|--------|----------|
| Observe | Mình đang quan sát điều gì? |
| Auction | Thị trường đang đấu giá như thế nào? |
| Market Context | Hành vi này đang diễn ra trong bối cảnh nào? |
| Momentum | Lực đang thay đổi như thế nào? |
| Structure | Thị trường đã phản ứng như thế nào? |
| Quality | Toàn bộ Pipeline đáng tin đến mức nào? |
| Decision | Kết luận hợp lý nhất là gì? |
| Signal Weight | Điều gì ảnh hưởng nhiều nhất đến kết luận? |
| Scenario Space | Những khả năng nào đang tồn tại? |
| Execution Planner | Nếu kịch bản này xảy ra, mình nên hành động như thế nào? |
| Reality Feedback | Thực tế đã diễn ra như thế nào? |

Mỗi Layer chỉ chịu trách nhiệm cho đúng một câu hỏi.

---

# Decision

Decision luôn là kết quả của toàn bộ Pipeline.

Decision không phải là điểm kết thúc.

Decision là đầu vào của:

- Signal Weight.
- Scenario Space.
- Execution Planner.

---

# Reality

Reality luôn có độ ưu tiên cao nhất.

Reality Feedback không bảo vệ Decision trước đó.

Reality cập nhật toàn bộ Pipeline.

Một chu kỳ suy luận mới luôn bắt đầu từ Reality.

---

# Quan hệ với Canon

Core Engine không chứa tri thức.

Core Engine tổ chức quá trình suy luận.

Canon cung cấp tri thức cho từng Layer.

Core Engine sử dụng Canon để xây dựng một chuỗi suy luận nhất quán.

---

# Quan hệ với Constitution

Constitution quy định các nguyên tắc nền tảng.

Architecture tổ chức quá trình suy luận.

Canon định nghĩa tri thức.

Core Engine vận hành quá trình suy luận.

Decision là kết quả của toàn bộ Pipeline.

---

# Thiết kế

Core Engine luôn vận hành theo một vòng lặp học hỏi.

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

Không bỏ qua Layer.

Không nhảy Layer.

Không suy luận ngược.

Mọi chu kỳ đều kết thúc bằng Reality và bắt đầu lại từ Observation.

---

# Tư tưởng cốt lõi

Core Engine không cố gắng luôn đúng.

Core Engine cố gắng đưa ra kết luận hợp lý nhất dựa trên bằng chứng hiện có.

Mỗi Layer giúp giảm thêm một phần sự không chắc chắn.

Reality luôn là tiêu chuẩn cuối cùng của mọi suy luận.

---

> Một Core Engine tốt không dự đoán tương lai.

> Một Core Engine tốt liên tục học hỏi từ thực tế.