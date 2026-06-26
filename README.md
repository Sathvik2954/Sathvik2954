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

Offline-first healthcare continuity platform connecting patients and doctors through a single portable health record that works with or without internet. Patients record symptoms by voice, track vitals, upload documents, and consult doctors asynchronously — all data queued locally in IndexedDB and synced automatically on reconnect. Includes scheduled WebRTC video calls with call audio saved to the patient timeline, conflict resolution via HTTP 409 on stale writes, and multilingual support in English, Hindi, and Telugu.

**Roles:** Patient · Doctor · Admin

[Live](https://continuum-alpha-two.vercel.app)

---

### SETHU
> `Next.js 14` `TypeScript` `Supabase` `PostgreSQL` `RLS` `FastAPI` `Mistral API` `RapidOCR` `pdf-lib` `pg_cron`

Role-based campus management platform for CBIT Hyderabad serving students, faculty, HODs, and administrators. Access control is enforced at the database layer through Row Level Security — every query auto-filters to what that role is permitted to see. Timetables can be imported from PDFs via OCR; the AI study planner (Mistral) reads subject annotations and the day's schedule to return a ranked priority list. Requests auto-generate approval PDFs, and pg_cron handles exam reminders and deadline alerts.

**Roles:** Student · Faculty · HOD · Admin

[Live](https://sethu-pied.vercel.app)

---

### Syncpad
> `React 19` `Liveblocks` `Yjs` `Monaco Editor` `LiveKit` `Node.js` `MongoDB` `Clerk` `Judge0`

Real-time collaborative coding interview platform built in 24 hours at CBIT Hacktoberfest 2025 — **Special Mention among ~500 teams**. Features multi-user CRDT-based code editing via Liveblocks and Yjs, audio/video conferencing via LiveKit WebRTC, code execution through Judge0, session replay for post-interview review, and a gamified daily quiz system. Resume analysis powered by Mistral AI extracts skills and generates candidate summaries.

**Contributions:** Quiz module, gamified daily quiz, Resume Analyzer, frontend UI and routing

---

## AI / ML Projects

### PathVQA — Multimodal Visual Question Answering
> `PyTorch` `EfficientNet-B0` `ResNet50` `Faster R-CNN` `BiLSTM` `GRU` `BAN` `Stacked Attention`

Research project designing and benchmarking three multimodal VQA architectures on the PathVQA dataset (32,799 QA pairs, 4,998 pathology images). Implemented region-based visual reasoning with Faster R-CNN + GRU + BAN, global CNN encoding with EfficientNet-B0 + BiLSTM + Bilinear Fusion, and iterative attention with ResNet50 + Stacked Attention. Best result: 60.39% overall exact match and 53.45% open-ended EM with EfficientNet-B0 + Bilinear Fusion. Key finding: fusion strategy has more impact than backbone complexity on pathology images.

---

### Zenvia — Fashion Intelligence Platform
> `Flask` `PyTorch` `ResNet-50` `MediaPipe Pose` `OpenCV` `SerpAPI` `Mistral API` `Cloudinary`

Full-stack AI platform with five integrated modules: real-time body size estimation via MediaPipe Pose, seasonal color classification using a 5-fold ResNet-50 ensemble (94.18% validation accuracy), live product discovery via SerpAPI Google Shopping, a virtual wardrobe with outfit scheduling and weather-based suggestions, and a conversational FashionBot powered by Mistral. **Presented at ICAIATI-2025**, paper under publication.

---

### Hindi News Classification System
> `IndicBERTv2` `Flask` `PyTorch` `HuggingFace Transformers` `EasyOCR` `BeautifulSoup` `Docker`

End-to-end Hindi NLP platform classifying news headlines into five categories through three input modes: typed text, live scraping from Amar Ujala, Dainik Jagran, Navbharat Times, and BBC Hindi, and OCR extraction from images and PDFs. Fine-tuned IndicBERTv2 outperforms mBERT (73.98%) and XLM-RoBERTa (78.06%) with 79.57% accuracy due to its Indic-specific pretraining. Deployed on HuggingFace Spaces via Docker.

[Live](https://huggingface.co/spaces/Sathvik2954/hindi-samachar-2)

---

## Data Science & Analytics Projects

### Telecom Churn Analysis
> `Python` `Scikit-learn` `RandomForest` `Pandas` `Matplotlib` `Seaborn`

Business-optimized churn prediction on 7,043 telecom customers. Instead of maximizing accuracy, the decision threshold was tuned from 0.5 to 0.45 to prioritize recall — because a missed churning customer (₹2,000 LTV loss) costs four times more than a wasted retention offer (₹500). RandomForest achieved 82.4% recall and 0.822 ROC-AUC, identifying 861 at-risk customers and projecting ₹161,500 net business value. Top churn drivers: tenure under 6 months (53.3% churn rate) and month-to-month contracts (42.7%).

---

### Olist E-Commerce Analytics
> `MySQL 8.0` `Python` `pandas` `SQLAlchemy` `Power BI` `DAX`

End-to-end analytics pipeline on 100,000+ Brazilian e-commerce orders from the Olist marketplace. Answered six business questions through 10 SQL queries covering revenue by category, delivery performance by state, late delivery impact on review scores, repeat purchase rate, payment method breakdown, and month-over-month revenue growth. Findings delivered through a three-page executive Power BI dashboard. Key finding: deliveries delayed 4+ days average a 1.86/5.0 review score versus 4.29/5.0 for early deliveries.

[Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

---

### Customer Reviews Topic Modeling
> `Gensim` `BERTopic` `Scikit-learn` `sentence-transformers` `UMAP` `HDBSCAN` `spaCy` `NLTK`

Unsupervised topic discovery across 630,000+ app reviews from 11 e-commerce platforms including Amazon, Flipkart, Myntra, and Meesho. Five methods benchmarked — LDA, NMF, LSA, BERTopic, LDA+Bigrams — with results aggregated into a consensus topic set via cosine similarity of topic-word vectors. NMF ranked first on both coherence (0.5739) and diversity (0.8333) across all 11 individual apps. All 10 consensus topics confirmed HIGH CONFIDENCE, covering delivery, refunds, customer service, app bugs, and pricing.

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
