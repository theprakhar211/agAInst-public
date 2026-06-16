<div align="center">

# ⚔️ ag**AI**nst

### *Most AI agrees with you. This one won't.*

**agAInst** is an AI-powered debate arena where you go head-to-head against an AI that genuinely pushes back — no validation, no agreement, just sharp arguments and a judge that doesn't care about your feelings.

<br/>

[![Next.js](https://img.shields.io/badge/Next.js-15-black?style=for-the-badge&logo=next.js)](https://nextjs.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![Groq](https://img.shields.io/badge/Groq-Llama_3.3_70B-F55036?style=for-the-badge)](https://groq.com)
[![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)](https://supabase.com)
[![Vercel](https://img.shields.io/badge/Vercel-black?style=for-the-badge&logo=vercel)](https://vercel.com)

<br/>

🌐 **[Live Demo](https://against-chi.vercel.app)** · 🐛 **[Report Bug](https://github.com/theprakhar211/agAInst/issues)** · ✨ **[Request Feature](https://github.com/theprakhar211/agAInst/issues)**

</div>

---

## 🎯 What is agAInst?

You enter any topic. You pick a side. The AI takes the **opposite position** and argues it with genuine conviction — no strawmen, no backing down, no agreeing with you just to be polite.

After **3 structured rounds**, a completely separate AI judge evaluates the entire debate and delivers a verdict — scored on logic, evidence, rebuttal quality, and clarity.

```
💬 You type your argument
        ↓
🤖 AI fires back with a real counter-argument  
        ↓
🔁 Repeat for 3 rounds (Opening → Rebuttal → Closing)
        ↓
⚖️  Independent AI judge evaluates everything
        ↓
🏆 Winner declared · Scores · Fallacies detected · Shareable verdict link
```

---

## ✨ What's Inside

- **VS AI** — debate any topic against Llama 3.3 70B arguing the opposite side
- **Local 2 Player** — two humans, one device, screen blurs between turns
- **Online PvP** — real-time multiplayer via Supabase Realtime, share a link to invite anyone
- **AI Judge** — independent LLM scores logic, evidence, rebuttal, and clarity across both sides
- **Argument Analyser** — fires in parallel per round, gives coaching feedback on your argument
- **Global Leaderboard** — ranked by win rate, total wins, or avg score
- **Shareable verdicts** — send any completed debate result to anyone, no login required
- **Trending topics** — live debate topics pulled fresh via Groq web search

---

## 🧠 How It Works

Three distinct AI agents with separate system prompts run in a pipeline:

```
🤖 DEBATER — argues the opposite side with conviction   (temp 0.8)
🔬 ANALYSER — scores your argument in parallel          (temp 0.3)
⚖️  JUDGE   — evaluates the full transcript after R3    (temp 0.2)
```

Fully **stateless API** — every request sends the complete conversation history. No server-side session state.

---

## 🛠️ Tech Stack

| Layer | Tech |
|-------|------|
| Frontend | Next.js 15, Tailwind CSS, Framer Motion |
| Backend | FastAPI, Python 3.11, slowapi (rate limiting) |
| AI | Groq API — Llama 3.3 70B |
| Database | Supabase (Postgres, Auth, Realtime, Storage) |
| Deployment | Vercel (frontend) · Render (backend) |

---

## 🚀 Running Locally

### Prerequisites
- Node.js 18+ · Python 3.11+
- [Groq API key](https://console.groq.com) (free)
- [Supabase](https://supabase.com) project (free)

### Backend

```bash
cd backend
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
```

Create `backend/.env`:
```env
GROQ_API_KEY=your_key_here
```

```bash
uvicorn main:app --reload --port 8000
```

### Frontend

```bash
cd frontend
npm install
```

Create `frontend/.env.local`:
```env
NEXT_PUBLIC_API_URL=http://localhost:8000
NEXT_PUBLIC_SUPABASE_URL=https://your-project.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=your-anon-key
```

```bash
npm run dev
```

✅ `http://localhost:3000`

---

## 🌐 Deployment

| | Platform | Notes |
|--|----------|-------|
| Frontend | Vercel | Root dir: `frontend` |
| Backend | Render | Root dir: `backend` · Start: `uvicorn main:app --host 0.0.0.0 --port $PORT` |

**Env vars:** Render → `GROQ_API_KEY` · Vercel → `NEXT_PUBLIC_API_URL`, `NEXT_PUBLIC_SUPABASE_URL`, `NEXT_PUBLIC_SUPABASE_ANON_KEY`

---

## 🗺️ Roadmap

- [x] Core 3-round VS AI debate loop
- [x] AI judge with structured JSON scoring + fallacy detection
- [x] Real-time argument analyser (parallel, non-blocking)
- [x] Local 2 Player mode with handoff screen
- [x] Online PvP with Supabase Realtime + share links
- [x] User accounts, cloud sync, guest migration
- [x] Global leaderboard (3 sort modes)
- [x] Shareable verdict links (public, no login required)
- [x] Rate limiting on all LLM endpoints
- [x] Side Flip mode · PDF export · Shareable result card
- [ ] Voice input
- [ ] ELO rating system

---

## 🔒 Source Code

The full source code is available on request. If you'd like to review it — reach out and I'll grant access.

📧 [theprakhar211@gmail.com](mailto:theprakhar211@gmail.com) · 💼 [LinkedIn](https://www.linkedin.com/in/prakhar-sharma-21112004-)

---

## 📄 License

MIT

---

<div align="center">

**Built by [Prakhar Sharma](https://github.com/theprakhar211)** · [Portfolio](https://prakhar-sharma.vercel.app)

⚔️ *Challenge your thinking. Sharpen your arguments. Win the debate.*

<sub>Next.js · FastAPI · Groq · Supabase · Llama 3.3 70B</sub>

</div>
