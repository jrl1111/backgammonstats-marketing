# BackgammonStats Marketing Site

Standalone static landing page served at **backgammonstats.com**.

This is a single-file static site — no build step, no framework, no bundler.

## Deploy

Hosted on Vercel as a separate project from the main app (which lives at `app.backgammonstats.com`).

### Initial setup
1. Push this folder to its own GitHub repo (e.g. `backgammonstats-marketing`).
2. In Vercel, create a new project from that repo.
3. Framework preset: **Other** (static). No build command needed.
4. Output directory: `.` (root).
5. Attach domains: `backgammonstats.com` + `www.backgammonstats.com`.

### Making changes
Edit `index.html` and push to main. Vercel auto-deploys in seconds.

## Signup form

Currently writes to `localStorage` only. To capture real leads, replace the
`handleSignup` function with a POST to Supabase, Formspree, ConvertKit, or
a simple Vercel Edge Function.
