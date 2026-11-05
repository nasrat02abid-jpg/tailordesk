# TailorDesk — Basic Offline Tailor Shop Software

**English + پښتو | Single-file HTML | No backend required**

## Run on your computer / په کمپیوټر کې چلول

1. Open `index.html` with Chrome or Edge.
2. Go to **Shop Settings / د دوکان تنظیمات** to enter your shop name, phone and address.
3. Click **New Order / نوی فرمایش**. Enter a customer's name, phone number, measurements, clothing details, price, advance and delivery date.
4. Click **Save Order / فرمایش ثبتول**.
5. In **All Orders / ټول فرمایشونه**, search, edit, update status and print a measurement/order slip.
6. In Settings, **Export Backup** regularly; use **Import Backup** to restore the JSON file.

**Important / مهم:** Orders are stored only in the browser's `localStorage` on that device and web origin. GitHub contains the application source, not customer orders. Do not commit your backup JSON files or personal customer data. Opening the app as a local file and opening the GitHub Pages site creates *separate* storage locations; export/import a backup if you want to move orders between them.

## Push to GitHub (PowerShell)

Create a new empty repository named `tailordesk` on GitHub (do **not** initialize it with a README).

```powershell
cd "C:\Projects\tailordesk"
git init -b main
git add .
git commit -m "Initial commit: basic bilingual TailorDesk"
git remote add origin https://github.com/YOUR-USERNAME/tailordesk.git
git push -u origin main
```

Replace `YOUR-USERNAME` with your GitHub username and adjust the folder path.

### Publish with GitHub Pages (optional)

1. Open the repository on GitHub.
2. Select **Settings → Pages**.
3. In **Build and deployment**, choose **Deploy from a branch**.
4. Select `main` and `/(root)`, then save.
5. Open `https://YOUR-USERNAME.github.io/tailordesk/` after it is deployed.

GitHub Pages makes the website publicly reachable. It is **not** a private multiuser database or customer portal. Data still saves per browser, not centrally.

## Update the project later

```powershell
git add .
git commit -m "Update tailor software"
git push
```

## Technology

- HTML + CSS + JavaScript
- `localStorage` persistence
- Browser printing via print dialog
- Backup/import using JSON
- No build tool, server or hosting necessary for offline use
