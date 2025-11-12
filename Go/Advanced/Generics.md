---
id: Generics
created_date: 2025-11-10
updated_date: 2025-11-10
type: note
link:
tags:
  - 11-2025
  - IT
  - go
---

# Generics

```go
func Print[T any](s T) {
    fmt.Println(s)
}
```

Используем дженерик, для автоопределения типа.
Этот тип можно использовать в коде
