# Code Runner API (Python Sandbox)

Production-ready Flask API for secure, sandboxed Python code execution.  
Includes rate-limiting, Docker, strong code validation, logging, modular structure — всё, что надо для продакшена и продажи.

---

## 🚀 Features

- Safe Python code execution in a temp-file sandbox
- Strict validation (blocks os, subprocess, sys, и прочую дичь)
- Rate limiting (anti-abuse, 3 per minute)
- Docker-ready, clean project structure
- Simple API, easy integration
- Logging (прозрачные логи для аудита)
- Полностью совместим с Postman, curl, любым front-end

---

## 📦 Endpoints

### POST `/run`

**Request:**
```json
{
  "code": "print('hello, world!')"
}
```

**Response:**
```json
{
  "stdout": "hello, world!",
  "stderr": "",
  "returncode": 0
}
```

---

## ⏱️ Rate limits

- `/run`: 3 per minute per IP

---

## ⚡ Quick Start

### Docker (recommended)
```bash
docker build -t code-runner-api .
docker run -d -p 5000:5000 code-runner-api
```

### Local
```bash
pip install -r requirements.txt
python app.py
```

---

## 🖼️ Screenshots

- `cmd_server_start.png` — Сервер запущен
- `cmd_running_api.png` — Живые логи API
- `postman_success.png` — Успешный запрос через Postman

---

## 📬 Contact

**Need this in another stack (Node.js, Go, etc)?**  
Contact: talabov.ali72@gmail.com  
Telegram: [@talabovali](https://t.me/talabovali)

*Note: Pricing may vary depending on complexity and target stack.*

---

**Ready for production and monetization. 100% tested.**
