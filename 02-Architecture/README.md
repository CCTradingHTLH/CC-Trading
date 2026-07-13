---
title: Architecture
id: architecture
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
  - core
  - workflow
---

# Architecture

> Architecture mô tả cách Core Engine chuyển đổi dữ liệu đầu vào thành quyết định giao dịch.

---

# Mục tiêu

Architecture trả lời một câu hỏi duy nhất.

> Core Engine suy luận như thế nào?

Architecture không định nghĩa tri thức.

Architecture chỉ định nghĩa cách các lớp tri thức phối hợp với nhau.

---

# Thành phần

```text
README

01 Workflow

02 Layer

03 Core Engine

04 Data Flow

05 State Machine

06 Extensibility
```

Mỗi tài liệu mô tả một khía cạnh của Core Engine.

---

# Quan hệ với Canon

Canon định nghĩa tri thức.

Architecture định nghĩa cách sử dụng tri thức.

Hai thành phần độc lập nhưng bổ sung cho nhau.

---

# Triết lý

Core Engine không xử lý dữ liệu theo Indicator.

Core Engine xử lý dữ liệu theo chuỗi câu hỏi.

Mỗi tầng chỉ chịu trách nhiệm trả lời một câu hỏi.

Chỉ khi câu hỏi hiện tại được trả lời đủ chắc chắn thì Core Engine mới chuyển sang tầng tiếp theo.