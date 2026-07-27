# MetaHire — AI Mock Interview Practice Platform

An AI-powered platform for practicing job interviews. Users go through simulated interview sessions with voice-based answers, webcam-based proctoring, and an integrated code editor for technical rounds — then receive AI-generated, per-question feedback and scoring to help them improve.

## Features

- **Voice-based interview answers** — users speak their answers, captured via browser speech recognition
- **Webcam proctoring** — real-time person/phone detection during the session (flags if the candidate leaves frame or uses a phone) using a TensorFlow.js object-detection model
- **Multi-language code editor** — built-in code editor (CodeMirror) supporting JavaScript, Python, C++, and Java for technical interview questions
- **AI-generated feedback & scoring** — each answer is scored (0–10) with detailed feedback, powered by Google's Gemini AI
- **Interview history** — past sessions, scores, and feedback are saved and viewable per user
- **Resume & profile upload** — user can upload a resume and profile photo (stored via Cloudinary)
- **Authentication** — JWT-based signup/login with password reset via email (Nodemailer)

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React (Vite), Chakra UI, Radix UI, Tailwind CSS |
| Code Editor | CodeMirror (JS, Python, C++, Java support) |
| Voice Input | react-speech-recognition |
| Proctoring | TensorFlow.js (coco-ssd object detection) |
| AI Feedback | Google Generative AI (Gemini) |
| Backend | Node.js, Express.js |
| Database | MongoDB (Mongoose) |
| Auth | JWT, bcrypt |
| File Storage | Cloudinary (resumes, profile photos) |
| Email | Nodemailer (password reset) |

## How It Works

1. User signs up / logs in (JWT-based auth)
2. User starts an interview session, selecting role/company context
3. During the session: webcam monitors for proctoring, user answers via voice or writes code in the built-in editor for technical questions
4. Each answer is sent for AI evaluation, which returns a score and feedback
5. After the session, the user can review a full feedback breakdown per question and track history over time

## Local Setup

### Backend
```bash
cd Backend
npm install
cp .env.example .env
# set MONGODB_URI, JWT_SECRET, CLOUDINARY credentials, GEMINI_API_KEY, SMTP credentials
npm run dev
```

### Frontend
```bash
cd FrontEnd
npm install
npm run dev
```

## Screenshots

*(Add 2–3 screenshots — the live interview screen with webcam + code editor, and a feedback/score breakdown, are the strongest ones to lead with.)*

---

Built by [Anshul Sharma](https://www.linkedin.com/in/anshul-sharma0707) · [Portfolio](https://anshulsharmaportfolio.netlify.app/)
