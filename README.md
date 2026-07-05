# SVANidhi+ 🚧 (Work in Progress)

> **From street to bank. One repayment at a time.**

Agentic AI system that reads PM SVANidhi vendor repayment behavior and proactively graduates eligible, low-risk vendors toward higher loan tranches, insurance, and savings products — built for the **SBI Hackathon @ Global Fintech Fest 2026**.

⚠️ **Status:** Active development. Architecture and scope may change. Not production-ready.

---

## The Problem

71.57 lakh PM SVANidhi vendors have taken a first-tranche loan — only 38% reach Tranche 2, and 9% reach Tranche 3. Yet among vendors who do progress, repayment discipline is strong (68%, 75% advancement rates). This isn't a credit-risk problem — it's a **visibility problem**. Nothing in the current system proactively identifies a ready vendor and reaches out.

## What SVANidhi+ Does

A three-layer agentic pipeline:

- **Intelligence Layer** — rule-based eligibility gate + ML readiness/priority score (XGBoost/LightGBM) + explainability breakdown
- **Trigger Layer** — event-driven (pub-sub): Graduation, Growth, Protection (composite) triggers
- **Outreach Layer** — LLM explains *why*, in the vendor's language, routed via their preferred channel; confidence-gated with human-in-the-loop review below 0.7

Full spec: see [`docs/project-brief.md`](./docs/project-brief.md) *(coming soon)*

## Tech Stack

| Layer | Tool |
|---|---|
| ML Model | XGBoost / LightGBM |
| Backend | FastAPI |
| LLM | Claude API / Groq (Llama 3) |
| Frontend | React.js |
| Database | PostgreSQL |
| Data Processing | Pandas, NumPy |
| Visualization | Recharts / Chart.js, Leaflet.js |
| Demo Data | Synthetic, persona-based |

## Repo Structure

```
svanidhi-plus/
├── backend/       # FastAPI app, scoring engine, trigger engine
├── frontend/      # React dashboard (vendor timeline, heatmap, alerts)
├── data/          # Synthetic persona-based vendor datasets
├── docs/          # Project brief, pitch deck assets
└── README.md
```

## Setup

*(Instructions coming as backend/frontend scaffolding is added)*

```bash
# Backend
cd backend
pip install -r requirements.txt --break-system-packages
uvicorn main:app --reload

# Frontend
cd frontend
npm install
npm run dev
```

## Roadmap

- [x] Project brief + architecture design
- [ ] Synthetic persona-based dataset (5 personas, 50–100 vendors)
- [ ] Eligibility gate (rule-based)
- [ ] Readiness score model + explainability layer
- [ ] Trigger engine (event-driven)
- [ ] LLM outreach layer + confidence gate
- [ ] React dashboard + district heatmap
- [ ] End-to-end demo (3–4 min)

## Disclaimer

All data used is **synthetic and persona-based**. No real customer, transaction, or repayment data is used at any stage.

---

*Built by [your name/team] — VIT Bhopal — SBI Hackathon, Global Fintech Fest 2026*