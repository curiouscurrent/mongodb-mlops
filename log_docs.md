# ✅ What actually happens

When you do:

```python
logging.debug("hello")
```

👉 This is what really happens:

---

## 🔁 Step-by-step flow

### 1. A **LogRecord** is created

```text
LogRecord:
   level = DEBUG
   message = "hello"
   file = ...
   line = ...
```

👉 This is a temporary object (not stored in logger)

---

### 2. Logger checks its level

```text
logger.level = DEBUG
```

👉 If message level >= logger level → continue
👉 Otherwise → ignore

---

### 3. Logger sends record to handlers

```text
handlers = [file_handler, console_handler]
```

Each handler decides:

* Should I log this?
* Where should I send it?

---

### 4. Handlers output the message

* File handler → writes to `.log` file
* Console handler → prints

👉 After that → message is **gone**

---

# 🔥 Key idea

👉 Logger does **NOT store logs**
👉 It just **processes and forwards them**

---

# 🧠 Correct mental model

```text
logger (object)
   ├── level (state)
   ├── handlers (state)
   └── formatter (state)

logging.debug("msg")
   ↓
create LogRecord
   ↓
pass to logger
   ↓
logger → handlers
   ↓
handlers → output
```


