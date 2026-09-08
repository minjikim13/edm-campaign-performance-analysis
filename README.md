# EDM Campaign Performance Analysis

SQL & Python analysis of 38 EDM campaigns (Aug 2025 - Sep 2026) for LIVE in Australia (LiA), diagnosing a -24.9pp open rate drop and a 10-15x engagement gap between promotional and informational content, with Tableau dashboards and business recommendations.

## One-line conclusion
Pure promotional emails convert 10-15x worse than informational content, and a sponsor list import that added mostly Chinese-background contacts caused open rates to drop from 56.4% to 31.5% (-24.9pp) - not because of deliverability failure, but because email is not this segment's habitual communication channel, even while living in Australia.

## Business Context
LiA relies on EDM as its primary owned channel to engage international students, but campaign performance was inconsistent. This analysis determines whether the issue was content strategy or structural list dilution following a sponsor data import.

## Key Findings
- **Content type gap:** Informational/onboarding emails achieved 8-13% CTOR vs. 0.81% for pure promotional campaigns.
- **List consolidation impact:** Average open rate fell from 56.4% (Jan-Apr 2026) to 31.5% (May-Sep 2026) following a sponsor list import that tripled the subscriber base.
- **Failed campaign case:** A July 2026 re-engagement send to 15,484 contacts produced the weakest result in the dataset (7.23% open, 0.13% CTOR).

## Repository Structure
- `data/cleaned/` - cleaned campaign dataset plus derived summary tables
- `notebooks/` - Python (pandas) cleaning/classification and SQL aggregation + before/after analysis
- `tableau/` - link to the interactive Tableau Public dashboard

## Tools & Skills
Python (pandas), SQL, Tableau, ActiveCampaign / GoHighLevel (CRM export), Excel

## Recommendations (proposed)
- Segment EDM reporting and sending by acquisition source (Organic vs. Sponsor-imported)
- Cap future sponsor list imports at 50% of the existing active list, with pilot testing first
- Install Google Postmaster Tools to monitor domain reputation directly
- Redesign the Promotion template using the story-first structure already achieving 13.2% CTOR
- Redirect the Chinese-background (2Airport) segment to WeChat/RedNote rather than Gmail EDM

## Links
- Tableau Dashboard: https://public.tableau.com/views/EDMCampaignPerformanceAnalysis/Dashboard1?:language=en-US&:display_count=n&:origin=viz_share_link
