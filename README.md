# BMRI Financial Analysis Backend

Automated financial analysis service for Bank Mandiri (BMRI) built with FastAPI.

---

## Features

- **FastAPI** web framework with asynchronous support.
- Configurable settings via `pydantic-settings` and `.env`.
- Modular structure with versioned routing (`/api/v1`).
- Interactive OpenAPI documentation (Swagger & ReDoc).
- Pre-configured unit tests with `pytest` and `httpx`.

---

## Project Structure

```
automated-bmri-financial-analysis/
├── app/
│   ├── api/
│   │   └── v1/
│   │       ├── endpoints/
│   │       │   └── health.py
│   │       └── router.py
│   ├── core/
│   │   └── config.py
│   ├── main.py
│   └── __init__.py
├── tests/
│   ├── __init__.py
│   └── test_health.py
├── .env.example
├── .gitignore
├── requirements.txt
└── README.md
```

---

## Getting Started

### 1. Prerequisites

- Python 3.10+ (tested on Python 3.12)

### 2. Environment Setup

Create and activate a virtual environment:

**On Linux/macOS:**

```bash
python -m venv .venv
source .venv/bin/activate
```

**On Windows (PowerShell):**

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables (Optional)

Copy `.env.example` to `.env`:

```bash
cp .env.example .env
```

### 5. Run Development Server

```bash
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
```

Or run directly:

```bash
python -m app.main
```

The application will be running at: `http://localhost:8000`

---

## API Documentation & Endpoints

- **Root:** [http://localhost:8000/](http://localhost:8000/)
- **Health Check:** [http://localhost:8000/health](http://localhost:8000/health) or [http://localhost:8000/api/v1/health](http://localhost:8000/api/v1/health)
- **Interactive Swagger Docs:** [http://localhost:8000/docs](http://localhost:8000/docs)
- **Alternative ReDoc:** [http://localhost:8000/redoc](http://localhost:8000/redoc)

---

## Running Tests

Execute unit tests with `pytest`:

```bash
pytest
```
