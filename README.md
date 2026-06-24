<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:161b22,100:0d1117&height=160&section=header&text=Peesari%20Sathvik%20Reddy&fontSize=40&fontColor=58a6ff&fontAlignY=42&animation=fadeIn" />

**AI/ML Engineer · Full Stack Developer · Problem Solver**

B.Tech Artificial Intelligence & Machine Learning · CBIT Hyderabad · CGPA 9.12

[![Gmail](https://img.shields.io/badge/reddysathvik2005@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:reddysathvik2005@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/peesari-sathvik-reddy-881967322/)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=flat-square&logo=vercel&logoColor=white)](https://sathvik2954.netlify.app/)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=flat-square&logo=leetcode&logoColor=black)](https://leetcode.com/u/Sathvik_2954/)

</div>

---

## About Me

I am a sociable and impact-driven developer with experience delivering ML and full-stack solutions through internships, research, and collaborative projects. I enjoy translating real-world problems into practical technology — and thrive in collaborative environments where taking initiative matters.

Currently pursuing B.Tech in AI/ML at CBIT Hyderabad (2023–2027).

---

## What I Build

| Domain | Focus |
|---|---|
| Software Engineering | Offline-first systems, real-time sync, conflict resolution, WebRTC, role-based auth |
| Full Stack Development | React, Next.js, Node.js, FastAPI, PostgreSQL, MongoDB |
| AI Engineering | Agentic AI, RAG pipelines, tool-calling agents, LLM integration, vector databases |
| Machine Learning | Computer vision, NLP, multimodal learning, transformer fine-tuning |
| Data Science & Analytics | Predictive modeling, SQL analytics, business dashboards, ROI optimization |

---

## SDE & Full Stack Projects

### CONTINUUM
> `React` `TypeScript` `Node.js` `Express` `MongoDB` `Dexie.js` `WebRTC` `Socket.io` `PWA` `i18next`

Offline-first healthcare continuity platform that connects patients and doctors through a single portable health record — one that works with or without internet. The core engineering problem: how do you build a medical system that never loses data, even when the network drops mid-session?

**Architecture**

```
Patient (offline)
  Symptom recording  →  IndexedDB blobs store (Dexie.js)
  Consultation form  →  IndexedDB sync_queue  (pending)
  Vitals log         →  IndexedDB sync_queue  (pending)

[network returns]

Sync engine fires on browser 'online' event
  Upload audio blobs  →  Express /uploads/audio/
  POST pending records →  Express → MongoDB Atlas
  Mark as synced       →  IndexedDB update
  Pull fresh data      →  Refresh IndexedDB cache
```

**Key Engineering Decisions**

| Problem | Solution |
|---|---|
| Offline data loss | Dexie.js IndexedDB queue; nothing written to server until connectivity confirmed |
| Stale write conflicts | Client sends `updatedAt`; server returns HTTP 409 on version mismatch; user notified, no silent loss |
| Video calls on mobile networks | Socket.io WebRTC signaling + Xirsys TURN for NAT traversal; call audio auto-saved to patient timeline |
| Multi-language support | i18next with English, Hindi, Telugu; language detection from browser |
| File storage | Multer for audio, documents, call recordings; client-side image compression before upload |

**Roles:** Patient · Doctor · Admin — fully separate dashboards, route guards, and data scopes  
**Live →** https://continuum-alpha-two.vercel.app

---

### SETHU
> `Next.js 14` `App Router` `TypeScript` `Supabase` `PostgreSQL` `RLS` `FastAPI` `Mistral API` `RapidOCR` `pdf-lib` `pg_cron`

Role-based campus management platform for CBIT Hyderabad. Serves four roles — student, faculty, head of department, administrator — with access control enforced at the database layer through Row Level Security, not the application layer. Every query is automatically filtered to what that role is permitted to see.

**Key Features by Role**

| Role | Core Capabilities |
|---|---|
| Student | Timetable view, exam schedule, subject annotations, AI study planner, formal request submission, resume profile builder |
| Faculty | Define subjects, manage timetables via PDF import, broadcast deadlines and notifications by year/section |
| HOD | Department-scoped approvals queue, event permission routing |
| Admin | Staff account provisioning, institution-wide notifications, full audit log |

**Key Engineering Decisions**

| Problem | Solution |
|---|---|
| Access control at scale | RLS policies on every Supabase table; wrong-role queries return empty, not errors |
| Timetable PDF import | RapidOCR extracts structure → Mistral cleans and formats → faculty reviews before commit |
| AI study planner | Mistral reads subject difficulty/relevance annotations + actual day's free hours → ranked study list |
| Approval document generation | pdf-lib generates branded PDFs on approval; signed URLs for private attachments |
| Automated reminders | Supabase pg_cron jobs for exam reminders at 7d / 3d / 1d; last-day deadline alerts |
| Login rate limiting | DB-backed rate limit table; failed attempts tracked per email with auto-reset |

**Live →** https://sethu-pied.vercel.app

---

### Syncpad
> `React 19` `Vite` `Liveblocks` `Yjs` `Monaco Editor` `LiveKit` `Node.js` `MongoDB` `Clerk` `Judge0`

Real-time collaborative coding interview platform built in 24 hours at CBIT Hacktoberfest 2025. **Special Mention** among ~500 teams for product completeness and innovation.

**Architecture**

```
Collaborative editor  →  Liveblocks + Yjs CRDT shared typing buffers + Monaco Editor
Audio/video           →  LiveKit WebRTC SDK with server-side room management
Code execution        →  Judge0 (RapidAPI) with hidden test case evaluation
Authentication        →  Clerk with protected routes and role-based access
Session replay        →  Full interview recording and post-session playback
Email notifications   →  Nodemailer with automated scheduling confirmations
```

**Feature Breakdown**

| Feature | Tech | Detail |
|---|---|---|
| Multi-user code editor | Liveblocks + Yjs | CRDT-based conflict-free shared editing; no last-write-wins data loss |
| A/V conferencing | LiveKit | WebRTC rooms with server SDK token generation |
| Problem library | MongoDB | Custom and hidden test cases, autosave on every keystroke |
| Resume analyzer | Mistral AI | Skill extraction, experience summary, candidate profile generation |
| Gamified quiz | Custom | Daily quiz with streaks, scoring, and leaderboard |
| Session replay | LiveKit recording | Full interview rewatch for interviewers post-session |

**Contributions:** Quiz module and gamified daily quiz system, Resume Analyzer (Mistral integration), frontend UI components, route architecture

---

## AI / ML Projects

### PathVQA — Multimodal Visual Question Answering
> `PyTorch` `EfficientNet-B0` `ResNet50` `Faster R-CNN` `BiLSTM` `GRU` `BAN` `Stacked Attention Networks`

Research project designing and benchmarking three multimodal VQA architectures on the PathVQA dataset — 32,799 QA pairs across 4,998 pathology images. The core challenge: open-ended medical questions require both precise visual localization and language understanding.

**Architectures Implemented**

| Method | Vision Encoder | Text Encoder | Fusion | Overall EM | Yes/No | Open-Ended EM | F1 |
|---|---|---|---|---|---|---|---|
| Method 1 | Faster R-CNN | GRU | Bilinear Attention Network (BAN) | 46.03% | 78.03% | 34.26% | 34.77% |
| Method 2 | EfficientNet-B0 | BiLSTM | Bilinear Fusion | **60.39%** | 79.27% | **53.45%** | **53.82%** |
| Method 3 | ResNet50 | LSTM | Stacked Attention + LayerNorm | 56.24% | **82.27%** | 46.66% | 47.82% |

**Key Findings**

- EfficientNet-B0 + Bilinear Fusion outperforms region-based Faster R-CNN by 14.36 percentage points on overall EM
- Fusion strategy (bilinear vs attention) has more impact on open-ended performance than backbone complexity
- ResNet50 + Stacked Attention achieves the highest Yes/No accuracy (82.27%) through iterative visual reasoning
- CNNs outperform Vision Transformers on pathology images — domain-specific texture matters more than global context

**Dataset:** He et al., 2020 — PathVQA (arxiv.org/abs/2003.10286)

---

### Zenvia — Fashion Intelligence Platform
> `Flask` `PyTorch` `ResNet-50` `5-fold Cross Validation` `MediaPipe Pose` `OpenCV` `SerpAPI` `Mistral API` `Cloudinary`

Full-stack AI platform with five integrated ML modules. **Presented at ICAIATI-2025**, paper under publication.

**Module Breakdown**

| Module | Tech | How It Works |
|---|---|---|
| Size Estimation | MediaPipe Pose + OpenCV | Detects 33 body landmarks via webcam; computes shoulder width and torso height; maps to XS–XXXL using a calibrated size chart |
| Seasonal Color Analysis | ResNet-50 ensemble | 5-fold cross-validation; ensemble prediction with accuracy-weighted voting across 5 saved checkpoints; classifies Winter/Autumn/Spring/Summer |
| Product Discovery | SerpAPI Google Shopping | Live product search filtered by detected size, color, gender, and category; surfaces Amazon IN, Flipkart, Myntra, AJIO results |
| Virtual Wardrobe | Cloudinary + localStorage | Drag-and-drop upload, outfit scheduling, email reminders via SMTP, weather-based outfit suggestions via OpenWeatherMap API |
| FashionBot | Mistral API | Conversational style assistant with chat history, personalized outfit advice, trend information |

**Model Performance**

```
Dataset         Roboflow seasonal color dataset (~6,770 images)
Architecture    ResNet-50 with custom fully connected head
Training        5-fold cross-validation
Inference       Accuracy-weighted ensemble across 5 fold checkpoints
Validation Acc  94.18%
Classes         Winter (Invierno) · Autumn (Otono) · Spring (Primavera) · Summer (Verano)
```

---

### Hindi News Classification System
> `IndicBERTv2` `Flask` `PyTorch` `HuggingFace Transformers` `EasyOCR` `BeautifulSoup` `HuggingFace Spaces` `Docker`

End-to-end Hindi NLP platform that classifies news into five categories through three distinct input modes: typed text, live web scraping, and OCR extraction from images and PDFs.

**Model Comparison**

| Model | Accuracy | Notes |
|---|---|---|
| mBERT (Multilingual BERT) | 73.98% | General multilingual; weaker on Indic morphology |
| XLM-RoBERTa | 78.06% | Stronger cross-lingual transfer |
| IndicBERTv2 | **79.57%** | Selected — pre-trained on Indic corpora; best on Hindi-specific vocabulary |

**Input Modes**

| Mode | Tech | Detail |
|---|---|---|
| Manual text | IndicBERTv2 inference | Headline → predicted category + confidence score (%) |
| Live scraping | BeautifulSoup + Requests | Pulls real-time headlines from Amar Ujala, Dainik Jagran, Navbharat Times, BBC Hindi; deduplicates; classifies each |
| OCR extraction | EasyOCR + PIL | Upload image or PDF → extract Hindi headings → classify each heading |

**Data Processing:** Hybrid balancing strategy — undersampling large classes + oversampling smaller classes; sentence truncation to first 1–2 sentences; label normalization across 14+ original IndicGLUE categories condensed to 5  
**Deployment:** HuggingFace Spaces (Docker container)  
**Live →** https://huggingface.co/spaces/Sathvik2954/hindi-samachar-2

---

## Data Science & Analytics Projects

### Telecom Churn Analysis
> `Python` `Scikit-learn` `RandomForest` `Pandas` `Matplotlib` `Seaborn`

Business-driven churn prediction on 7,043 telecom customers. The objective was not to maximize accuracy but to optimize decision threshold for real business ROI — because missing a churning customer (₹2,000 LTV loss) costs four times more than a wasted retention offer (₹500).

**Business Context**

```
Annual churn rate    26.5%  (~1,900 customers/year)
LTV per customer     Rs. 2,000
Retention offer cost Rs. 500
Annual revenue loss  Rs. 3,800,000 (without intervention)
```

**Model & Threshold Optimization**

| Metric | Default (0.5) | Optimized (0.45) |
|---|---|---|
| Recall | ~76% | **82.4%** |
| Precision | ~45% | 38.9% |
| Customers targeted | lower | 861 at-risk customers |
| Net business value | lower | **Rs. 161,500** |

ROC-AUC: 0.822

**Churn Drivers Identified**

| Driver | Feature Importance | Churn Rate |
|---|---|---|
| Tenure < 6 months | 6.64% | 53.3% |
| Month-to-month contract | 5.85% | 42.7% |
| No tech support | 5.07% | elevated vs supported customers |
| 1-year contract | — | 11.3% |
| 2-year contract | — | 2.8% |

**Segmentation for Targeting**

| Segment | Count | Recommended Action | Budget |
|---|---|---|---|
| High risk (0.5–0.7) | 662 | Personal call + Rs.500 discount | Rs. 331,000 |
| Medium risk (0.35–0.5) | 464 | Email + service check | Rs. 46,400 |
| Monitor (<0.35) | 283 | No immediate action | — |

---

### Olist E-Commerce Analytics
> `MySQL 8.0` `Python` `pandas` `SQLAlchemy` `Power BI` `DAX`

End-to-end analytics pipeline on 100,000+ Brazilian e-commerce orders from the Olist marketplace. SQL-first analysis covering six business questions, with findings delivered through a three-page executive Power BI dashboard.

**Business Questions & Findings**

| Question | Key Finding |
|---|---|
| Revenue by category | Health & Beauty leads at 1,233,131 BRL (8,647 orders); Watches & Gifts second at 1,166,176 BRL |
| Delivery vs review score | Early deliveries average 4.29/5.0; deliveries delayed 4+ days average 1.86/5.0 — a 2.43-point drop |
| Delivery performance by state | Significant state-level variance; geolocation data excluded from joins due to duplicate zip code coordinates |
| Repeat purchase rate | 3.0% — only 2,801 of 93,358 unique customers returned; reflects real marketplace behavior |
| Payment methods | Credit cards dominate: 12,542,084 BRL across 76,505 orders; avg transaction 163 BRL at 3.5 installments |
| Revenue growth | Peak: November 2017 at 1,153,364 BRL (+53.6% MoM) driven by Black Friday campaigns |

**SQL Techniques Used**

| Query | Concept |
|---|---|
| Monthly revenue trend | CTE + date truncation |
| MoM growth rate | CTE + `LAG()` window function |
| Category revenue share | CTE + `SUM() OVER()` |
| Late delivery impact | `CASE WHEN` + `DATEDIFF()` |
| Repeat purchase rate | Self-join CTE on customer orders |

**Pipeline:** Kaggle CSV → pandas + SQLAlchemy data loader → MySQL `olist_db` (9 tables) → SQL analysis → Power BI dashboard (3 pages: Business Overview, Delivery & Satisfaction, Customers & Sellers)  
**Dataset →** https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

---

### Customer Reviews Topic Modeling
> `Python` `Gensim` `BERTopic` `Scikit-learn` `sentence-transformers` `UMAP` `HDBSCAN` `spaCy` `NLTK`

Large-scale unsupervised NLP pipeline discovering universal complaint and satisfaction themes across 630,000+ app reviews from 11 major e-commerce platforms. Five topic modeling methods benchmarked and aggregated into a consensus topic set via cosine similarity of topic-word vectors.

**Dataset**

```
Platforms    Amazon · Flipkart · Myntra · Meesho · Snapdeal · Alibaba · Aliexpress
             Lazada · Daraz · Shein · Walmart
Total        629,989 reviews available
Sample used  10,000 per app (110,000 total, random seed 42)
After clean  97,619 reviews retained
```

**Method Benchmark — Combined Corpus**

| Method | Coherence (c_v) | Diversity | Notes |
|---|---|---|---|
| NMF | **0.5739** | **0.8333** | Best on coherence and diversity; #1 across all 11 individual apps |
| LDA + Bigrams | 0.5363 | 0.7400 | Phrase detection improves topic granularity |
| LDA | 0.5288 | 0.7800 | Solid baseline |
| BERTopic | 0.5189 | 0.8296 | 59.6% outlier rate due to review heterogeneity; surfaces niche actionable topics |
| LSA | 0.4805 | 0.4800 | Weakest diversity |

**Consensus Topics (all 10 confirmed HIGH CONFIDENCE)**

| Topic | Label | Method Agreement |
|---|---|---|
| 0 | Account and Payment Issues | 3/5 |
| 1 | Order Cancellation and Refunds | 5/5 |
| 2 | App Performance and Bugs | 4/5 |
| 3 | Delivery Delays | 5/5 |
| 4 | Search and Browse UX | 5/5 |
| 5 | Fashion and Sizing | 4/5 |
| 6 | Positive Experience | 5/5 |
| 7 | In-store and Inventory | 4/5 |
| 8 | Customer Service | 5/5 |
| 9 | Price and Product Quality | 5/5 |

**Key Insight:** Negative reviews contain precise vocabulary (cancel, refund, fake, fraud, crash, freeze). Positive reviews surface only generic sentiment words. BERTopic uniquely identifies niche signals — dark mode requests, wishlist bugs, localisation complaints — missed entirely by bag-of-words methods.

**Dataset →** https://www.kaggle.com/datasets/peesarisathvikreddy/customer-e-commerce-reviews

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
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
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

## Connect With Me

> *"Bide your Time. Hide your Strength."*

[![Gmail](https://img.shields.io/badge/reddysathvik2005@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:reddysathvik2005@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/peesari-sathvik-reddy-881967322/)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=flat-square&logo=vercel&logoColor=white)](https://sathvik2954.netlify.app/)

<div align="center">

*"First, solve the problem. Then, write the code."* — John Johnson

⭐ If you find my work useful, drop a star! ⭐

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:161b22,100:0d1117&height=100&section=footer" />
