# Deliverable 1: the problem, and where to start

## The problem

- The app shows a client's wealth one way: grouped by account, by where the money is held. One path through it, no way to re-sort.
- A valuable minority, roughly 10 to 15 percent by Calum's estimate, do not think that way. Three mismatches:
  - Private-equity clients hold a liquid portfolio and one locked for 8 to 12 years, and want them kept apart, not merged in one list.
  - Sophisticated clients navigate by asset class, not by custody, and want exposure across every wrapper before drilling in.
  - Joint profiles, which are most clients, cannot isolate Mine, Partner's or Joint for tax or an accountant.
- All three are handled today by hand-built PDFs from the client team.
- Separately: about a quarter of clients never open the app. The value sits with the adviser, and those clients are the least sticky.
- The common thread is one mindset: the client wants a single, centralised tool that works the way they already think.

## The shape of the fix

```
NET WORTH  £8,420,000
│
├─ Perspective   pick one, the total does not change
│     Account        default, the current app grouping
│     Asset class    composition
│     Liquidity      time to cash
│
└─ Ownership scope   narrows whichever perspective is active
      All  ·  Mine  ·  Partner's  ·  Joint
```

- Ownership is a scope, not a fourth perspective. It sits in the header and narrows whichever perspective is active.

## Principles

- Meet the client's mental model rather than ask them to learn Y TREE's filing system. The product is modular: it offers perspectives, it does not impose one.
- Keep the account view as the default. The majority like it and resist change.
- Macro first, then an optional micro dive into why performance moved. That is the bet on financial literacy, and literacy is what keeps the less engaged clients in the app.
- Move the interface only where a new perspective or a control needs the room. Leave the rest.

## Prioritisation

1. Home: account view as the default, plus two opt-in perspectives (Asset class, Liquidity) and an ownership scope. Productises the manual PDF; the 85 percent keep the view they know.
2. Export of the current view, and an Analytics screen for the client who goes looking: performance explained, composition, a pivot.
3. Depth for the 10 to 15 percent: private-equity commitments, calls and coverage; property as both an asset and a cashflow. The same drill structure the app already uses.

## Not now

- Open-ended dashboard building. Large build, real data-quality risk.
- Removing or demoting the account view.
- In-app trading. A philosophy filter, not an information-architecture gap.
- A dedicated tax tool or other product expansions. The ownership scope covers the tax conversation for now.
- Tiering: which features reach which client tier. A commercial decision, not modelled here.
- Children and next generation. Real, out of scope for this exercise.

## Later, if the appetite is there

- Advisory-report social proof next to a holding or a decision. Reassures, and heads off the "let me check with someone" instinct. Risk: accountability, since third-party opinions inside Y TREE's product raise "who stands behind this".
- A teaching notification: a short, periodic "what moved, and why". Feeds the literacy loop. Risk: tone and frequency, it must read as a health update, not a market alert.

## Assumptions

- The backend can return the same holdings in another cut, in any format.
- The 10 to 15 percent overlaps the less sticky, higher-value clients who get a PDF today.
- Grouped views must reconcile to net worth, with liabilities inside the cut.
- Financial literacy varies. Depth belongs on optional views, never the default.

## Open questions

- The real split: liquid against illiquid, against by asset class, and how many clients receive bespoke reports.
- Why the clients who avoid the app prefer a human. Anecdote only.
- Compliance wording on the benchmark, and on "approve".
- Whether trusts and SPVs belong in version one.
- Y TREE's own client-facing voice. All copy in the prototype is placeholder.

## Where to start

- The Home screen, with one added control: the account view still the default, one tap from the other two. It is the mismatch clients named, and the lowest-risk place to hold the line between the 85 percent and the 15 percent.
