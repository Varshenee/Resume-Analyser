# AI Resume Analyzer

An AI-powered cloud-native resume analysis platform that evaluates resumes for ATS (Applicant Tracking System) compatibility using Google Gemini AI.

The application automatically analyzes uploaded PDF resumes, generates ATS scores, provides personalized improvement suggestions, and visualizes analytics through Looker Studio using a fully serverless, event-driven architecture on Google Cloud Platform.
https://www.youtube.com/watch?v=3YgFpGqTN3k 

---

## Overview

In today's competitive job market, most resumes are filtered by Applicant Tracking Systems (ATS) before reaching recruiters. Many qualified candidates are rejected due to poor formatting, missing keywords, weak descriptions, or lack of measurable achievements.

This project automates resume evaluation using Artificial Intelligence and Google Cloud services to provide instant ATS feedback and actionable recommendations.

---

## Features

### AI-Powered Resume Analysis
- ATS compatibility scoring
- Resume quality evaluation
- AI-generated improvement suggestions
- Structured feedback using Gemini AI

### Cloud-Native Architecture
- Serverless processing
- Event-driven workflow
- Automatic trigger-based analysis
- Scalable cloud deployment

### Analytics Dashboard
- Resume score tracking
- ATS performance visualization
- Historical analysis
- Real-time reporting using Looker Studio

---

## System Architecture

```text
User Uploads Resume
        │
        ▼
Flask Web Application
        │
        ▼
Google Cloud Storage
        │
        ▼
Eventarc Trigger
        │
        ▼
Cloud Function
        │
        ▼
PDF Text Extraction (pdfplumber)
        │
        ▼
Gemini AI Analysis
        │
        ▼
BigQuery Storage
        │
        ├────────► Flask Results Dashboard
        │
        └────────► Looker Studio Analytics
```

---

## Technologies Used

| Category | Technology |
|-----------|------------|
| Frontend | HTML, CSS |
| Backend | Flask |
| Cloud Storage | Google Cloud Storage |
| Event Trigger | Eventarc |
| Serverless Processing | Cloud Functions |
| Deployment | Google Cloud Run |
| AI Model | Gemini 2.5 Flash |
| Database | BigQuery |
| Analytics | Looker Studio |
| PDF Processing | pdfplumber |

---

## APIs & Cloud Services

| API / Service | Purpose |
|---------------|---------|
| Gemini API | Resume evaluation and ATS scoring |
| Google Cloud Storage API | Resume file storage |
| BigQuery API | Analysis result storage and retrieval |
| Cloud Run API | Application deployment |
| Cloud Functions API | Serverless resume processing |
| Eventarc API | Event-driven trigger management |
| Looker Studio | Analytics dashboard and visualization |

---

## Workflow

### 1. Resume Upload
Users upload PDF resumes through the Flask web application.

### 2. Cloud Storage
The uploaded resume is stored in a Google Cloud Storage bucket.

### 3. Event Trigger
Eventarc detects the upload event and automatically triggers the processing service.

### 4. PDF Text Extraction
The resume text is extracted using the pdfplumber library.

### 5. AI Analysis
Gemini AI evaluates:
- Resume formatting and structure
- ATS keyword compatibility
- Skills relevance
- Education and experience alignment
- Projects and achievements

### 6. Result Storage
ATS scores and improvement suggestions are stored in BigQuery.

### 7. Dashboard Display
Results are displayed through:
- Flask ATS Dashboard
- Looker Studio Analytics Dashboard

---

## Key Challenges Solved

### Duplicate Event Processing
Cloud Storage occasionally triggered multiple processing events for the same file upload.

**Solution:**  
Implemented idempotency checks using BigQuery before processing resumes.

### API Quota Optimization
Repeated AI calls resulted in unnecessary Gemini API consumption.

**Solution:**  
Added duplicate detection logic to prevent repeated processing.

### Asynchronous Processing
Results could be requested before AI analysis completed.

**Solution:**  
Implemented a loading workflow before displaying ATS results.

---

## Screenshots

### Home Page
![Home Page](screenshots/home.png)

### Resume Upload
![Resume Upload](screenshots/upload.png)

### ATS Results Dashboard
![ATS Dashboard](screenshots/dashboard.png)

### BigQuery Results
![BigQuery](screenshots/bigquery.png)

### Looker Studio Analytics Dashboard
![Looker Studio](screenshots/looker-dashboard.png)

### Cloud Run Deployment
![Cloud Run](screenshots/cloud-run.png)

---

## Deployment

The application is deployed using Google Cloud Run and integrates multiple Google Cloud Platform services.

### Deployment Components
- Google Cloud Run
- Google Cloud Storage
- Eventarc
- Cloud Functions
- Gemini AI
- BigQuery
- Looker Studio

---

## Future Enhancements

- Job-role-specific ATS analysis
- Resume benchmarking and comparison
- User authentication and profiles
- Resume history tracking
- Recruiter dashboard
- Custom fine-tuned HR models
- Advanced analytics and reporting

---

## Learning Outcomes

This project demonstrates practical implementation of:

- Cloud Computing
- Serverless Architecture
- Event-Driven Systems
- Artificial Intelligence Integration
- Big Data Analytics
- Cloud Deployment
- Real-Time Processing Pipelines

---

## Authors

**Group 4**

- Anabha N N
- Anushka Das
- Varshenee Thiruvenkatam

---

## Project Highlights

- AI-Powered ATS Resume Analysis
- Google Gemini AI Integration
- Event-Driven Serverless Architecture
- Google Cloud Platform Deployment
- BigQuery Analytics Pipeline
- Looker Studio Reporting Dashboard
- Real-Time Resume Evaluation
- Cloud-Native Application Design
