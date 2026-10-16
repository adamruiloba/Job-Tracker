# Job Tracker (painter jobs, time & pay)

One file: `index.html`. Hosted for free with GitHub Pages, data stored in **your own Google account**.

## How it works day to day
**One address = one job, and you're paid per job.** Everything for that address lives in one place.
1. **Clock In**: one tap. It finds the street address from your location. At a brand-new place it shows the address so you can fix it before saving. If the address (or a spot within ~300 m) already belongs to a job, you're clocked into that same job.
2. **Clock Out**: one tap. You stay on the Clock tab, so the next job is one tap away. Adding a note for the day is optional ("Add notes").
   - **Two jobs in one day?** While clocked in, tap **Switch to another job**. It clocks you out and into the next job (by location, a recent job, or an address). Each job keeps its own hours, and the ledger shows both under one day total.
   - If two entries overlap in time, the app warns you when you save.
3. **Jobs tab**: one card per address, showing how long it took, what was done, and whether it's paid. Search by address or notes, or pick a date.
4. **Job page** (the heart of the app):
   - **How long it took**: days, total hours and the date range.
   - **Job notes**: the paint and materials used, and what was done.
   - **Photos** for the job, each with its date.
   - **Pay for this job**: what it pays, what you've received, what's still owed.
   - **Days worked**: each day's hours and notes.
   - **Mark job finished** when you're done.
   - **Merge with another job**: if two jobs are really the same place, merge them. Days, photos, notes and pay all move into one job. The app also merges jobs automatically when the house number and street match, even if the city, state or ZIP is spelled differently. Apartments with different unit numbers stay separate.
5. **Pay tab**: what you're owed across all jobs, with "Mark paid in full" in one tap.

## The ledger (accountant view)
Open `ledger.html` (the 📒 link on the Pay tab and on every job page). It's a clean, printable report with three views:
- **By job**: one row per job with hours, job pay, paid, due and $/hr, plus totals.
- **By day**: each day, which job(s) you worked, hours, and the day's share of the job pay.
- **Day × job grid**: a monthly grid of hours, jobs down the side and days across the top.

Filter by date range or use the quick buttons (this month, last month, this year). Export to CSV or print. It reads the data saved on that phone, so open the Job Tracker first if it looks empty.

## Put it online (same way as Letters)
1. In your GitHub repo choose **Add file → Upload files**, upload `index.html`, and commit.
2. Repo **Settings → Pages**: deploy from the main branch (you probably already did this for Letters).
3. Open `https://YOURNAME.github.io/REPO/` on your phone and use **Add to Home Screen**.

## Turn on Google sync (one time, ~5 min)
Creates a Google Sheet called "Painter Job Tracker" and a Drive folder "Painter Jobs/<address>" for photos. Sign in with the same Google account on any phone and everything shows up.

1. <https://console.cloud.google.com/> → create a project.
2. **APIs & Services → Library**: enable **Google Drive API** and **Google Sheets API**.
3. **OAuth consent screen**: External, add your app name and email, add yourself as a **Test user**.
4. **Credentials → Create credentials → OAuth client ID → Web application**. Under **Authorized JavaScript origins** add `https://YOURNAME.github.io`.
5. Paste the Client ID into the app's **Settings** tab and tap **Save & sync**.

The app only has the `drive.file` permission, so it can only see files it created itself.

## Good to know
- It works offline and saves on the phone first. Tap **Sync** (top right) when you have signal. It also syncs by itself a few seconds after changes while you're signed in.
- The Google Sheet is readable by you. Open it any time, or share it with someone.
- Location needs permission the first time. If it can't find you, pick or type the address instead.
- Address lookup uses OpenStreetMap's free service, so addresses are usually right but you can edit them on the job page.
