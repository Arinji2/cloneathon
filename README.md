# Theo Clonathon

## Starting the Database & Redis with Docker

This project uses **PostgreSQL** for the database and **Redis** for caching.  
The simplest way to get started is with Docker:

```bash
docker compose up -d
```

If you ever need to reset your local DB and Redis from scratch (⚠️ this erases all data), run:

```bash
docker compose down -v
```

---

## Install Dependencies

Make sure you have [pnpm](https://pnpm.io/) installed (or an equivalent installed) Then, run:

```bash
pnpm install
```

---

## Environment Setup

Create a `.env.local` file in your project root (next to `package.json`) and add the following:

```env
# PostgreSQL
POSTGRES_URL='postgresql://nextjsuser:nextjspassword@localhost:5432/clonathon'

# Redis
REDIS_URL='redis://localhost:6379'

# Google Generative AI API
GOOGLE_GENERATIVE_AI_API_KEY=your-api-key
```

You can get a free API key for the Google Generative AI API from:  
 https://aistudio.google.com/

---

## Running Migrations

Once your database is up, apply migrations using:

```bash
pnpm db:migrate
```

---

## Starting the Dev Server

To run the app locally:

```bash
pnpm dev
```
