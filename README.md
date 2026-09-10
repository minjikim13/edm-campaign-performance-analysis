# 📊 EDM Campaign Performance Analysis (Python & SQL)

SQL, Python and Tableau analysis of 38 EDM campaigns (Aug 2025 – Sep 2026) for LIVE in Australia (LiA), diagnosing a -24.9pp open rate drop and a 10-16x engagement gap between promotional and informational content.

## One-line conclusion
Pure promotional emails convert 10-16x worse than informational content, and a sponsor list import that added mostly Chinese-background contacts caused open rates to drop from 56.4% to 31.5% (-24.9pp) – not because of deliverability failure, but because email is not this segment's habitual communication channel, even while living in Australia.

## Business Context
LiA relies on EDM as its primary owned channel to engage international students, but campaign performance was inconsistent. This analysis was conducted to determine whether the issue was content strategy or structural list dilution following a sponsor data import, and to define specific, testable actions to fix the weakest-performing campaign category.

## Key Questions
- Does email content type (informational vs. promotional) affect open and click behaviour?
- Did the May 2026 sponsor list consolidation affect performance, and if so, by how much?
- Are any segments showing early signs of list fatigue (high unsubscribe/bounce)?
- What specific, testable actions would improve the weakest-performing campaign category?

## Tools & Skills
- **SQL**: GROUP BY aggregation, cross-tool verification
- **Python**: data cleaning and classification (pandas)
- **Excel**: initial benchmarking against defined thresholds
- **Tableau**: dashboard and visual storytelling

## Data Preparation
Key data issues addressed:
- Parsed inconsistent date formats across 13 months of exports
- Converted percentage-string fields (Open Rate, CTOR, Unsubscribe Rate, Bounce Rate) to numeric
- Classified all 38 campaigns into 6 content-type categories using subject line keywords
- Final dataset: 38 campaigns, Aug 2025 – Sep 2026.

## Key Insights
**Content Type**
- Promotional campaigns convert 10-16x worse than every other category (0.81% CTOR vs. 8.3-13.2% for informational, event-based, and reminder campaigns).
- The two most recent promotion sends (Aug/Sep 2026) hit CTOR of just 0.12-0.13%, showing the gap is widening, not closing.

**List Consolidation**
- Average open rate fell from 56.4% (Jan–Apr 2026) to 31.5% (May–Sep 2026), coinciding exactly with a sponsor list import that tripled the subscriber base.
- The imported (2Airport) segment's 1.14% unsubscribe rate already exceeds the 1% critical threshold.

**Failed Campaign Case**
- A July 2026 re-engagement send to 15,484 contacts produced the weakest result in the dataset: 7.23% open rate, 0.13% CTOR, 1.02% bounce rate.

## Recommendations
- Segment EDM reporting and sending by acquisition source (Organic vs. Sponsor-imported), rather than blending them into one open-rate metric.
- Cap future sponsor list imports at 50% of the existing active list, with pilot testing required before full integration.
- Install Google Postmaster Tools to monitor domain reputation and spam complaint rate directly, rather than inferring from open rate alone.
- Redesign the Promotion template using the story-first, single-CTA structure already achieving 13.2% CTOR in Event-based campaigns.
- Redirect the Chinese-background (2Airport) segment to WeChat/RedNote rather than Gmail EDM – WeChat remains their dominant day-to-day channel even after relocating to Australia, so low email engagement likely reflects channel habit, not inbox placement failure.

## Repository Structure
- `notebooks/`: `01_Python_Cleaning_Classification.ipynb` (data prep, classification, Before/After analysis), `02_SQL_Before_After_Analysis.ipynb` (SQL deep-dive aggregation)
- `data/cleaned/`: cleaned campaign dataset plus derived summary tables
- `tableau/`: dashboard link and description

## Tableau Dashboard
https://public.tableau.com/views/EDMCampaignPerformanceAnalysis/Dashboard1?:language=en-US&:display_count=n&:origin=viz_share_link
