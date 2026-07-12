---
title: Input Specification
id: architecture-input-specification
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
  - input
  - data-schema
---

# Input Specification

Input Specification định nghĩa toàn bộ dữ liệu đầu vào của CC Trading.

Mọi phân tích đều phải bắt đầu từ Input.

Nếu Input không đầy đủ hoặc không đúng định dạng.

↓

Output mặc định là

```text
WAIT
```

---

# Nguyên tắc

Input Specification chỉ ghi nhận và chuẩn hóa dữ liệu.

Input Specification không đưa ra kết luận.

Mọi diễn giải sẽ được thực hiện trong Core Engine.

---

# Quy ước

Nếu một trường dữ liệu không ghi rõ khung thời gian.

↓

Mặc định sử dụng khung thời gian chuẩn của CC Trading.

---

# Khung thời gian mặc định

| Thành phần | Khung thời gian |
|------------|----------------:|
| Auction | M5 |
| EMA20 | M5 |
| OI | M5 |
| Delta | M5 |
| Volume | M5 |
| CVD | M5 |
| Aggressive Liquidation | M5 |
| Funding | Realtime |
| VPIN | Realtime |
| Volume Profile | M30 |
| Long / Short Ratio | H1 |
| Fear & Greed | Daily |
| SonicR | Theo biểu đồ |
| RSI | Theo biểu đồ |

---

# 1. Auction (A)

Khung thời gian mặc định

```text
M5
```

Định dạng

```text
A:
State / Event (Value), EMA Direction (Value), POC, VP1
```

Ví dụ

```text
A:

HB / XD (-1700), EMA↓(-1383), POC:63886, VP1:64087
```

---

## 1.1 State

State mô tả trạng thái hiện tại của Auction.

Ví dụ

```text
HA

HB

BC

SC
```

State luôn đứng đầu.

---

## 1.2 Event

Event mô tả sự kiện vừa xảy ra.

Ví dụ

```text
XU

XD

XUF

XDF
```

Nếu Event có giá trị đi kèm.

Ví dụ

```text
XD (-1700)
```

↓

Giá trị trong ngoặc là **Auction Value**.

Auction Value phản ánh cường độ của Event tại thời điểm xuất hiện.

---

## 1.3 EMA

Định dạng

```text
EMA↑(-1383)
```

Trong đó

```text
-1383
```

là **EMA20 Value**.

EMA20 Value phản ánh giá trị của EMA20 tại thời điểm ghi nhận.

Không phải khoảng cách giữa giá và EMA.

---

## 1.4 Auction POC

Nếu POC và VP1 xuất hiện trên cùng dòng với Auction.

Ví dụ

```text
A:

...

POC:63886

VP1:64087
```

↓

Đây là POC và VP1 của Auction.

---

# 2. Open Interest

Khung thời gian mặc định

```text
M5
```

Định dạng

```text
OI:
0.19
```

Giá trị thể hiện thay đổi Open Interest.

---

# 3. Delta

Khung thời gian mặc định

```text
M5
```

Định dạng

```text
D:

-84 / -33 / 5
```

Ba giá trị lần lượt là

```text
n-2

↓

n-1

↓

n
```

tức ba cây nến M5 gần nhất.

Không phải ba khung thời gian.

Delta phản ánh Evolution của Aggression.

---

# 4. Volume

Khung thời gian mặc định

```text
M5
```

Định dạng

```text
V:

R46 / G21 / R13
```

Ba giá trị lần lượt là

```text
n-2

↓

n-1

↓

n
```

tức ba cây nến M5 gần nhất.

Ký hiệu

```text
G

=

Bull Volume

R

=

Bear Volume
```

Volume phản ánh Evolution của Momentum.

---

# 5. CVD

Khung thời gian mặc định

```text
M5
```

Định dạng

```text
CVD:

-1.2K
```

Giá trị Cumulative Volume Delta tại thời điểm ghi nhận.

---

# 6. Aggressive Liquidation

Khung thời gian mặc định

```text
M5
```

Định dạng

```text
Agg Liq:

L 1.2M

S 800K
```

Trong đó

```text
L

=

Long Liquidation

S

=

Short Liquidation
```

---

# 7. Funding

Khung thời gian mặc định

```text
Realtime
```

Định dạng

```text
Funding:

0.004%
```

Funding Rate tại thời điểm ghi nhận.

---

# 8. VPIN

Khung thời gian mặc định

```text
Realtime
```

Định dạng

```text
VPIN:

0.79
```

---

# 9. Volume Profile

Khung thời gian mặc định

```text
M30
```

Định dạng

```text
Volume Profile

POC

VAH

VAL
```

Hoặc

```text
VP

POC

VAH

VAL
```

Nếu POC xuất hiện sau mục Volume Profile (hoặc VP).

↓

Đây là POC của Volume Profile.

Không phải POC của Auction.

---

# 10. Long / Short Ratio

Khung thời gian mặc định

```text
H1
```

Định dạng

```text
Global

Top Accounts

Top Positions
```

Ví dụ

```text
Global:

1.02

Top Accounts:

1.40

Top Positions:

1.37
```

---

# 11. Fear & Greed

Khung thời gian mặc định

```text
Daily
```

Định dạng

```text
Fear & Greed:

25
```

---

# 12. SonicR

Khung thời gian

Theo biểu đồ được cung cấp.

Ví dụ

- D1
- H4
- H1
- M15

Đọc các thành phần:

- EMA34
- EMA89
- EMA200
- EMA610

---

# 13. RSI

Khung thời gian

Theo biểu đồ được cung cấp.

Ví dụ

```text
RSI H4:

54.4
```

hoặc

```text
RSI D1:

61.2
```

---

# Input Canon

Input Specification chỉ định nghĩa:

- dữ liệu là gì;
- được ghi như thế nào;
- ý nghĩa của từng trường;
- khung thời gian mặc định của từng trường.

Input Specification không giải thích thị trường.

Việc diễn giải được thực hiện trong Core Engine.

---

# Triết lý

```text
Raw Market

↓

Standardized Input

↓

Core Engine
```

Input Specification chuẩn hóa dữ liệu.

Input Specification không đưa ra kết luận.

Mọi kết luận đều thuộc Core Engine.

Nếu Input Specification thay đổi.

↓

Core Engine phải cập nhật theo.

Nếu Core Engine thay đổi.

↓

Input Specification không cần thay đổi.