---
id: Http-Server
created_date: 2025-11-01
updated_date: 2025-11-01
type: note
link:
tags:
  - 11-2025
  - IT
  - go
---

# Обработка запросов с помощью http.Handler и http.HandleFunc

`http.Handler` и `http.HandleFunc` — это два способа обработки HTTP-запросов в Go.

`http.Handler` — интерфейс, который определяет метод `ServeHTTP` и с его помощью принимает `http.ResponseWriter` и `*http.Request`