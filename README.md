<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:161b22,100:0d1117&height=180&section=header&text=Peesari%20Sathvik%20Reddy&fontSize=38&fontColor=58a6ff&fontAlignY=38&desc=AI%2FML%20Engineer%20%7C%20Full%20Stack%20Developer%20%7C%20Applied%20AI%20Researcher&descAlignY=58&descColor=8b949e&animation=fadeIn" />

[![Gmail](https://img.shields.io/badge/reddysathvik2005%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:reddysathvik2005@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/YOUR_LINKEDIN)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=flat-square&logo=vercel&logoColor=white)](https://YOUR_PORTFOLIO_URL)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=flat-square&logo=leetcode&logoColor=black)](https://leetcode.com/YOUR_LEETCODE)

</div>

---

```
B.Tech, Artificial Intelligence & Machine Learning
Chaitanya Bharathi Institute of Technology, Hyderabad
CGPA: 9.12 / 10  |  2023 – 2027

IIIT Hyderabad — Certificate of Proficiency in AI/ML  |  May – Sep 2025
AWS Certified Cloud Practitioner
Salesforce Certified Agentforce Specialist (2025)
```

---

## Stack

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)

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
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![Render](https://img.shields.io/badge/Render-46E3B7?style=flat-square&logo=render&logoColor=black)

**AI / ML**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)

**Tools**

![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat-square&logo=power-bi&logoColor=black)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white)

---

## Projects

### CONTINUUM
`React` `Vite` `TypeScript` `Node.js` `MongoDB` `Dexie.js` `WebRTC` `Socket.io` `i18next`

Offline-first healthcare continuity platform. Patients maintain a portable health record — consultations, vitals, lab reports, conditions, medications — shared with specific doctors. Everything works without internet; data syncs automatically on reconnect.

```
Architecture highlights
- Sync engine: IndexedDB (Dexie.js) queue → Express → MongoDB on reconnect
- Conflict resolution: client sends updatedAt, server rejects stale writes (HTTP 409)
- WebRTC: Socket.io signaling server, Xirsys TURN for NAT traversal
- Call recordings auto-saved to patient timeline
- Role-based access: patient / doctor / admin
- i18n: English, Hindi, Telugu
```

[Live](https://continuum-alpha-two.vercel.app)

---

### SETHU
`Next.js 14` `TypeScript` `Supabase` `PostgreSQL` `FastAPI` `Mistral API` `RapidOCR` `pdf-lib`

Role-based campus management platform for CBIT Hyderabad. Access control enforced at the database layer via Row Level Security — not the application layer.

```
Architecture highlights
- RLS on every table: queries auto-filtered by role regardless of API call
- PDF timetable import: OCR extraction → structured review → save
- AI study planner: Mistral reads subject annotations + day timetable → ranked priority list
- Request/approval engine: 7 types, 2 routing paths, auto-generated branded PDFs
- Scheduled jobs: pg_cron for exam reminders (7d / 3d / 1d), request cleanup
- Rate limiting: DB-backed, covers login and admin actions
```

[Live](https://sethu-pied.vercel.app)

---

### Syncpad
`React 19` `Vite` `Liveblocks` `Yjs` `Monaco Editor` `LiveKit` `MongoDB` `Clerk`

Real-time collaborative coding interview platform. Built in 24 hours at CBIT Hacktoberfest 2025. **Special Mention** among approximately 500 teams.

```
Architecture highlights
- Collaborative editor: Liveblocks + Yjs CRDT shared typing buffers + Monaco
- A/V conferencing: LiveKit WebRTC SDK
- Code execution: Judge0 via RapidAPI
- Session replay for post-interview review
- Resume analysis: Mistral AI
- Auth: Clerk with role-based protected routes
```

Contributions: quiz module, gamified daily quiz system, Resume Analyzer (Mistral), frontend UI components and routing.

---

### EngiQuery
`FastAPI` `Python` `Groq (Llama 3.3 70B)` `ChromaDB` `sentence-transformers` `pdfplumber`

Agentic AI platform for engineering document analysis. The LLM selects which tool to invoke based on query intent — not a static RAG pipeline.

```
Agent tools
- document_search     → multi-document Q&A with source citations
- cross_compare       → specification comparison across documents
- contradiction_check → conflict detection across documents
- compliance_check    → gap analysis against a standard
- email_workflow      → query + send full report via Gmail SMTP

All embeddings and vector storage are local (ChromaDB).
LLM inference via Groq free tier only.
Supports PDF, DOCX, TXT.
```

---

### PathVQA
`PyTorch` `EfficientNet-B0` `ResNet50` `Faster R-CNN` `BiLSTM` `GRU` `BAN` `Stacked Attention`

Multimodal VQA benchmarking on the PathVQA dataset (32,799 QA pairs, 4,998 pathology images). Three architectures implemented and compared.

| Architecture | Overall EM | Yes/No Acc | Open-Ended EM | F1 |
|---|---|---|---|---|
| EfficientNet-B0 + BiLSTM + Bilinear Fusion | **60.39%** | 79.27% | **53.45%** | 53.82% |
| ResNet50 + Stacked Attention + LayerNorm | 56.24% | **82.27%** | 46.66% | 47.82% |
| Faster R-CNN + GRU + BAN | 46.03% | 78.03% | 34.26% | 34.77% |

```
Key findings
- Bilinear fusion improves multimodal alignment significantly
- CNNs outperform Vision Transformers on pathology images
- Fusion strategy has more impact than backbone complexity
- Region-based models (Faster R-CNN) improve localization tasks
```

---

### RAY — Resume-based Application Yield
`Next.js 14` `TypeScript` `FastAPI` `Python` `Mistral AI` `TF-IDF` `Scikit-learn`

Resume-to-job matching platform. Upload PDF or DOCX → Mistral extracts skills and experience level → TF-IDF cosine similarity scores live job listings from JSearch and Adzuna APIs.

[Live](https://job-recommender-sigma.vercel.app)

---

### Zenvia
`React` `Flask` `PyTorch` `ResNet-50` `MediaPipe` `SerpAPI` `Mistral API` `OpenCV`

Integrated fashion intelligence platform. Presented at **ICAIATI-2025**, paper under publication.

```
Modules
- Size estimation:    MediaPipe Pose detects shoulder width + torso height → maps to XS–XXXL
- Color analysis:     ResNet-50 ensemble (5-fold CV) → seasonal palette (Winter/Autumn/Spring/Summer)
                      Validation accuracy: 94.18%
- Product discovery:  SerpAPI Google Shopping, filtered for Amazon IN / Flipkart / Myntra / AJIO
- Virtual wardrobe:   Cloudinary storage, outfit scheduling, weather-based suggestions
- FashionBot:         Mistral LLM conversational style assistant
```

---

### Telecom Churn Analysis
`Python` `Scikit-learn` `RandomForest` `Pandas`

Business-optimized churn prediction on 7,043 telecom customers. Decision threshold tuned for ROI, not accuracy.

```
Model: RandomForest  |  100 trees  |  max_depth=10  |  class_weight=balanced
Split: 80/20 stratified

Threshold shift: 0.5 -> 0.45
Rationale: FN cost (lost customer, Rs.2000) > FP cost (wasted offer, Rs.500)

Results
  Recall:   82.4%    ROC-AUC: 0.822
  Precision: 38.9%   F1:      54.3%

Business impact
  Customers targeted:  861
  Retention cost:      Rs.430,500
  Revenue saved:       Rs.672,000
  Net value:           Rs.161,500

Top churn drivers
  1. Tenure < 6 months  (53% churn rate)
  2. Month-to-month contract  (42.7% churn rate)
  3. No tech support
```

---

### Hindi News Classification System
`Flask` `PyTorch` `IndicBERTv2` `EasyOCR` `BeautifulSoup` `HuggingFace Spaces`

End-to-end Hindi NLP pipeline with three input modes: manual text, live web scraping, and OCR from images or PDFs.

```
Model comparison
  mBERT (Multilingual):   73.98%
  XLM-RoBERTa:            78.06%
  IndicBERTv2:            79.57%  <-- selected

Sources scraped: Amar Ujala, Dainik Jagran, Navbharat Times, BBC Hindi
Deployment: HuggingFace Spaces (Docker)
```

[Live](https://huggingface.co/spaces/Sathvik2954/hindi-samachar-2)

---

### Customer Reviews Topic Modeling
`Python` `Gensim` `BERTopic` `Scikit-learn` `UMAP` `HDBSCAN` `spaCy` `NLTK`

Unsupervised topic discovery across 630,000+ app reviews from 11 e-commerce platforms.

```
Sample: 10,000 reviews per app (110,000 total, seed=42)
After preprocessing: 97,619 retained
Methods: LDA, NMF, LSA, BERTopic, LDA+Bigrams  |  K=10 across all

Method comparison (combined corpus)
  NMF            coherence=0.5739  diversity=0.8333  <- ranked #1 on all 11 apps
  LDA + Bigrams  coherence=0.5363  diversity=0.7400
  LDA            coherence=0.5288  diversity=0.7800
  BERTopic       coherence=0.5189  diversity=0.8296
  LSA            coherence=0.4805  diversity=0.4800

Consensus: 10 topics, all HIGH CONFIDENCE
  Delivery Delays / Order Cancellation & Refunds / Customer Service
  Price & Product Quality / Search & Browse UX / Positive Experience
  App Performance & Bugs / Fashion & Sizing / Account & Payment Issues
  In-store & Inventory
```

[Dataset](https://www.kaggle.com/datasets/peesarisathvikreddy/customer-e-commerce-reviews)

---

## Stats

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=YOUR_GITHUB_USERNAME&show_icons=true&theme=github_dark&hide_border=true&count_private=true&title_color=58a6ff&icon_color=58a6ff&text_color=8b949e&bg_color=0d1117)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_GITHUB_USERNAME&layout=compact&theme=github_dark&hide_border=true&langs_count=8&title_color=58a6ff&text_color=8b949e&bg_color=0d1117)

![Streak](https://github-readme-streak-stats.herokuapp.com?user=YOUR_GITHUB_USERNAME&theme=github-dark-blue&hide_border=true&ring=58a6ff&fire=58a6ff&currStreakLabel=58a6ff)

</div>

---

<div align="center">
<sub>Hyderabad, India &nbsp;|&nbsp; Open to internships and research collaborations</sub>
</div>
