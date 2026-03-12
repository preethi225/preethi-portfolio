# 🌐 Preethi — Personal Portfolio Website

A single-page portfolio website built with **HTML/CSS/JavaScript** (frontend), **Node.js + Express** (backend), and **MongoDB Atlas** (cloud database). Deployed globally on **Render.com**.

![CI Pipeline](https://github.com/preethi225/preethi-portfolio/actions/workflows/main.yml/badge.svg)

---

## 🔗 Live Demo
👉 **[https://preethi-portfolio-ve5z.onrender.com](https://preethi-portfolio-ve5z.onrender.com)**

---

## 📁 Project Structure

```
preethi-portfolio/
├── public/
│   └── index.html        ← Frontend (single page portfolio)
├── .github/
│   └── workflows/
│       └── ci.yml        ← CI/CD Pipeline (GitHub Actions)
├── server.js             ← Backend (Node.js + Express)
├── package.json          ← Dependencies
├── .env.example          ← Environment variables template
├── .gitignore
└── README.md
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | HTML5, CSS3, Vanilla JavaScript |
| Backend | Node.js, Express.js |
| Database | MongoDB Atlas (cloud) |
| Hosting | Render.com |
| Version Control | GitHub |
| CI/CD Pipeline | GitHub Actions |

---

## ✨ Features

- Responsive single-page portfolio
- Smooth scroll animations
- Contact form that saves messages to MongoDB
- REST API (`POST /api/contact`, `GET /api/contact`)
- GitHub Actions pipeline runs on every push
- Globally deployed (accessible from anywhere)

---

## 🚀 How to Run Locally

### Prerequisites
- Node.js v18+
- MongoDB Atlas account (free tier)

### Steps

```bash
# 1. Clone the repository
git clone https://github.com/preethi225/preethi-portfolio.git
cd preethi-portfolio

# 2. Install dependencies
npm install

# 3. Create .env file
cp .env.example .env
# Edit .env and add your MongoDB URI

# 4. Start the server
npm start

# 5. Open in browser
# Visit: http://localhost:3000
```

---

## 🌍 Deployment (Render.com)

1. Push code to GitHub
2. Go to [render.com](https://render.com) → New Web Service
3. Connect your GitHub repo
4. Set environment variable: `MONGO_URI = your_mongodb_atlas_uri`
5. Build command: `npm install`
6. Start command: `npm start`
7. Deploy!

---

## 📡 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/contact` | Save a contact message |
| GET | `/api/contact` | Retrieve all messages |
| GET | `/api/health` | Server health check |

---

## 👩‍💻 Author

**Preethi** — BCA CS Student specialization in CLOUD COMPUTING , 2025 Batch  
GitHub: [@preethi225](https://github.com/preethi225)

---

## 📋 Project Workflow

```
Local Dev → Git Commit → GitHub (Public Repo) → CI Pipeline (GitHub Actions) → Render.com Hosting → Live on Web Browser
```

This follows the Modern Web Development Workflow:
**Local Git → GitHub → CI/CD → Hosting → Web Browser** ✅
