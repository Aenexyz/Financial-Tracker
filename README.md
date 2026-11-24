# Vault: personal finance tracker

A mobile-first web app for tracking bank balances, crypto, credit cards, loans, cashflow and expenses. It's built for the iPhone and runs entirely in the browser.

## Features

- **Passcode lock.** The app opens on a keypad and locks itself after 30 seconds in the background.
- **Savings:** a card for each bank account, plus crypto grouped by exchange, showing each coin held.
- **Cards:** credit card balances, how much of the limit is used, and how much is available.
- **Loans:** remaining balance, how much is paid off, the monthly payment and the interest rate.
- **Cashflow:** weekly or monthly income against expenses and loan repayments, and how much is left over.
- **Expenses:** spending grouped by category, viewable per week or per month.
- **Multiple currencies.** Each account or item has its own currency, and totals convert into the main currency (₱ PHP by default). You can edit the exchange rates in Settings.
- **Backup and restore** using a JSON file.
- **Works offline.** A service worker (`sw.js`) keeps a copy of the app, so it opens with no internet and picks up updates when you're back online.

## Where your data is stored

Everything is saved in your browser's `localStorage`, **on your device only**. Nothing is sent to a server, and none of your financial data goes into this repository.

- Your data survives refreshes and closing the browser.
- Your data does **not** sync between devices or browsers. Use **Settings → Save backup file** and **Restore from backup file** to move it.
- Clearing your browser data deletes it. Back up regularly.

## Running it

Open `index.html` in any browser, or enable **GitHub Pages** (Settings → Pages → Deploy from branch → `main` / root). On an iPhone, open the Pages URL, tap **Share → Add to Home Screen**, and it will open like an app.

> The passcode is a privacy screen, not encryption. It keeps people from glancing at your balances, but it is not real security. The code checks it against a hash, and that hash is visible in this repository.
