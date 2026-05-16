# 🔗 LinkNet ISP Management System

> A fully offline, password-protected web app for managing petty cash, daily costs, conveyance bills, and inventory for a small-to-mid ISP business. No server needed — runs entirely in the browser.

![GitHub Pages](https://img.shields.io/badge/Hosted%20on-GitHub%20Pages-blue?style=flat-square&logo=github)
![No Backend](https://img.shields.io/badge/Backend-None%20(localStorage)-green?style=flat-square)
![Single File](https://img.shields.io/badge/App-Single%20HTML%20File-orange?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=flat-square)

---

## 📸 Features

| Module | Description |
|---|---|
| 💰 **Petty Cash** | Track income & expenses; balance auto-deducts Daily Cost and Conveyance |
| 📋 **Daily Cost** | Log operational costs (fuel, labor, tools, electricity, etc.) |
| 🚗 **Conveyance Bill** | Staff travel bills with From→To, purpose, vehicle, staff-wise summary |
| 📦 **Inventory** | Stock IN/OUT for 11 ISP products with low-stock alerts |
| 📜 **Stock Log** | Full movement history with per-entry delete and stock reversal |
| 📊 **Export** | Multi-sheet Excel report (Summary, Cash, Daily Cost, Conveyance, Inventory, Stock) |
| ⚡ **Dashboard** | Live overview of balance, expenses, stock levels, and recent activity |
| ⚙️ **Settings** | Change password, export/import JSON backup |

---

## 📦 Inventory Products Tracked

- Fiber Cable
- TJB
- Tie
- Patchcord
- Sleeve
- UTP Cable
- ONU
- MC
- Adapter
- SFP Module
- Router

---

## 🏦 Petty Cash Balance Formula

```
Net Balance = Total Income
            − Cash Expenses
            − Daily Costs
            − Conveyance Bills
```

All three cost types are deducted automatically and shown in a color-coded breakdown bar on the Petty Cash page.

---

## 🚀 Hosting on GitHub Pages

### Step 1 — Create Repository
1. Go to [github.com](https://github.com) → **New repository**
2. Name it (e.g. `linknet-isp`) → Set to **Public** → Click **Create repository**

### Step 2 — Upload Files
Upload these files to the root of your repository:
```
linknet-isp/
├── index.html        ← Main app
├── manifest.json     ← PWA manifest
└── README.md         ← This file
```

> **Note:** The `icons/` folder is optional. If you skip it, the app still works — only the PWA install icon will be missing.

### Step 3 — Enable GitHub Pages
1. In your repo, go to **Settings** → **Pages**
2. Under **Source**, select `Deploy from a branch`
3. Choose branch: `main` (or `master`), folder: `/ (root)`
4. Click **Save**

### Step 4 — Access Your App
After ~1 minute your app will be live at:
```
https://YOUR-USERNAME.github.io/linknet-isp/
```

---

## 🔐 Login

| Field | Default |
|---|---|
| Password | `admin123` |

> Change the password immediately after first login via **Settings → Change Password**.

The password is stored in your browser's `localStorage`. It never leaves your device.

---

## 💾 Data Storage

All data is stored in **browser localStorage** — no server, no database, no internet required after first load.

| Key | Contents |
|---|---|
| `ln_cash` | Petty cash transactions |
| `ln_dc` | Daily cost records |
| `ln_cv` | Conveyance bills |
| `ln_invlog` | Inventory movement log |
| `ln_stock` | Current stock levels |
| `ln_pw` | Hashed login password |

### ⚠️ Important — Back Up Regularly
Because data lives in the browser, **clearing browser data will erase everything**.

Use **Settings → Export JSON** regularly to back up your data. You can reimport it anytime with **Import JSON**.

---

## 📊 Excel Export

The export module generates a `.xlsx` file with up to 6 sheets:

| Sheet | Contents |
|---|---|
| Summary | Balance overview + stock snapshot |
| Petty Cash | All income & expense rows with totals |
| Daily Cost | All cost records with monthly subtotals |
| Conveyance | Bills with staff-wise summary table |
| Inventory Log | All IN/OUT movements |
| Stock Levels | Current stock with LOW alerts |

Supports **custom date range** filtering and **quick export** buttons (Today / This Month / All Data).

---

## 🛠️ Tech Stack

- **Vanilla HTML + CSS + JavaScript** — zero frameworks, zero build step
- **[SheetJS (xlsx)](https://sheetjs.com/)** — Excel export via CDN
- **Google Fonts** — JetBrains Mono + Sora via CDN
- **localStorage** — all data persistence

---

## 📁 File Structure

```
linknet-isp/
├── index.html          ← Entire app (single file)
├── manifest.json       ← PWA web app manifest
├── README.md           ← This documentation
└── icons/              ← (Optional) PWA icons
    ├── icon-192.png
    └── icon-512.png
```

---

## 📲 Install as Mobile App (PWA)

Because `manifest.json` is included, you can install this as a home screen app:

**Android (Chrome):**
1. Open the GitHub Pages URL in Chrome
2. Tap the **⋮ menu** → **Add to Home screen**
3. Tap **Install**

**iOS (Safari):**
1. Open the GitHub Pages URL in Safari
2. Tap the **Share** button → **Add to Home Screen**
3. Tap **Add**

---

## 📝 License

MIT License — free to use, modify, and distribute.

---

## 👤 Author

Built for **LinkNet ISP**, Chattogram, Bangladesh.
