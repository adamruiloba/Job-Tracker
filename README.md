# Job Tracker (painter jobs, time & pay)

One file: `index.html`. Hosted for free with GitHub Pages, data stored in **your own Google account**.

## How it works day to day
**One address = one job, and you're paid per job.** Everything for that address lives on its job page.
1. **Clock tab**: type the job's address (or pick one you've already saved) and tap **Clock In**. While you're clocked in, tap names to say **who's working today**. **Clock Out** is one tap. **Switch job** moves you to a second job the same day.
2. **Jobs tab**: one card per job showing the owner's name and phone (tap to call), days, hours, crew size, what was done, and pay status. Cards have a **🧭 Directions** button for Google Maps.
   - **Search** finds a job by owner name, phone number, address, paint, notes, contacts, or crew name. Filter by Open, Finished or Unpaid.
3. **Job page**, in five sections:
   - **📋 Details**: address, **owner** (first and last name, phone, special info), and the paint and what was done.
   - **👷 Days & crew**: every day worked with exactly who was there. Day one might be 2 people, day three 4, the last day 1. Totals show each person's days and man-hours.
   - **📷 Photos**, each with its date.
   - **📝 Notes**: dated notes (neighbor complaints, requests, gate codes) and **other contacts** such as the building owner, with name, role and phone.
   - **💵 Pay**: what the job pays, what you've received, what's still owed.
4. **Pay tab**: what you're owed across all jobs, with "Mark paid in full" in one tap.
5. **Settings → Your crew**: add the people who work with you once, then just tap names each day.

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
