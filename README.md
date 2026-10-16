# Job Tracker (painter jobs, time & pay)

One file: `index.html`. Hosted for free with GitHub Pages, data stored in **your own Google account**.

## How it works day to day
**One address = one job.** Everything for that address lives in one place: your days worked, hours, pay, and photos.
1. **Clock In**: one tap. It finds the street address from your location. At a brand-new place it shows the address so you can fix it before saving. If the address (or a spot within ~300 m) already belongs to a job, you're clocked into that same job. It never makes a second job for the same address.
2. **Clock Out**: one tap. Then jot what you did that day.
3. **Jobs tab**: one card per address, showing days, total hours, pay status and photo count. Search by address or notes, or pick a date to see which jobs you worked that day.
4. **Job page**: clock in or out, total time, the pay you get for the whole job (and what you've received so far), every day worked, and all photos with their dates.
5. **Pay tab**: what you're owed, what you've been paid, hours, average $/hour. "Mark paid in full" is one tap.

Jobs saved by an older version are merged automatically: duplicate addresses become one job, and pay moves from the individual days up to the job.

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
