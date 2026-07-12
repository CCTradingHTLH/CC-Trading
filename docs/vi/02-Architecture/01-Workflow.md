---
title: Workflow
id: architecture-workflow
version: 2.0
status: Freeze
author: HTLH
language: vi
created: 2026-07-12
last_updated: 2026-07-12
review_cycle: Monthly
confidence: 100%
tags:
  - workflow
  - architecture
---

# Workflow

> Workflow mô tả trình tự suy luận của Core Engine.

---

# Workflow

```text
Input

↓

Auction

↓

Market Context

↓

Momentum

↓

Structure

↓

Quality

↓

Decision

↓

Execution
```

---

# Nguyên tắc

Workflow luôn đi từ:

- dữ liệu;
- hành vi;
- bối cảnh;
- lực;
- xác nhận;
- đánh giá;
- quyết định;
- thực thi.

Không được bỏ qua bất kỳ tầng nào.

Không được đưa ra Decision khi Workflow chưa hoàn thành.