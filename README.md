# Y TREE — portfolio-view prototype

Take-home case study for a Mobile Product Manager role at Y TREE (an FCA-regulated wealth manager).

## The problem

The app organises a client's wealth by where each asset is custodied, with essentially one path through it. A minority of clients (roughly 10 to 15 percent, the most complex and least sticky) think in a different structure. This prototype adds ways to see the same wealth by **asset class**, by **liquidity**, and by **owner**, without disturbing the default view the majority rely on.

## Run it

Single self-contained file, no build step.

- Open `index.html` in a browser, or
- Serve the folder with any static server: `npx serve` / `python -m http.server`, or
- Deploy as a static site (Vercel / Netlify / GitHub Pages). Root is the repo, output directory is `.`, no build command.

### Deploy to Vercel

1. Push this repo to GitHub (done).
2. vercel.com/new, import the repo.
3. Framework preset: **Other**. Build command: none. Output directory: `.` (or leave blank).
4. Deploy. Every push to `main` redeploys.

## What's in it

- **Web-app shell**: mock phone with explanatory side panels on desktop (over 1080px wide); full screen on mobile.
- **Home**: net worth in a chosen currency; three separate streams (your actions, markets and efficiency, your notes); a sliding "wallet" strip of perspectives.
- **Performance**: line / composition columns / pivot table. Free date range (from and to), a draggable window that pans and resizes, axis modes (value, indexed to 100, period change), compare overlays (previous provider, market, contributions, risk-level path), projection, a table under the chart.
- **Perspectives**: Structure (by institution, plus contributed-versus-growth), Asset class (colour-coded pie plus table plus read against the agreed risk level), Liquidity (pie plus table plus what is accessible before tax). The "why this view" rationale lives in the desktop side panel.
- **Equities**: every holding combined across providers, currency exposure with the native split, a look-through note, a live Approve / Decline / Ask decision with its supporting documents, and the advice history.
- **Private equity**: committed / called / uncalled / distributed, a capital-call calendar, per-fund currency.
- **Alerts**: one filterable folder. Items needing a response pinned at the top, everything else chronological by month.
- **Notes**: per screen, timestamped (added and last updated), plus an "all notes" view at `#/notes`.

The written problem statement and prioritisation is a separate document (published as an artifact, not in this repo).

## Design system

- Watch-house palette: green dial accent `#2F8F5B` (interactive only), gold `#B4863A` (trend line and material accents), neutral charcoal ground.
- Fraunces for figures and headings, Inter for UI.
- Chart method: pick the form first, colour by the job it does, a validated categorical palette for asset-class identity only, a table under every chart, one axis, tap to read.

## Data

One fictional client, about 8.4m GBP, figures reconciled across every screen. Near the top of the `<script>`:

- `L` — leaf holdings `[category, owner, assetClass, liquidity, value, account]`
- `EQ`, `PE`, `PE_CALLS`, `ADVICE`, `ALERTS`
- `buildNW()` — synthesises the monthly net-worth history with real market episodes (2020 crash, 2022 bear, 2024 rally, 2025 correction, a sharp move this month) and lumpy contributions (a business sale, an inheritance, annual ISA).

## Known gaps and TODO

- [ ] Performance: device-test the brush pan and resize, the free date inputs, and the composition columns across browsers.
- [ ] Pivot table: add cost-basis, unrealised-gain and fund look-through as columns. Wire real fund look-through instead of the single illustrative Apple line on the Equities screen.
- [ ] Provider tree: make Structure's "down to each account" an actual expandable drill (Coutts, Monzo, Wise, a Revolut S&P 500 pot). Right now it is described in copy only, and the leaf data does not include those accounts.
- [ ] Currency: detail screens should distinguish hedged vs unhedged. Add a native-currency field to each leaf.
- [ ] Sub-asset-class ladders (region, sector, market cap, style, bond duration and credit quality). Not started.
- [ ] Analyst granularity not yet covered: per-holding fees and yield, concentration metrics, benchmark-relative active weights, factor exposure, PE IRR / DPI / TVPI / vintage, stress scenarios.
- [ ] Mobile: test wallet swipe vs scroll (an open research question in the notes). Side panels are desktop-only by design.
- [ ] Accessibility pass: visible focus states on the custom buttons, `prefers-reduced-motion`, and a contrast audit of the categorical palette on the exact surface colour.
- [ ] Notes are stored in `localStorage` only, per device.

## Structure of the code

All in `index.html`. Order inside `<script>`: data, `state`, helpers, `SCREENS` (side-panel copy), `render()` router, then one `render*` function per screen, then components (`walletStrip`, `donut`, `pieBlock`, `perfLineChart`, `compositionCols`, `renderPivot`, `brush*`, `noteBlock`), then the sheets, then the event listeners at the bottom.
