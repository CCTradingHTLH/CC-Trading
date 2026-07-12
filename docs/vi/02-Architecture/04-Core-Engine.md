---
title: Core Engine
id: architecture-core-engine
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
  - core-engine
  - decision
---

# Core Engine

Core Engine là bộ não của CC Trading.

Core Engine tiếp nhận dữ liệu đã được chuẩn hóa từ Input.

↓

Diễn giải dữ liệu.

↓

Đưa ra quyết định.

Core Engine không tạo dữ liệu.

Core Engine không thực hiện giao dịch.

Core Engine chỉ suy nghĩ.

---

# Vai trò

```text
Raw Market

↓

Input

↓

Core Engine

↓

Output Layer
```

Core Engine là nơi duy nhất được phép diễn giải dữ liệu.

---

# Kiến trúc

Core Engine được chia thành năm Engine độc lập.

```text
Context Engine

↓

Structure Engine

↓

Momentum Engine

↓

Quality Engine

↓

Decision Engine
```

Mỗi Engine chỉ chịu trách nhiệm cho một nhiệm vụ.

Không Engine nào được vượt quyền.

---

# 1. Context Engine

## Mục tiêu

Trả lời câu hỏi.

> Thị trường đang ở đâu?

Ví dụ.

- HTF Bull
- HTF Bear
- Pullback
- Distribution
- Accumulation
- Range

Context luôn được xác định đầu tiên.

Mọi Engine phía sau đều phụ thuộc Context.

---

# 2. Structure Engine

## Mục tiêu

Trả lời câu hỏi.

> Ai đang kiểm soát thị trường?

Structure Engine đọc.

- Auction
- EMA
- POC
- SonicR
- Structure

Structure Engine không đánh giá Momentum.

---

# 3. Momentum Engine

## Mục tiêu

Trả lời câu hỏi.

> Lực hiện tại mạnh hay yếu?

Momentum Engine đọc.

- Delta
- Volume
- OI
- CVD
- Funding
- VPIN
- Aggressive Liquidation

Momentum phản ánh tốc độ thay đổi của lực mua và lực bán.

Momentum không xác định xu hướng.

---

# 4. Quality Engine

## Mục tiêu

Trả lời câu hỏi.

> Thiết lập hiện tại có đủ chất lượng không?

Quality Engine đánh giá.

- Pullback Quality (PQ)
- Future Expansion Quality (FEQ)

Nếu Quality không đạt.

↓

Decision mặc định là

```text
WAIT
```

---

# 5. Decision Engine

## Mục tiêu

Tổng hợp toàn bộ kết quả.

```text
Context

+

Structure

+

Momentum

+

Quality

↓

Decision
```

Decision chỉ có ba trạng thái.

```text
LONG

SHORT

WAIT
```

Decision Engine không đọc dữ liệu thô.

Decision Engine chỉ sử dụng Output của các Engine trước.

Decision Engine không quan tâm PnL.

Decision Engine chỉ quan tâm chất lượng của quyết định.

---

# Quan hệ giữa các Engine

```text
Context

↓

Structure

↓

Momentum

↓

Quality

↓

Decision
```

Đây là chuỗi xử lý một chiều.

Không được phép.

- bỏ qua Engine;
- đổi thứ tự Engine;
- quay ngược lên Engine trước.

Mỗi Engine chỉ được phép sử dụng Output của Engine trước.

---

# Ranh giới

Core Engine kết thúc tại Decision.

Sau Decision.

↓

Output Layer chịu trách nhiệm.

- Chuẩn hóa kết quả.
- Tạo tín hiệu giao dịch.
- Chuẩn bị Entry.
- Chuẩn bị Stop Loss.
- Chuẩn bị Take Profit.
- Chuẩn bị Risk.
- Chuyển sang Execution.

Execution không thuộc Core Engine.

Execution thuộc Output Layer.

---

# Nguyên tắc

Core Engine tuân thủ các nguyên tắc sau.

- Không tạo dữ liệu.
- Không thay đổi Input.
- Không thực hiện giao dịch.
- Không bỏ qua Engine.
- Không vượt quyền giữa các Engine.

Nếu thiếu dữ liệu ở bất kỳ bước nào.

↓

Decision mặc định là

```text
WAIT
```

---

# Core Philosophy

```text
Input

↓

Thinking

↓

Decision

↓

Output Layer

↓

Execution
```

Core Engine chỉ chịu trách nhiệm cho **Thinking**.

Mọi hành động đều diễn ra sau Core Engine.

---

# Triết lý

Core Engine không dự đoán thị trường.

Core Engine chỉ diễn giải thị trường.

Một quyết định chỉ được tạo ra khi đã hoàn thành đầy đủ.

- Context
- Structure
- Momentum
- Quality

Nếu một trong bốn thành phần chưa hoàn chỉnh.

↓

Không được phép giao dịch.