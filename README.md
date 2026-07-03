# AdaptLearn — Adaptive Project Generator

An AI-powered tool that generates hands-on coding/learning projects personalized to a student's actual coursework — built for the **Principled AI Spark Challenge** hackathon.

## The Problem

AI has made it easier than ever to skip the practical, hands-on learning that turns classroom knowledge into real skill — while simultaneously raising the bar for what "practical experience" employers expect. Good grades alone don't build that experience.

## The Idea

AdaptLearn generates custom project ideas tailored not just to a student's general interests, but to their actual classwork and skill level — by combining their course syllabi and (optionally) Canvas submission history with an LLM that proposes, validates, and scaffolds a project brief around it. For privacy, only the student's own grades/submissions feed the model — teacher-authored material (assignment instructions, course content) outside the syllabus is explicitly excluded.

## Features

- **Dashboard** — overview of courses and active projects
- **Course Progress** — track progress against enrolled course programs
- **Project Hub / Library / Detail** — browse, generate, and manage personalized project briefs
- **Project Mentor / Mentor chat** — AI chat assistant (Groq-hosted Llama 3.3 70B) for project guidance
- **Deliverable Calendar** — export project milestones (`.ics` calendar export via `src/utils/ics.ts`)
- **PDF export** of project briefs (`jspdf`)
- Local-first data via **Dexie** (IndexedDB) — works without a backend server

## Tech Stack

React 18 · TypeScript · Vite · Tailwind CSS · Zustand · Dexie (IndexedDB) · React Router · Groq API (Llama 3.3 70B) · Framer Motion

## Setup

```bash
npm install
cp .env.example .env   # then add your own Groq API key
npm run dev
```

See [`docs/GROQ_SETUP.md`](docs/GROQ_SETUP.md) for detailed Groq API setup, troubleshooting, and security notes.

## Team

Built by **Team H2** for the Principled AI Spark Challenge hackathon:

| Name | Role |
|---|---|
| David Ekechukwu | Project Lead & Visionary |
| Michael Howell | Canvas/Database Backend Developer & Slides Creator |
| [Mohammed Tauseef Ahmed](https://github.com/taus-ahmed) | AI Engineer, Frontend Developer & Survey |
| [Nandana Vikraman](https://github.com/NandanaVikraman) | Website Design Lead, Frontend Developer & Data Analyst |

Full pitch deck: [`docs/Hackathon_Pitch_Deck.pdf`](docs/Hackathon_Pitch_Deck.pdf)

## What's Next

Ideas the team identified for extending this beyond the hackathon: broadening AI/dev-tool literacy assumptions so it's useful beyond technical majors, and deeper Canvas integration for automatically scoping projects around real assignment performance.
