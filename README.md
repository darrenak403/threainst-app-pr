# StreamMatch — Dating & Video Chat App

A small demo dating app built with Next.js, Supabase (Auth + Postgres), and Stream (chat & video). It includes profile management, matching, real-time chat and optional video calls.

<!-- Add a screenshot of the app below -->

![StreamMatch screenshot](./screenshots/placeholder.svg)


The placeholder image `screenshots/placeholder.svg` is included as a starting point.

## Quick Start

1. Install dependencies:

```bash
npm ci
```

2. Create `.env.local` in the project root and add required environment variables (see below).

3. Run the dev server:

```bash
npm run dev
```

4. Open http://localhost:3000

## Environment Variables

Create a `.env.local` file with at least the following:

```bash
NEXT_PUBLIC_APP_URL=http://localhost:3000
NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
SUPABASE_SERVICE_ROLE_KEY=your_supabase_service_role_key
NEXT_PUBLIC_STREAM_API_KEY=your_stream_api_key
STREAM_API_SECRET=your_stream_api_secret
```

Get Supabase keys from your Supabase project Settings → API. Get Stream keys from the Stream dashboard.

> Note: `.env.local` is ignored by git. Add secrets to your hosting provider (Vercel/GitHub Actions) when deploying.

## Deploy

This app requires server-side features (authentication, database). Deploy to Vercel or any platform that supports Next.js server builds.

- Push your repo to GitHub.
- Configure environment variables in your hosting dashboard.
- Connect repository and deploy (Vercel auto-deploy recommended).

## Project Structure (short)

- `app/` — Next.js app router pages and layout
- `components/` — React components (chat UI, match card, etc.)
- `lib/supabase/` — Supabase client helpers (`client.ts`, `server.ts`)
- `lib/actions/` — Server actions for profile, matches, stream
- `scripts/` — utility scripts (seed / fake data)

## Notes

- The project uses `@supabase/ssr` for server-side Supabase integrations.
- If you plan to use Stream video, install and configure Stream client SDK and secrets.

If you want, I can also generate a smaller screenshot or update the placeholder image path.
