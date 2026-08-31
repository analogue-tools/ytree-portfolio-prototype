# Y TREE: three perspectives on one portfolio

Take-home for a Mobile Product Manager role at Y TREE, an FCA-regulated wealth manager.
Built as an iteration of the current Y TREE app, not a redesign.

- Live: https://ytree-case-study.vercel.app
- Deliverables: `DELIVERABLE_1.md` (the problem and the plan), `DELIVERABLE_2.md` (the prototype decisions)

## The idea

- The app already shows a client's wealth one way: grouped by account. One path, no way to re-sort.
- A valuable minority think in exposure, in time to cash, and by owner. Today they wait for a hand-built PDF from the client team.
- This keeps the account view as the default and adds two more ways to read the same total, plus an ownership scope. Interested clients opt in; everyone else sees no change.

## What is in the prototype

- **Home.** Net worth, a chart with a draggable date brush, contributions, market context, and "See this another way": Account (default), Asset class (donut), Liquidity (two bars). Every grouping totals £8,420,000.
- **Whose.** A header filter: All, Mine, Partner's, Joint. Narrows every screen.
- **Analytics.** The performance quartet (contributions, return against a benchmark, performance explained, what to do next), a four-series line chart with a projection, Composition over time, and a pivot Table.
- **Drills.** The current app's structure kept intact: total value and last-valued date, performance (YTD or ITD, £ or %), holdings, risk, fees. Private equity and investment property have their own detail screens.
- **Export.** A header icon; the download follows the current owner, filter, window and tab.

## Run it

- Single self-contained `index.html`, no build.
- Open it in a browser, or serve the folder (`npx serve`).
- Deploy as a static site: framework preset Other, no build command, output dir `.`.

## Design

- Dark indigo canvas, one teal accent (`#3ED9CE`), asset classes carry their own hues.
- System font stack. 44px tap targets. Colour is never the only signal.
- Calm and status first, in line with Y TREE's "health tracker" direction. Not a trading app.

## Data

- One fictional client, net worth £8,420,000, reconciled across every perspective, every owner filter and the pivot. All figures illustrative.
- Near the top of the `<script>`: the leaf rows (account, owner, asset class, liquidity, value), the group definitions, the asset-class colours, and the drill data.
