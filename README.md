<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:161b22,100:0d1117&height=160&section=header&text=Peesari%20Sathvik%20Reddy&fontSize=40&fontColor=58a6ff&fontAlignY=42&animation=fadeIn" />

**AI/ML Engineer · Full Stack Developer · Applied AI Researcher**

B.Tech Artificial Intelligence & Machine Learning · CBIT Hyderabad · CGPA 9.12

[![Gmail](https://img.shields.io/badge/reddysathvik2005@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:reddysathvik2005@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/YOUR_LINKEDIN)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=flat-square&logo=vercel&logoColor=white)](https://YOUR_PORTFOLIO_URL)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=flat-square&logo=leetcode&logoColor=black)](https://leetcode.com/YOUR_LEETCODE)

</div>

---

## About Me

I build complete systems — from offline sync engines and agentic AI workflows to multimodal research pipelines and campus-wide platforms.

My work spans healthcare, education, developer tools, NLP, computer vision, and business analytics. I care about production correctness, real metrics, and engineering decisions that hold up under pressure.

- Currently pursuing B.Tech in AI/ML at CBIT Hyderabad (2023–2027)
- Completed 5-month AI/ML training program at IIIT Hyderabad — iHub-Data (May–Sep 2025)
- Research presented at ICAIATI-2025 · Paper under publication
- Special Mention · CBIT Hacktoberfest 2025 · ~500 teams
- Vice President · Robotics & Innovation Club · CBIT (2024–2026)

---

## What I Build

| Domain | Focus |
|---|---|
| Software Engineering | Offline-first systems, real-time sync, conflict resolution, WebRTC, auth |
| Full Stack Development | React, Next.js, Node.js, FastAPI, PostgreSQL, MongoDB |
| AI Engineering | Agentic AI, RAG, tool-calling, LLM integration, vector databases |
| Machine Learning | Computer vision, NLP, multimodal learning, federated learning |
| Data Science | Predictive modeling, topic modeling, business ROI optimization |

---

## Featured Projects

### CONTINUUM
> `React` `TypeScript` `Node.js` `MongoDB` `Dexie.js` `WebRTC` `Socket.io` `i18n`

Offline-first healthcare continuity platform connecting patients and doctors through a shared portable health record. Patients record symptoms by voice, track vitals, and consult doctors — all without internet. Data syncs automatically on reconnect.

| What | How |
|---|---|
| Offline sync | IndexedDB (Dexie.js) queue → Express → MongoDB on reconnect |
| Conflict resolution | Client sends `updatedAt`; server rejects stale writes (HTTP 409) |
| Video calls | Socket.io signaling + Xirsys TURN; call audio saved to patient timeline |
| Roles | Patient / Doctor / Admin — separate dashboards and access scopes |
| i18n | English, Hindi, Telugu |

[Live](https://continuum-alpha-two.vercel.app)

---

### SETHU
> `Next.js 14` `TypeScript` `Supabase` `PostgreSQL` `FastAPI` `Mistral API` `RapidOCR` `pdf-lib`

Role-based campus management platform for CBIT Hyderabad. Access control enforced at the database layer via Row Level Security — not the application layer.

| What | How |
|---|---|
| Access control | RLS on every table; queries auto-filtered by role at DB level |
| Timetable import | Upload PDF → OCR extracts structure → faculty reviews → saves |
| AI study planner | Mistral reads subject annotations + today's timetable → ranked priority list |
| Requests | 7 types, 2 routing paths, auto-generated approval PDFs, signed URLs |
| Reminders | pg_cron scheduled jobs for exam reminders at 7d / 3d / 1d |

[Live](https://sethu-pied.vercel.app)

---

### Syncpad
> `React 19` `Liveblocks` `Yjs` `Monaco Editor` `LiveKit` `MongoDB` `Clerk`

Real-time collaborative coding interview platform. Built in 24 hours at CBIT Hacktoberfest 2025. **Special Mention** among ~500 teams.

| What | How |
|---|---|
| Collaborative editor | Liveblocks + Yjs CRDT shared typing buffers + Monaco |
| A/V conferencing | LiveKit WebRTC SDK |
| Code execution | Judge0 via RapidAPI |
| Resume analysis | Mistral AI — skill extraction and summary generation |
| Session replay | Full interview recording and playback |

Contributions: quiz module, gamified daily quiz, Resume Analyzer, frontend UI and routing.

---

### EngiQuery
> `FastAPI` `Python` `Groq (Llama 3.3 70B)` `ChromaDB` `sentence-transformers`

Agentic AI platform for engineering document analysis. The LLM selects which tool to invoke based on query intent — not a static RAG pipeline.

```
Agent tools
  document_search     multi-document Q&A with source citations
  cross_compare       specification comparison across documents
  contradiction_check conflict detection across documents
  compliance_check    gap analysis against a standard
  email_workflow      query + send full report via Gmail SMTP

All embeddings and vector storage are local.
```

---

### RAY — Resume-based Application Yield
> `Next.js 14` `TypeScript` `FastAPI` `Mistral AI` `TF-IDF` `Scikit-learn`

Resume-to-job matching platform. Upload PDF or DOCX → Mistral extracts skills and experience → TF-IDF cosine similarity scores live job listings from JSearch and Adzuna.

[Live](https://job-recommender-sigma.vercel.app)

---

## AI / ML Projects

### PathVQA — Multimodal Visual Question Answering
> `PyTorch` `EfficientNet-B0` `ResNet50` `Faster R-CNN` `BiLSTM` `GRU` `BAN` `Stacked Attention`

Three multimodal VQA architectures benchmarked on the PathVQA dataset (32,799 QA pairs, 4,998 pathology images).

| Architecture | Overall EM | Yes/No | Open-Ended EM |
|---|---|---|---|
| EfficientNet-B0 + BiLSTM + Bilinear Fusion | **60.39%** | 79.27% | **53.45%** |
| ResNet50 + Stacked Attention + LayerNorm | 56.24% | **82.27%** | 46.66% |
| Faster R-CNN + GRU + BAN | 46.03% | 78.03% | 34.26% |

Finding: fusion strategy has more impact than backbone complexity on pathology images.

---

### Zenvia — Fashion Intelligence Platform
> `Flask` `PyTorch` `ResNet-50` `MediaPipe` `OpenCV` `SerpAPI` `Mistral API`

Integrated fashion platform with five AI modules. Presented at **ICAIATI-2025**, paper under publication.

```
Size estimation   MediaPipe Pose → shoulder width + torso height → XS–XXXL
Color analysis    ResNet-50 ensemble (5-fold CV) → seasonal palette
                  Validation accuracy: 94.18%
Product search    SerpAPI Google Shopping → Amazon IN / Flipkart / Myntra / AJIO
Virtual wardrobe  Cloudinary storage, scheduling, weather-based suggestions
FashionBot        Mistral LLM conversational style assistant
```

---

### Hindi News Classification
> `IndicBERTv2` `Flask` `PyTorch` `EasyOCR` `BeautifulSoup` `HuggingFace Spaces`

End-to-end Hindi NLP pipeline with three input modes: manual text, live scraping, and OCR from images/PDFs.

```
mBERT (Multilingual)  73.98%
XLM-RoBERTa           78.06%
IndicBERTv2           79.57%   selected

Sources: Amar Ujala, Dainik Jagran, Navbharat Times, BBC Hindi
```

[Live](https://huggingface.co/spaces/Sathvik2954/hindi-samachar-2)

---

### Federated Learning
> `Python` `PyTorch` `Distributed Training`

Privacy-preserving distributed ML system covering federated learning, model aggregation strategies, and non-IID data handling.

---

## Data Science Projects

### Telecom Churn Analysis
> `Python` `Scikit-learn` `RandomForest` `Pandas`

Business-optimized churn prediction on 7,043 customers. Threshold tuned for ROI, not accuracy.

```
Threshold shift: 0.5 → 0.45
Rationale: missed customer (Rs.2000) costs more than wasted offer (Rs.500)

Recall: 82.4%   ROC-AUC: 0.822   Net business value: Rs.161,500

Top drivers
  1. Tenure < 6 months — 53% churn rate
  2. Month-to-month contract — 42.7% churn rate
  3. No tech support
```

---

### Customer Reviews Topic Modeling
> `Gensim` `BERTopic` `Scikit-learn` `UMAP` `HDBSCAN` `spaCy`

Unsupervised topic discovery across 630,000+ app reviews from 11 e-commerce platforms.

```
Methods: LDA, NMF, LSA, BERTopic, LDA+Bigrams   K=10 across all methods

NMF ranked #1 on coherence (0.5739) and diversity (0.8333) — best on all 11 individual apps

10 consensus topics — all HIGH CONFIDENCE
  Delivery Delays · Refunds · Customer Service · Price & Quality
  App Bugs · Search UX · Positive Experience · Fashion & Sizing
  Account & Payments · In-store & Inventory
```

[Dataset](https://www.kaggle.com/datasets/peesarisathvikreddy/customer-e-commerce-reviews)

---

## Tech Stack

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)

**Frontend**

![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)

**Backend**

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)

**Databases & Infra**

![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazon-aws&logoColor=white)

**AI / ML**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)

**Tools**

![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat-square&logo=power-bi&logoColor=black)

---

## Certifications & Achievements

| | |
|---|---|
| AWS Certified Cloud Practitioner | Amazon Web Services |
| Salesforce Certified Agentforce Specialist | Salesforce · 2025 |
| Certificate of Proficiency in AI/ML | IIIT Hyderabad — iHub-Data · May–Sep 2025 |
| Special Mention · Hacktoberfest 2025 | ~500 teams · product completeness & innovation |
| Research Publication | ICAIATI-2025 · Zenvia · Under publication |
| Vice President · Robotics & Innovation Club | CBIT · 2024–2026 |

---

## GitHub Stats

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=YOUR_GITHUB_USERNAME&show_icons=true&theme=github_dark&hide_border=true&count_private=true&title_color=58a6ff&icon_color=58a6ff&text_color=8b949e&bg_color=0d1117)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_GITHUB_USERNAME&layout=compact&theme=github_dark&hide_border=true&langs_count=8&title_color=58a6ff&text_color=8b949e&bg_color=0d1117)

![Streak](https://github-readme-streak-stats.herokuapp.com?user=YOUR_GITHUB_USERNAME&theme=github-dark-blue&hide_border=true&ring=58a6ff&fire=58a6ff&currStreakLabel=58a6ff)

</div>

---

<div align="center">
<sub>Hyderabad, India &nbsp;·&nbsp; Open to internships and research collaborations &nbsp;·&nbsp; reddysathvik2005@gmail.com</sub>
</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:161b22,100:0d1117&height=100&section=footer" />
