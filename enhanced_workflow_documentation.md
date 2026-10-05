# Reproducible Market Intelligence Workflow

## Purpose

This workflow turns a product-level market dataset into decision-ready pricing, competitor, category and sustainability insights.

## Pipeline

### Phase 1 — Collection / ingestion
**Script:** `python 1_data_collection_kaggle.py`

Responsibilities:
- load an approved/static source;
- standardise source fields;
- identify eco-relevant products;
- enrich records with sustainability attributes;
- create the initial analysis file.

### Phase 2 — Data quality
**Script:** `data_cleaning.py`

Responsibilities:
- standardise column names;
- validate prices and ratings;
- handle missing values according to field purpose;
- normalise categories and brands;
- calculate discounts and price tiers;
- extract sustainability attributes;
- identify/remove duplicates;
- generate cleaning documentation.

Critical identifiers such as product names are **not fabricated** when missing.

### Phase 3 — Intelligence analysis
**Script:** `Analysis_insights.py`

Produces:
- pricing statistics;
- category price comparisons;
- discount analysis;
- price/rating relationship;
- brand performance scoring;
- competitive positioning;
- sustainability attribute prevalence;
- sustainability price premiums;
- category opportunity scoring;
- website/source comparisons;
- strategic recommendations.

### Phase 4 — Reporting
**Script:** `dashboard.py`

Produces:
- interactive price dashboard;
- interactive competitor dashboard;
- interactive market-trends dashboard;
- dashboard index;
- HTML insight report;
- PDF executive report.

## Refresh cycle

For a production implementation:

**Ingestion → QA → transformation → analysis → stakeholder validation → dashboard/report publication → archive snapshot → next period**

Historical snapshots should be retained to enable genuine month-over-month and trend analysis.

## Quality-control checklist

Before publishing an insight:

- [ ] Source provenance is documented.
- [ ] Critical fields have been validated.
- [ ] Duplicate handling has been reviewed.
- [ ] Derived metrics have documented formulas.
- [ ] Composite-score weights have a business rationale.
- [ ] Sample sizes are adequate for the comparison.
- [ ] Synthetic/demo data is clearly separated from observed data.
- [ ] Recommendations distinguish evidence from assumptions.
- [ ] Visualisations have readable labels and appropriate scales.
- [ ] Limitations are visible to decision-makers.

## Extension path

The prototype can be upgraded with:
- scheduled API/feed ingestion;
- a relational warehouse;
- product and brand entity resolution;
- historical price tracking;
- anomaly alerts;
- price elasticity modelling;
- NLP classification of sustainability claims;
- automated executive briefings;
- role-based dashboards.
