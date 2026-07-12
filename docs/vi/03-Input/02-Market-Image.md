---
title: Market Image
id: market-image
version: 2.0
status: Stable
author: HTLH
language: vi
created: 2026-07-12
last_updated: 2026-07-12
review_cycle: Monthly
confidence: 100%
tags:
  - input
  - market-image
---

# Market Image

> Market Image định nghĩa các nguồn quan sát của hệ thống.

---

# Mục tiêu

Chuẩn hóa cách thu thập dữ liệu từ thị trường.

Không phụ thuộc vào người sử dụng.

Không phụ thuộc vào nền tảng.

---

# Các nguồn quan sát

## MC

**Market Context**

Quan sát thị trường thông qua các biểu đồ nhiều khung thời gian.

---

## Derivatives

Quan sát thị trường phái sinh.

---

## Macro

Quan sát môi trường thị trường.

---

## Execution

Quan sát dữ liệu phục vụ xác nhận điểm vào.

---

# Vai trò

```text
Market

↓

Market Image

↓

Observation

↓

Core Engine
```

Market Image chỉ mô tả **nguồn gốc của Observation**.

Nó không diễn giải.

Không đánh giá.

Không đưa ra kết luận.

---

# Nguyên tắc

Mỗi nguồn quan sát chỉ chịu trách nhiệm cung cấp dữ liệu.

Việc diễn giải dữ liệu thuộc về các thành phần phía sau.

---

# Triết lý

Quan sát thị trường từ nhiều góc nhìn.

Chuẩn hóa thành một ngôn ngữ chung.

Đó là nền tảng của mọi quá trình suy luận.