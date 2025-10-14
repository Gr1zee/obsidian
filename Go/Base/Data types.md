---
id: Data
created_date: 2025-09-11
updated_date: 2025-09-11
type: note
link: "[[Variables]]"
tags:
  - 09-2025
  - go
  - IT
---

# Data types


## Числа

```Go
var i int = 10 // Платформозависимо 32/64
// uint8, uint16, int 32, int64
```

```Go
//float32, float64
var pi float32 = 3.141
var e = 2.718
gRatio := 1.618
```

## Bool
```Go
var b bool // false по умолчанию
var s = true
cond := true
```

## Strings

```Go
var str tring

var hello string = "Hello \n"
var world string = `World\n\t` // Пишет спец символы
```

- <mark style="background: #BBFABBA6;">*Поддерживает Utf-8*</mark>

```Go
s1 := "Hello"
s2 := "world"
s3 := s1 + s2 + "!" 
```

- <mark style="background: #BBFABBA6;">Работает конкатенация строк</mark>


```Go
s1[0] = 72
```

- <mark style="background: #FF5582A6;">!Строки неизменяемы</mark>

### Получение длины строки:
```Go
byteLen := len(s1) // 19 байт
symb = utf8.RuneCountInString(s1) // 10 рун
```

```Go
s3 = s1[:12]
```
	Срезы