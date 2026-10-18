# 🏛️ MyZone – SFRC360
### AI-Enabled Digital Campus Platform
**One Platform. Every Campus Service. Powered by AI.**

> Developed for The Standard Fireworks Rajaratnam College for Women (Autonomous), Sivakasi  
> Affiliated with Madurai Kamaraj University

MyZone – SFRC360 is a digital campus management platform designed to bring academic services, institutional information, and campus resources together in one unified environment.

The platform features role-based portals for students, faculty, parents, and administrators, alongside **Pragya AI**, a conversational campus assistant designed to simplify access to college-related information.

By combining campus management with AI-assisted information access, MyZone aims to make institutional services more accessible, organized, and efficient.

---

## ✨ Key Features

### 🎓 1. Student Portal
A centralized space for students to access academic information and campus services.

- Attendance and examination details.
- Internal assessment marks and academic performance.
- Timetables, course materials, and learning resources.
- Placement information and student activities.
- Campus facilities and transportation details.
- Institutional announcements and notifications.

### 👩‍🏫 2. Faculty Portal
Tools to support academic activities and faculty-related information management.

- Student attendance management.
- Internal assessment and marks entry.
- Academic resources and learning material management.
- Student mentorship information.
- Research and publication-related information.

### 👨‍👩‍👧 3. Parent Portal
A dedicated interface for parents to stay informed about academic progress.

- Attendance monitoring.
- Academic performance and examination information.
- College announcements and event updates.
- Relevant student-related notifications.

### 🛡️ 4. Administrative Portal
A centralized interface for managing institutional information and campus operations.

- User and department management.
- Academic and institutional data management.
- Campus services, events, and notifications.
- Role-based access management.
- Administrative monitoring and audit records.

### 🤖 5. Pragya AI — Campus Digital Assistant

**Pragya AI is the conversational intelligence component of MyZone.**

It is designed to help users find college-related information through natural-language queries.

Key areas of assistance include:

- Admissions and academic departments.
- Faculty information.
- Fee-related queries.
- Transportation information.
- Ph.D. guidance.
- Institutional contact details.

#### AI Architecture

The assistant can combine structured information lookup with semantic retrieval to provide relevant responses.

**Conceptual workflow:**

`User Query -> Query Processing -> Information Retrieval -> Response Generation`

Where implemented, **Retrieval-Augmented Generation (RAG)** can connect a language model with relevant institutional information to support context-aware answers.

### 🏫 6. Campus Services
- College events and student activities.
- Campus facilities and resources.
- Transportation information.
- Institutional announcements and updates.

### 🔐 7. Security and Access Control
- User authentication.
- Role-based authorization.
- Role-specific access restrictions.
- Controlled access to institutional information.
- Audit logging and data integrity support.

---

## 🛠️ Technology Stack

The following technologies represent the project's intended or reported stack. Retain each item only if it is present in, or actively used by, the codebase.

| Layer | Technology |
|---|---|
| Frontend | Next.js, React, TypeScript |
| UI Styling | Tailwind CSS, Lucide Icons |
| Backend | Python, FastAPI |
| Database | PostgreSQL, Supabase |
| Authentication | Supabase Auth |
| Vector Search | pgvector |
| AI Integration | LLM APIs, Retrieval-Augmented Generation (RAG) |
| Testing | Pytest, Playwright |
| Development Tools | Git, GitHub |

---

## 🏗️ System Architecture

MyZone follows a modular architecture that separates the user interface, backend services, institutional data, and AI-assisted information retrieval.


### Application Workflow

```text
User
  ↓
Role-Based Portal
  ↓
Backend API
  ↓
Database and Campus Services

```

## 📁 Repository Structure

```
SFRC-Student-Portal/
├── myzone-sfrc360/             # Next.js 16 Production Frontend Application
│   ├── app/                    # App Router (Student, Faculty, Parent, Admin portals)
│   ├── components/             # Reusable UI components, layout shell & Pragya AI Drawer
│   ├── lib/                    # Supabase client, API clients, authentication & hooks
│   └── public/                 # Static assets, branding logos, mascot animations & manifest
├── backend/                    # FastAPI High-Performance Backend Application
│   ├── app/
│   │   ├── ai/                 # Pragya AI Service, multi-turn resolver & providers
│   │   ├── api/                # REST API routers & endpoints (v1)
│   │   ├── core/               # Database engine, JWT authentication & audit logging
│   │   ├── models/             # SQLAlchemy ORM models & database schemas
│   │   ├── rag/                # Document chunking, embedding generation & retrieval
│   │   └── tests/              # Automated backend test suites
│   └── requirements.txt        # Python backend dependencies
├── SFRC_Assist/                # Standalone Institutional Assistant & Reference SQLite DB
├── Images/                     # College emblems, crests, and identity graphics
├── .gitignore                  # Git ignore rules for clean repository state
└── README.md                   # Project documentation
```

---

## 🚀 Getting Started Locally

### 1. Frontend Setup (`myzone-sfrc360`)
```bash
cd myzone-sfrc360
npm install
npm run dev
```
*Frontend runs at `http://localhost:3000`*

### 2. Backend Setup (`backend`)
```bash
cd backend
python -m venv venv
venv\Scripts\activate          # On Windows
pip install -r requirements.txt
uvicorn app.main:app --host 0.0.0.0 --port 8000 --reload
```
*Backend API runs at `http://localhost:8000` with Swagger docs at `http://localhost:8000/docs`*

---

## 📄 License & Credits
Developed for **The Standard Fireworks Rajaratnam College for Women, Sivakasi**.  
All rights reserved © 2026.
