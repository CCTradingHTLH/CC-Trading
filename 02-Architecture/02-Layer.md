---
title: Layer
id: architecture-layer
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
  - layer
---

# Layer

> Mỗi Layer chỉ chịu trách nhiệm trả lời một câu hỏi.

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

CC Trading không nhảy cóc giữa các Layer.

Mỗi Layer chỉ trả lời đúng một câu hỏi.

Mỗi Layer chỉ sử dụng kết quả của Layer trước đó.

Chỉ khi câu hỏi hiện tại được trả lời đủ rõ ràng thì hệ thống mới chuyển sang Layer tiếp theo.

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

Mỗi Layer đều có trách nhiệm riêng.

Không Layer nào được phép thay thế Layer khác.

---

> Một Layer tốt không trả lời nhiều câu hỏi.

> Một Layer tốt chỉ trả lời đúng một câu hỏi.