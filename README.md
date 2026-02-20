# 🤖 TalentAI - AI-Powered Recruitment System

A full-stack AI recruitment platform that automates candidate screening through resume analysis, skill quizzes, text interviews, and video interviews.

---

## ✨ Features

- **ATS Resume Analysis** — Upload PDF, DOCX, or TXT resumes and get an AI-powered score with project insights
- **Skill Quiz** — Auto-generated technical questions based on the job role
- **Text Interview** — Conversational AI interview with real-time scoring
- **Video Interview** — Record and analyze candidate video responses
- **Subscription Plans** — Basic ($29), Premium ($79), and Pro ($199) tiers
- **Recruiter Dashboard** — View and manage all candidates in one place
- **Multi-AI Support** — Works with Google Gemini, OpenAI GPT-4, or Anthropic Claude
- **Cloud Storage** — Optional Google Cloud Storage for resumes and videos

---

## 🗂 Project Structure

```
talentai/
├── frontend/          # React app (Create React App + Tailwind CSS)
│   ├── public/
│   │   └── index.html
│   ├── src/
│   │   ├── App.js         # Main application component
│   │   ├── App.css        # Custom styles
│   │   ├── index.js       # React entry point
│   │   └── index.css      # Tailwind imports
│   ├── tailwind.config.js
│   └── package.json
│
├── backend/           # Node.js / Express API server
│   ├── server.js          # Main server file
│   ├── .env.example       # Environment variable template
│   └── package.json
│
├── .gitignore
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

- Node.js v18 or higher
- npm or yarn
- A Google Gemini API key (free at [makersuite.google.com](https://makersuite.google.com/))

---

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/talentai.git
cd talentai
```

---

### 2. Set up the Backend

```bash
cd backend
npm install
```

Create your environment file:

```bash
cp .env.example .env
```

Open `.env` and fill in your values — at minimum, set `JWT_SECRET` and `GOOGLE_GEMINI_API_KEY`.

Start the backend server:

```bash
npm start        # production
npm run dev      # development (with auto-reload via nodemon)
```

The API will run on **http://localhost:3001**

---

### 3. Set up the Frontend

```bash
cd ../frontend
npm install
npm start
```

The React app will open at **http://localhost:3000**

---

## 🔑 Environment Variables

See `backend/.env.example` for the full list. Key variables:

| Variable | Description |
|---|---|
| `JWT_SECRET` | Secret key for signing auth tokens |
| `AI_PROVIDER` | `gemini` (default), `openai`, or `claude` |
| `GOOGLE_GEMINI_API_KEY` | Your Gemini API key |
| `OPENAI_API_KEY` | Your OpenAI key (if using OpenAI) |
| `GOOGLE_CLOUD_PROJECT_ID` | GCP project ID (optional) |
| `GOOGLE_CLOUD_BUCKET_NAME` | GCS bucket name (optional) |

---

## 🌐 Deployment

### Frontend → Vercel / Netlify
```bash
cd frontend
npm run build
# Upload the build/ folder to Vercel or Netlify
```

### Backend → Railway / Render / Heroku
Point your platform to the `backend/` directory and set all environment variables through the platform's dashboard.

---

## 🛠 Tech Stack

**Frontend:** React 18, Tailwind CSS, Lucide Icons  
**Backend:** Node.js, Express, Multer, JWT, bcrypt  
**AI:** Google Gemini Pro / OpenAI GPT-4 / Anthropic Claude  
**Storage:** Local filesystem or Google Cloud Storage  

---

## 📄 License

MIT License — free to use and modify.
