# urWallet 💰

AI-powered personal expense tracking application with smart categorization and financial insights.

## Overview

urWallet helps you track expenses, set budgets, and get AI-powered insights about your spending habits.

| Feature | Description |
|---------|-------------|
| 📊 **Dashboard** | View expenses, savings, and investments at a glance |
| 🤖 **AI Categorization** | Automatic transaction categorization using Groq AI |
| 💡 **AI Insights** | Monthly spending analysis and recommendations |
| ⚠️ **Spike Detection** | Alerts when spending increases significantly |
| 🔐 **Supabase Auth** | Secure authentication with Google Sign-In |
| 🌙 **Dark/Light Mode** | Theme customization |
| 💵 **Multi-Currency** | Select currency per transaction (9 currencies supported) |

## Architecture

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│                 │     │                 │     │                 │
│    Frontend     │────▶│    Backend      │────▶│   PostgreSQL    │
│    (React)      │     │   (FastAPI)     │     │                 │
│                 │     │                 │     │                 │
└────────┬────────┘     └────────┬────────┘     └─────────────────┘
         │                       │
         │                       │
         ▼                       ▼
┌─────────────────┐     ┌─────────────────┐
│    Supabase     │     │     Groq AI     │
│ Authentication  │     │   (LLaMA 3.3)   │
└─────────────────┘     └─────────────────┘
```

## Repositories

| Repository | Description | Tech Stack |
|------------|-------------|------------|
| [**urwallet-backend**](https://github.com/rxhuljoshi/urwallet-backend) | REST API server | FastAPI, PostgreSQL, Supabase |
| [**urwallet-frontend**](https://github.com/rxhuljoshi/urwallet-frontend) | Web application | React 19, TailwindCSS, shadcn/ui |

## Quick Start

### Prerequisites

- Docker & Docker Compose
- Supabase project with Authentication enabled
- (Optional) Groq API key for AI features

### Clone with Submodules

```bash
git clone --recurse-submodules https://github.com/rxhuljoshi/urWallet.git
cd urWallet
```

### Setup

```bash
# Backend setup
cd backend
cp .env.example .env
# Add your Firebase credentials and Groq API key to .env

# Frontend setup
cd ../frontend
cp .env.example .env
# Add your Firebase config to .env
```

### Run with Docker

```bash
# Start backend (PostgreSQL + API)
cd backend
docker-compose up -d

# Start frontend
cd ../frontend
docker-compose up -d
```

| Service | URL |
|---------|-----|
| Frontend | http://localhost:3000 |
| Backend API | http://localhost:8000 |
| API Docs | http://localhost:8000/docs |

## Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | React 19, TailwindCSS, shadcn/ui, Recharts |
| Backend | Python FastAPI, SQLAlchemy (async) |
| Database | PostgreSQL |
| Auth | Supabase Authentication |
| AI | Groq (LLaMA 3.3 70B) |
| Container | Docker, Docker Compose |
| Web Server | Nginx (production) |

## License

MIT

---

**Made with ❤️ by [rxhuljoshi](https://github.com/rxhuljoshi)**
