---
title: Architecture
id: architecture
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
  - core
  - workflow
---

# Architecture

> Architecture mô tả cách CC Trading tổ chức quá trình suy luận từ dữ liệu đầu vào đến quyết định.

---

# Mục tiêu

Architecture trả lời một câu hỏi duy nhất.

> Hệ thống suy luận như thế nào?

Architecture không định nghĩa tri thức.

Architecture không tạo quyết định.

Architecture định nghĩa cách các thành phần của hệ thống phối hợp để tạo nên quá trình suy luận.

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

Mỗi tài liệu mô tả một khía cạnh của kiến trúc tổng thể.

---

# Quan hệ với Canon

| Thành phần | Vai trò |
|------------|----------|
| **Architecture** | Định nghĩa cách hệ thống vận hành. |
| **Canon** | Định nghĩa tri thức mà hệ thống sử dụng. |

Architecture quyết định tri thức được luân chuyển như thế nào.

Canon quyết định tri thức đó có ý nghĩa gì.

Hai thành phần độc lập nhưng bổ sung cho nhau.

---

# Triết lý

CC Trading không xử lý dữ liệu theo Indicator.

CC Trading xử lý dữ liệu thông qua một chuỗi câu hỏi.

Mỗi tầng chỉ chịu trách nhiệm trả lời một câu hỏi.

Mỗi Engine chỉ giải quyết đúng trách nhiệm của mình.

Chỉ khi bằng chứng hiện tại đủ rõ ràng, hệ thống mới chuyển sang tầng suy luận tiếp theo.

---

> Một kiến trúc tốt không cố gắng trả lời mọi câu hỏi.
>
> Một kiến trúc tốt tổ chức các câu hỏi theo đúng thứ tự.