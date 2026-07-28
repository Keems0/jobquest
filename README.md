# JobQuest — job-hunt dashboard

A gamified dashboard for digital-marketing & branding roles (remote + Oman).
It loads listings from `jobs.json`, which a scheduled agent refreshes every morning.

## Files
- `index.html` — the dashboard (open this).
- `jobs.json` — the live job list. The morning agent rewrites this; the page reads it on load.

## One-time setup (do this once)

1. **Create the repo** on GitHub named `jobquest` (public). Upload `index.html`, `jobs.json`, and this README (drag-drop into the "Add file → Upload files" screen works).
2. **Enable GitHub Pages:** repo → **Settings → Pages** → *Source: Deploy from a branch* → Branch: `main` / folder: `/ (root)` → **Save**.
   Your dashboard goes live at: `https://<your-username>.github.io/jobquest/` (give it ~1 minute).
3. **Connect GitHub to claude.ai** so the morning agent can push updates:
   claude.ai → your profile → **Settings → Connectors / GitHub** (or during the routine setup), and authorize the `jobquest` repo.
4. Confirm your **GitHub username** and repo name so the routine can be pointed at it.

## How the daily refresh works
Every morning the agent searches the job boards, merges new roles into `jobs.json`,
and pushes the change. GitHub Pages redeploys automatically. Open your Pages URL → new jobs are
already on the board. Your progress (name, XP, statuses, notes) lives only in your browser and is
never uploaded or overwritten.
