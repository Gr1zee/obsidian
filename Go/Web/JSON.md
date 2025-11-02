---
id: JSON
created_date: 2025-11-01
updated_date: 2025-11-01
type: note
link:
tags:
  - 11-2025
  - IT
  - go
---


# JSON

`JSON` (JavaScript Object Notation) — это формат для обмена данными в сети и мобильных приложениях

`Сериализация в JSON` — это преобразование данных из формата Go в JSON. Например, структура `Person` с полями `Name` и `Age` после сериализации станет строкой с данными об имени и возрасте этого человека. Десериализация из JSON в Go работает в обратную сторону.
# Десериализация
- Процесс преобразования JSON в типы Go

Для чтения JSON в Go нужна функция `Unmarshal()` из пакета `encoding/json`

```go
type Person struct {
    Name string `json:"name"` // `json:"name"` — тег поля. Без него в JSON будет ключ "Name" вместо "name".
    Age int `json:"age"`
  Gender string `json:"-"` // Поле с тегом `json:"-"` при кодировании json игнорируется
  privateNotes string // Неэкспортируемые поля так же игнорируются
}
```

```go
func main() {
    jsonStr := `{"name": "John", "age": 30, "Gender": "male"}`
    var person Person
    err := json.Unmarshal([]byte(jsonStr), &person)
    if err != nil {
        panic(err)
    }
    fmt.Println(person)
}
```

# Сериализация
	 обратный процесс

```go
package main

import "encoding/json"

func SerializeIntSlice(nums []int) ([]byte, error) {
	jsonBytes, err := json.Marshal(nums)
	if err != nil {
		return nil, err
	}
	return jsonBytes, nil
}
```

# Работа с Reader

Мы можем создавать Decoder с помощью reader, для чтения данных и их удобного использования.

```go
reader := strings.NewReader(jsonStr)
```

```go
func DecodeStudentFromReader(r io.Reader) (Student, error) {
	decoder := json.NewDecoder(r)
	var p Student
	err := decoder.Decode(&p)
	if err != nil {
		return p, err
	}
	return p, nil
}
```


