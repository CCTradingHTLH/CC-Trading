---
title: Validation
id: validation
version: 2.0
status: Stable
author: HTLH
language: vi
created: 2026-07-12
last_updated: 2026-07-12
review_cycle: Monthly
confidence: 95%
tags:
  - input
  - validation
---

# Validation

> Validation xác nhận Observation đã đủ điều kiện để bắt đầu suy luận.

---

# Mục tiêu

Đảm bảo Core Engine chỉ suy luận khi dữ liệu đã đầy đủ.

---

# Quy trình

text Market  ↓  Observation  ↓  Validation  ↓  Knowledge 

---

# Kiểm tra

Validation trả lời ba câu hỏi:

### 1. Observation đã đầy đủ chưa?

Ví dụ:

- Market Image
- Derivatives
- Macro

---

### 2. Observation có mâu thuẫn không?

Nếu các Observation xung đột, quá trình suy luận phải dừng lại.

---

### 3. Observation có đáng tin cậy không?

Nếu dữ liệu thiếu hoặc không nhất quán, không được tiếp tục.

---

# Kết quả

Validation chỉ có hai trạng thái:

text PASS  FAIL 

PASS cho phép Core Engine tiếp tục.

FAIL đưa hệ thống về trạng thái chờ.

---

# Triết lý

Không phải mọi dữ liệu đều đáng để suy luận.

Chỉ những Observation đã được xác nhận mới trở thành nền tảng cho tri thức.