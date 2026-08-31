# Y TREE Mobile PM Case Study

Matches the take-home: Deliverable 1 is problem and priority. Deliverable 2 is the prototype talking sheet.

**Live prototype:** https://ytree-case-study.vercel.app  
**Client:** Jeanne · net **£8,420,000** · joined 15 Feb 2025 · adviser Priya Shah · agreed risk **70** · mix **~63**

---

## Deliverable 1: Problem statement and prioritisation

### What is the problem?

- The app has one path: by account / where money is held.
- Most clients love that path and do not love change.
- A high-value minority thinks in exposure, liquidity, and whose it is.
- The team already writes that as a monthly PDF. That is a workaround, not a product.
- Equities and bonds reprice daily; PE and property update on statements.
- Mixing those cadences without a cue feels like false precision.
- Performance is visible. It is not explained (contributions vs market vs benchmark).

### What to do first, and why

1. **Home with three curated lenses** — keep Account as default; add Asset class and Liquidity.
2. **Performance explainability** — attribution and benchmark on Analytics, not a prettier line on Home.
3. **Whose + export** — tax / accountant cut without a fourth home.
4. **PE / illiquid depth** — commitments, calls, coverage. For the 10–15%, not a new default.

### What not to focus on

- Open-ended dashboard builder or drag-your-own categories.
- Replacing the current home for the ~85%.
- In-app trading, stock pages, or a daily-PnL aesthetic.
- Children / next-gen, advice-on-the-curve, live-action status (already shipped).
- A whole-app redesign or a second UHNW product.

### Assumptions

- The current account list is the right default.
- Backend can already show the same holdings in another cut.
- Liabilities belong in Asset class and Analytics so totals match headline net worth.
- Benchmark and export fields can be disclosed at a suitable level.

### Still open

- Compliance wording on the benchmark.
- Trust / SPV in MVP vs later.
- Notification governance for decision cards.

### Where to start

- Home, same as today, with one extra control: three lenses plus Whose.
- If the default list still feels like the current app, the 15% can stay in-product without teaching the 85% a new one.

---

## Deliverable 2: Prototype talking sheet

Scan left = what this frame does. Right = the locked rule that does not change.

---

### 1. What problem does this prototype solve?

| This frame | Locked decision |
| --- | --- |
| One Home, one total, three ways to group the same book. | The mismatch is a high-value minority, not a majority IA failure. |
| Account stays the default list, with the old category names. | Most clients love the app as-is and do not love change. |
| Asset class and Liquidity are opt-in cuts of the same £8.42m. | Productise the monthly PE / sophisticated PDF, not a second product. |
| Whose sits in the header, not as a fourth home. | Joint households need All / Mine / Partner’s / Joint for tax, across every view. |

---

### 2. Who is it for, and what stays the same for everyone else?

| This frame | Locked decision |
| --- | --- |
| Fictional client: Jeanne, net £8,420,000, joined 15 Feb 2025, adviser Priya Shah. | One household, figures reconciled. Not a demo of many personas. |
| Agreed risk 70; mix ~63 as calm copy, not an amber warning. | Health-tracker tone. Do not scold a market-check open. |
| Account list still uses Investment and cash accounts, properties, PE, collectables, EIS, liabilities. | Default path is the current app. Empty types stay hidden. |
| Asset class and Liquidity sit next to the total, not behind a first-run tour. | Let the 10–15% find it. The ~85% must not feel the app changed. |

---

### 3. How is Home structured, and why this order?

| This frame | Locked decision |
| --- | --- |
| Title is **Net worth**. No greeting. | This is a book, not a chat. |
| Gold Analytics icon in the header, distinct from the teal privacy eye. | Analytics is a destination, not a Home card. |
| Whose chip in the header: All / Mine / Partner’s / Joint. | Ownership is household-wide, not buried in Filter. |
| Download icon only in the header. No Export chip. | Export follows the current view. It is not a Filter control. |
| Filter chip in the sticky bar: class / account / access. | Filter is what is in the book. Not dates, not Whose, not Compare. |
| Headline £8.42m, period delta since joining, then `Risk mix 63 of 100 · agreed 70`. | Total is net of liabilities (−£2,802,531). Never label gross £11.22m as Total. |
| Net-worth chart, then From / To plus a draggable brush under it. | Date lives under the chart. No 6M / 12M / 3Y / 5Y / YTD pills. |
| **Net contributions** as a static row. No chevron, not a link. | Contributions are a readout on Home. Interpretation lives on Analytics. |
| **Market quick look** next: public indices in %, PE “No new valuation”. | Market look is market %, not a £ forecast of Jeanne’s book. |
| Then three lenses: Account / Asset class / Liquidity. Then the list. | Lenses sit next to the money, not buried down the page. |
| **+ Add a note** stays after the first save. | Notes are per screen. Adding again stays available. |

---

### 4. How do the three lenses work?

| This frame | Locked decision |
| --- | --- |
| Account (default): **Accounts and properties**, old category names, Total £8.42m. | Formal names only: Account / Asset class / Liquidity. Not “What it is” / “When usable”. |
| Asset class: donut plus Equities, Bonds, Cash, Property, PE, collectables, EIS, Liabilities. | Same money, regrouped. Liabilities as a negative so the list totals to the headline. |
| Liquidity: **Available within days** vs **Long term, 8 to 12 years**, plus Liabilities as mortgages. | PE two-portfolio cut. Liabilities are not an access bucket. |
| Cash vs PE uncalled commitments shows coverage, not a ticker. | Planning question: can I meet the next call? |
| Switching lenses does not change the £8.42m total. | Same book, three groupings. Never a second, gross total. |

---

### 5. How do Whose, Filter, Date, Compare, and Export stay distinct?

| This frame | Locked decision |
| --- | --- |
| **Whose:** header pill opens All / Mine / Partner’s / Joint, each with a £ figure. | Whose is never inside Filter. Joint is not the household total. |
| **Filter:** one chip. Sheet is asset class, account, and access speed. | One chip = class / account / access. Not dates, not Compare, not Whose. |
| **Date:** From / To fields plus a draggable brush under the chart. | Brush must stay draggable. No range pills. |
| **Compare:** chip under the Analytics graph. Extra curves on by default. | Compare is not a Filter. Curves: total, Y TREE benchmark, invested capital, dashed projection to ~Feb 2027. |
| **Export:** header download icon → CSV of current Whose / Filter / window / tab. | No Export chip. Official statement is a compact placeholder link, not an invented PDF body. |

---

### 6. What does Analytics explain that Home does not?

| This frame | Locked decision |
| --- | --- |
| Title is **Analytics**. Gold Home icon returns you. | Home keeps the total, brush, contributions, market look, and lenses. |
| **Total value** chart with Compare chip; extra curves on by default. | Compare lives here. Projection is illustrative, dashed, to ~Feb 2027. |
| **Net contributions**, then **Benchmark comparison** (yours vs Y TREE). | Attribution starts here, not on Home. |
| **Performance explained:** collapsed, down arrow, one column. | Open it: choices in the portfolio, then market traction. |
| **What we advise:** pending Priya item with Review, or mix within agreed risk 70. | Reassure, not a task list. |
| **Risk distribution:** cash and gilts low, property 37, Apax 113, EIS 213. | Same money cut by risk so 63 is an average. Preset only. Not a fourth home lens. |
| **Composition:** stacked bars, cadence filter, mortgages below zero. | Bar height = total. Needs regular review vs Long term. Total is £8.42m. |
| **Table:** default columns are Time. | Other dims: Asset class, Account, Whose, Liquidity. Same window as the chart. |
| Notes + **+ Add a note** at the bottom. | Same note pattern as Home. |

---

### 7. How do drills treat illiquids / PE / cash / property without becoming a trading app?

| This frame | Locked decision |
| --- | --- |
| Shared drill: lighter chart, From / To + brush, Performance YTD / ITD and £ / %. | Same skeleton. Not a new product per asset type. |
| Bonds / Equities: instrument first, subtitle **Held at [wrapper]**. | No Revolut / stock pages. Custody is a line, not the primary IA. |
| Citi Private Bank: cash pots Spending / Savings / Personal, limited-data banner. | Account drill stays a custody view, not a trading terminal. |
| Property: value, mortgage, equity. Cashflow is income, not a second valuation. | Property is statement-driven, not daily-priced. |
| PE list: committed / called / uncalled, cash vs Q4 call, next-5-years bars. | PE keeps its data shape. Not a listed ticker. |
| PE fund: NAV, statement date, IRR / MOIC / TVPI / DPI. | Copy the old PE screen. Private equity ≠ EIS. |
| Collectables: last valued date, no daily chart. | Cadence is valuation, not a market sparkline. |
| EIS (Private investments): holding + statement link, risk 213. | Separate from PE funds. |
| Liabilities: Coutts mortgages, next payment, end date. Negative in every total. | Mortgages sit in the book so grouped totals match headline net worth. |
| Official statement: compact icon → placeholder issuer link. | Do not invent PDF bodies. |

---

### 8. What did we deliberately not do?

| This frame | Locked decision |
| --- | --- |
| No 6M / 12M / 3Y / 5Y / YTD pills on any chart. | Date is From / To + brush only. |
| No Export chip. No Whose inside Filter. | Five jobs, five controls. |
| No greeting on Home. No Analytics essays on Home. | Home = am I okay. Analytics = why did this move. |
| No custom dashboard builder. No drag-your-own categories. | Presets only. Full customisation is a massive lift. |
| No in-app trading. No Revolut / stock pages. | Y TREE shows holdings. It does not operate them. |
| No advice plotted on the wealth curve. | Out of scope. They are exploring it later. |
| No children / next-gen. No whole-app redesign. No live-action rebuild. | Stay on portfolio view. Live actions already shipped. |
| Brush stays draggable. | Date control is a window, not a preset pill row. |
