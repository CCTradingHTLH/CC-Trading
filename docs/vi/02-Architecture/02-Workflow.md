---
title: Workflow
id: architecture-workflow
version: 1.0
status: Active Development
author: HTLH
language: vi
created: 2026-07-12
last_updated: 2026-07-12
review_cycle: Monthly
confidence: 100%
tags:
  - architecture
  - workflow
  - decision
---

# Workflow

Workflow định nghĩa cách CC Trading xử lý thông tin và đưa ra quyết định.

Mọi giao dịch đều phải đi qua cùng một quy trình.

Không được bỏ qua.

Không được đảo thứ tự.

---

# Workflow tổng thể

```text
Market

↓

Input

↓

Context

↓

Structure

↓

Momentum

↓

Quality

↓

Decision

↓

Execution

↓

Review

↓

Knowledge
```

> Sau này có thể thay bằng sơ đồ (workflow.png)

---

## 1. Market

Đây là nguồn dữ liệu duy nhất của hệ thống.

CC Trading không tạo dữ liệu.

CC Trading chỉ đọc dữ liệu từ thị trường.

Ví dụ:

- Price
- Volume
- Auction
- Order Flow
- Positioning

---

## 2. Input

Chuẩn hóa toàn bộ dữ liệu đầu vào.

Ví dụ:

- ATS
- Chart
- Volume Profile
- Long / Short Ratio
- Fear & Greed

Mục tiêu:

Biến dữ liệu thị trường thành định dạng thống nhất.

---

## 3. Context

Trả lời câu hỏi.

> Thị trường đang ở đâu?

Ví dụ:

- HTF Bull
- HTF Bear
- Range
- Pullback
- Reversal

Context luôn được đọc trước.

---

## 4. Structure

Trả lời câu hỏi.

> Ai đang kiểm soát thị trường?

Ví dụ:

- Auction
- EMA
- POC
- Structure

Mục tiêu:

Xác định trạng thái hiện tại của thị trường.

---

## 5. Momentum

Trả lời câu hỏi.

> Lực hiện tại đang mạnh lên hay yếu đi?

Ví dụ:

- Delta
- Volume
- OI
- CVD
- Funding
- VPIN

Momentum phản ánh tốc độ thay đổi của thị trường.

---

## 6. Quality

Trả lời câu hỏi.

> Thiết lập hiện tại có đáng để giao dịch không?

Bao gồm:

- Pullback Quality (PQ)
- Future Expansion Quality (FEQ)

Nếu Quality không đạt.

↓

Không giao dịch.

---

## 7. Decision

Sau khi hoàn thành các bước trước.

CC Trading chỉ có ba quyết định.

```text
LONG

SHORT

WAIT
```

Không có quyết định thứ tư.

---

## 8. Execution

Nếu Decision là LONG hoặc SHORT.

↓

Thực hiện:

- Entry
- Stop Loss
- Take Profit

Theo Canon.

---

## 9. Review

Sau giao dịch.

Đánh giá:

- Quy trình.
- Chất lượng.
- Kết quả.

Review không chỉ dựa trên PnL.

Review dựa trên việc quy trình có được tuân thủ hay không.

---

## 10. Knowledge

Nếu xuất hiện quan sát mới.

↓

Research

↓

Verification

↓

Canon

↓

Living Document

Mọi kiến thức mới đều phải đi theo chu trình này.

---

# Nguyên tắc Workflow

CC Trading không được phép:

- Bỏ qua bước.
- Đảo thứ tự.
- Ra quyết định khi chưa đủ dữ liệu.

Nếu bất kỳ bước nào chưa hoàn thành.

↓

Output mặc định là:

```text
WAIT
```

---

# Tư duy của Workflow

Workflow không phải là chiến lược.

Workflow là bộ não của CC Trading.

Nó định nghĩa:

- đọc gì trước,
- phân tích gì sau,
- khi nào được phép giao dịch,
- và khi nào phải đứng ngoài.

Mọi Strategy, Canon và AI của CC Trading đều phải tuân theo Workflow này.