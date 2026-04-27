\# FitTrack — Cloud Workout Tracker



A single-page workout tracker. Log strength sets/reps/weights, cardio, save reusable workout plans, see your calendar history and progress charts. Data lives in your browser (`localStorage`) so it works offline; you can export/import a JSON backup to move between devices.



Once you publish this to GitHub Pages it's reachable from any device with a browser — phone, laptop, tablet.



---



\## Quick local test.



Just open `index.html` in your browser by double-clicking it. That's it — no build step.



---



\## Deploy to GitHub Pages (free, public URL)



You'll end up with a URL like `https://<your-username>.github.io/fittrack/`.



\### 1. Create a GitHub account (skip if you have one)

Go to https://github.com and sign up.



\### 2. Create a new repository

\- Click \*\*New\*\* (or go to https://github.com/new).

\- Repository name: `fittrack` (or anything you like).

\- Set it to \*\*Public\*\* (Pages requires Public on free plans).

\- \*\*Do NOT\*\* check "Add a README" — we already have one.

\- Click \*\*Create repository\*\*.



\### 3. Push the files



Open a terminal in this folder (the one with `index.html` and this README) and run:



```bash

git init

git add index.html README.md

git commit -m "Initial commit"

git branch -M main

git remote add origin https://github.com/<YOUR\_USERNAME>/fittrack.git

git push -u origin main

```



Replace `<YOUR\_USERNAME>` with your GitHub username.



> If git asks for credentials, use a \*\*Personal Access Token\*\* as the password (Settings → Developer settings → Personal access tokens → Tokens (classic) → Generate new token, scope: `repo`).



\### 4. Turn on GitHub Pages

\- In your repo on GitHub: \*\*Settings\*\* → \*\*Pages\*\* (left sidebar).

\- Under \*\*Build and deployment\*\* → \*\*Source\*\*, choose \*\*Deploy from a branch\*\*.

\- Branch: \*\*main\*\*, folder: \*\*/ (root)\*\*. Click \*\*Save\*\*.

\- Wait ~1–2 minutes. The page will show a green box with your live URL.



Your tracker is live at `https://<your-username>.github.io/fittrack/`.



\### 5. Bookmark it on your phone

\- Open the URL in mobile Safari/Chrome.

\- "Add to Home Screen" — it now behaves like an app.



---



\## Updating the site later



Just edit `index.html`, then:



```bash

git add .

git commit -m "Update"

git push

```



Pages re-publishes within ~1 minute.



---



\## How your data works



\- All data is stored in your browser under the key `fittrack.v1` (localStorage).

\- It is \*\*not\*\* sent to any server — there is no backend.

\- To use the same data on another device: hit \*\*⬇ Export\*\* on device A to download the JSON, then \*\*⬆ Import\*\* on device B.

\- Clearing browser data will wipe your workouts, so export backups occasionally.



---



\## Features



\- Log strength exercises with multiple sets (reps × weight) and a "done" checkbox per set

\- Log cardio (run/bike/row/swim/etc.) with duration, distance, calories

\- Save reusable \*\*workout plans\*\* (templates) and load them in one tap

\- \*\*Calendar\*\* view showing which days you trained this month

\- \*\*Stats\*\* dashboard: total volume, cardio minutes, day streak, workouts/week chart, per-exercise progress chart

\- \*\*Personal records\*\* auto-tracked from your logs

\- Dark/light theme

\- JSON export/import for backup and cross-device sync

\- Works offline once loaded



---



\## Want real cloud sync later?



Local storage is per-browser. If you outgrow that, the easy upgrade is:



\- \*\*Firebase\*\* (free tier, drop-in auth + Firestore database).

\- \*\*Supabase\*\* (free tier, Postgres + auth).



Either can be wired in by replacing the `loadState`/`saveState` functions in `index.html`. Open an issue or ping for guidance.

