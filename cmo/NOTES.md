# CRO Overview: notes (23 Nov 2026)

## Files
- `cro-layouts.html`: the current work. Every data item from both office screens, laid out three ways (Layouts 1, 2, 3; switch in the yellow bar). Text is 12 px, tile figures 20 px, table rows 21 px.
- `cro-overview.html`, state `#asbuilt`: the two office screens recreated from the photos as one page, on the same data. Its `#redesign` state was rejected (it dropped data and was sized like a slide) and is kept only for the record.

## What is on the page (nothing dropped)
- Five KPI tiles as in the office build: Spend to date, Forecast period-end, Breached, Will breach, Unattributed spend. Each keeps its bar, segments or sparkline and its foot line.
- Function envelopes, all 14 functions plus Unattributed and an All functions total. Columns: Function, Functional head, Spend to date, Envelope, Envelope utilisation, Forecast period-end, Status, Share of total, vs last month, 21 days.
- Monthly spend from Dec 2025 to Dec 2026, Nov and Dec as forecasts. Each month shows its spend and its envelope.
- Where this month went, by source, region, tier and model, plus the cache line.
- The one change: the status badge no longer repeats the percent ("Breached (104%)" becomes "Breached"), because the utilisation column already shows it.

## The layouts
1. **Stacked:** tiles, then the full-width table, then the monthly chart and the breakdowns side by side. Closest to the office build. Fits 1440 x 900 just about; the monthly chart is tight.
2. **Table with side rail:** tiles, then the table on the left with the head's name under the function. The rail on the right holds the monthly spend as 13 rows (month, bar, spend, envelope, %) and the four breakdowns in a 2 x 2 grid. Fits 1440 x 900 with room to spare. **Recommended.**
3. **History under the tiles:** a full-width monthly strip under the tiles, which is the history of the first two tiles, then the table, then the breakdowns in one row. Reads top to bottom best, but needs about one scroll.

## Data
One set, from the CAO photo: 14 functions, $47,300 approved, $36,940 spent on day 20 of 30, straight-line forecast $55,410 (likely $53,194 to $57,626). The two photos did not agree; the old overview showed $48,161 for the month, and its Dec 2025 to Sep series is kept as photographed. Invented: three functions (Liquidity Risk, Climate Risk & ESG, Stress Testing), the monthly envelopes, October's total ($88,690) and the December forecast. Unattributed forecast is $2,114: the $55,410 total less the functions' rounded forecasts.

## Open data questions for the office
- "vs last month" needs a stated basis: the same 20 days of October, or the whole of October.
- The December forecast column needs a method. Next month's envelope is not approved yet.

## Lessons from the rejected rounds
- A dashboard sets a height budget first: everything fits in 1440 x 900. The standard's 28 px figures, roomy tiles and two-line rows break that budget.
- "Based on the data-viz gurus" means Few (dense, one screen), not Knaflic (slides).
- The task was arrangement, not reduction. Every item on the existing screens stays unless the owner removes it.
