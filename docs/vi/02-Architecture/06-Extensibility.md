---
title: Extensibility
id: architecture-extensibility
version: 2.0
status: Freeze
author: HTLH
language: vi
created: 2026-07-12
last_updated: 2026-07-12
review_cycle: Monthly
confidence: 100%
tags:
  - architecture
  - extensibility
---

# Extensibility

> Extensibility mô tả cách mở rộng hệ thống mà không phá vỡ kiến trúc hiện tại.

---

# Mục tiêu

Cho phép bổ sung tri thức mới.

Không thay đổi Workflow.

Không thay đổi Core Engine.

---

# Nguyên tắc

Mỗi Canon mới phải thuộc đúng Layer.

Ví dụ.

```text
RSI Wave

↓

Momentum
```

---

```text
Volume Profile

↓

Quality
```

---

Không được đặt sai Layer.

Ví dụ.

RSI Wave nằm trong Structure.

Volume Profile nằm trong Momentum.

---

# Workflow

Canon mới phải trả lời đúng một câu hỏi.

Không được trả lời nhiều Layer cùng lúc.

---

# Core Engine

Core Engine không cần biết Canon mới hoạt động như thế nào.

Core Engine chỉ sử dụng kết quả mà Canon trả về.

---

# Khả năng mở rộng

Có thể bổ sung.

- Canon mới.
- Input mới.
- Indicator mới.
- AI Model mới.

Miễn là không thay đổi nguyên lý suy luận của Core Engine.

---

# Triết lý

Core Engine ổn định.

Canon tiến hóa.

Workflow bất biến.