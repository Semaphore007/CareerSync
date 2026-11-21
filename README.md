# 🚀 CareerSync – AI-Powered ATS Resume Analyzer

<p align="center">
  <b>Intelligent Resume Analysis | Semantic Job Matching | AI-Powered Career Insights</b>
</p>

<p align="center">
  An AI-powered resume intelligence platform that evaluates resume compatibility with job descriptions, identifies skill gaps, and generates actionable recommendations using NLP, semantic similarity, and Large Language Models.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10%2B-blue?logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/FastAPI-Backend-009688?logo=fastapi&logoColor=white"/>
  <img src="https://img.shields.io/badge/Streamlit-Frontend-FF4B4B?logo=streamlit&logoColor=white"/>
  <img src="https://img.shields.io/badge/NLP-spaCy-09A3D5"/>
  <img src="https://img.shields.io/badge/AI-Groq%20LLM-orange"/>
  <img src="https://img.shields.io/badge/Database-Supabase-3ECF8E?logo=supabase&logoColor=white"/>
</p>

---

## 📌 Overview

**CareerSync** is an AI-driven Applicant Tracking System (ATS) resume analyzer designed to bridge the gap between candidate profiles and job requirements.

Traditional keyword-based resume screening often fails to understand contextual relevance between skills, experience, and job descriptions. CareerSync addresses this limitation through NLP-based information extraction and semantic similarity techniques.

The platform analyzes uploaded resumes against target job descriptions, calculates an ATS compatibility score, identifies missing skills and keywords, and leverages LLMs to generate personalized improvement suggestions.

## ✨ Key Features

### 🧠 Intelligent Resume Analysis
- Upload resumes in PDF, DOC, and DOCX formats.
- Extract relevant information, skills, and professional experience.
- Process resume content using NLP techniques.

### 🎯 Semantic Job Matching
- Compare resumes with job descriptions using Sentence Transformers.
- Measure contextual similarity beyond exact keyword matching.
- Identify relevant skills and missing job-specific keywords.

### 📊 ATS Compatibility Scoring
- Generate an overall resume compatibility score.
- Evaluate multiple dimensions:
  - Resume formatting
  - Keyword relevance
  - Content quality
  - Skill validation
  - ATS compatibility

### 🤖 LLM-Powered Recommendations
- Generate contextual resume improvement suggestions.
- Identify areas requiring optimization.
- Provide actionable feedback using Groq-powered LLM integration.

### 🔐 Authentication & Analysis History
- Secure user authentication through Supabase.
- Support email/password and Google OAuth authentication.
- Save previous resume analyses for future reference.

### 📄 PDF Report Generation
- Generate downloadable resume analysis reports.
- Structure results into readable sections using Jinja2 and WeasyPrint.

---

## 🛠️ Tech Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Frontend | Streamlit |
| Backend | FastAPI |
| NLP | spaCy |
| Semantic Similarity | Sentence Transformers |
| Embedding Model | all-MiniLM-L6-v2 |
| NLP Model | en_core_web_md |
| LLM Integration | Groq API (Llama 3) |
| Authentication | Supabase Auth |
| Database | Supabase |
| PDF Generation | WeasyPrint, Jinja2 |
| API Documentation | Swagger UI, OpenAPI |
| Development | Jupyter Notebook, Git, GitHub |

---

## 🏗️ System Architecture

CareerSync follows a modular frontend-backend architecture.

```text
             ┌─────────────────────────┐
             │        USER             │
             └────────────┬────────────┘
                          │
                          ▼
             ┌─────────────────────────┐
             │   Streamlit Frontend    │
             │                         │
             │ Resume Upload           │
             │ Job Description Input  │
             │ Analysis Dashboard      │
             └────────────┬────────────┘
                          │
                          ▼
             ┌─────────────────────────┐
             │     FastAPI Backend     │
             │                         │
             │ Resume Processing       │
             │ API Request Handling    │
             └────────────┬────────────┘
                          │
             ┌────────────┼────────────┐
             ▼            ▼            ▼
       ┌──────────┐ ┌───────────┐ ┌────────────┐
       │ spaCy    │ │ Sentence  │ │ Groq LLM   │
       │ NLP      │ │Transformers│ │            │
       │          │ │           │ │Suggestions │
       └────┬─────┘ └─────┬─────┘ └─────┬──────┘
            │             │             │
            └─────────────┼─────────────┘
                          ▼
             ┌─────────────────────────┐
             │   ATS Scoring Engine    │
             │                         │
             │ Semantic Matching      │
             │ Skill Validation       │
             │ Keyword Analysis       │
             │ Compatibility Scoring  │
             └────────────┬────────────┘
                          │
             ┌────────────┼────────────┐
             ▼                         ▼
       ┌─────────────┐          ┌─────────────┐
       │  Supabase   │          │ PDF Report  │
       │  Database   │          │ Generation  │
       └─────────────┘          └─────────────┘
                          │
                          ▼
             ┌─────────────────────────┐
             │   Analysis Dashboard    │
             │                         │
             │ ATS Score & Feedback    │
             │ Skill Gap Insights      │
             │ Improvement Suggestions │
             └─────────────────────────┘
```

---

## 🔍 How It Works

1. **Resume Upload:** Users upload their resumes in supported document formats.
2. **Information Extraction:** The backend processes resume content and extracts relevant information using NLP.
3. **Job Description Analysis:** The target job description is processed to identify important skills and requirements.
4. **Semantic Matching:** Sentence Transformers generate embeddings to evaluate contextual similarity between resume content and job requirements.
5. **ATS Evaluation:** The system evaluates resume compatibility across multiple scoring dimensions.
6. **AI Recommendations:** Groq LLM generates contextual feedback and improvement suggestions.
7. **Results & Reports:** Users receive their analysis results, can revisit saved analyses, and generate PDF reports.

---

## 📂 Project Structure

```text
CareerSync/
│
├── backend/
│   ├── main.py
│   ├── api/
│   ├── core/
│   ├── services/
│   └── ...
│
├── frontend/
│   ├── streamlit_app.py
│   ├── views/
│   ├── components/
│   └── ...
│
├── jupyter notebooks/
│   └── Research and dataset preparation
│
├── ml model/
│   └── Exported ML artifacts
│
├── requirements.txt
├── .env.example
├── .gitignore
└── README.md
```

---

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/CareerSync.git

cd CareerSync
```

### 2. Create a Virtual Environment

**Windows:**

```bash
python -m venv venv

venv\Scripts\activate
```

**Linux / macOS:**

```bash
python3 -m venv venv

source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Download the spaCy NLP Model

```bash
python -m spacy download en_core_web_md
```

### 5. Configure Environment Variables

Create a `.env` file using `.env.example` as a reference.

Configure the required credentials:

```env
SUPABASE_URL=your_supabase_url
SUPABASE_KEY=your_supabase_service_key
SUPABASE_ANON_KEY=your_supabase_anon_key

GROQ_API_KEY=your_groq_api_key
```

Configure the Streamlit secrets separately using the provided example:

```text
frontend/.streamlit/secrets.toml
```

Never commit API keys, service-role credentials, or private configuration files to GitHub.

### 6. Start the FastAPI Backend

Open a terminal and execute:

```bash
uvicorn backend.main:app --reload --host 0.0.0.0 --port 8000
```

Backend URL:

```text
http://localhost:8000
```

Interactive API Documentation:

```text
http://localhost:8000/docs
```

### 7. Start the Streamlit Frontend

Open another terminal:

```bash
streamlit run frontend/streamlit_app.py
```

Frontend URL:

```text
http://localhost:8501
```

---

## 🧪 Core Technical Concepts

| Concept | Application |
|---|---|
| Natural Language Processing | Resume information extraction and text processing |
| Semantic Similarity | Contextual resume-job description matching |
| Text Embeddings | Numerical representation of resume and job description content |
| Cosine Similarity | Measuring similarity between vector representations |
| Large Language Models | Generating contextual resume recommendations |
| REST API Development | Communication between frontend and backend |
| Authentication | Secure user access and session management |
| Database Integration | Persistent analysis history |
| Document Processing | Resume parsing and PDF report generation |

---

## 🎯 Project Objectives

- Improve resume-job description compatibility analysis.
- Reduce dependence on basic keyword-only matching.
- Apply NLP and transformer-based models to recruitment workflows.
- Provide explainable, actionable resume improvement insights.
- Demonstrate practical integration of AI models with production-oriented backend services.

---

## 🚀 Future Enhancements

- [ ] Resume optimization based on target job descriptions.
- [ ] Advanced skill-gap analysis and learning recommendations.
- [ ] Job recommendation engine based on candidate profiles.
- [ ] Support for additional resume formats.
- [ ] Resume version comparison and tracking.
- [ ] Expanded ATS evaluation metrics.
- [ ] Docker-based deployment.
- [ ] Enhanced analytics dashboard.

---

## 🔒 Security & Privacy

- Store sensitive credentials in environment variables.
- Never expose Supabase service-role credentials in client-side code.
- Keep `.env` and Streamlit secrets out of version control.
- Use authorized access to resume data and analysis history.

---

## 👨‍💻 Author

**Siddharth Gautam**

Computer Science & Engineering | AI/ML Enthusiast

- GitHub: https://github.com/SiddharthGautam282003
- LinkedIn: https://www.linkedin.com/in/siddharth-gautam-883539238

---

<p align="center">
  <b>CareerSync — Align Your Skills. Strengthen Your Career.</b>
</p>

<p align="center">
  ⭐ If you find this project interesting, consider giving the repository a star!
</p>
