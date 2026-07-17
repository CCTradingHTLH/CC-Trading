---
title: Derivatives
id: derivatives
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
  - derivatives
---

# Derivatives

> Derivatives chuẩn hóa các Observation đến từ thị trường phái sinh.

---

# Mục tiêu

Quan sát hành vi của dòng tiền trên thị trường phái sinh.

Không dự đoán giá.

Không tạo kết luận.

---

# Thành phần

Observation có thể bao gồm:

- Open Interest
- Funding Rate
- CVD
- VPIN
- Auction Flow
- Aggressive Orders
- Liquidation
- Basis

---

# Vai trò

```text
Derivatives

↓

Observation

↓

Canon
```

Derivatives chuyển đổi dữ liệu phái sinh thành Observation đã được chuẩn hóa.

Canon không đọc trực tiếp dữ liệu phái sinh.

Canon chỉ sử dụng Observation đã được xác nhận.

---

# Nguyên tắc

Mỗi Observation phản ánh một góc nhìn của thị trường.

Không Observation nào đủ để tạo ra Decision một cách độc lập.

Observation từ Derivatives phải được kết hợp với các nguồn quan sát khác trong Canon.

Observation không mang ý nghĩa kết luận.

---

# Triết lý

Dòng tiền không nói thị trường sẽ đi đâu.

Dòng tiền chỉ phản ánh điều thị trường đang làm.

Ý nghĩa của dòng tiền chỉ xuất hiện khi được đặt trong bối cảnh của toàn bộ Canon.

---

> Derivatives cung cấp bằng chứng.

> Canon diễn giải bằng chứng.