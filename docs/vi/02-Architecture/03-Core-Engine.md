---
title: Core Engine
id: architecture-core-engine
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
  - core-engine
  - reasoning
---

# Core Engine

> Core Engine là bộ não suy luận của CC Trading.

---

# Mục tiêu

Core Engine chuyển đổi dữ liệu đầu vào thành quyết định giao dịch.

Core Engine không dự đoán thị trường.

Core Engine chỉ suy luận dựa trên dữ liệu hiện có.

---

# Triết lý

Core Engine không cố tìm tín hiệu.

Core Engine cố giảm sự không chắc chắn.

Sau mỗi Layer.

Mức độ hiểu biết phải tăng lên.

Mức độ chắc chắn phải tăng lên.

Decision chỉ xuất hiện khi toàn bộ Workflow đã hoàn thành.

---

# Reasoning Workflow

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

Core Engine không được thay đổi thứ tự này.

---

# Reasoning Principle

Core Engine suy luận bằng chuỗi câu hỏi.

```text
Q1

Mình có dữ liệu gì?

↓

Q2

Giá đang làm gì?

↓

Q3

Thị trường đang ở đâu?

↓

Q4

Lực đang đi đâu?

↓

Q5

Giá có xác nhận lực đó không?

↓

Q6

Có đáng giao dịch không?

↓

Q7

Nên làm gì?

↓

Q8

Thực hiện như thế nào?
```

Một câu hỏi chỉ được trả lời sau khi câu hỏi trước đã hoàn thành.

---

# Layer Responsibility

| Layer | Câu hỏi |
|--------|----------|
| Input | Mình có dữ liệu gì? |
| Auction | Giá đang làm gì? |
| Market Context | Thị trường đang ở đâu? |
| Momentum | Lực đang đi đâu? |
| Structure | Giá có xác nhận lực không? |
| Quality | Có đáng giao dịch không? |
| Decision | Nên làm gì? |
| Execution | Thực hiện như thế nào? |

Mỗi Layer chỉ chịu trách nhiệm cho đúng một câu hỏi.

---

# Confidence

Core Engine không trực tiếp tạo Decision.

Core Engine tạo ra mức độ Confidence sau mỗi Layer.

Confidence tăng dần khi Workflow tiến về phía trước.

Nếu một Layer không đủ xác nhận.

Workflow dừng lại.

Decision sẽ là Wait.

---

# Decision

Decision luôn là kết quả.

Không bao giờ là điểm bắt đầu.

Decision chỉ được tạo khi.

- Workflow hoàn thành.
- Confidence đủ cao.
- Không còn xung đột giữa các Layer.

---

# Wait

Wait là một Decision hợp lệ.

Wait không có nghĩa là thiếu dữ liệu.

Wait có nghĩa là Confidence hiện tại chưa đủ để hành động.

---

# Quan hệ với Canon

Core Engine không chứa tri thức.

Core Engine chỉ sử dụng Canon.

Canon trả lời từng câu hỏi.

Core Engine tổng hợp các câu trả lời thành một quyết định cuối cùng.

---

# Quan hệ với Constitution

Constitution quy định nguyên tắc.

Canon định nghĩa tri thức.

Core Engine suy luận.

Decision hành động.

---

# Thiết kế

Core Engine luôn đi theo một chiều.

```text
Observe

↓

Understand

↓

Confirm

↓

Evaluate

↓

Decide

↓

Execute
```

Không tồn tại suy luận ngược.

Không bỏ qua Layer.

Không nhảy Layer.

---

# Tư tưởng cốt lõi

Core Engine không cố gắng luôn đúng.

Core Engine chỉ cố gắng đưa ra quyết định sáng suốt nhất có thể.

Mỗi Layer giúp giảm thêm một phần sự không chắc chắn.

Decision luôn là kết quả của toàn bộ quá trình suy luận.