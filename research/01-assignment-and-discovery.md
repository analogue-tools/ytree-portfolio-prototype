# Research brief — Y TREE Mobile PM take-home

**Source of truth:** Calum Cammack interview, 25 Aug 2026 (~50 min), plus assignment email and take-home brief.
**Gemini notes:** treated as lossy; corrections in **C.9**.
**Convention:** *Fact* = Calum/email/brief said it. *Inference* = recommended interpretation. Numbers only as spoken.

---

## A. What the assignment is

### Company, product, role

**Y TREE** is a UK wealth manager. Product job: a **complete picture of a client’s wealth** — pension, ISA, private equity, company shares, property, art. The **mobile app** is where most clients see that picture and navigate it.

Hiring for **Mobile Product Manager**. Calum is Head of Product; the session treats him as proxy for client team, advisers, design, and engineering.

### Problem as framed *before* discovery vs *after*

**Before (assignment email):** The app organises wealth into a **Y TREE-designed structure with essentially one path**. Over the past year, clients have said, in different ways, that **this is not how they think about their money**. Take-home = propose solution(s). Session = real investigation, not a pitch.

**After (interview):** The mismatch is **not universal**. It is concentrated among **higher-net-wealth / sophisticated / PE** clients, and it is **specific**:

1. **Liquid vs illiquid** as two portfolios (PE example, ~00:30–31:40)
2. **Asset class vs custody** (where money is held) (~00:32:49)
3. **Mine / partner’s / genuinely joint** on a joint profile (~00:33:52)

Workaround today: **semi-bespoke monthly reports** for higher net wealth, prepared by the team (~00:14:56, ~00:36:00). Engineering: **preset views OK; full customisation not** (~00:36:51). Product constraint: **majority love the app as-is and don’t love change**; new portfolio-view functionality **might only be used by 10–15%** — Jeanne linked this to the 25% non-app users; Calum agreed (~00:47:21).

*Inference:* Pre-session framing sounds like “the IA is wrong for clients.” Post-session it is “the IA is right for most; it is wrong for a high-value minority, and changing it carelessly would harm the majority.”

### Who it is for

**Users (product):** Main clients — not children for this exercise (~00:04:08). Majority joint profiles (~00:10:42). Two overlapping groups:

- **~75% monthly active** who already use the app and (Calum emphasises) **a lot of them love it as it is** (~00:12:49, ~00:47:21)
- **~25% who do not use the app**, relying entirely on human advisory (~00:12:49–13:53). Anecdotal reason among ultra-HNW / sophisticated / PE: structure doesn’t match how they view assets (~00:14:56). Calum agreed this maps to the 10–15% who would want an alternative portfolio view (~00:47:21)

**Evaluators:** Calum (and likely design/product peers). They are not testing wealth-management knowledge. They are testing **how you approach a problem, run discovery, and think about the people using the product** (email). On the call: **document is not the main focus**; **high-quality design of a few main screens** is (~00:39–44).

### Two deliverables and what “good” looks like

**Deliverable 1 — Problem statement and prioritisation** (brief says cover all of this; Calum says **short context, ~one page**, so he knows what you’re solving):

- Problem framing from what was *heard* — exact problems, themes, groupings
- Prioritisation: what matters most and why; **what Y TREE should NOT focus on**
- Assumptions and outstanding questions
- Where to start, and why

**Deliverable 2 — Solution prototype:** tangible digital experience for the chosen problem(s). **UX is most important.** What’s on each screen and why; user’s mindset (thinking, feeling, needing) at that moment. Considered, not generic. Annotations OK.

Calum’s bar for the artefact:

- **2–5 main screens**, interaction design, information hierarchy, layout — **not a whole app**
- **ONE well-designed solution** over many
- Don’t spend huge time; **don’t care about engineering for this exercise** (assume you can show data in any format, ~00:28:57)
- Wacky / out-of-product ideas can live in the doc as later
- PM craft: **copy, how much info to show, what to hide, how to introduce features without confusing users who don’t need them**

### Hard constraints and anti-goals

| Do | Don’t |
|---|---|
| Stay on **portfolio view** (~00:47:21) | Rest of the app |
| **Presets**, not open-ended customisation (~00:36:51) | Full user-defined structure |
| Preserve path for people who **love it as-is** | Force a new IA on everyone |
| Focus on **main clients** | Children / under-18 onboarding (~00:04:08) |
| One considered solution, 2–5 screens | Many concepts, whole-app redesign |
| Short written context | Document-as-the-deliverable |
| Optional / later: tax reports, advice-on-trajectory | Engineering feasibility theatre; in-app trading |

### How they will score

Assessed on: **depth of problem understanding**, **solution thinking grounded in the problem**, **prototype quality**, **UX (most important)**, **clarity of communication**.

**Anti-AI-slop:** they will review closely for **nuance from the interview** — tensions, current journey specifics, attention to detail. Generic wealth-app screens will score poorly.

**People-thinking:** not “HNWs want dashboards.” It is: different financial literacy, different asset-type engagement, majority vs minority, joint household, philosophy vs actual open-the-app behaviour.

### Role signal

Designers create a **toolkit**. The PM **organises components, copy, density, hide vs show, and how to introduce features without confusing users who wouldn’t use them — while letting interested users know**. That *is* the job this exercise is sampling.

---

## B. Stakeholders and tensions

### Map

| Stakeholder | What they care about (from Calum) |
|---|---|
| **Client team / advisers** | Chat (WhatsApp group); recurring “what’s happening / when’s this coming in”; explain the portfolio; semi-bespoke reports for higher NW; advice 3–4×/year through the app; first-year leavers if service isn’t what they wanted |
| **Design** | Toolkit; screens; hierarchy; introducing optional views without confusing the rest |
| **Engineering** | Current structure is **partly legacy**; backend work needed but easier now. **Preset views = fine. Complete customisation = massive lift + data-quality problems** (~00:28:57, ~00:36:51) |
| **UHNW / sophisticated / PE** | App “doesn’t reflect how they view their assets”; get **team-prepared reports**; pay more (~00:14:56, ~00:36:00) |
| **Mass of clients (love-as-is)** | Single path; only see asset types they have; don’t love change (~00:24:25, ~00:47:21) |
| **Joint partners** | Majority of accounts; currently **no way to see what I own vs my partner** (~00:10:42, ~00:33:52) |
| **75% MAU** | Use the app; main interaction; client-driven outside advice/actions |
| **25% non-app** | Rely **entirely on human advisory**; value attached to advice not digital → **less sticky** (~00:13:53) |
| **10–15% “would ever want this view”** | Calum’s estimate for alternative portfolio functionality; Jeanne linked to the 25%; Calum agreed (~00:47:21) |
| **Children 18+** | Same app, different controls; **tend not to use it; out of scope** (~00:04:08) |
| **Tax advisers** | Informal today; future: pre-prepared reports; “most boring but high workflow stickiness / churn reduction” (~00:34:54) |

### Explicit tensions (fact unless marked inference)

1. **Health-tracker philosophy vs daily check in volatile markets.** Philosophy: long-term, “close your phone and not look for a year” (~00:09:50). Behaviour: **volatile markets = main reason clients open the app** — see how world events affect *them* (~00:07:26). Strategy is *moving toward* health-tracker (“Am I as efficient as I possibly can be?”) while still showing the detail for people who want it.

2. **Love-the-app-as-is vs structure-doesn’t-match.** “A lot of clients love the app as it is. Not universal. Clients don’t love change.” (~00:47:21) vs year of feedback that the structure isn’t how they think about money (email) and PE/sophisticated discovery (~00:14:56, ~00:30:23).

3. **Bespoke reports that don’t scale.** Higher NW get reports that *do* match mental models (liquid/illiquid; asset class). Majority do **not** receive regular reports (~00:45:17). Reports are a human workaround, not a productised view.

4. **Simplify balance sheets vs PE complexity as wealth grows.** “Generally join with MORE complicated balance sheet; Y TREE makes it simpler.” Exception: as they get wealthier they get PE / private markets they couldn’t access before (~00:23:32). Noise **grows as you have more types** (~00:24:25).

5. **75% MAU vs 25% human-only vs 10–15% alternative view.** Strong digital engagement overall (“pretty good for fintech”) *and* a non-trivial group whose value is advice, not the app — **less sticky**. The new view is for a minority, but that minority overlaps the less-sticky / higher-pay group. *Inference:* solving for 10–15% is a retention/value play, not a majority-UX play.

6. **Show everything vs hide for people who don’t need it.** PM judgment Calum called out: introduce without confusing users who wouldn’t use it; let interested users know without distracting others (~00:39–44).

7. **Detail-focused sophisticated clients vs low personal-finance literacy.** Same app. Sports people / some lawyers can “know nothing about money”; some clients want “all models, calculations, every number.” General rule (not always true): **higher net wealth → more financially sophisticated and detail-focused** (~00:05:07–06:15).

8. **Cannot trade in-app vs desire to see exactly what you hold.** Trading happens at InvestEngine etc.; Y TREE **shows** the account and breakdown (e.g. 200 units of Apple + a tracker), not just “money in Wise” (~00:21:31).

9. **Advice lives in profile, not beside the wealth trajectory.** Backlog of tailored advice exists; “cannot currently see advice alongside the wealth trajectory curve”; exploring it; “one day that’s the idea”; high accountability (~00:48:28). Out of scope for the exercise but strategic.

10. **Empty categories already hidden vs “customisation.”** “That’s basically customisation if you like — you only see the asset caches that you have.” (~00:24:25) That is **presence/absence**, not **re-slicing**.

---

## C. Structured discovery findings

### 1. Who the people are

Grounded personas (not generic “HNW”):

**A. The PE professional (sophisticated, often younger-career or mid)**
Career mix: “lots of PE professionals” (~00:01). Often financially sophisticated, but **some don’t know lots about personal finance** (different area of finance) (~00:05:07). Risk: high, money locked long time (~00:19:24). Significant money in **their own PE funds — illiquid, locked 8–12 years**. They see **two portfolios**: liquid vs illiquid; want different metrics; illiquid “should in theory get higher returns”; want to **compare** the two. Liquid = check regularly; illiquid doesn’t change much (~00:30:23–31:40).

**B. The senior lawyer / professional-services director (high success, variable literacy)**
“Senior lawyer partners; senior directors in professional services.” Some “highly successful but personal finance literacy can be low.” Opposite risk story: “senior lawyers with all money in cash after 20 years” (~00:19:24). Education journey: higher risk might mean retire earlier.

**C. The CEO / founder**
Named in the career mix (~00:01). No extra behavioural detail from Calum.

**D. The professional sportsperson (smaller proportion, younger)**
30s; “can know nothing about money” (~00:01, ~00:05:07).

**E. Age / life stage (distribution, not a persona)**
Normal distribution **peaking around 50**. Most clients last 10 years of career (50s, 60s) **plus many retired**. Long tail to ~**85**. 30s–40 **maybe ~15%**. Sports people pull the younger tail (~00:01–03:13).

**F. The household, not the individual**
**Majority = joint profile.** “If they have a partner it’s very unusual they won’t be on the platform.” Plan for the **family unit**. Mix of made-own-money and inheritance; lots of conversations about passing wealth (~00:04:08, ~00:10:42). On death: if partner, they already joined as joint; **stays with partner who decides** whether to stay. If single, work with family; usually hear from family (~00:03:13).

**G. Children 18+**
Same app, different controls; **tend not to use it as much. Out of scope.** (~00:04:08)

**H. Detail-seekers vs health-check users**
Same product, opposite info appetite. General rule: higher NW → more detail-focused; exceptions (less-wealthy, earlier career, very sophisticated) (~00:05:07–06:15).

**Literacy:** “varies a lot.” Do not design as if all clients are PE-fluent.

---

### 2. Jobs-to-be-done / moments they open the app

| Moment | Cadence / trigger | Mindset (Calum’s language) |
|---|---|---|
| **World-events / markets check** | Equities/bonds priced daily. **Volatile markets = main reason they open the app** (~00:07:26) | “See how world events affect THEM.” Liquid side. |
| **Long-term allocation / PE** | PE / unlisted: **maybe updated every 6 months**; “less to look at daily” (~00:07:26) | Long-term allocation thinking; illiquid “check less often” |
| **Efficiency / “health tracker” (intended future)** | Strategy direction, not current primary open-reason (~00:09:50) | “Am I as efficient as I possibly can be? Is there anything I could be doing…?” If everything is green → OK. Ignore today’s ±5%. |
| **Advice / action** | **Most clients average 3–4 times/year**; some more, some once a year (~00:45:17) | Sign a form, approve advice, update a balance they don’t have access to |
| **Chat / “what’s happening”** | Recurring in WhatsApp group with client team (~00:27:49) | What’s happening with this, when’s this coming in, I don’t understand this (portfolio) |
| **Live actions on home** | Feature released (not on the old demo) to **counter** those chat questions (~00:27:49) | Something is in progress — don’t need to ask |
| **Client-driven life change** | Outside scheduled advice (~00:45:17) | Questions, call with adviser, life change |
| **Notifications** | **ONLY** for: need to do something, chat message, or advice. So **~3–4 times/year** (~00:45:17) | Not a daily-alert product |

**Main interaction = the app, as frequently as they like.** Majority do **not** receive regular reports. Client team reaches out with updates/questions on chat (~00:45:17).

**First-year job (stickiness):** “If engaged and find value in first couple of years, they stay long term.” Leavers often **within first year**: service wasn’t what they wanted, **or they wanted active trading** (not Y TREE philosophy) (~00:12:49).

---

### 3. Mental models of wealth (“doesn’t match”)

Calum: **“Everyone sees wealth slightly differently.”** (~00:32:49) Words they use: balance sheet, total balance sheet, wealth, portfolio — **usually “portfolio”** (~00:25:27).

**Current Y TREE model (one path):** categories by **account / asset cache / where money is held**. Demo: investment cash accounts, residential property, business interests, etc. Drill: account types → investments and cash accounts → e.g. **Citi Private Bank (one of your portfolios)** → analysis and charts. **“Set route.”** (~00:24:25–26:52)

**Mismatch A — Liquid vs illiquid (PE, most concrete)**
“They see portfolio as TWO portfolios: liquid (cash + normal liquid investments) vs illiquid.” Want **different performance metrics and information**. Illiquid should in theory get higher returns. Want to **compare liquid vs illiquid**. Current structure **doesn’t reflect this — they just want those two main buckets.** (~00:30:23–31:40)

**Mismatch B — Asset class vs custody (more sophisticated clients)**
Current: “Investment and cash accounts split by **WHERE money is held** (four different places).” Feedback: navigate by **ASSET CLASS not custody**. From the screen: entire portfolio split **% equities vs % bonds**, then that route. When in equities, all equities info, **then maybe split across providers at that level.** (~00:32:49)

**Mismatch C — Ownership on joint profiles (less cohort-specific)**
“Currently no way to see what I own vs my partner.” Helpful **out of interest AND for tax/accountants**. Filter: **my assets / partner’s / genuinely jointly owned.** (~00:33:52)

These are **different slices of the same data**, not three unrelated products. *Inference:* presets that re-cut the same portfolio, not three apps.

---

### 4. Current journey and information architecture

**Home / portfolio view (demo, slightly old)** (~00:24:25–26:52)

- Categories: investment cash accounts, residential property, business interests, etc.
- **If no PE, you don’t see PE section.** Some clients: just investment/cash + maybe property.
- Noise grows as you have more types.
- **No way to resort / filter / view data differently.**
- Drill: account types → investments and cash → provider/portfolio (e.g. Citi Private Bank) → analysis and charts.
- **PE fund view is a different data shape:** committed, what’s coming up next 5 years, PE-specific performance metrics. All set. No way to change categories or navigate differently.

**Home additions (not on demo):** live actions in progress — to reduce “what’s happening / when’s this coming in” chat (~00:27:49).

**Chat:** WhatsApp group with client team. Also a feedback channel (“I don’t understand this (portfolio)”).

**Advice:** through the app as needed. Lives in **profile section**, tailored to what they’re trying to achieve (invest excess cash, move accounts, reallocate). **Cannot currently see advice alongside the wealth trajectory curve** (~00:48:28).

**Notifications:** actions, chat, advice only (~00:45:17).

**Prospect / join journey (context, not in-app IA)** (~00:17:14): pitch → try-before-you-buy analysis of current providers vs most efficient solution (almost always over 3–5 years they realise they’re losing money) → high-level life strategy / wealth trajectory (age vs wealth) → show the app: everything in one place.

**Risk implementation** (~00:20:30): they choose a risk level → distributed asset selection. **100 = all diversified equities. 30 = smaller % equities, cash equivalents, bonds.** Always: most efficient solution they have access to + a risk level. Some 100% in; some in stages; some keep a sleeve for their own active trading (e.g. 80% to Y TREE).

**Trading:** cannot trade on Y TREE app. External provider; Y TREE **shows** holdings in detail (~00:21:31).

---

### 5. Evidence of pain

| Evidence | What it is | Strength (Calum’s own) |
|---|---|---|
| Discovery interviews with **ultra-HNW / sophisticated / PE** | Most common reason they don’t use the app: **doesn’t reflect how they view their assets** (~00:14:56) | Anecdotal; “incomplete data” on why they prefer humans |
| **Semi-bespoke reports** for higher NW | Team shows wealth the way they think — e.g. PE report **split liquid/illiquid**; other clients **by asset class** (~00:36:00) | Direct product-workaround; only for higher NW |
| **Chat** | Recurring: status of actions; “I don’t understand this (portfolio)” (~00:27:49) | Qualitative ops signal; they already shipped live-actions for the status part |
| **25% non-users** | Rely entirely on advisory; value on advice not digital → less sticky (~00:13:53) | Usage fact; *reason* is incomplete |
| **Calum: 10–15%** would ever want this portfolio view; Jeanne linked to the 25%; he agreed (~00:47:21) | Estimate, not measured | Directionally: minority, high value |
| First-year leavers | Service mismatch **or wanted active trading** (~00:12:49) | Related but **different problem** (philosophy, not IA) |
| Email framing | Year of clients saying structure isn’t how they think about money | Consistent with interview, not quantified |

**Do not treat “25% don’t use the app” as proven = “because of IA.”** Calum said incomplete data; IA mismatch is the *most common anecdotal reason among ultra-HNW / sophisticated / PE*.

---

### 6. What already works

- **75% monthly active** — “pretty good for fintech” (~00:12:49)
- **A lot of clients love the app as it is** (~00:47:21)
- **Hide empty categories** — only see asset caches you have (~00:24:25)
- **Simplify on join** — generally more complicated balance sheet in → simpler with Y TREE (~00:23:32)
- **Holdings transparency** — see 200 units of Apple + a tracker, not a black box (~00:21:31)
- **Live actions on home** — already addressing a chat-pain (~00:27:49)
- **Referrals / intro language** (Calum **doesn’t have data**; quoting intro emails): “completely different approach”, “refreshing transparent take”, “I’ve been losing/wasting so much money last 15 years, wish I’d come to Y sooner.” (~00:16:06)
- **Try-before-you-buy efficiency analysis** — almost always over 3–5 years they realise they’re losing money vs most efficient solution (~00:17:14)
- **Churn below 5%/year**; if value in first couple of years, they stay; theoretical lifespan **~20–22 years from churn math** (they **don’t have accurate tenure** yet) (~00:11:41–12:49)
- **Joint household as default** — unusual not to have partner on platform (~00:10:42)
- **Philosophy fit as a filter** — people who wanted active trading leave; that’s working as designed (~00:12:49)

---

### 7. Business / product strategy context

- **Long-term investing, not beating the market every day.** “What do you want to achieve in your life? We’ll set your risk targets to achieve that.” (~00:09:50)
- **App strategy moving toward health-tracker / efficiency**, while still showing detail for people who want it. Green = OK; today’s ±5% shouldn’t matter if you’re keeping up with the market long term.
- **Always recommend most efficient solution + a risk level.** Efficiency is the commercial and advice spine (prospect analysis, referrals about wasted money, future “am I efficient?”).
- **No in-app trading.** External accounts are *shown*, not operated.
- **Y TREE PE / private markets fund** — need certain wealth; locked up; higher entrance fee (~00:23:32). This is how complexity *increases* with wealth.
- **Tax:** no official partnership yet; future more formal; send pre-prepared reports; boring but **workflow stickiness / churn reduction** (~00:34:54). Ownership filter is adjacent.
- **Advice + trajectory together** = “one day that’s the idea”; high accountability (~00:48:28). Not this exercise.
- **Value of non-app clients sits in human advice** → less digitally sticky (~00:13:53). Making the app match their mental model is a **stickiness** play for people who currently prefer the PDF/report.

---

### 8. Constraints

**For the real product**

- **Preset views = fine. Complete user customisation = massive engineering lift + data quality problems. Don’t go fully open-ended.** (~00:36:51)
- **Don’t confuse the ~85–90%** who wouldn’t use the new view; clients don’t love change (~00:47:21)
- **Children out of scope** (~00:04:08)
- Current IA is **partly legacy architecture** (~00:28:57)

**For this exercise**

- **Assume you can show the data in any format you want** (~00:28:57)
- **Don’t worry about engineering**
- **Don’t worry about the rest of the app; keep focused on portfolio view** (~00:47:21)
- Short written context; **2–5 screens**; one solution
- Don’t spend huge time

---

### 9. Gemini note corrections

| Gemini note | Verdict vs transcript |
|---|---|
| Client base: senior lawyers, executives, PE, athletes; age peaks ~50 | **Partial.** Transcript: senior lawyer **partners**; senior **directors in professional services**; **CEOs/founders**; PE; **professional sports people** (younger, 30s, **smaller proportion**). Peak ~50 is right; omitted **50s–60s last 10 years of career + many retired**, **long tail ~85**, **30s–40 maybe ~15%**. “Executives” and “athletes” are glosses. |
| Accounts typically joint; children get access at 18 | **Mostly true.** **Majority** joint; children **once over 18**, same app, **different controls**. Gemini omits: **don’t worry about children; they tend not to use the app as much; focus on main clients.** |
| On death: stays with surviving partner or family | **True but underspecified.** Partner: already joint; **partner decides whether to stay**. Single: work with family on what they want; usually hear from family. |
| Churn <5%; theoretical lifespan 20–22 years | **True**, with caveats Gemini dropped: **below 5%/year**; **don’t have accurate tenure yet**; lifespan is **from churn math**; many clients been there the whole ~10 years of the firm. |
| 75% monthly active; 25% rely on human advisory | **Slightly overstated.** 75% MAU is fact. 25% **do not use the app**; *those* rely entirely on human advisory. The 75% **also** get advice through the app (3–4×/year). Human advisory is not exclusive to the 25%. |
| HNW: current structure doesn’t reflect how they view assets | **Narrowed too far / too wide.** Evidence is **anecdotal from ultra-HNW / sophisticated / PE discovery**. General rule: higher NW → more sophisticated/detail-focused, **exceptions exist**. Not “all HNW.” |
| Referrals: transparency + efficiency analysis | **Lossy.** Calum **doesn’t have referral data**. Intro emails: “completely different approach”, “refreshing **transparent** take”, **wasting money 15 years / wish I’d come sooner**. Efficiency analysis is the **prospect try-before-you-buy** flow, not a measured referral driver. |
| Philosophy: long-term health tracker not daily trading | **Direction, not present tense.** Current philosophy = long-term, not beating the market daily. Health-tracker is **where they want to move the app**. They will **still show all this for people who want it**. Daily opens in volatile markets are real **now**. |
| Equities update daily; PE ~every 6 months | **True.** Equities/**bonds** priced every day. PE/**unlisted company**: **maybe** updated every 6 months. |
| Clients want navigate by asset class; filter individual/partner/joint | **Over-universalised.** Asset class = **more sophisticated clients**. Ownership = **another piece of feedback, less attributed to a particular cohort**. Gemini **entirely omitted liquid vs illiquid** — Calum’s primary “doesn’t match” example. Wording is **my / partner’s / genuinely jointly owned**, not “individual / partner / joint.” |
| Full customisation = engineering challenge; presets feasible | **True.** |
| Prioritize interaction design, info hierarchy, layout; concise 1-page doc | **True**, plus: 2–5 screens, one solution, PM hide/show/introduction judgment, majority love as-is. |

**Biggest Gemini miss:** the **liquid vs illiquid two-portfolio** PE story (~00:30–31:40) and the **10–15% / don’t love change / love-as-is** constraint (~00:47:21).

---

### 10. Outstanding questions / data gaps Calum admitted

He said he doesn’t know, or data is incomplete:

1. **Why non-app users prefer humans** — “Incomplete data”; anecdotal from ultra-HNW / sophisticated / PE only (~00:14:56)
2. **Referrals** — “Calum doesn’t have data” (~00:16:06)
3. **Accurate tenure** — don’t have it yet; 20–22 years is theoretical from churn (~00:11:41)
4. **Whether 10–15% is measured** — stated as “might only be 10–15%”; Jeanne mapped to the 25%; he **agreed** — still an estimate (~00:47:21)
5. **Size of each mental-model cohort** — no split of how many want liquid/illiquid vs asset class vs ownership
6. **How many clients receive bespoke reports** — “only for higher net wealth”; “majority do NOT receive regular reports” — no count
7. **Literacy distribution** — “varies a lot”; higher NW → more sophisticated is a **general rule, not always true**
8. **% of clients who are PE / have illiquid** — PE section hidden if you don’t have it; no base rate
9. **Joint vs single mix** — “majority” joint; no number
10. **Chat volume / “I don’t understand this portfolio” vs status questions** — qualitative only; live actions already shipped for status
11. **Tax-adviser workflow today** — work with them, no official partnership; ownership filter is asserted, not measured
12. **Whether non-use in year 1 is IA vs service vs trading-philosophy** — leavers in first year named service + active trading, **not** IA

*Inference for Deliverable 1:* list these as assumptions/questions; do not invent rates.

---

## D. Problem groupings for Deliverable 1 (candidates, not final priority)

### Theme 1 — Portfolio IA doesn’t match sophisticated mental models
**Who:** PE / ultra-HNW / financially sophisticated; the people who get (or would need) bespoke reports.
**Evidence:** discovery interviews (~00:14:56); PE liquid/illiquid (~00:30–31:40); asset-class vs custody (~00:32:49); reports that already implement these cuts (~00:36:00).
**JTBD:** See *my* wealth the way *I* already think about it, so the app is usable without waiting for a human PDF.
**Severity:** High for a **minority** who pay more and are less digitally sticky; low for the love-as-is majority.
**In-scope for take-home:** **Yes — this is the portfolio-view brief.**

Sub-problems (same theme, different slice):

| ID | Slice | Who | In-scope? |
|---|---|---|---|
| 1a | Liquid vs illiquid as two buckets + compare | PE / illiquid holders | Yes |
| 1b | Navigate by asset class, then provider | More sophisticated clients | Yes |
| 1c | Ownership: mine / partner / genuinely joint | Joint profiles; tax/accountants | Yes (filter on portfolio view) |

### Theme 2 — Optional power vs “don’t confuse people who love it”
**Who:** 10–15% vs everyone else.
**Evidence:** ~00:47:21; PM hide/show/introduction (~00:39–44); engineering presets not customisation (~00:36:51).
**JTBD (majority):** Keep checking the familiar path. **JTBD (minority):** Find a view that matches me without being made to feel the app “changed.”
**Severity:** High *product-risk* if you get introduction wrong — even if Theme 1 is the user pain.
**In-scope:** **Yes — it is the introduction/IA problem sitting on top of Theme 1.** Calum asked for this judgment explicitly.

### Theme 3 — Human workaround (reports) instead of product
**Who:** Higher NW only.
**Evidence:** ~00:14:56, ~00:36:00; majority get no regular reports (~00:45:17).
**JTBD:** Get a view that matches how I think, on my phone, not via the team.
**Severity:** Cost-to-serve + stickiness.
**In-scope:** Yes as *outcome* of Theme 1 (productise the report’s mental model). Not in-scope as “design a PDF.”

### Theme 4 — “I don’t understand this portfolio” / explanation
**Who:** Lower literacy (sports, some lawyers) and anyone lost in the set route.
**Evidence:** chat (~00:27:49); literacy varies (~00:05:07).
**JTBD:** Understand what I’m looking at without asking the team.
**Severity:** Real, but mixed with Theme 1 (wrong structure vs unclear copy/density).
**In-scope:** Only as **copy, hierarchy, progressive disclosure** on portfolio screens — not a learning product.

### Theme 5 — Status of in-flight actions (chat load)
**Who:** Clients asking “what’s happening / when’s this coming in.”
**Evidence:** ~00:27:49; **they already released live actions on home** (not on demo).
**JTBD:** Know progress without pinging WhatsApp.
**Severity:** Was high; **already being addressed.**
**In-scope for take-home:** **No — Calum said they shipped it; stay on portfolio view.** Mention as “do not refocus here.”

### Theme 6 — Health-tracker / efficiency vs market-check behaviour
**Who:** Strategy wants everyone; behaviour of many is daily/volatile check.
**Evidence:** ~00:07:26 vs ~00:09:50.
**JTBD (today):** How did the world affect *my* liquid wealth. **JTBD (strategy):** Am I efficient; is anything green/red. **Severity:** Strategic, not the stated take-home.
**In-scope:** Lightly — a health/efficiency readout can sit *on* a better portfolio view; **do not replace** the market-check job. Wacky/later in the doc.

### Theme 7 — Advice not visible next to wealth trajectory
**Who:** Clients with a tailored advice backlog.
**Evidence:** ~00:48:28; “one day that’s the idea”; difficult.
**JTBD:** See what I should do in the same frame as where I’m going.
**In-scope:** **No** (rest of app / later). Anti-goal for prototype.

### Theme 8 — Tax-adviser workflow
**Who:** Joint households, accountants.
**Evidence:** ownership filter (~00:33:52); future partnership (~00:34:54).
**JTBD:** Send a view tax people can use.
**In-scope:** Ownership filter **yes** if chosen; formal tax-report partnership **no** (later / doc).

### Theme 9 — First-year leavers who wanted trading
**Evidence:** ~00:12:49.
**In-scope:** **No.** Philosophy filter, not portfolio IA. Y TREE will not become a trading app (~00:21:31).

### Theme 10 — Children / next-gen engagement
**In-scope:** **No.** Calum: don’t worry; they don’t use it as much (~00:04:08).

---

**Candidate “where to start” (for a later synthesizer — not a locked priority):**
Theme 1 + Theme 2 together: **one optional preset portfolio view** that productises the report mental model (likely **liquid/illiquid** as the sharpest quoted mismatch, or **asset class** if you argue it covers more sophisticated clients), with an introduction pattern that leaves the current custody path intact. Ownership as a **filter on that view**, not a third IA. Explicitly **not** Themes 5, 7, 9, 10.

---

## E. Implications for the prototype

### Must preserve the existing path

- Keep the **set route**: account/custody types → provider (Citi Private Bank etc.) → analysis.
- Keep **hiding empty categories** (no PE section if no PE).
- Do not rename “portfolio” away — that’s the usual client word (~00:25:27).
- Assume many users **will never switch** and **should not feel the app changed**.

### Introduction pattern for optional views (10–15%)

Calum’s PM test: **let interested users know without distracting others.**

Implications (inference, grounded in his words):

- Alternative view is **opt-in**, not a new default.
- Discovery: something findable for people who already think “this doesn’t make sense / I’d rather get my monthly report” (~00:36:00) — e.g. control near the current high-level view, not a first-run tour for everyone.
- Copy should sound like **another way to look at the same wealth**, not “we redesigned your portfolio.”
- Preset names should use **their** language (liquid / illiquid; equities vs bonds), not internal Y TREE category names.
- Switching back must be obvious (love-as-is + don’t love change).

### Candidate views (presets, not custom)

1. **Liquid vs illiquid** — two main buckets; different metrics; compare; liquid checked often, illiquid not. Closest to PE report they already produce.
2. **Asset class** — % equities vs % bonds (etc.) at the top; drill into class; **then** split across providers.
3. **Ownership filter** — my / partner’s / genuinely jointly owned. Works **across** 1 or 2; tax/accountant job.

*Inference:* One hero preset (1 *or* 2) + ownership as filter is closer to “one well-designed solution” than three equal IAs.

### Mindset states to design for (what’s on screen and why)

1. **Volatile-market check** — liquid equities/bonds; “how did the world affect *me*”; daily prices exist. Do not scold them with health-tracker copy in this moment. Still true that ±5% today isn’t the philosophy.
2. **PE client comparing buckets** — two portfolios; illiquid locked 8–12 years; committed / upcoming 5 years / PE metrics already exist in the PE fund view; want comparison and the theory of higher illiquid return.
3. **Tax / accountant question** — joint profile; “what is mine vs partner vs genuinely joint”; out of interest *and* practical.
4. **“Am I efficient?” health check** — future strategy; green/OK; “is there anything I could be doing?” Aligns with advice backlog *eventually*, but advice-on-curve is out of scope. A light efficiency/status treatment is compatible; a full health-tracker product is not this exercise.

Also hold: **low literacy** users on the default path — density and jargon on the *optional* view can be higher than on the default, which is how you avoid confusing people who don’t need it.

### What NOT to build in the prototype

- Whole app, chat, notifications, children’s experience
- In-app trading / InvestEngine flows
- Open-ended custom dashboards / drag-your-own categories
- Replacing the current custody path
- Advice-next-to-wealth-trajectory (call it later)
- Formal tax-adviser export as the hero (ownership filter is enough if needed)
- First-run redesign / forced education for 100% of users
- Daily-PnL trading aesthetic that fights the long-term philosophy
- Live-actions status (already shipped)
- Engineering diagrams, data-model essays
- Multiple competing solutions as the main artefact

**Wacky/later (doc only, Calum’s invitation):** advice on the trajectory curve; tax-adviser packaged reports; fuller health-tracker; anything beyond 2–5 portfolio screens.
