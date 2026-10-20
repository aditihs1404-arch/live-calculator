# live-calculator

A live Indonesian Rupiah (IDR) currency calculator in a single `index.html`, with no build step and no API key.

## Use it

Open `index.html` in a browser. You can also host it on GitHub Pages: go to Settings → Pages and deploy from this branch.

- Type an amount (either `1.000.000,50` or `1,000,000.50` works) and pick a currency: SGD, USD, EUR, JPY, RMB, GBP or AUD. One side is always IDR.
- **Swap** flips the direction, for example USD → IDR or IDR → USD.
- Rates refresh automatically every 15s, 30s, 1 min or 5 min (you choose). They also refresh when you come back to the tab.
- The result flashes when the rate changes. The table shows the change (▲/▼) since the last update.
- A small chart tracks the rate for as long as the page stays open.
- At the bottom, Tether Gold (XAUT) and Bitcoin (BTC) are priced in USD with their 24-hour change (from CoinGecko, falling back to Coinbase).

## Rate sources

1. [Coinbase exchange rates](https://api.coinbase.com/v2/exchange-rates?currency=IDR) is the main source. It updates through the day.
2. [open.er-api.com](https://open.er-api.com/v6/latest/IDR) is the fallback. It updates once a day.

Rates are mid-market and for reference only. Banks and money changers add their own margin.
