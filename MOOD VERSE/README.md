# MoodVerse MVP

MoodVerse is a Next.js MVP for creating original personal writing inspired by broad music moods. It supports a landing page, multi-step creation flow, output/refinement screen, and inspiration library page with mock data.

## Stack

- Next.js App Router
- React
- Tailwind CSS
- shadcn/ui-style primitives
- Framer Motion
- Lucide icons

## Rights Guardrail

The product direction is mood-based only. It should not copy, quote, remix, or reproduce copyrighted song lyrics, and it should not imitate a named song or artist.

## Run Locally

```bash
npm install
cp .env.example .env.local
npm run dev
```

Open `http://localhost:3000` or the port printed by Next.js.

## OpenAI API

Add the server-side API key to `.env.local`:

```bash
OPENAI_API_KEY=your_key_here
OPENAI_MODEL=gpt-5.4-mini
```

The create flow sends generation requests to `POST /api/generate`. The route
calls the OpenAI Responses API from the server and returns structured JSON with
the generated text, title, emotion tags, and suggested refinements.

Never expose the API key through a `NEXT_PUBLIC_*` environment variable. Local
`.env*` files are ignored by git, except for the key-free `.env.example`.
