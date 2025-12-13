
# Student Feedback Portal (Flask) — CI/CD with GitHub Actions + Docker + Render

A minimal Flask app that collects anonymous course feedback and shows an admin view.
CI/CD via GitHub Actions:
- **install** → **lint/test** → **build** → **deploy (optional to Render)**.

## Quick Start (Local)

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
flask --app app run --host 0.0.0.0 --port 8000
```

Open http://localhost:8000

## Run tests & lint locally
```bash
pip install -r requirements.txt
pip install pytest flake8
flake8 .
pytest -q
```

## Docker (Local)
```bash
docker build -t student-feedback-portal:dev .
docker run -p 8000:8000 student-feedback-portal:dev
