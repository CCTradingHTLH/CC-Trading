# 📈 Auction

> **Hiểu điều gì đang xảy ra giữa người mua và người bán.**

---

# Mục tiêu

Auction là tầng đầu tiên của Canon.

Nó mô tả quá trình cạnh tranh giữa người mua và người bán để hình thành giá.

Auction **không dự đoán xu hướng**.

Auction chỉ trả lời một câu hỏi:

> **Ai đang kiểm soát thị trường ở thời điểm hiện tại?**

---

# Vai trò

Trong hệ thống CC Trading, Auction luôn được quan sát đầu tiên.

Nó cung cấp những tín hiệu ban đầu về sự thay đổi của dòng tiền, lực mua và lực bán trước khi các yếu tố khác như Momentum hay Structure xác nhận.

Workflow:

```text
Observation

↓

Auction

↓

Momentum

↓

Structure

↓

Quality

↓

Decision
```

---

# Cấu trúc

```text
01 Definition

↓

02 State

↓

03 Transition

↓

04 Examples
```

---

# Nguyên tắc

Auction không tạo Decision.

Auction chỉ tạo Observation.

Decision chỉ được đưa ra sau khi kết hợp:

- Auction
- Momentum
- Structure
- Quality

---

# Mục tiêu cuối cùng

Xây dựng một mô hình có khả năng mô tả mọi trạng thái của cuộc đấu giá trên thị trường bằng các khái niệm rõ ràng, nhất quán và có thể suy luận.

---

> **Observation before Prediction.**
>
> *Hiểu điều gì đang xảy ra trước khi cố gắng dự đoán điều sẽ xảy ra.*