# Transition

> Cách Auction chuyển từ State này sang State khác.

---

# Transition là gì?

Transition là quá trình thay đổi State.

State không thay đổi ngẫu nhiên.

Nó luôn được kích hoạt bởi một hoặc nhiều Event.

---

# Mô hình

```text
Observation

↓

Event

↓

State

↓

Transition

↓

State mới
```

---

# Ví dụ

Long Flush

↓

Absorption

↓

Buyer Control

---

POC được chấp nhận

↓

Acceptance

↓

Buyer Control

---

POC bị từ chối

↓

Rejection

↓

Seller Control

---

Momentum suy yếu

↓

Exhaustion

↓

Neutral

---

# Nguyên tắc

Không Transition nào được xác nhận chỉ bởi một Observation.

Transition luôn cần sự đồng thuận của nhiều Observation.