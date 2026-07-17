---
title: Architecture
id: architecture
version: 3.1
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

Architecture định nghĩa cấu trúc và sự phối hợp giữa các thành phần của hệ thống.

Architecture tổ chức quá trình chuyển đổi từ Observation đến Decision thông qua một Workflow thống nhất.

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

Architecture tổ chức cách tri thức được luân chuyển.

Canon cung cấp tri thức cho từng bước suy luận.

Hai thành phần độc lập nhưng bổ sung cho nhau.

---

# Triết lý

CC Trading tổ chức quá trình suy luận thông qua một chuỗi câu hỏi.

Mỗi Layer trả lời một câu hỏi.

Mỗi Engine thực hiện một trách nhiệm.

Mỗi bước suy luận kế thừa kết quả của bước trước để từng bước làm rõ bức tranh của thị trường.

---

> Một kiến trúc tốt không cố gắng trả lời mọi câu hỏi.
>
> Một kiến trúc tốt tổ chức các câu hỏi theo đúng thứ tự.