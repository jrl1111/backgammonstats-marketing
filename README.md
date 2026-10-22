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

Both forms (the hero's email field and the full waitlist form) post to the
Supabase table `waitlist_signups` (`full_name`, `email`, `sites[]`, `typical_pr`) with the
public anon key; row-level security allows inserts only. `handleSignup` in the
page's script is the only place sign-ups are sent. A failed request shows an
error under the form and keeps what was typed.

## Social image

`og.png` (1200 × 630) is referenced by the Open Graph / Twitter tags.
