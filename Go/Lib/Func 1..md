---
id: Func
created_date: 2025-09-12
updated_date: 2025-09-12
type: note
link:
tags:
  - go
  - IT
  - 09-2025
---

# Func 1.

Любая программа на Go начинается с объявления пакета `package main` и главной точки запуска нашего кода — `func main() {}`. Что происходит дальше?

### Ввод в stdin

```go
fmt.Scanln(&name)
```

### Вывод в консоль

```go
fmt.Println("Введи своё имя:")
```


## Пример

```go
package main

import "fmt"

func main() {
	var name string // Задание переменной name
	fmt.Println("Введи своё имя:") // Вывод в консоль сообщения
	fmt.Scanln(&name) // Считывание из консоли значения name
	
	resultMessage := fmt.Sprintf("Привет, %s!", name) // Формирование финального сообщения
	fmt.Println(resultMessage) // Вывод результата
}
```