# FitFlow Redesign - System Architecture & Engineering Foundation

## 📌 Project Overview
FitFlow is a health and fitness mobile tracking platform redesigned to solve severe user retention drop-off through human-centered engineering. Key features include:
- **AI-Powered Adaptive Workout Plans ("Daily Flow")**
- **Camera-Based Nutrition Logging (Computer Vision)**
- **Private Social Accountability Circles**

This repository hosts the multi-service system architecture, engineering specifications, and architectural artifacts developed for **IT3060: Human-Computer Interaction (SLIIT)**.

---

## 🏗️ Project Directory Structure

```text
fitflow-redesign/
├── .github/
│   └── workflows/
│       └── ci.yml             # CI/CD automated build & verification pipeline
├── frontend/                  # React Native mobile client (iOS & Android)
│   └── package.json
├── backend/                   # Node.js + Express API Gateway & core services
│   └── package.json
├── ai-service/                # Python + FastAPI computer vision & ML engine
│   └── requirements.txt
├── docs/                      # Technical reports, matrices, & architecture diagrams
│   ├── architecture/
│   │   ├── architecture-diagram.png
│   │   └── comparison-matrix.md
│   └── adrs/
│       └── adr-001.md
├── .gitignore
└── README.md
🚀 Recommended Technology Stack (Stack A)
Layer    Technology    Justification
Mobile Frontend    React Native (TypeScript)    ~85–90% code reusability across iOS/Android; 60 FPS workout animations via Fabric & Reanimated.
API Gateway / Core    Node.js + Express    High concurrency event loop; rapid MVP iteration; shared TypeScript data models with mobile.
AI Microservice    Python + FastAPI    Native integration with TensorFlow Lite, OpenCV, and PyTorch for meal image classification.
Primary Database    PostgreSQL    Strict ACID transactions, Row-Level Security (RLS), and GDPR compliance for sensitive health logs.
Real-time Layer    Firebase Firestore    Low-latency social circles, real-time community challenges, and active leaderboards.
Authentication    Firebase Auth    Turnkey OAuth (Google/Apple), MFA, and secure JWT verification with minimal maintenance.
🛠️ Local Development Setup
1. Frontend (Mobile Client)
code
Bash
cd frontend
npm install
npm start
2. Backend (Core API)
code
Bash
cd backend
npm install
npm run dev
3. AI Service (Computer Vision & Recommendations)
code
Bash
cd ai-service
pip install -r requirements.txt
python app.py
