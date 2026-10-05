# Data Provenance & Responsible Use

## What is included in this portfolio version?

The repository contains a **200-record demonstration dataset** designed to make the full market-intelligence workflow reproducible offline.

- **15 records:** manually captured product listings from Package Free Shop (`manual_packagefree.csv`).
- **185 records:** synthetic demonstration records generated to exercise the pipeline across multiple brands, categories, prices, ratings, review counts and sustainability attributes.
- The synthetic records are explicitly marked `data_provenance = synthetic_demo`.
- The manually captured records are marked `data_provenance = manual_sample`.

The portfolio version therefore **does not claim that all 200 observations are live-market observations**. The purpose is to demonstrate the engineering, analytical and decision-support workflow without relying on live scraping or exposing private data.

## Why this matters

A strong market-intelligence system needs to distinguish between:

1. **Observed data** — directly captured from a source;
2. **Derived data** — calculated or classified from observed fields; and
3. **Synthetic/demo data** — generated solely for reproducible development and demonstration.

This distinction is preserved in the dataset and documentation.

## Source limitations

The included manual sample is a small snapshot and is not intended to represent the full Package Free Shop catalogue. Prices, availability, ratings and product attributes can change.

The synthetic component is **not evidence of actual market share, consumer demand or competitor performance**. Any business recommendation shown in the demo should therefore be interpreted as an example of how the system converts structured market data into decisions—not as a forecast of the real market.

## Production extension

For production use, the same pipeline can ingest:

- licensed marketplace/catalogue datasets;
- approved retailer feeds or APIs;
- scheduled exports from internal commerce systems;
- approved web data collection where permitted;
- historical snapshots to support genuine month-over-month analysis.

Before deployment, source-level validation, licensing/terms review, deduplication across retailers and a reproducible collection timestamp should be added.

## Analytical caution

The project uses a composite **Success Score** combining normalized rating, review volume and price. It is an analytical prioritization metric, not a causal measure of product success. Its weights should be validated with business stakeholders and sensitivity-tested before operational use.
