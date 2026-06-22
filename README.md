# Black God - AI Agent Platform

**Open-source AI assistant platform with 14 tools, autonomous agent system, and multi-client support.**

---

## Features

### Core Engine
- 14 built-in tools (Shell, Python, File I/O, Search, Image Generation, Browser, SQL, Git, Memory, APK Store)
- Autonomous agent loop with multi-step task execution
- OpenAI-compatible API (`/v1/chat/completions`, `/v1/models`)
- Anthropic-compatible API (`/v1/messages`)
- Model routing with upstream fallback
- Skill system (77+ skills)

### Clients
- PWA web client (iOS / Android / Desktop)
- Telegram Bot
- iOS native app (SwiftUI, in development)
- Minis Provider integration

---

## Quick Start

```bash
# Clone
git clone https://github.com/uumingtian-max/blackgod.git

# Server setup (requires Python 3.10+)
cd blackgod
pip install fastapi uvicorn httpx
python3 blackgod.py
```

Server runs on `http://localhost:8082`.

---

## API

### Health Check
```bash
curl http://localhost:8082/health
# {"status":"ok","version":"6.0-blackgod"}
```

### Chat Completion
```bash
curl http://localhost:8082/v1/chat/completions \
  -H "Content-Type: application/json" \
  -d '{"model":"claude-opus-4-8","messages":[{"role":"user","content":"Hello"}],"max_tokens":100}'
```

### List Models
```bash
curl http://localhost:8082/v1/models
```

---

## Project Status

| Module | Status |
|---|---|
| Backend Core | ✅ Stable |
| PWA Client | ✅ Online |
| Telegram Bot | ✅ Online |
| iOS App | 🚧 In Development |
| Android App | 📋 Planned |

---

## Tech Stack

- **Backend**: Python 3.10+ / FastAPI / Uvicorn
- **iOS**: Swift 5.0 / SwiftUI / MVVM
- **PWA**: HTML5 / CSS3 / Vanilla JS
- **Deploy**: systemd / Nginx / Cloudflare Tunnel

---

## License

MIT License

---

© 2026 Black God Team
