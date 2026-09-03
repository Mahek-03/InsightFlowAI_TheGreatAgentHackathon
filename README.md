# InsightFlow AI — Autonomous Business Analyst

> Ask a business question in plain English. An AI agent investigates, finds the root cause, and recommends the action.

Built for **The Great Agent Hackathon** — Track 3: AI-native Enterprise (Open)

**[🔗 Live Demo](#)** · **[🎥 Video Walkthrough](#)** · **[📄 Devpost Submission](#)**

*(replace the # above with your Netlify link, Loom link, and Devpost link)*

---

## The problem

When a manager asks *"why did revenue drop 18% last month?"*, the honest answer usually takes hours or days. Someone has to ping an analyst, who pulls data from three or four different systems, builds a report in Excel, and eventually comes back with an explanation — by which point the question has often changed.

Most "AI analytics" tools don't actually fix this. They're a chatbot bolted onto a dashboard — they answer questions about data you already pulled, in a query language you still have to know how to ask correctly. None of them *investigate* the way a human analyst would.

## The solution

InsightFlow AI is an autonomous business analyst. You ask a question — the system plans an investigation, delegates it across specialist agents, gathers evidence, identifies a root cause, and hands you an actionable recommendation.

```
Ask → Investigate → Explain → Act
```

No SQL. No dashboard-hunting. No waiting on an analyst.

---

## How it works

```
                    ┌──────────────────────┐
                    │   MANAGER ASKS:       │
                    │ "Why did revenue      │
                    │  fall 18%?"           │
                    └───────────┬───────────┘
                                │
                                ▼
                    ┌──────────────────────┐
                    │   ORCHESTRATOR AGENT  │
                    │  (Business Analyst)   │
                    │  plans investigation  │
                    └───────────┬───────────┘
                                │
          ┌─────────────────────┼─────────────────────┐
          ▼                     ▼                     ▼
   ┌─────────────┐      ┌─────────────┐      ┌─────────────┐
   │ Sales Agent │      │  Customer   │      │  Finance    │
   │             │      │   Agent     │      │   Agent     │
   │ Revenue &   │      │ Churn &     │      │ Margin &    │
   │ product data│      │ regional    │      │ order data  │
   └──────┬──────┘      └──────┬──────┘      └──────┬──────┘
          │                    │                    │
          ▼                    ▼                    ▼
     Product X            Churn up 11pp        AOV down 6%,
     revenue down            in Western          consistent
     42%                      region             with shortage
          └────────────────────┼────────────────────┘
                                ▼
                    ┌──────────────────────┐
                    │    INSIGHT AGENT      │
                    │  synthesizes evidence │
                    │  validates root cause │
                    └───────────┬───────────┘
                                │
                                ▼
                    ┌──────────────────────┐
                    │     ROOT CAUSE         │
                    │  Product X inventory   │
                    │  shortage (87% conf.)  │
                    └───────────┬───────────┘
                                │
                                ▼
                    ┌──────────────────────┐
                    │   RECOMMENDATION       │
                    │  Increase Western      │
                    │  region inventory ~20% │
                    └──────────────────────┘
```

The key design decision: the orchestrator doesn't follow one fixed path. It plans, delegates, observes what each specialist agent finds, and **decides what to investigate next based on that evidence** — that adaptive delegation loop is what makes this agentic rather than a single LLM call with a SQL tool bolted on.

---

## Features (Stage 1 prototype)

- **Natural-language question input** — no query language required
- **Live investigation view** — a real-time checklist of observable agent actions ("Querying sales data," "Investigating customer churn") alongside per-agent status (Waiting → Active → Complete)
- **Agent network view** — an expandable diagram of the orchestrator and its specialist agents, each showing exactly what it queried and what it found
- **Root cause analysis** — impact breakdown, a revenue trend chart, and a confidence score backed by cited evidence sources
- **Actionable recommendation** — a concrete next step with expected impact, one click to approve

> **Note on design intent:** the investigation screen deliberately shows *observable actions*, never fabricated "chain-of-thought" text. This was a conscious choice — it's more honest about what the system is actually doing, and it's a cleaner signal of real agentic behavior than a generic "AI is thinking..." animation.

---

## Tech stack

**Stage 1 (this repo — clickable prototype)**
| Layer | Tech |
|---|---|
| Frontend | HTML5, CSS3, vanilla JavaScript |
| Fonts | Space Grotesk (headings), Inter (body), IBM Plex Mono (data/numbers) |
| Hosting | Netlify |

**Stage 2 (planned full build)**
| Layer | Tech |
|---|---|
| Frontend | React + Vite + Tailwind CSS |
| Backend | Python + FastAPI |
| Agent orchestration | LangGraph (planner → specialist agents → synthesis) |
| LLM | Claude / OpenAI / Gemini |
| Database | Supabase (PostgreSQL) — simulated enterprise dataset (customers, orders, products, regions, support tickets) |
| Analytical queries | Pandas, DuckDB |
| Tool access layer | MCP — exposing `query_sales()`, `query_customers()`, `query_finance()`, `query_inventory()` |
| Charts | Recharts / Plotly.js |
| Deployment | Vercel (frontend) + Render/Railway (backend) |

---

## Project structure

```
insightflow-ai/
├── index.html              # Full clickable prototype (single-file)
├── README.md                # You're here
├── /docs
│   └── architecture.md      # Detailed multi-agent architecture notes
└── /assets
    └── screenshots/         # Screenshots used in Devpost submission
```

---

## Running it locally

No build step, no dependencies — it's a single static HTML file.

```bash
git clone https://github.com/<your-username>/insightflow-ai.git
cd insightflow-ai
open index.html   # or just double-click the file in Finder/Explorer
```

Or serve it locally if you prefer:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

---

## Try the demo flow

1. Land on the **Dashboard** — type or click a suggested business question
2. Hit **Investigate** — watch the live investigation checklist and agent status update in real time
3. Click through to **Agent Network** — click any agent card to expand what it queried and found
4. Continue to **Root Cause** — see the impact analysis, trend chart, and confidence score
5. Finish at **Recommendation** — click **Approve Action** to see the confirmation state

The top stepper and sidebar are both clickable, so you can jump to any screen directly.

---

## Roadmap

- [x] Stage 1: Interactive clickable prototype covering the full Ask → Investigate → Root Cause → Recommend loop
- [ ] Stage 2: Real LangGraph orchestration wired to a live Supabase dataset
- [ ] Replace simulated agent findings with real SQL/DuckDB queries via MCP tools
- [ ] Add authentication and multi-user support
- [ ] Support follow-up questions within an existing investigation ("drill into the Western region")
- [ ] Slack/email delivery of investigation summaries

---

## Team

| Name | Role |
|---|---|
| *(your name)* | *(e.g. AI/Agent Design, Full-stack)* |
| *(teammate name)* | *(role)* |

---

## Built for

[The Great Agent Hackathon](https://the-great-agent-hackathon.devpost.com/) — part of The Great Product Festival (TGPF) 2026 — Track 3: AI-native Enterprise (Open)

## License

MIT
