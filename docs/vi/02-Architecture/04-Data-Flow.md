---
title: Data Flow
id: architecture-data-flow
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
  - data-flow
---

# Data Flow

> Data Flow mô tả cách thông tin di chuyển trong Core Engine.

---

# Mục tiêu

Data Flow đảm bảo toàn bộ quá trình suy luận diễn ra theo một chiều.

Không tồn tại suy luận ngược.

Không tồn tại vòng lặp.

---

# Flow

```text
Input

↓

Observation

↓

Knowledge

↓

Confidence

↓

Decision

↓

Execution
```

---

# Ý nghĩa

## Observation

Thu thập dữ liệu.

Ví dụ.

- Price
- Volume
- RSI
- EMA
- Delta
- OI
- Funding

---

## Knowledge

Canon diễn giải dữ liệu.

Ví dụ.

- Auction
- Momentum
- Structure
- Quality

---

## Confidence

Core Engine tổng hợp các kết quả từ Canon.

Mỗi Layer làm giảm thêm một phần sự không chắc chắn.

---

## Decision

Decision luôn là kết quả.

Không phải điểm bắt đầu.

---

## Execution

Decision được chuyển thành hành động.

---

# Nguyên tắc

Thông tin chỉ đi theo một chiều.

```text
Input

↓

Knowledge

↓

Confidence

↓

Decision
```

Không Layer nào được sửa kết quả của Layer trước.

Layer sau chỉ được phép sử dụng kết quả đã được xác nhận.

---

# Triết lý

Core Engine không truyền dữ liệu.

Core Engine truyền sự hiểu biết.