---
id: Interface
created_date: 2025-10-13
updated_date: 2025-10-13
type: note
link:
tags:
  - 10-2025
  - go
  - IT
---

# Interface

Интерфейс — это **тип**, который определяет **набор методов**. Любой тип, реализующий все методы интерфейса, **автоматически считается его реализацией**.

```go
type InterfaceName interface {
    Method1() ReturnType
    Method2(paramType) ReturnType
    // ...
}
```


Реализация происходит **неявно**:
```go
type Dog struct{}
type Cat struct{}

func (d Dog) Speak() string {
    return "Woof!"
}

func (c Cat) Speak() string {
    return "Meow!"
}
```
Оба типа `Dog` и `Cat` реализуют интерфейс `Speaker`, потому что у них есть метод `Speak()` с подходящей сигнатурой.