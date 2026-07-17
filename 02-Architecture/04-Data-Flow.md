---
title: Data Flow
id: architecture-data-flow
version: 3.0
status: Freeze
author: HTLH
language: vi
created: 2026-07-12
last_updated: 2026-07-17
review_cycle: Monthly
confidence: 100%
tags:
  - architecture
  - data-flow
---

# Data Flow

> Data Flow mô tả cách bằng chứng và tri thức di chuyển trong CC Trading.

---

# Mục tiêu

Data Flow đảm bảo toàn bộ quá trình suy luận diễn ra theo một hướng nhất quán.

Thông tin không được suy luận ngược.

Tri thức chỉ được mở rộng khi có thêm bằng chứng.

Reality luôn là điểm bắt đầu của chu kỳ tiếp theo.

---

# Flow

```text
Observation

↓

Evidence

↓

Reasoning

↓

Decision

↓

Explanation

↓

Scenario

↓

Execution

↓

Reality

↓

Learning

↓

Observation
```

Data Flow tạo thành một vòng lặp học hỏi liên tục.

---

# Ý nghĩa

## Observation

Thu thập dữ liệu từ thị trường.

Ví dụ:

- Price
- Volume
- Delta
- CVD
- Open Interest
- Funding
- EMA
- RSI

---

## Evidence

Chuẩn hóa dữ liệu thành các quan sát có ý nghĩa.

Ví dụ:

- Auction Observation
- Market Context Observation
- Momentum Observation
- Structure Observation

---

## Reasoning

Canon tổng hợp bằng chứng thông qua các Core Engines.

Reasoning bao gồm:

- Auction
- Market Context
- Momentum
- Structure
- Quality

---

## Decision

Reasoning tạo ra kết luận hợp lý nhất tại thời điểm hiện tại.

Decision không phải điểm kết thúc.

Decision là đầu vào cho các bước tiếp theo.

---

## Explanation

Signal Weight giải thích vì sao Decision được hình thành.

Mọi Decision đều có thể được truy vết.

---

## Scenario

Scenario Space mô hình hóa các khả năng có thể xảy ra.

Decision không dự đoán tương lai.

Decision chuẩn bị cho nhiều khả năng.

---

## Execution

Execution Planner chuyển từng Scenario thành kế hoạch hành động cụ thể.

---

## Reality

Reality phản ánh điều thực sự đã xảy ra.

Reality luôn có độ ưu tiên cao nhất.

---

## Learning

Reality Feedback cập nhật tri thức của hệ thống.

Mọi kết quả đều trở thành Observation của chu kỳ tiếp theo.

---

# Nguyên tắc

Thông tin luôn di chuyển theo một chiều.

```text
Observation

↓

Evidence

↓

Reasoning

↓

Decision

↓

Explanation

↓

Scenario

↓

Execution

↓

Reality

↓

Learning

↓

Observation
```

Không Layer nào được sửa kết quả của Layer trước.

Layer sau chỉ được sử dụng những kết quả đã được xác nhận.

Reality luôn có quyền cập nhật toàn bộ Pipeline.

---

# Triết lý

CC Trading không truyền dữ liệu.

CC Trading truyền sự hiểu biết.

Không phải mọi Observation đều tạo ra Decision.

Nhưng mọi Decision đều phải có thể giải thích.

Mọi Reality đều trở thành tri thức cho chu kỳ tiếp theo.

---

> Dữ liệu tạo nên bằng chứng.

> Bằng chứng tạo nên suy luận.

> Suy luận tạo nên quyết định.

> Thực tế tạo nên tri thức.