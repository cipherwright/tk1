# Ideas from the Torii AI Management Platform video (23 Nov 2026)

Source: the 4:42 product walkthrough on toriihq.com/products/ai-management-platform, viewed frame by frame (a still every 12 to 14 seconds, with the captions). The "why" for each item paraphrases the narrator where the captions said it. Where they didn't, it is my reading and is marked *(inferred)*.

The last column says what happened to each idea in `cro-dashboard-v2.html`.

---

## 1. AI Pulse: the live view (0:00 to 0:30)

A real-time screen, refreshed every 5 minutes, with a "Live · last 5 min" marker. Its caveat line says the figures are an estimated token value at standard API rates, not the invoice amount.

| On screen | Why | In v2 |
|---|---|---|
| **Active users now** (46, active in the last 5 min, −9 vs the previous 5 min), with a sparkline | Shows how much AI is being used right now, against a moment ago | No. A CRO doesn't act on minute-by-minute use |
| **AI calls per minute** (33.4, 5-min average, −2%), with a sparkline | The rate of activity | No |
| **Token value rate** ($645/hr, about 1.5B tokens/hr, +17%), with a sparkline | The rate at which money is being spent | No. Average a day per function covers it |
| **Projected today** ($8.4K at the current rate, by end of day) | Turns the rate into a figure for the day *(inferred)* | No. Charon projects to month end instead |
| **Active users** avatar wall (46 active, 20 live) | Puts faces on the usage *(inferred)* | No. Decoration |
| **Model pulse**: a dot per model currently in use | Shows which models are live, across vendors. The narrator stressed real-time spend by model | Partly: the model mix heatmap, monthly not live |
| **Top cost drivers** table: model, trend sparkline, $ per hour, tokens per minute, share bar; a group-by switch (model, …) and CSV export | Shows what is driving cost right now | Yes in spirit: top spenders table and "On Opus" column |
| **Where in the world** map | Shows where usage comes from | No. Region is already a list in "Where this month went" |

## 2. Integrations: where the data comes from (0:30 to 0:42)

| On screen | Why | In v2 |
|---|---|---|
| Five source cards with a status each: AI telemetry (Active), AI apps (1 needs attention), HRMS (Connected), Identity provider (Connected), Vibe-coded apps (Not connected) | You can only trust the numbers if the feeds are working *(inferred)* | Yes: freshness dots under the tabs |
| **Connected sources (14)** table: source, type, status ("Receiving events", "Warning", "Healthy"), last sync (59 minutes ago, 22 days ago) | Claude Code, Codex CLI and Gemini CLI send telemetry. HR systems (BambooHR, HiBob) say who owns the spend and which team they belong to (narrator) | Yes: usage, billing and HR directory dots, with HR shown as 4 days old |

## 3. AI Cost Overview (0:42 to 1:30)

| On screen | Why | In v2 |
|---|---|---|
| **Total AI cost** ($41,652, last 30 days, all categories, ↑68.8% vs last month) | The headline cost | Already there: Spend to date tile |
| **Projected annual cost** ($1,360,848, assuming recent growth) | Turns a month into the number a budget owner plans with *(inferred)* | Yes: "2026 projected" in the Monthly spend header |
| **Cost contribution** stacked bar: Subscriptions 43% ($17,906), On-demand 26%, API/Platform 10%, Vibe coding 21% | Splits spend by how it's paid: seats, on-demand credits, API and platform (narrator) | Charon equivalent already there: By source / By tier |
| **AI spend trend**: actuals (solid), current month estimate (a point), forecast (dashed) to Mar 2027 on a shaded future area | Shows spend over time and where it's heading (narrator) | Already there: Monthly spend, Nov and Dec as forecasts |
| **Spend by department** donut ($242.8K attributed), view-by switch (Workday department). Note: based on cost attributable to individuals; doesn't follow the period chosen; select a slice to see its tools | Who is spending, by org unit | Already there: Function envelopes |
| **Department drill-down** (Sales, $48,596): spend by category, then by tool, $ and % (Cursor alone 64%) | Find exactly where a department's spend goes; for Sales it was Cursor (narrator) | Yes: select a function row to open the side panel |
| **Top AI tools** table: tool, category, cost, % of total, with a total row | Which products cost most | Charon equivalent: By model |
| **Spend by person** table: 700 people; user, tools used, total cost, then one column per tool; group-by; columns picker (10); CSV. Note: per-person cost covers only tools that report it, so the total above is higher | Cost per individual (narrator) | Yes: Top spenders table, plus "Export all 306 as CSV" |

## 4. AI Usage: one person (1:42 to 2:18)

| On screen | Why | In v2 |
|---|---|---|
| Tiles: **Total token value** ($63), **Sessions** (30), **Requests** (170), **Total tokens** (135.2M) | How much one person uses it; the narrator pointed at session count | Sessions and per-session spend in Top spenders |
| **Billed cost by tool** (Cursor $383, Lovable $93.40, total $477) | What the person actually costs, against the value estimate | No. Charon has one tool |
| **Subscription efficiency** gauge: 15x value per $1 (seat $30, value $450) | What the firm gets back for each licence seat (narrator) | No. Charon has no seat price |
| **Model mix** heatmap: this person's share of tokens per model against the org average, priciest model first, value per 1M tokens ($0.47 vs $0.38); darker = larger share; select a cell to see who is behind it | Compare a person's model choice with the average (narrator) | Yes: Model mix by function, with an All spend row; firm average tick in the side panel |
| **Daily token value** bars; **token value by tool/provider** bars; **Plan limits** | Their pattern over the month and their limits | Partly: daily bars in the side panel, At cap signal |

## 5. AI Usage: the whole company (2:18 to 2:42)

| On screen | Why | In v2 |
|---|---|---|
| Tiles: total value ($1,810, ↑18%), active users (60, 78% of the workforce, 1,094 sessions), value per active user ($30), tokens (4.8B) | Company-wide use (narrator) | Yes: People active, 90% of those with access |
| **Activity over time**: daily value stacked by model; switches for metric, stack-by, provider | Day-by-day spend split by model | Partly: daily spend per function in the side panel |
| **Daily active users** line; **Daily token value** bars | Adoption trend next to the cost trend | Yes: People active each day |
| **Requests vs token value per user** scatter, outliers named | Find the individuals who really drive usage (narrator) | Partly: histogram and top spenders. A scatter needs request data Charon may not have |
| **Subscription efficiency** for the org ($12,000 paid, $180,000 of value, 15x); model breakdown; value by model | The return on the whole subscription | No |

## 6. AI Adoption (2:42 to 3:10)

| On screen | Why | In v2 |
|---|---|---|
| **AI summary** at the top, generated from the selected period and filters, ending with a "recommended focus" | One paragraph to read before the charts *(inferred)* | Yes: Summary strip, written from the figures, not by a model |
| Users / Groups tabs | The same view per person or per team | Functions and people are both on the page |
| **Active users** (60, 78% of the workforce, flat) | Adoption | Yes |
| **Median value per user** ($25, ↑25%), with a mini distribution | The typical user, not skewed by heavy users *(inferred)* | Yes: median spend per person vs October |
| **P90 value per user** ($57, ↑24%) | Where the heavy users are | Yes |
| **Top 10% share** (20% of value comes from the top 10%) | Whether use is spread out or concentrated. The summary called 20% balanced | Yes: 36%, against 42% in October |
| **Daily active users**, current vs previous period (dashed), weekends shaded | Compare like with like | Yes, aligned on weekdays four weeks earlier |
| **Biggest movers**: largest increases and decreases by person | Some will be power users, others need help (narrator) | Yes |
| **Distribution histogram** of value across users, with median and P90 lines; select a bar to filter the table | The shape of usage in one picture | Yes, without the filter |
| **User table**: user, signal (Low / Rising), value, vs previous, trend, % of total, percentile, tokens, sessions | Start conversations with people early and often (narrator) | Yes: Top spenders with At cap / Rising / New |

## 7. AI apps and per-app pages (3:10 to 4:04)

| On screen | Why | In v2 |
|---|---|---|
| App cards with member or seat counts (OpenAI 700 members, Cursor 350, Copilot 400 seats …); "Resync extension data"; export as .md | How many people are attached to each tool (narrator) | No. Charon has one tool |
| **OpenAI page**: tabs Overview / Members / Spend / Billing & Limits / Usage / Projects / Keys. Spend last 30 days ($3,874) with sparkline and last 12 months; **soft limit $1,500, hard limit $30,000**; **available credit** ($1,724.80, flagged Low, 2%); trust tier; org counts (340 projects, 700 members, 620 API keys); top projects by spend; spend by model; daily spend; recent billing days with CSV; "Other data is 22 days old" | Vendor account health: limits, credit running out, key sprawl *(inferred)* | Partly: freshness. Soft/hard limits are Charon's envelopes and daily caps |
| **Lovable page**: credits remaining (24,681 of 40,050, 62% left, "how is this calculated?", resets today); total projects and cost; published apps (public vs private); team (members, builders, admins); top projects by cost; credit breakdown by source (monthly, rollover, daily, with lapsed rollover noted); daily activity | Credit-based tools need "how much is left and when it resets" *(inferred)* | No. A credit model doesn't apply |

## 8. Integrations graph (4:04 to the end)

| On screen | Why | In v2 |
|---|---|---|
| A graph of built projects linked to the company systems they touch (AWS, GitHub, Gong, HubSpot, OpenAI); filter and search ("git" leaves 5 projects on GitHub) | Shows which internal apps connect to which systems, for security's peace of mind (narrator) | No. It belongs in a security view, not the CRO overview |

## 9. Hero mock-up at the top of the page (not in the video)

The overview card at the top of the page shows:
- Total spend ($148,402, ↑18%) and tokens (412M, ↑24%).
- Spend by model, weekly, with a **"+$8.4k spike" annotation** on the chart.
- Top users with dollars.
- A "by team" donut.
- "1,284 users attributed to a model".

**Idea worth keeping:** label an anomaly on the chart itself, rather than leaving it for the reader to find. Not used yet. It would fit September's $197,657 bar in Monthly spend.

---

## Patterns across the whole product
- **Every figure has a comparison** ("vs previous 5 min", "vs last month", "vs previous period"). A number on its own is never shown.
- **Every list can be drilled into or exported** (select a slice, select a cell, CSV).
- **A note says what each number covers** ("not your invoice amount", "does not follow the period selected", "how is this calculated?").
- **Typical vs heavy**: median, P90 and top-10% share, not only totals and averages.
- **Freshness is shown everywhere** ("Live", "59 minutes ago", "22 days old").

## Not carried over, and why
- Live per-minute tiles, avatar walls, world map, model pulse: dramatic, but nothing for a CRO to act on.
- Subscription efficiency (value per $1): Charon has no seat price to divide by.
- Multi-vendor tool pages, credits and resets, integrations graph: Charon tracks one tool (Claude Code) and the CRO isn't its admin.

Ideas still open for Charon: the spike annotation (section 9); the requests vs spend scatter, if request counts are available; a "how is this calculated?" note on the forecast tile.
