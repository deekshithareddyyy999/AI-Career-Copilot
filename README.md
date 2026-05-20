# AI Career Copilot

> An intelligent career intelligence platform that analyzes resumes, identifies skill gaps, and generates personalized learning roadmaps to help you land your dream role in tech.

---

## Features

- **Resume Analysis** — Upload your PDF or DOCX resume and get instant skill extraction and gap analysis.
- **Skill Gap Report** — See exactly which skills you're missing for your target role with a quantified readiness score.
- **Learning Roadmap** — Receive a personalized step-by-step learning plan (4-week or 8-week) with curated courses, projects, and milestones.
- **Job Market Demand Analyzer** — Explore top in-demand skills for your chosen career role, categorized by demand level with visual charts.
- **Mock Interview** — Practice with role-specific multiple-choice questions and get instant scoring with detailed feedback.
- **Career Advice** — Get contextual career guidance from an AI assistant available throughout the app.
- **User Profile & History** — Track your analysis history, progress, and aggregate stats over time.

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | React 18 + TypeScript + Vite |
| Styling | Tailwind CSS + shadcn/ui |
| Animations | Framer Motion |
| Backend | Supabase (Auth, Postgres, Edge Functions) |
| AI | Gemini Flash / GPT models via edge functions |
| Charts | Recharts |
| Icons | Lucide React |

---

## Getting Started

### Prerequisites

- Node.js (v18+)
- npm or bun

### Installation

```bash
# Clone the repository
git clone <YOUR_GIT_URL>

# Navigate to the project directory
cd ai-career-copilot

# Install dependencies
npm install

# Start the development server
npm run dev
```

The app will be available at `http://localhost:5173`.

### Environment Variables

This project uses Supabase for backend services. Create a `.env` file in the root with the following:

```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_PUBLISHABLE_KEY=your_supabase_key
VITE_SUPABASE_PROJECT_ID=your_project_id
```

---

## Project Structure

```
src/
├── components/         # Reusable UI components & shadcn/ui
├── contexts/           # React contexts (Auth, etc.)
├── hooks/              # Custom React hooks
├── integrations/       # Supabase client & types
├── lib/                # Utility functions, data, parsers
├── pages/              # Route-level page components
├── App.tsx             # Main app with routing
└── main.tsx            # Entry point

supabase/
└── functions/          # Edge functions (AI prompts, mock interviews)
```

---

## Pages

| Route | Description |
|-------|-------------|
| `/` | Landing page with feature overview |
| `/upload` | Resume upload and analysis |
| `/dashboard` | Analysis results & skill gap report |
| `/learning-path` | Personalized learning roadmap |
| `/job-market` | Skill demand analyzer by role |
| `/mock-interview` | AI-powered MCQ practice test |
| `/profile` | User history & aggregate stats |
| `/about` | About the project |

---

## Backend (Python FastAPI)

A complementary Python backend is available for local development. It handles:

- Resume text extraction (PDF/DOCX)
- Skill extraction & gap analysis
- AI-powered roadmap generation

Refer to `BACKEND_SPEC.md` for setup instructions.

---

## Deployment

This project is built with Vite and can be deployed to any static hosting platform (Vercel, Netlify, Cloudflare Pages, etc.).

```bash
# Build for production
npm run build

# Preview production build locally
npm run preview
```

---

## License

MIT
