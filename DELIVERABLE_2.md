# Deliverable 2: the prototype, and the decisions behind it

Live: https://ytree-case-study.vercel.app

## Intent

- The app as a tool a client reasons with, not a dashboard they only read.
- Keeps the account view as the default; adds Asset class, Liquidity, and an ownership scope.
- The composition and the pivot are the running totals and cross-tabs an analyst builds by hand in Excel, brought in-app.
- It also does interpretive work: explains a move, surfaces the one decision that needs a yes, sketches a path forward.
- Borrows patterns from products clients already use.
- Net worth reconciles to £8,420,000 across every perspective, every owner filter, and the pivot.
- All copy is illustrative and would align to Y TREE's client-facing voice. Tiering is not modelled.

## Locked decisions

| Decision | What | Why | How |
|---|---|---|---|
| Modular, not opinionated | Three perspectives, filters, toggles the client turns on | The mismatch is mental model, not missing data, so the client picks the cut | Account is the default; everything else is opt-in |
| One control, three perspectives | Account, Asset class, Liquidity | Three curated cuts cover exposure, liquidity horizon and ownership without the cost and data risk of open customisation | A segmented control on Home |
| Interface moves only where a control needs room | Restructure Home and Analytics; leave the drill and the account grouping | Analyst controls need space; the rest of the app already works | New hierarchy on two screens only |
| Same money, regrouped | Every grouped Total reads £8,420,000 | A regrouped view only works if it still adds up to net worth | Liabilities carried as a negative segment in every cut |
| Ownership is a global scope | All, Mine, Partner's, Joint | The tax use case is "isolate an entity, then read whatever view I am on", which is a scope, not a grouping | One header control, not inside Filter |
| Filter, Date and Compare are three jobs | Three separate controls | One label for three jobs means nothing | Filter groups the book; Date is From and To plus a brush; Compare toggles chart series |
| Tactile date control, not preset chips | A draggable brush plus From and To fields | No fixed set of windows came out of the interview; a continuous control feels responsive and tactile, and the fields keep an exact date one tap away | Brush under the chart, fields beside it |
| Home against Analytics | Home is the state of wealth; Analytics is the interpretation | Home stays a macro glance; Analytics holds the micro dive into why performance moved, which is the literacy hook | Home: net worth, chart, contributions, market context, perspectives, list. Analytics: quartet, composition, pivot, risk mix |
| The performance quartet | Contributions; return against a benchmark; performance explained; what to do next | Shows the value Y TREE has created: what the client added, what the market did, the benchmark, and the next step | Analytics owns the stack; Home keeps only contributions |
| Performance explained | Collapsed by default, one column | The micro step for the client who wants it; the majority never open it | A disclosure arrow |
| What to do next | Empty, or the one decision that needs a yes | Gives the client clarity over their financials without inventing work | "Plan on track", or a live recommendation: a rebalance or a new investment to approve |
| Tone | A health tracker, not a Bloomberg terminal | Clients open the app in volatile weeks | Market movement in its own card, as index moves, not a pound forecast for the client's wealth |
| Official statements, not research pages | A compact link to the real document | A brokerage research interface nudges toward trading; Y TREE is advisory and long-term | The link points only to the genuine statement |
| Export | Download the current view as PDF or CSV | Productises the monthly pack the client team builds by hand; appetite may vary by tier | A header icon; the file follows the current owner, filter, window and tab |
| Risk distribution | On Analytics only | The "63 of 100" on Home is an average and hides a barbell, private equity near 113 against cash near zero | Home shows the number; Analytics shows the breakdown |
| Asset-class drill rows read instrument first | Instrument, then wrapper | The account view labels a row by its wrapper, which prompts "are these bonds?" | "UK gilts, held at Fidelity GIA" |

## Screen walkthrough

### Home, "Net worth"

The health check. The majority never leave the account view.

- Title "Net worth", no greeting. One chrome row: title, Whose, Analytics, privacy, download.
- Risk line: "Mix 63 of 100, agreed 70". A mandate line in plain ink, not an amber warning.
- Chart with From and To fields and a draggable brush. A tap drops a hairline on the curve and updates the figure above it.
- Contributions: money in, against the line. The only part of the quartet kept on Home.
- Market context: index moves, and "no new valuation" for private equity.
- Perspectives: Account (default), Asset class (donut), Liquidity (two bars). Same total.
- List: includes Collectables, Private investments and Liabilities. Total still £8,420,000.

### Analytics

Interpretation.

- Filter: one chip (class, account, access). Slices the book only.
- Line: four series on by default: total value, the Y TREE benchmark, invested capital, and a dashed projection to about February 2027, labelled illustrative.
- Compare: its own chip; toggles series, not a filter.
- The performance quartet.
- Risk distribution: where the 63 comes from.
- Composition: stacked bars over time, height is net worth, liabilities below zero, nets to £8,420,000.
- Table: the same figures as a pivot. Any dimension against any other, with Time available as a column.

### Drills

The current app's structure: total, performance, holdings, risk, fees. Unchanged.

- Provider, for example Citi: the dropdowns, the limited-data banner, cash pots, the benchmark, Risk, Fees.
- Asset class, for example Bonds: the instrument, then "held at [wrapper]".
- PE fund: commitments, the 2025 to 2029 call bars, vintage, IRR, MOIC, TVPI, DPI, statement date.
- Investment property: purchase price, mortgage, equity, then cashflow (rent against expenses) kept separate from the valuation.
- Collectables, EIS, Liabilities: the current app's cards.

Messages, Notifications and Profile stay as the advisory shell. Decisions appear only as alerts.

## Deliberately left out

- Removing the account view, or making another perspective the default
- A dashboard builder
- Brokerage-style stock or instrument pages
- A pound figure for the market's effect on the client's wealth
- Invented statement documents
- Preset range chips on the chart
- Ownership inside Filter
- A second export control
- A dedicated tax tool or other product expansions
- Tier strategy

## Still to do

- Commit the live build to `main` and point production at it, so the repo, the demo and this document describe the same build.
