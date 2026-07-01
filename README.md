<div align="center">

# AI Resume Analysis & Job Tracking System

<br/>

[![Vercel](https://img.shields.io/badge/Frontend-Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://vercel.com/)
[![Render](https://img.shields.io/badge/Backend-Render-46E3B7?style=for-the-badge&logo=render&logoColor=black)](https://render.com/)
[![Cloudinary](https://img.shields.io/badge/Storage-Cloudinary-3448C5?style=for-the-badge&logo=cloudinary&logoColor=white)](https://cloudinary.com/)
[![pnpm](https://img.shields.io/badge/Managed_with-pnpm-F69220?style=for-the-badge&logo=pnpm&logoColor=white)](https://pnpm.io/)
[![Monorepo](https://img.shields.io/badge/Architecture-Monorepo-8B5CF6?style=for-the-badge&logo=turborepo&logoColor=white)](https://pnpm.io/workspaces)
[![GitHub Actions](https://img.shields.io/badge/CI/CD-GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)](https://github.com/features/actions)
[![Sentry](https://img.shields.io/badge/Monitoring-Sentry-362D59?style=for-the-badge&logo=sentry&logoColor=white)](https://sentry.io/)
<br/>
[![Vite](https://img.shields.io/badge/Vite_8-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev/)
[![shadcn/ui](https://img.shields.io/badge/shadcn%2Fui-000000?style=for-the-badge&logo=shadcnui&logoColor=white)](https://ui.shadcn.com/)
[![React](https://img.shields.io/badge/React_19-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://react.dev/)
[![Express](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)](https://www.mongodb.com/atlas)
<br/>
[![License](https://img.shields.io/badge/License-MIT-22C55E?style=for-the-badge)](./LICENSE)
[![Gemini AI](https://img.shields.io/badge/Gemini_2.5_Flash-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://aistudio.google.com/)
[![DeepSeek](https://img.shields.io/badge/DeepSeek_V3-FF6B35?style=for-the-badge&logo=openai&logoColor=white)](https://www.deepseek.com/)

<br/>

🧑‍💻 Production grade platform — 🚧 Actively under development — ⭐ Star the repo to follow the journey

</div>

---

## 🧐 The Problem

Job seekers today juggle multiple **disconnected tools** — one for **resume feedback**, another for **tracking job applications** and countless **resume templates** scattered across the internet. There is no single platform that seamlessly combines **AI-driven resume feedback**, **application tracking** and **resume inspiration** in one place. This platform eliminates the need to switch between multiple tools by bringing all these **essential features** together in a **single unified experience**.

## 💡 The Solution

This platform brings everything together:

- **Upload your resume** → Get instant AI-powered ATS scoring, keyword analysis and personalized interview questions
- **Track your applications** → Monitor status, set email reminders and view dashboard stats
- **Browse real resumes** → Learn from others, find inspiration and share your own

---

## ✨ Core Features

### 📄 AI-Powered Resume Checker

Upload your resume (PDF) and optionally paste a job description — the AI returns a full structured analysis:

| Section                     | What You Get                                                   |
| --------------------------- | -------------------------------------------------------------- |
| **Match Analysis**          | Strong / Partial / Weak verdict with missing keywords & issues |
| **Improvement Suggestions** | Actionable, specific tips to strengthen your resume            |
| **Interview Questions**     | 10–50 personalized questions based on your resume + JD         |
| **Analysis History**        | All past analyses saved — revisit anytime                      |
| **Works without JD**        | Analyze your resume on its own, no job description required    |

---

### 🌐 Resume Gallery

A community-driven space to share and discover resumes for inspiration:

- 📋 Browse a public grid of resumes with avatar + uploader name
- ❤️ Like resumes and filter by **Most Liked** or **Newest**
- 👤 Visit uploader profiles and see all their public resumes
- 🗑️ Delete your own upload — removes from both MongoDB **and** Cloudinary

---

### 📊 Job Application Tracker

Keep every application organized in one powerful dashboard:

- Track company, role, status, applied date, job URL, and notes
- **9 granular status stages:**

  | Status              | Icon |
  | ------------------- | ---- |
  | Applied             | 📝   |
  | Viewed              | 👀   |
  | Interview Scheduled | 📞   |
  | Technical Round     | 💻   |
  | HR Round            | 👔   |
  | Offer               | ✅   |
  | Rejected            | ❌   |
  | On Hold             | ⏸️   |
  | Withdrawn           | 🚫   |

- **Email reminders** — set a reminder for any interview (24h before, 1h before, or custom)
- **Dashboard stats** — total apps, monthly activity, interview rate, offer rate, rejection rate

---

### 🔐 Authentication

- **Email/Password** signup with email verification (re-send supported)
- **Google OAuth 2.0** — via `@react-oauth/google` (frontend) + `google-auth-library` (backend token verification)
- **Guest Mode** — try the AI Resume Checker without creating an account  
  _(Protected by IP-based rate limiting + Cloudflare Turnstile to prevent bot abuse)_

---

### 👤 User Profile

- Update name, email, and password
- Upload / change profile picture (JPG/PNG, max 2MB, stored on Cloudinary)
- Add optional social links: **LinkedIn**, **GitHub**, **Portfolio**

---

## 🛠️ Tech Stack

> This project goes well beyond a typical MERN stack application.

| Layer               | Technologies                                                                                                                                                 |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Frontend**        | React 19, React Compiler, Vite 8, TailwindCSS 4, shadcn/ui, React Router v7, TanStack Query v5, React Hook Form, Zod, Axios, React Hot Toast, Phosphor Icons |
| **Backend**         | Node.js, Express, JWT (Access + Refresh tokens), argon2, Multer, pdf-parse, Agenda.js                                                                        |
| **AI**              | Google Gemini 2.5 Flash (`gemini-2.5-flash`) — Primary · DeepSeek V3 (`deepseek-chat`) — Fallback                                                            |
| **Database**        | MongoDB Atlas + Mongoose (ODM)                                                                                                                               |
| **Storage**         | Cloudinary (profile images + resume PDFs)                                                                                                                    |
| **Email**           | Resend SDK (3,000 emails/month free)                                                                                                                         |
| **Testing**         | Vitest · React Testing Library · Supertest                                                                                                                   |
| **Monitoring**      | Sentry (5K errors/month free), Winston structured logging                                                                                                    |
| **CI/CD**           | GitHub Actions (lint + test on every push)                                                                                                                   |
| **Hosting**         | Vercel (Frontend) · Render (Backend) · UptimeRobot (keep-alive pings)                                                                                        |
| **Package Manager** | pnpm Workspaces (Monorepo)                                                                                                                                   |

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                      Frontend (React SPA)                   │
│       Vite · React 19 · TailwindCSS 4 · shadcn/ui          │
│    React Router v7 (library mode) · TanStack Query v5       │
└──────────────────────────┬──────────────────────────────────┘
                           │  HTTPS / REST API
                           ▼
┌─────────────────────────────────────────────────────────────┐
│                    Backend (Express API)                    │
│             Node.js · JWT · Helmet.js · Zod                 │
│          express-rate-limit · Multer · Agenda.js            │
│                  Route → Controller → Service → Model       │
│                     (API versioned at /api/v1/)             │
└────┬─────────────┬────────────────┬────────────────┬────────┘
     │             │                │                │
     ▼             ▼                ▼                ▼
MongoDB         Gemini 2.5      Cloudinary        Resend
Atlas           Flash API       (Storage)         (Email)
(Primary DB)    + DeepSeek V3
                (AI Fallback)
```

---

## 🔒 Security

Production-level security practices implemented throughout:

| Practice           | Implementation                                                                                                 |
| ------------------ | -------------------------------------------------------------------------------------------------------------- |
| Password Hashing   | **argon2** (memory-hard, stronger than bcrypt)                                                                 |
| Session Management | **JWT** with HttpOnly cookies (prevents XSS token theft)                                                       |
| Token Strategy     | **Access + Refresh token** rotation                                                                            |
| Input Validation   | **Zod** schemas on every route (frontend + backend)                                                            |
| Security Headers   | **Helmet.js** configured for production                                                                        |
| Rate Limiting      | **express-rate-limit** — tiered limits (5 req/15 min for auth users, strict IP limits for guests on AI routes) |
| File Safety        | **Multer** type/size restrictions (PDF only, max 5MB)                                                          |
| Bot Prevention     | **Cloudflare Turnstile** on Guest Mode AI access                                                               |
| Observability      | **Winston** structured auth logging — no passwords or tokens ever logged                                       |

---

## ⚙️ Key Engineering Decisions

<details>
<summary><strong>🧠 Why SHA-256 Caching for AI Responses?</strong></summary>

Calling the Gemini 2.5 Flash API costs real tokens and takes 2–5 seconds. If two users submit the same resume + job description (a very common scenario with popular templates), making two separate API calls is wasteful.

Before every AI call, the backend generates a `SHA-256` hash of `(resumeText + jobDescription)`. It first queries MongoDB for an existing record with that hash. If found → instant response (~50ms, zero cost). If not → call the AI, store the result with the hash for future reuse.

**Result:** Latency drops from ~5s → ~50ms for cache hits. Free-tier tokens are preserved.

</details>

<details>
<summary><strong>⏰ Why Agenda.js over node-cron for Email Reminders?</strong></summary>

`node-cron` is an in-memory scheduler — if the server restarts (Render's free tier does this after 15 min of inactivity), all scheduled jobs are **permanently lost**. You'd need to manually re-hydrate pending jobs from MongoDB on every boot.

`Agenda.js` stores jobs **natively in MongoDB**. On any restart, it automatically reconnects and resumes all pending reminders — zero manual recovery code needed. This is the architecturally correct choice for a server that restarts unpredictably.

</details>

<details>
<summary><strong>🤖 Why Dual AI Providers (Gemini + DeepSeek)?</strong></summary>

Gemini 2.5 Flash is the primary provider — excellent structured JSON output, strong reasoning, and Google's infrastructure reliability. However, AI APIs can experience rate limits or downtime.

`aiService.js` implements an **automatic fallback pattern**: try Gemini 2.5 Flash → if it fails/times out → retry with DeepSeek V3 → return result from whichever succeeds. Both providers are normalized to the same response shape, so the rest of the application is unaware of which provider was used. This ensures near-100% uptime for the core feature.

</details>

<details>
<summary><strong>📄 Why pdf-parse over pdfjs-dist?</strong></summary>

`pdfjs-dist` is Mozilla's full PDF **rendering engine** — designed to display PDFs visually in the browser. Using it on the server to extract text is like using a graphics engine to read a text file: it works, but carries unnecessary rendering complexity, a large bundle size, and browser-specific code.

`pdf-parse` is a lightweight, focused library built specifically for server-side text extraction. API: `pdf(buffer).then(data => data.text)` — one line, exactly what's needed. No rendering pipeline, no canvas dependency.

</details>

<details>
<summary><strong>🔑 Why React Router v7 in Library Mode (Not Framework Mode)?</strong></summary>

React Router v7's framework mode (the "Remix mode") handles SSR, bundling, and server actions — great for full-stack apps where the router is also the server. This project has a **dedicated Express backend** that already handles all business logic and database access.

Using library mode (`createBrowserRouter` + `RouterProvider`) gives robust, type-safe client-side routing as a pure SPA while keeping the frontend strictly decoupled from the backend. Framework mode would add SSR complexity with zero benefit.

</details>

<details>
<summary><strong>📦 Why pnpm Workspaces for a Monorepo?</strong></summary>

`pnpm` uses a **global content store with hard links** — packages are stored once and referenced everywhere, instead of being duplicated per project like npm/yarn. This saves significant disk space and speeds up installs.

`pnpm` also enforces a **strict non-flat node_modules** structure, preventing phantom dependencies — a common hidden-bug source with npm/yarn's flat structure where you can accidentally use packages you never explicitly declared.

The monorepo setup lets `client/` and `server/` share a single Git repo, unified scripts, and consistent tooling (ESLint, Prettier) without duplicating config.

</details>

---

## 🧪 Testing Strategy

| Layer               | Tool                           | Coverage                                          |
| ------------------- | ------------------------------ | ------------------------------------------------- |
| Backend API         | Supertest                      | Auth flow, resume upload, job CRUD                |
| Frontend Components | Vitest + React Testing Library | Form validation, protected routes, key components |
| Edge Cases          | Vitest                         | Empty PDFs, API failures, large files             |

> A dedicated test suite — even lean and well-targeted — sets this apart from the majority of portfolio projects.

---

## 🧑‍💻 Deployment

| Service            | Purpose                       | Free Tier                                |
| ------------------ | ----------------------------- | ---------------------------------------- |
| **Vercel**         | Frontend hosting (React SPA)  | Unlimited personal projects              |
| **Render**         | Backend hosting (Express API) | 750 hrs/month (sleeps after 15 min idle) |
| **UptimeRobot**    | Keep-alive pings every 10 min | 50 monitors free                         |
| **MongoDB Atlas**  | Database                      | 512 MB forever free                      |
| **Cloudinary**     | Media storage & CDN           | 25 GB/month free                         |
| **Resend**         | Email delivery                | 3,000 emails/month free                  |
| **Sentry**         | Error monitoring              | 5,000 errors/month free                  |
| **GitHub Actions** | CI/CD pipeline                | 2,000 min/month free                     |

> UptimeRobot pings the `/health` endpoint every 10 minutes, keeping Render awake so Agenda.js scheduled email reminders never miss a beat.

---

## 👨‍💻 About & Connect

I'm actively open to **Software Engineering** and **Full Stack Developer** roles. If you're a recruiter or founder looking for an engineer who ships complete, resilient, and user-focused products — let's talk.

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/YashMishra0101)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/yash-mishra-356280223/)
[![X](https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white)](https://x.com/YashRKMishra1)

</div>

---

<div align="center">
  <i>Built with passion for learning, job preparation and pushing the boundaries of what a portfolio project can be.</i>
  <br/><br/>
  <i> If this project inspires you, give it a star ⭐</i>
</div>
