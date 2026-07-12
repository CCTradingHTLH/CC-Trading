---
title: Layer
id: architecture-layer
version: 2.0
status: Freeze
author: HTLH
language: vi
created: 2026-07-12
last_updated: 2026-07-12
review_cycle: Monthly
confidence: 100%
tags:
  - architecture
  - layer
---

# Layer

> Mỗi Layer chỉ chịu trách nhiệm trả lời một câu hỏi.

---

# Layer

## Input

**Mình có dữ liệu gì?**

---

## Auction

**Giá đang làm gì?**

---

## Market Context

**Thị trường đang ở đâu?**

---

## Momentum

**Lực đang đi đâu?**

---

## Structure

**Giá có xác nhận lực đó không?**

---

## Quality

**Có đáng giao dịch không?**

---

## Decision

**Làm gì?**

---

## Execution

**Làm như thế nào?**

---

# Triết lý

Core Engine không nhảy cóc.

Core Engine chỉ chuyển sang Layer tiếp theo khi Layer hiện tại đã được xác nhận.

```text
Input

↓

Auction

↓

Context

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

Mỗi Layer đều có trách nhiệm riêng.

Không Layer nào được phép thay thế Layer khác.