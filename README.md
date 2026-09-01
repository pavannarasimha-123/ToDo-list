# Pavan's Daily Tracker

A single-file personal tracker: daily task list, a rotating DSA pattern-of-the-day
(132 patterns across 15 categories), streaks, a consistency heatmap, and a daily
"what did you learn today" log.

Everything — HTML, CSS, and JavaScript — lives in `index.html`. There is nothing to
install and no build step.

## How data is stored

This version saves everything in your **browser's `localStorage`**, so it works as a
plain static site with no backend. That means:

- Data persists across visits **as long as you use the same browser on the same
  device** and don't clear site data/cookies for the page.
- It does **not** sync across devices or browsers — a different browser or device
  starts with a fresh, empty tracker.
- Usernames and passwords are stored in plain text in `localStorage`. This is fine for
  personal/casual use, but don't reuse a real password you use elsewhere, and don't
  put sensitive information into it — anyone with access to the browser (or its dev
  tools) can read the stored data.

Default login: **pavan / pavan123** — you can also register new accounts from the
page itself; each account gets its own separate tasks/streak/history.

## Deploy to GitHub Pages

1. Create a new GitHub repository (public, so Pages can serve it for free), e.g.
   `pavan-tracker`.
2. Add `index.html` to the root of the repository (exactly as-is, filename must stay
   `index.html` so GitHub Pages serves it as the homepage).
3. Commit and push:
   ```bash
   git init
   git add index.html README.md
   git commit -m "Add daily tracker"
   git branch -M main
   git remote add origin https://github.com/<your-username>/pavan-tracker.git
   git push -u origin main
   ```
4. On GitHub: go to **Settings → Pages**.
5. Under **Build and deployment → Source**, choose **Deploy from a branch**.
6. Pick branch **main** and folder **/ (root)**, then **Save**.
7. Wait a minute or two — GitHub will give you a live URL, typically:
   `https://<your-username>.github.io/pavan-tracker/`

That URL is now your personal tracker, live and bookmarkable.

## Files in this project

- `index.html` — the entire app (structure, styling, and logic in one file).
- `README.md` — this file.

## Notes

- Works fully offline once loaded (no external calls except Google Fonts, if your
  browser has them cached; the fonts referenced in CSS are system fallbacks if not
  available, so it still works without internet).
- To reset everything, clear the site's local storage from your browser's dev tools,
  or open the site in a private/incognito window for a clean slate without affecting
  your saved data.
  Live link:https://to-do-list-u5vk.vercel.app/
