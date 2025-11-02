---
id: Logs
created_date: 2025-11-01
updated_date: 2025-11-01
type:
link:
tags:
  - 11-2025
  - go
  - IT
---


# Slog

Для начала создаем logger:

```go
logger := slog.New(slog.NewJSONHandler(file, nil))
```

Если вместо этого типа используется `TextHandler`, каждая запись журнала будет отформатирована в соответствии со стандартом Logfmt:

```go
logger := slog.New(slog.NewTextHandler(os.Stdout, nil))
```

Существуют разные уровни логов:

```go
logger.Debug("Debug message")   
logger.Info("Info message")    
logger.Warn("Warning message")    
logger.Error("Error message")
```


Мы можем добавлять различные параметры в логировании с помощью slog.String, slog.Int и т.д.
```go
	logger.Info("user action", slog.String("User", user), slog.String("Action", action))
```

