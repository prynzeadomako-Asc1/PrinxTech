AI Productivity Suite — MVP (Simplified)

This is a simplified, runnable MVP for the AI Productivity Suite targeted at SMEs.
It includes:
- Frontend: React + Vite + Tailwind (minimal)
- Backend: FastAPI (SQLite) with an /ai/chat endpoint that uses OpenAI if a key is set,
  otherwise returns a mock response so you can test locally without a key.

Quick local run (recommended):
1. Backend:
   - Open a terminal, cd into backend/
   - (Optional) create and activate a Python virtualenv
   - pip install -r requirements.txt
   - set environment variable OPENAI_API_KEY if you have one (optional)
   - uvicorn app.main:app --reload --port 8000
   - Visit http://localhost:8000/health

2. Frontend:
   - Open another terminal, cd into frontend/
   - npm install
   - npm run dev
   - Visit the address printed by Vite (usually http://localhost:5173) and use the app

Notes:
- The AI endpoint will call OpenAI when OPENAI_API_KEY is present in the backend environment.
  If not present, it returns a mock assistant message for easy testing.
- This repo is intentionally small and simplified to help you run and explore the MVP quickly.
- If you'd like, I can extend this to use Postgres + Docker, add authentication, or wire up WhatsApp/Mobile Money.
