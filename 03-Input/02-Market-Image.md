---
title: Market Image
id: market-image
version: 3.0
status: Stable
author: HTLH
language: vi
created: 2026-07-12
last_updated: 2026-07-17
review_cycle: Monthly
confidence: 100%
tags:
  - input
  - market-image
---

# Market Image

> Market Image định nghĩa các góc nhìn mà CC Trading sử dụng để quan sát thị trường.

---

# Mục tiêu

Chuẩn hóa cách hệ thống thu thập Observation từ nhiều nguồn khác nhau.

Không phụ thuộc vào người sử dụng.

Không phụ thuộc vào nền tảng giao dịch.

Không phụ thuộc vào một loại dữ liệu duy nhất.

---

# Các nguồn quan sát

## Market Context

Quan sát cấu trúc tổng thể của thị trường.

Ví dụ:

- Multi-Timeframe
- Trend
- Range
- Key Levels

---

## Derivatives

Quan sát hành vi của thị trường phái sinh.

Ví dụ:

- Open Interest
- Funding
- Liquidation
- Basis

---

## Macro

Quan sát môi trường thị trường.

Ví dụ:

- News
- Economic Events
- Market Correlation
- Liquidity Environment

---

## Execution

Quan sát dữ liệu phục vụ quá trình thực thi.

Ví dụ:

- Order Flow
- Volume Profile
- Footprint
- DOM
- Liquidity

---

# Vai trò

```text
Reality

↓

Market

↓

Market Image

↓

Observation

↓

Canon
```

Market Image xác định nguồn gốc của Observation.

Market Image không diễn giải dữ liệu.

Market Image không đánh giá dữ liệu.

Market Image không đưa ra kết luận.

---

# Nguyên tắc

Mỗi nguồn quan sát chỉ chịu trách nhiệm cung cấp dữ liệu.

Một Observation có thể kết hợp nhiều nguồn.

Việc diễn giải Observation thuộc về Canon.

---

# Triết lý

Không có một góc nhìn nào phản ánh toàn bộ thị trường.

Market Image giúp hệ thống quan sát cùng một thị trường từ nhiều góc nhìn khác nhau.

Mọi góc nhìn đều được chuẩn hóa thành cùng một ngôn ngữ Observation.

---

> Thị trường là một.

> Góc nhìn có thể khác nhau.

> Observation là ngôn ngữ chung của mọi góc nhìn.