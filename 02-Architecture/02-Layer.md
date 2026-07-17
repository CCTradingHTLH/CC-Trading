---
title: Layer
id: architecture-layer
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
  - layer
---

# Layer

> Mỗi Layer chịu trách nhiệm trả lời một câu hỏi.

---

# Layer

## Observe

**Mình đang quan sát điều gì?**

---

## Auction

**Thị trường đang đấu giá như thế nào?**

---

## Market Context

**Hành vi này đang diễn ra trong bối cảnh nào?**

---

## Momentum

**Lực đang thay đổi như thế nào?**

---

## Structure

**Thị trường đã phản ứng như thế nào trước sự thay đổi của lực?**

---

## Quality

**Toàn bộ Pipeline đáng tin đến mức nào?**

---

## Decision

**Kết luận hợp lý nhất tại thời điểm hiện tại là gì?**

---

## Signal Weight

**Điều gì ảnh hưởng nhiều nhất đến kết luận?**

---

## Scenario Space

**Những khả năng nào đang tồn tại?**

---

## Execution Planner

**Nếu kịch bản này xảy ra, mình nên hành động như thế nào?**

---

## Reality Feedback

**Thực tế đã diễn ra như thế nào?**

---

# Triết lý

CC Trading tổ chức quá trình suy luận thành các Layer nối tiếp nhau.

Mỗi Layer trả lời một câu hỏi.

Mỗi Layer kế thừa kết quả của Layer trước.

Mỗi câu trả lời làm tăng thêm mức độ hiểu biết về thị trường trước khi chuyển sang Layer tiếp theo.

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

Mỗi Layer có một trách nhiệm rõ ràng.

Toàn bộ Workflow được hình thành từ sự phối hợp của các Layer.

---

> Một Layer tốt chỉ trả lời một câu hỏi.

> Một Workflow tốt kết nối các câu trả lời thành một quá trình suy luận.