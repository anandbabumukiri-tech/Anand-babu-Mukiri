# CODENG — Play. Learn. Code. Build.

## What is in this zip
- `index.html` — working front-end demo (multilingual onboarding EN/TE/HI, Python `print` lesson, challenge flow). Open it in a browser; no install needed.
- `supabase/migrations/001_init.sql` — database schema + row-level security (draft, NOT yet run or tested).
- `.env.example` — settings you must provide.

## Status (honest)
Working in the demo: language choice, lesson modes, challenge check, XP once per challenge (saved on this device only).
NOT done: real login/OTP/password reset, database wiring, AI tutor, real code execution, admin area, other languages and tracks, automated tests.
The demo's Preview/Submit only pattern-matches `print("...")`; it is not code execution. Telugu/Hindi text is a draft and needs native-speaker review.

## Beginner steps
1. Open `index.html` to see the demo.
2. Create a free project at supabase.com. In SQL Editor, paste and run `001_init.sql`.
3. Auth > Providers: enable Email (and Phone with an SMS provider such as Twilio for OTP).
4. Copy `.env.example` to `.env` and fill in values. Never put server keys in browser code.
5. Next build steps: Supabase login screens; a server function that sends code to a sandbox (e.g. Judge0), checks hidden test cases, then inserts progress + XP; an AI tutor server endpoint with rate limits.

## Known limitations
See Status. Security rules in the SQL must be tested (try reading another user's rows) before launch.
