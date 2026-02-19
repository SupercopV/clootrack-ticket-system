# clootrack-ticket-system

# 🎫 AI-Powered Support Ticket Classification System

A full-stack support ticket management system with **AI-based auto-classification**, built using **React, Django, PostgreSQL, Docker, and OpenAI**.

The system automatically classifies support tickets into category and priority using an LLM, and provides a modern dashboard for managing ticket lifecycle and analytics.

---

# 🚀 Features

## 🎟 Ticket Management

* Create support tickets
* AI auto-classification (category & priority)
* Change ticket status (Open ↔ Closed)
* Delete tickets
* Search tickets
* Filter by category & priority

## 🤖 AI Classification

The system analyzes ticket description and predicts:

* Category → billing, technical, account, general
* Priority → low, medium, high, critical

## 📊 Dashboard

* Total tickets
* Open tickets
* Avg tickets per day
* Priority breakdown

## 🎨 Modern UI

* Card-based layout
* Color-coded badges
* Animated ticket cards
* Responsive dashboard

---

# 🏗 Tech Stack

**Frontend**

* React
* Axios
* Framer Motion
* CSS

**Backend**

* Django
* Django REST Framework
* PostgreSQL
* OpenAI API

**DevOps**

* Docker
* Docker Compose

---

# 🤖 LLM Used

**Model:** OpenAI GPT
**Purpose:** Ticket classification

### Why this model?

* Strong text understanding
* Accurate classification for short descriptions
* Fast API response suitable for real-time UX
* Easy integration with Python backend

The model converts free-text ticket descriptions into structured fields:

```
description → category + priority
```

---

# ⚙️ Design Decisions

### 1️⃣ AI-assisted classification

Instead of rule-based keywords, an LLM was used to:

* Handle ambiguous descriptions
* Improve classification accuracy
* Simulate real SaaS automation workflows

### 2️⃣ RESTful backend

Django REST Framework chosen for:

* Clean API structure
* Serializer validation
* Rapid development

### 3️⃣ Dockerized architecture

Entire app runs via:

```
docker compose up --build
```

This ensures:

* Reproducibility
* Easy reviewer setup
* No local dependency issues

### 4️⃣ PostgreSQL database

Used instead of SQLite to reflect production-ready architecture.

### 5️⃣ Modern React UI

Implemented:

* Search & filters
* Status actions
* Animated cards
* Dashboard stats

This mimics real customer-support products.

---

# 📂 Project Structure

```
clootrack-ticket-system/
│
├── backend/
│   ├── project/
│   ├── tickets/
│   ├── requirements.txt
│   └── Dockerfile
│
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── Dockerfile
│
├── docker-compose.yml
├── .env
└── README.md
```

---

# 🐳 Setup & Run

## 1️⃣ Add Environment Variable

Create `.env` in project root:

```
OPENAI_API_KEY=your_openai_key_here
```

(API key is NOT hardcoded per instructions)

---

## 2️⃣ Run Entire App

```
docker compose up --build
```

This starts:

* PostgreSQL
* Django backend
* React frontend

---

# 🌐 Access

Frontend → http://localhost:3000
Backend → http://localhost:8000

---

# 🧪 API Endpoints

## Tickets

* `GET /api/tickets/`
* `POST /api/tickets/create/`
* `PATCH /api/tickets/{id}/status/`
* `DELETE /api/tickets/{id}/delete/`

## AI

* `POST /api/tickets/classify/`

## Stats

* `GET /api/tickets/stats/`

---

# 🤖 AI Example

**Input**

```
"My payment failed but amount deducted"
```

**Output**

```
Category: billing
Priority: high
```

---

# 📊 Screenshots

<img width="1919" height="901" alt="Screenshot 2026-02-19 121050" src="https://github.com/user-attachments/assets/5230adb2-74b4-4200-a8a4-44f8cb3fedf4" />

<img width="1919" height="884" alt="Screenshot 2026-02-19 121129" src="https://github.com/user-attachments/assets/11f348dd-a714-4743-a796-54ffff80ec52" />

<img width="1906" height="409" alt="Screenshot 2026-02-19 121145" src="https://github.com/user-attachments/assets/df2abce8-12ea-4a86-a0f4-f79e7b09af95" />




---

# 🧑‍💻 Author

**Vamshi Bayagani**
AI & Full-Stack Developer

---

# 📄 License

MIT
