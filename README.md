<div align="center">

<img width="500" src="https://raw.githubusercontent.com/arasgungore/animated-svgs/main/circuit-board/circuit-board.svg">

# 🚀 **AI Research Scout**

### *Autonomous AI Agent That Scours the Internet for the Latest Breakthroughs in AI, ML, LLMs & RAG*

#### **Smart ingestion → Adaptive clustering → LLM digest → Daily emails with top innovations.**

</div>

---

<div align="center">

![Stars](https://img.shields.io/github/stars/ahmed?style=for-the-badge\&color=0aefff)
![Issues](https://img.shields.io/github/issues/ahmed?style=for-the-badge\&color=ff6b6b)
![Python](https://img.shields.io/badge/Python-3.13-blue?style=for-the-badge)
![LangGraph](https://img.shields.io/badge/LangGraph-Orchestrated-black?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)

</div>

---

# ⚡ **Overview**

**AI Research Scout** is a next-gen automation agent that continuously scans:
✔ arXiv
✔ Semantic Scholar
✔ Crossref
✔ GitHub releases
✔ RSS feeds
✔ Engineering blogs
✔ Paper PDFs

And transforms them into:
→ **Ranked topic clusters**
→ **Curated reading lists**
→ **LLM-generated digests**
→ **Daily/Weekly HTML email briefs**

Powered by **LangGraph orchestration**, **SQLite vector storage**, and **Google Gemini embeddings**, the system operates as a full-stack intelligence pipeline.

This repo contains the **architecture, schemas, and foundational boilerplate** for the full agent.

---

# ✨ **Animated System Flow**

<div align="center">
<img width="750" src="https://raw.githubusercontent.com/arasgungore/animated-svgs/main/lines/lines.svg">
</div>

```
┌───────────────────┐
│ Schedule Trigger  │ ─────► Starts Daily Pipeline
└───────────────────┘
           │
           ▼
┌───────────────────┐
│  Source Fetchers  │ ─────► arXiv / GitHub / RSS / Crossref
└───────────────────┘
           │
           ▼
┌───────────────────────────┐
│ Normalization + Extraction│
└───────────────────────────┘
           │
           ▼
┌────────────────────┐
│ Embeddings Engine  │ ─────► Gemini / ST Models
└────────────────────┘
           │
           ▼
┌──────────────────────┐
│ Clustering + Scoring │ ─────► Novelty / Impact
└──────────────────────┘
           │
           ▼
┌────────────────────────┐
│ Digest Composer (LLM)  │
└────────────────────────┘
           │
           ▼
┌───────────────────┐
│ Email Dispatcher  │ ─────► HTML Digest
└───────────────────┘
```

---

# 🔮 **Core Value Proposition**

> *“Instead of searching for innovation, innovation comes to you.”*

This agent gives you **continuous competitive intelligence on emerging AI research**, compressed into a frictionless reading workflow.

Perfect for:
• Founders
• Researchers
• Engineers
• Product leads
• VCs
• Competitive analysts

---

# 🧠 **LangGraph Architecture**

This system uses a **modular LangGraph pipeline** with ~22 nodes:

* Source scanners (parallel)
* PDF downloader
* Text extractor
* Normalizer
* Embedding generator
* Duplicate detection
* Topic clustering
* Topic ranking
* Reading-list assembler
* Digest composer
* Email sender
* Reply monitor
* Mark-read endpoint

Full node list defined in `/src/nodes/`.

---

# 🗄 **Database Schema (SQLite)**

Full schema is in `/src/db/schema.sql`.

* `topics`
* `items`
* `topic_items`
* `email_log`
* `user_actions`

Optimized for a lightweight local / GitHub Actions deployment.

---

# 🛠 **Local Setup**

```
git clone https://github.com/<your-username>/ai-research-scout
cd ai-research-scout
pyenv local 3.13.0
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

Run local pipeline:

```
python src/run.py
```

---

# 🔥 **Deployment (Hybrid Runtime)**

* **GitHub Actions:** Scheduled crawler + digest generator
* **Vercel / FastAPI:** Interactive read tracking endpoint
* **SQLite (local or cloud-sync)** for embedding store

CI/CD templates provided in `/infra/github-actions/`.

---

# 📨 **Email Digest Preview**

<div align="center">
<img width="600" src="https://raw.githubusercontent.com/arasgungore/animated-svgs/main/pulse/pulse.svg">
</div>

```
📌 Topic: Reinventing RAG — Structure-Aware Retrieval
• Paper 1 — 2-minute summary
• Paper 2 — 3-minute breakdown
• GitHub Repo — key insights
• Blog — what changed this week

📌 Topic: SOTA LLM Efficiency
• Paper 1 — memory optimization
• Repo — quantization updates
...
```

HTML templates stored in `/src/templates/`.

---

# 🌐 **Tech Stack**

| Layer          | Technology                                    |
| -------------- | --------------------------------------------- |
| Orchestration  | **LangGraph**                                 |
| LLM            | **Gemini Flash 2.0 / 2.1**, local ST fallback |
| Vector Store   | **SQLite + numpy**                            |
| API Framework  | **FastAPI**                                   |
| Scheduled Jobs | **GitHub Actions**                            |
| PDF Parsing    | **PyMuPDF**                                   |
| Clustering     | **scikit-learn**                              |
| Email          | **SMTP / Gmail API**                          |

---

# 📦 **Project Structure**

```
ai-research-scout/
│
├── src/
│   ├── nodes/
│   ├── ingestion/
│   ├── pipelines/
│   ├── db/
│   ├── utils/
│   └── templates/
│
├── tests/
├── infra/
├── README.md
└── requirements.txt
```

---

# 🧩 **Roadmap**

* [ ] Deploy Mark-Read microservice to Vercel
* [ ] Add vector search UI
* [ ] Add multi-user support
* [ ] Add Slack + Telegram digest delivery
* [ ] Add multi-agent reflection to improve topic scoring
* [ ] Add real-time “Breaking AI” alert mode

---

# 🏆 **Credits**

Built with precision & obsession by **Bakhshi**.
Architected for innovators who don’t wait for the future — they monitor it.

---
