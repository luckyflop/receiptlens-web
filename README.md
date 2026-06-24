# Receipt Lens — Website

Landing page, privacy policy, and terms for **Receipt Lens**, hosted with GitHub Pages at
**https://luckyflop.github.io/receiptlens-web/**

Receipt Lens is an AI receipt scanner that extracts the store, date and total from a receipt,
converts currencies, and organizes expenses. It ships in two forms:

- **Chrome extension — “Receipt Lens AI”** (desktop)
  Install: https://chromewebstore.google.com/detail/hhflggooefmfddnckdploepficheflej
- **Android app — “Receipt Lens”** (mobile, Gulf Arabic / RTL), package `com.luckyflop.receiptlens`
  Adds automatic expense categorization, a monthly summary, multi-currency support, and a
  **Zakat calculator** (live gold/silver nisab + lunar-year hawl tracking).

## How it works

- **AI extraction:** receipt images are processed by **OpenAI GPT-4o** to return the store, date and total.
- **Currency conversion:** live exchange rates from a public rate API.
- **Auth:** Google Sign-In (basic email + profile only).
- **Pro / billing:**
  - Chrome extension → **Polar** subscription ($4.99/mo)
  - Android app → **Google Play Billing** managed via **RevenueCat** ($2.99/mo)
- **Free plan:** 5 scans, then Pro for unlimited scanning.
- Receipt images are processed and **not stored** on the server; only plan/usage status is kept.

## Files

| File | Purpose |
|------|---------|
| `index.html` | Landing page (both products) |
| `privacy.html` | Privacy Policy (Chrome Web Store + Google Play) |
| `terms.html` | Terms of Use |
| `success.html` | Polar payment-success redirect page |
| `style.css` | Shared styles (brand: indigo `#4F46E5` + green `#16A34A`) |
| `app-icon.png` | Brand icon (logo / favicon) |
| `screenshot.png` | Product screenshot used in the hero |

## Updating links before public launch

The Android app is published once it clears Google Play testing. Until then the Google Play
buttons are marked **“Coming soon”**. When the app is live:

1. In `index.html`, find each Google Play link and **remove** `aria-disabled="true"`.
2. Change the button text from **“Coming soon on Google Play” / “Coming soon”** to **“Get it on Google Play”**.

The Play listing URL is already set to `https://play.google.com/store/apps/details?id=com.luckyflop.receiptlens`.

## Deploy (GitHub Pages)

This repo serves from the `main` branch root. After pushing changes, GitHub Pages updates within a minute or two.
Settings → Pages → Source: `Deploy from a branch` → Branch: `main` / `/ (root)`.

## Contact

luckyflopbtt@gmail.com · X: [@ReceiptlensAI](https://x.com/ReceiptlensAI)

© 2026 Receipt Lens · LuckyFlop. Licensed under MIT (see `LICENSE`).
