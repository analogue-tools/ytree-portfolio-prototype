# Y TREE — problem and where to start

One page of context for the prototype. Source: interview with Calum Cammack, 25 Aug 2026. Not a second product.

**Prototype:** `C:\Users\jeann\.claude\ATclaude0308\index.html`  
**Annotations:** left panel of that file, live per screen.

## Problem framing

Y TREE already gives clients a complete picture of their wealth. The mobile app is how most of them see it. That picture is organised into **one structure Y TREE designed**: by account / where the money is held (Fidelity GIA, HL SIPP, the London house…). There is **one path** through it.

Over the past year, clients have said this is **not how they think about their money**. That is not a majority complaint. A lot of clients **love the app as it is** and **do not love change**. The mismatch is concentrated, and it is specific.

Three different “doesn’t match” stories came up. They are slices of the same data, not three products.

1. **Liquid vs illiquid (PE / private-market clients).** They already see two portfolios: cash and listed investments they check when markets move, versus money locked **8–12 years**. They want different information on each, and to compare them. Today the app mixes both into the same account list. The client team already prepares **semi-bespoke reports** that split liquid / illiquid for higher-net-wealth clients. That is a human workaround, not a product.

2. **Asset class vs custody (more sophisticated clients).** They want to start from **% equities vs % bonds** (true exposure across every wrapper), then drill. Today they start from “where it sits” and cannot get that cut without asking.

3. **Mine / partner’s / genuinely joint (joint profiles; less cohort-specific).** Majority of clients are a joint household. There is currently **no way** to see that split. It is asked out of interest and for tax / accountants.

A fourth, quieter problem sits on top of those: **~25% do not use the app**. Their value sits with the adviser, so they are less sticky. Anecdotally, among ultra-HNW / PE discovery, the most common reason is the structure. Calum’s estimate: an alternative portfolio view might only ever be used by **10–15%**. That is the group this change is for.

What this is *not*: people being lost, or wanting a trading app. Y TREE’s philosophy is long-term. Clients still open the app in **volatile markets** to see how the world affected *them*. Equities and bonds reprice daily; PE may update every six months. The app should respect both cadences.

## Prioritisation

**Do first.** Productise the reports the team already writes: **keep today’s account path as the default**, and add **two opt-in presets** (investment type; access speed) plus a **whose-assets filter**. Introduction is the product decision. Interested users must find it; everyone else must not feel the app changed.

**Do next, lightly.** Ownership filter already helps the accountant conversation. A simple export is enough to show the workflow. Formal tax-adviser partnership is later.

**Do not focus on now**

- Open-ended customisation / drag-your-own categories (Calum: massive engineering lift and data-quality risk; presets are fine)
- Replacing the current home for the ~85%
- In-app trading
- Children / next-gen (Calum: out of scope)
- Advice plotted on the wealth curve (they are exploring it; not this exercise)
- Live action status (already shipped to cut “what’s happening?” chat)
- First-year leavers who wanted active trading (philosophy filter, not IA)
- A whole-app redesign, extra tabs, or a second product for UHNW

## Assumptions

- The current account list is the right default. Changing it would harm more people than it helps.
- The 10–15% overlaps the less-sticky, higher-value clients who today get a PDF.
- Backend can already show the same holdings in another cut (Calum: assume any format).
- Literacy varies. Sports people and some senior lawyers may know little about personal finance; some PE clients want every number. Same app. Depth belongs on the optional views, not on the default list.
- “Whose assets” is a filter, not a fourth home.

## Outstanding questions

Calum does not have complete data on: why non-app users prefer humans (anecdote only); referral mix; accurate tenure; how many people want liquid/illiquid vs asset class; how many receive bespoke reports; literacy distribution; PE base rate. Also open: compliance wording on approve / benchmark, and whether trusts / liabilities belong in v1.

## Where to start

**Home, same as today, with one extra control.**

Start there because that is the problem they named: one path, wrong for a valuable minority, dangerous to change for everyone else. If the default list still feels like the current app, and two presets plus “Whose” productise the reports, the 15% can stay in the app instead of waiting for Priya’s PDF without teaching the other 85% a new product.

**Analytics (what ships).** Line is the default graph. Filter, Account, Date and Compare stay visible at rest. After the performance quartet, Risk distribution shows the same money cut by risk. Composition is stacked bars by asset class (bar height = period total, mortgages below zero so the total is £8.42m) with a cadence filter: Needs regular review (equities, bonds, cash) vs Long term (property, business, PE, collectables, private investments, mortgages). Table is a pivot. The From / to + brush date control sits directly under the chart.
