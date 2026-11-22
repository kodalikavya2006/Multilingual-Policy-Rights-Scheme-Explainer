# Scheme Saathi

A beginner-friendly MVP for explaining public schemes, rights, and government documents in accessible language.

## Run locally

### Backend (Python 3.10+)

```powershell
cd backend
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
Copy-Item ..\.env.example .env
# Put your Gemini key in backend/.env as GEMINI_API_KEY=your_key.
uvicorn app.main:app --reload
```

### Frontend (Node.js 18+)

```powershell
cd frontend
npm install
npm run dev
```

Open the Vite URL shown in the terminal. The API is available at http://localhost:8002 and interactive docs at http://localhost:8002/docs.

## Current MVP behavior

- Responsive overview with language selector, scheme discovery cards, document upload, and a conversational question field.
- PDF text extraction with page-aware source context; scanned PDFs receive a clear OCR-unavailable message.
- Optional Gemini summaries and chat, with a no-key fallback and a policy against unsupported claims.
- Eligibility intake form that avoids guessing and explains that final approval belongs to the scheme authority.
- Rights explorer landing cards and browser speech recognition where available.

## Important limitations

This starter does not yet connect a verified government knowledge base, Supabase, semantic retrieval, OCR, or text-to-speech. Chat does not invent scheme facts when no verified context is supplied. Scheme cards are discovery prompts, not eligibility determinations. Add official source ingestion and citations before relying on the application for policy decisions.
