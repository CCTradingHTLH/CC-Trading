---
title: Derivatives
id: derivatives
version: 3.1
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

Derivatives ghi nhận hành vi của dòng tiền và hoạt động trên thị trường phái sinh.

Các Observation này bổ sung một góc nhìn quan trọng cho quá trình suy luận của Canon.

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

Derivatives chuyển đổi dữ liệu từ thị trường phái sinh thành Observation đã được chuẩn hóa.

Canon kết hợp các Observation này với những nguồn quan sát khác để xây dựng tri thức.

---

# Nguyên tắc

Mỗi Observation phản ánh một khía cạnh của hành vi thị trường.

Các Observation từ Derivatives được kết hợp với:

- Market Context
- Macro
- Execution

để hình thành một bức tranh quan sát toàn diện.

Giá trị của từng Observation phụ thuộc vào bối cảnh của toàn bộ Pipeline.

---

# Triết lý

Dòng tiền phản ánh cách thị trường đang vận động.

Derivatives giúp hệ thống quan sát hành vi đó dưới góc nhìn của thị trường phái sinh.

Ý nghĩa của các Observation được hình thành khi chúng được đặt trong bối cảnh của Canon.

---

> Derivatives cung cấp bằng chứng.
>
> Canon diễn giải bằng chứng.