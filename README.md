# Y TREE: the same wealth, three lenses

Take-home for a Mobile Product Manager role at Y TREE (an FCA-regulated wealth manager).

## The problem

Y TREE's app shows a client's wealth one way: grouped by which institution holds each
asset, with one path through it and no way to re-sort. A minority of clients, mostly
private-equity professionals and other sophisticated investors (and the ~25% who bypass
the app for a hand-made monthly report), think in **asset class** and in **how quickly
they can reach their money**. Joint-profile clients also want to split the total by
**owner** for tax.

The catch: ~85% like the app as it is and dislike change, and full user customisation is
a large engineering lift. So: a small set of preset lenses, opt-in, default untouched.

## The solution in this prototype

One home screen with three view states, plus one drill-down:

- **By provider.** The current default, unchanged. For assets not priced daily it shows
  the last valuation date, never a day-to-day change.
- **By asset class.** The same wealth combined across every provider. A labelled pie and
  a table. Tapping *Equities* opens the drill.
- **By liquidity.** Two buckets, Liquid vs Locked, each with its own check-in language,
  plus "what you could reach now, before tax".
- **Whose assets.** All / Mine / Partner's / Joint, recomputes every view. One tap to
  "prepare a statement for your accountant" (replacing the client team's manual monthly PDF).
- **Equities drill.** Every equity holding you own, combined across providers. The one
  place total exposure to a single fund or company is visible.

The two new lenses are introduced with a single dismissible line. The home leads with a
calm status ("everything is on track, the next thing that needs you is…"), not a chart,
in line with Y TREE's stated "health tracker" direction.

## Run it

Single self-contained `index.html`, no build.

- Open it in a browser, or serve the folder (`npx serve`), or
- Deploy as a static site. Framework preset **Other**, no build command, output dir `.`.

### Vercel

vercel.com/new, import this repo, choose Other, no build, output `.`, then Deploy.

## Design

- Warm near-black app on a warmer, darker "desk"; one accent only (warm gold `#C69A4E`,
  deliberately not blue).
- Fraunces for currency figures and headings, Inter for UI.
- 17px base, 44px tap targets, colour never the only signal (every pie segment is
  labelled and in the table), no gamification, "not financial advice" footer.
- Desktop shows the app in an iPhone-proportioned frame with one context panel; below
  1000px it fills the screen.

## Data

One fictional client, ~£8.42m, reconciled across every view. Near the top of the
`<script>`: `LEAF` (`[providerGroup, account, owner, assetClass, liquidity, value]`),
`GROUPS`, `AC` (asset-class colours), `EQ` (the equities drill).

## History

Earlier commits contain a much larger exploration (~18 screens: analytics, messages,
pivot builder, notes, currency switch, active/passive slices, etc.). That was cut back
deliberately: the assignment rewards one focused solution with exceptional UX and
clarity, not a whole app. `git log` has the full version if any of it is worth
re-introducing.
