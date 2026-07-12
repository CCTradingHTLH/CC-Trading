---
title: Auction
id: canon-auction
version: 1.0
status: Active Development
author: HTLH
language: vi
created: 2026-07-12
last_updated: 2026-07-12
review_cycle: Monthly
confidence: 100%
tags:
  - canon
  - auction
  - market
---

# Auction

> Auction mô tả hành vi của giá quanh EMA20 và trạng thái vận động hiện tại của thị trường.

---

# Định nghĩa

Auction là lớp tri thức đầu tiên của CC Trading.

Auction diễn giải hành vi của giá thông qua:

- vị trí so với EMA20;
- trạng thái Compression;
- hành vi Cross.

---

# Vai trò

Auction là nền tảng của toàn bộ quá trình phân tích.

```text
Auction

↓

Structure

↓

Momentum

↓

Quality

↓

Decision
```

---

# Thuật ngữ

| Code | Tên đầy đủ | Ý nghĩa |
|------|------------|----------|
| HA | Hold Above EMA20 | Giá duy trì phía trên EMA20. |
| HB | Hold Below EMA20 | Giá duy trì phía dưới EMA20. |
| BC | Bull Compression | Trạng thái nén trong xu hướng tăng. |
| SC | Bear Compression | Trạng thái nén trong xu hướng giảm. |
| XD | Cross Down | Giá cắt xuống EMA20. |
| XDF | Cross Down Failed | Cross Down thất bại. |
| XU | Cross Up | Giá cắt lên EMA20. |
| XUF | Cross Up Failed | Cross Up thất bại. |

---

# Quan hệ với Core Engine

Auction là lớp tri thức đầu tiên được Core Engine sử dụng để diễn giải thị trường.

---

# Triết lý

Giá là kết quả.

Auction là hành vi.

CC Trading đọc hành vi của thị trường thông qua Auction.