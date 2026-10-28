# Job Tracker (painter jobs, time & pay)

One file: `index.html`. Hosted for free with GitHub Pages, data stored in **your own Google account**.

## How it works day to day
**One address = one job.** Everything for that address lives on its job page, and every job shows a photo of the house so you know it at a glance.
1. **Clock tab**: type the job's address and tap **Clock In**, or tap **Clock in** next to one of your jobs. Opening a job never clocks you in; only a Clock In button does. While you're clocked in, tap **Edit** to say who's working. **Clock Out** is one tap, and the app suggests Full or Half day from your hours (you can change it).
2. **Calendar tab**: a month view (or week view) like Google Calendar. Each day shows a photo tile for every job you worked. Tap a day to see the jobs, times, full or half day, crew, pay, and tags like "Day 2 of 3", "🚩 Started" and "🏁 Finished".
3. **Jobs tab**: one card per job with its house photo, owner, status, dates, and pay. **Search** by owner name, phone, address, paint, notes, contacts, or crew name. Opening a job shows:
   - A **photo banner** (add or change it with the 📷 button). Under it: **Clock in**, **Directions**, **Call**, **Finish**.
   - **Started / Finished / Took**: when the job began, ended, and how many days and hours it took.
   - **Details**: owner (name, phone, special info), paint and what was done, address.
   - **Days**: each day with Full/Half, its pay rate, the crew who worked, and optional notes on what each person did.
   - **Photos**: tap ★ to pick the cover photo.
   - **Notes**: dated notes and other contacts.
   - **Pay**: pay **by the day** (each day has its own rate) or **one price** for the whole job, plus what you've received and what's still owed.
4. **Pay tab**: owed and received totals, and what's waiting on payment. Links to the **ledger** and the **report**.
5. **Settings**: your employees (add, rename, remove), your usual **full-day and half-day rates** (they fill in automatically), and who the report is for.

### Who worked (employees)
On a day, tap **Edit crew**. A list of your employees appears: tick who worked, and, only if you want, tap **＋ note** to say what that person did. Notes are optional and never required.

## The report for your boss
Open **Pay → 📤 Report** (`report.html`). It lists each job worked with its address, the days (Full or Half), and what's earned, paid, and owed, with totals. Choose This month, Last month, All time, or Unpaid only. **Send** opens your phone's share sheet (text, WhatsApp, email). You can also copy it as text or print it to a PDF. Jobs from earlier that are still unpaid are listed at the bottom.

## The ledger (accountant view)
Open `ledger.html` (the 📒 link on the Pay tab and on every job page). It's a clean, printable report with three views:
- **By job**: one row per job with the owner, hours, man-hours, job pay, paid, due and $/hr, plus totals.
- **By day**: each day, which job(s) you worked, hours, who was on the crew, and the day's share of the job pay.
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
- Tap **🧭 Directions** on a job (on the Jobs list, the job page, or the Clock tab) to open Google Maps directions to the address.
