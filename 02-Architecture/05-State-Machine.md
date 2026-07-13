---
title: State Machine
id: architecture-state-machine
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
  - state-machine
---

# State Machine

> State Machine mô tả trạng thái suy luận của Core Engine.

---

# Mục tiêu

Core Engine chỉ được phép ở một State tại một thời điểm.

State luôn tiến về phía trước.

---

# State

```text
Input

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

Execution
```

---

# Chuyển State

Core Engine chỉ được chuyển State khi Layer hiện tại đã hoàn thành.

Ví dụ.

```text
Momentum

↓

Structure
```

Hợp lệ.

---

```text
Momentum

↓

Decision
```

Không hợp lệ.

---

# Wait

Wait là một State hợp lệ.

Wait xảy ra khi.

- Confidence chưa đủ.
- Layer hiện tại chưa hoàn thành.
- Có xung đột giữa các Layer.

---

# Nguyên tắc

Không được bỏ qua State.

Không được quay ngược State.

Không tồn tại vòng lặp.

---

# Triết lý

State không đại diện cho dữ liệu.

State đại diện cho mức độ hiểu biết của Core Engine.