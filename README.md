# Endowment Withdrawal Planner

A mobile-friendly Progressive Web App (PWA) for calculating annual retirement withdrawals using the Yale endowment smoothing formula with guard rail zones.

## What it does

Each year you enter your current portfolio value and high water mark. The app calculates how much you can safely withdraw using:

- **Yale smoothing formula** — blends 70% of last year's inflation-adjusted withdrawal with 30% of your target rate applied to the current portfolio. This keeps income stable while still responding to market conditions.
- **Guard rail zones** — three zones that protect the portfolio in down markets:
  - **Green** — portfolio within 20% of high water mark. Take the full Yale amount.
  - **Yellow** — portfolio dropped 20–30%. Freeze withdrawals at inflation-adjusted prior year amount.
  - **Red** — portfolio dropped more than 30%. Stop all withdrawals and use emergency funds.

All settings, prior year withdrawal, and history are saved locally on the device. Nothing is sent anywhere.

## Installing on iPhone

1. Open the app URL in **Safari**
2. Tap the **Share** button (box with arrow at the bottom of the screen)
3. Tap **Add to Home Screen**
4. The app installs and opens full-screen like a native app

## Using on desktop

Open the URL in any browser. Works the same as on mobile.

## Getting started

1. Go to **Settings** — enter your portfolio value, withdrawal rate (default 4%), and inflation
2. Leave *Prior year withdrawal* blank for your first year
3. Go to **Calculate** — enter this year's portfolio value and high water mark
4. Tap **Calculate** to preview, then **Record** to save
5. Repeat each year — the app carries the prior year withdrawal forward automatically

## Running locally

No server required. Just open `index.html` in any browser.

## Files

| File | Purpose |
|------|---------|
| `index.html` | The complete app |
| `manifest.json` | PWA install metadata |
| `sw.js` | Service worker for offline use |

## Notes

- The withdrawal rate defaults to 4% — change it in Settings to match your own plan
- The guard rail thresholds (20% and 30%) are also adjustable in Settings
- In a red zone year, the prior year withdrawal amount is preserved so the formula resumes correctly when the market recovers
- The high water mark should be updated whenever the portfolio reaches a new all-time high
