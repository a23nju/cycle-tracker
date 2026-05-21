# Cycle Tracker — Project Notes

## What this is
A menstrual cycle tracker web app built for a beginner user. Single HTML file with no build step.

## Live URL
https://cycle-tracker-anjaly.netlify.app

## Hosting
- Hosted on Netlify under account: anjuelsavarghese@gmail.com
- Site ID: 6e8f7355-3d0a-4282-adcf-4a0d324cc82b
- To redeploy: `NETLIFY_AUTH_TOKEN=<token> npx netlify-cli@latest deploy --dir . --prod --site 6e8f7355-3d0a-4282-adcf-4a0d324cc82b`

## Stack
- Pure HTML + CSS + JavaScript (no framework, no build step)
- No backend currently — data saved to localStorage
- No login/auth — single user app
- Firebase project exists (menstural-tracker) but Firestore was not enabled (billing required)

## Files
- `index.html` — entire app in one file

## Features
- Dashboard: current cycle phase, next period date, ovulation & fertile window
- Log: period dates, flow intensity, symptoms, mood, pain slider, stress slider, temperature, exercise, skin/cravings chips, water intake, sleep hours, diary notes
- Calendar: monthly view with period/fertile/ovulation days colour coded
- Insights: cycle stats, average length, mood & symptom trends
- History: past period logs with delete option
- Profile: user name, PIN lock toggle, CSV data export
- Settings: adjustable cycle length (20–45 days) and period length (2–10 days)

## Data Storage
All data stored in localStorage with keys:
- `ct_settings` — cycle length and period length
- `ct_periods` — array of period logs (id, startDate, endDate)
- `ct_logs` — object keyed by date string (symptoms, mood, water, sleep, notes, flow, pain, stress, temp, exercise, skin, cravings)
- `ct_name` — user's display name
- `ct_pin` — PIN code (if set)
- `ct_pin_enabled` — whether PIN lock is active

## GitHub
- Repo: https://github.com/a23nju/cycle-tracker
- To push updates: `git add . && git commit -m "your message" && git push`

## Next Steps (pending)
- Add Supabase backend for proper data persistence across devices
- Add user login/accounts
- User is signing up for Supabase — once done, update app to use Supabase auth + database
