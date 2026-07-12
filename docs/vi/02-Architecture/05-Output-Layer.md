---
title: Output Layer
id: architecture-output-layer
version: 1.0
status: Canon
author: HTLH
language: vi
created: 2026-07-12
last_updated: 2026-07-12
review_cycle: Monthly
confidence: 100%
tags:
  - architecture
  - output
  - execution
---

# Output Layer

Output Layer là cầu nối giữa Core Engine và Execution.

Output Layer không suy nghĩ.

Output Layer không diễn giải thị trường.

Output Layer chỉ chuyển Decision thành tín hiệu giao dịch.

---

# Vai trò

```text
Input

↓

Core Engine

↓

Output Layer

↓

Execution
```

---

# Thành phần

Output Layer gồm.

```text
Decision

↓

Signal

↓

Entry

↓

Stop Loss

↓

Take Profit

↓

Risk

↓

Execution
```

---

# Decision

Decision chỉ có ba trạng thái.

```text
LONG

SHORT

WAIT
```

Decision được tạo bởi Core Engine.

Output Layer không được phép thay đổi Decision.

---

# Signal

Signal chuẩn hóa Decision.

Ví dụ.

```text
LONG

↓

LONG SIGNAL
```

Signal chỉ là tín hiệu.

Không phải lệnh giao dịch.

---

# Entry

Output Layer xác định.

- vùng Entry.
- loại Entry.

Ví dụ.

- Market
- Limit

---

# Stop Loss

Output Layer chuẩn hóa Stop Loss.

Core Engine không tính Stop Loss.

---

# Take Profit

Output Layer chuẩn hóa Take Profit.

Có thể.

- TP1
- TP2
- TP3

---

# Risk

Output Layer chuẩn hóa.

- Position Size
- Risk %
- RR

Risk không ảnh hưởng Decision.

---

# Execution

Execution là bước cuối cùng.

Execution chỉ xảy ra khi.

```text
Decision ≠ WAIT
```

---

# Nguyên tắc

Output Layer.

- không đọc dữ liệu thô.
- không diễn giải thị trường.
- không thay đổi Decision.

Output Layer chỉ chuẩn hóa Output của Core Engine.

---

# Triết lý

Core Engine quyết định.

Output Layer thực hiện.