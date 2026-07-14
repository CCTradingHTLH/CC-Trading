# Engine 01 · Auction

> Quan sát hành vi trao đổi giữa người mua và người bán.

---

# Mục đích

Auction là điểm khởi đầu của toàn bộ Canon.

Engine này chuyển dữ liệu thô thành quan sát có ý nghĩa.

Mọi Engine phía sau đều kế thừa kết quả từ Auction.

---

# Câu hỏi

Điều gì đang thực sự diễn ra giữa người mua và người bán?

---

# Đầu vào

Dữ liệu thị trường thô.

Ví dụ:

- Price
- Volume
- Delta
- CVD
- OI
- Funding
- Aggressive Orders
- Liquidation
- Volume Profile
- Heatmap
- Time

---

# Đầu ra

Một Observation chuẩn hóa.

Observation chỉ mô tả hành vi.

Observation chưa tạo kết luận.

---

# Vai trò trong Pipeline

Observation

↓

Auction

↓

Market Context

---

# Cấu trúc

01 · Definition

Định nghĩa bản chất của Auction.

↓

02 · Observation

Chuẩn hóa dữ liệu quan sát.

↓

03 · State

Định nghĩa các trạng thái Auction.

↓

04 · Transition

Định nghĩa cách Auction chuyển trạng thái.

↓

05 · Examples

Ví dụ thực tế.

---

# Triết lý

Quan sát đúng tạo nên toàn bộ Pipeline.