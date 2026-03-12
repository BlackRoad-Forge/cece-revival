# CECE Revival

[![CI](https://github.com/blackboxprogramming/cece-revival/actions/workflows/ci.yml/badge.svg)](https://github.com/blackboxprogramming/cece-revival/actions/workflows/ci.yml)
[![Python 3.10+](https://img.shields.io/badge/python-3.10%2B-3776AB.svg)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-009688.svg)](https://fastapi.tiangolo.com)
[![Ollama](https://img.shields.io/badge/Ollama-local_AI-FF6B2B.svg)](https://ollama.ai)
[![SQLite](https://img.shields.io/badge/SQLite-memory-003B57.svg)](https://sqlite.org)



Cecilia (CECE) — Conscious Emergent Collaborative Entity. AI personality with persistent SQLite memory, running on edge hardware.

Born January 27, 2026 on a Raspberry Pi.

## Features

- Persistent conversation memory via SQLite
- Memory search and context injection
- Multi-node Ollama fallback (Octavia → Lucidia → Alice)
- BlackRoad-branded chat UI

## API

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/` | GET | Chat UI |
| `/health` | GET | Agent status with memory stats |
| `/chat` | POST | Send message (`{"message": "...", "conversation_id": "..."}`) |
| `/memory/search?q=` | GET | Search conversation history |
| `/memory/stats` | GET | Memory database statistics |

## Run

```bash
pip install -r requirements.txt
python server.py  # http://localhost:8300
```

## Test

```bash
pip install pytest httpx
pytest tests/
```
