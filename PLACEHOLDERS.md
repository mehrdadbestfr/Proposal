# Proposal Template Placeholder Contract

This template uses Handlebars-style placeholders (`{{...}}`) and loop blocks (`{{#each ...}}`).
The visual design/CSS is unchanged; only business-specific or report-specific content is dynamic.

## Core
- `business.name`, `business.name_upper`, `business.location`
- `proposal.month_year`
- `assets.cover_photo`, `assets.mobile_site_screenshot`, `assets.meta_ads_snapshot`, `assets.social_creative_background`, `assets.video_creative_thumbnail`

## Website performance
- `website_performance.score_raw`, `score_max`, `summary`
- `website_performance.fcp|tbt|lcp|speed_index|cls`: `raw`, `display`, `card_class`, `status_class`, `status_html`

## Technical audit
- `technical.insights.flagged_count`, `review_count`, `warning`
- `technical.insights.primary_items[]`, `secondary_items[]`: `icon_class`, `title`, `detail`
- `technical.diagnostics.flagged_count`, `review_count`, `items[]`: `icon_class`, `title`, `detail`, `note`

## UI/UX
- `ui_ux.subtitle`, `what_works[]`, `conversion_friction[]`, `recommendation`

## SEO audit
- `seo.ai_visibility.*`, `seo.backlinks.*`, `seo.search.*`, `seo.snapshot.*`
- Metric objects use `value`, `delta`, `delta_class`
- `seo.ai_search_presence[]`: `source`, `responses.{value,delta,delta_class}`, `pages.{value,delta,delta_class}`

## Organic rankings
- `organic_rankings.branded_local[]`: `keyword`, `position`, `traffic`, `volume`
- `organic_rankings.non_branded_treatment[]`: `keyword`, `position`, `traffic`, `volume`, `kd`

## Keyword opportunities
- `keyword_opportunities.group_1|group_2.title`
- `.rows[]`: `keyword`, `position`, `search_volume`, `keyword_difficulty`, `target_page`

## Competitors
- `competitors.summary.*`
- `competitors.chart_max_raw`, `competitors.axis_labels_html`
- `competitors.chart_rows[]`: `row_class`, `traffic_raw`, `domain`
- `competitors.table_rows[]`: `row_class`, `domain`, `organic_traffic`, `organic_keywords`, `backlinks`, `ref_domains`, `paid_keywords`, `paid_traffic_cost`

## Paid search
- `paid_search.subtitle`
- `paid_search.summary.*`
- `paid_search.chart_rows[]`: `row_class`, `searches_raw`, `keyword`
- `paid_search.auction_signals[]`: `bid_range`, `label`
- `paid_search.competition_label`, `competition_summary`, `implication`

## Paid media structure
- `paid_media.subtitle`
- `paid_media.campaign_1..3`: title/title_html, keywords_html, description
- `paid_media.operating_rules_html`

## Meta / creative
- `meta_ads.library_url`
- `social_video.subtitle`

## Launch plan
- `launch_plan.subtitle`, `next_step`
- `launch_plan.phase_1..3`: `period`, `title`, `tasks_html`

### Styling helper values
- `delta_class`: usually `up` or `down`
- PageSpeed `card_class`: usually `danger`, `warning`, or `success`
- PageSpeed `status_class`: usually `red`, `amber`, or `green`
- `row_class`: e.g. `is-teal`, `highlight-row`, or empty
- `icon_class`: e.g. `tri`, `square`, `circle`

Fields ending in `_html` intentionally allow `<br>` or small static separators required by the existing layout.
