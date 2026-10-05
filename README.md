# 🤖 AI Career Guidance Platform

An **AI-powered Career Guidance Platform** designed to help students and early-career software professionals identify suitable career roles based on their **skills, experience, academic background, and career goals**.

The platform brings multiple career-support features into a single profile-driven workspace, providing personalized career recommendations and role-fit scores.

---

## 🚀 Features

### ✅ Career Advisor

* Analyzes user skills and experience.
* Recommends suitable career roles.
* Provides comparative **fit scores**.
* Identifies matching skills.
* Suggests skills that users can improve.

### 🔐 User Authentication

* User registration.
* User login.
* Authentication validation.
* JWT-based access flow.
* Duplicate email validation.
* Invalid password handling.

### 📄 Resume Analyzer

**Planned Feature**

* Resume parsing using NLP.
* Skill and entity extraction.
* ATS optimization suggestions.
* Identification of missing keywords.

### 🎤 Interview Simulator

**Planned Feature**

* AI-based mock interviews.
* Role-specific questions.
* Conversational interview sessions.
* Feedback on answers and communication.

### 📚 Learning Roadmaps

**Planned Feature**

* Personalized learning paths.
* Skill-gap based recommendations.
* Learning milestones.
* External learning resource integration.

### 🧑‍💻 AI Mentor

**Planned Feature**

* AI-powered technical guidance.
* Personalized project suggestions.
* Technical question answering.

### 📊 Market & Salary Insights

**Planned Feature**

* Technology hiring trends.
* Regional salary information.
* Career market insights.

---

## 🏗️ System Architecture

```text
┌──────────────────────────────┐
│        User Browser          │
│      React / Next.js         │
└──────────────┬───────────────┘
               │
               │ JSON / HTTPS
               ▼
┌──────────────────────────────┐
│       FastAPI Backend        │
│        Python REST API       │
└──────────────┬───────────────┘
               │
       ┌───────┴────────┐
       │                │
       ▼                ▼
┌──────────────┐  ┌───────────────┐
│ AI Provider  │  │  PostgreSQL   │
│ Gemini/Claude│  │ Prisma ORM    │
└──────────────┘  └───────────────┘
```

The architecture separates the frontend, backend API, AI provider, and database into independent layers, allowing the underlying AI provider to be changed without redesigning the frontend or database.

---

## 🛠️ Technology Stack

| Technology                  | Purpose                 |
| --------------------------- | ----------------------- |
| **Python**                  | Backend development     |
| **FastAPI**                 | REST API development    |
| **React / Next.js**         | Frontend interface      |
| **Tailwind CSS**            | UI styling              |
| **PostgreSQL**              | Database                |
| **Prisma ORM**              | Database management     |
| **Artificial Intelligence** | Career recommendations  |
| **Gemini / Claude**         | AI provider integration |
| **JWT**                     | Authentication          |

The project report identifies Python, FastAPI, modern client components, PostgreSQL/Prisma, and provider-agnostic AI integration as core technologies.

---

## 📂 Project Structure

```text
AI-Career-Guidance-Platform/
│
├── frontend/
│   ├── components/
│   ├── pages/
│   ├── public/
│   └── package.json
│
├── backend/
│   ├── main.py
│   ├── api/
│   ├── models/
│   ├── services/
│   └── requirements.txt
│
├── prisma/
│   └── schema.prisma
│
├── README.md
└── .env.example
```

> The exact folder structure may vary depending on the implementation of the project.

---

## 🔑 Career Recommendation API

### Endpoint

```text
POST /api/v1/advisor/recommend
```

### Example Request

```json
{
  "user_id": "user123",
  "skills": [
    "Python",
    "Pandas",
    "SQL"
  ],
  "experience_years": 1
}
```

### Example Response

```json
[
  {
    "role_title": "Data Analyst",
    "fit_score": 91,
    "matching_skills": [
      "Python",
      "Pandas",
      "SQL"
    ]
  }
]
```

The report's API implementation uses `ProfileSchema` for user skills and experience and returns role title, fit score, and matching skills.

---

## 📊 Example Career Recommendations

| Career Role               |  Fit Score | Matching Skills          |
| ------------------------- | ---------: | ------------------------ |
| Data Analyst              | **91/100** | Python, Pandas, SQL      |
| Machine Learning Engineer | **78/100** | Python, Machine Learning |
| Backend Developer         | **66/100** | FastAPI, SQL             |

Example recommendations in the project include learning **Power BI/Business Intelligence** for Data Analyst, **PyTorch, Deep Learning and MLOps** for ML Engineer, and **Node.js, System Design and Docker** for Backend Developer.

---

## 🗄️ Database

The project uses **PostgreSQL** with **Prisma ORM**.

Main database models include:

```text
User
 │
 └── Profile
       │
       └── Recommendations
```

The `User` model stores account information, the `Profile` model stores skills and experience, and the `Recommendation` model stores recommended roles and fit scores.

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/AI-Career-Guidance-Platform.git
```

### 2. Navigate to the project

```bash
cd AI-Career-Guidance-Platform
```

### 3. Install backend dependencies

```bash
cd backend
pip install -r requirements.txt
```

### 4. Start the FastAPI server

```bash
uvicorn main:app --reload
```

The API will be available locally through the FastAPI development server.

### 5. Install frontend dependencies

```bash
cd ../frontend
npm install
```

### 6. Start the frontend

```bash
npm run dev
```

---

## 🔐 Environment Variables

Create a `.env` file and configure the required values:

```env
DATABASE_URL="postgresql://username:password@localhost:5432/career_guidance"

AI_API_KEY="your-api-key"

JWT_SECRET="your-secret-key"
```

**Do not upload your `.env` file or API keys to GitHub.**

Add this to `.gitignore`:

```text
.env
node_modules/
__pycache__/
*.pyc
```

---

## 🧪 Testing

The authentication system was tested for:

* ✅ Valid registration
* ✅ Duplicate email
* ✅ Correct login
* ✅ Invalid password

The project report records all four authentication scenarios as passed.

---

## 🎯 Project Objectives

1. Create a unified profile and career dashboard.
2. Implement user authentication.
3. Develop an AI Career Advisor.
4. Generate career-role recommendations.
5. Provide role-fit scores.
6. Identify skill gaps.
7. Create a scalable backend architecture.
8. Support future AI-powered career services.

---

## 🔮 Future Development

The planned development roadmap includes:

* 📄 Automated PDF resume analysis.
* 🎤 AI conversational mock interviews.
* 📚 Dynamic personalized learning roadmaps.
* 🔐 OAuth2 social login.
* 🐳 Docker-based deployment.
* ☁️ Cloud deployment.
* 📊 Real-time market and salary insights.

These features are identified as future development horizons in the project report.

---

## 👨‍💻 Developer

**SIBINESH J**

B.Tech – Artificial Intelligence & Data Science

J.N.N Institute of Engineering

Internship Project – **AI Career Guidance Platform**

Internship Organization: **Aura Institute of Software Technology**

---

## 📜 Project Information

**Project:** AI Career Guidance Platform
**Internship Duration:** 3 August 2026 – 17 August 2026
**Technology Domain:** Artificial Intelligence & Data Science
**Backend:** Python + FastAPI
**Database:** PostgreSQL + Prisma
**Frontend:** React / Next.js

The project was developed as part of a 15-day internship focused on Python with AI applications, RESTful services, and responsive frontend components.

---

## ⭐ Acknowledgement

This project was developed during an internship at **Aura Institute of Software Technology** with guidance and technical support throughout the internship.

---

## 📄 License

This project is intended for **educational and academic purposes**.
