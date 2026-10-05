# Data Sources

## Portfolio demonstration dataset

This portfolio version uses a transparent, offline-friendly demonstration dataset.

### Observed/manual sample
- **15 product records** manually captured from Package Free Shop.
- Original file: `manual_packagefree.csv`.
- Fields include product name, brand, category, listed price, sale price, rating, review count, sustainability attributes and collection date.
- These records are labelled `manual_sample` in the portfolio dataset.

### Synthetic demonstration records
- **185 records** generated for reproducible pipeline demonstration.
- The synthetic generator varies brand, category, price, discount, rating, review count and sustainability attributes.
- These records are labelled `synthetic_demo`.
- They are not claims about actual market share, demand or competitor performance.

## Why synthetic data is included

The goal is to demonstrate a complete market-intelligence workflow without depending on live scraping, private datasets or unstable external endpoints. A production deployment would replace the demonstration input with an approved, licensed or internally controlled data source.

## Production-ready source options

The collection layer can be adapted to:
- licensed marketplace datasets;
- approved retailer APIs or feeds;
- scheduled internal catalogue exports;
- approved web data collection;
- historical snapshots for time-series monitoring.

## Data processing

The pipeline performs:
1. source field mapping;
2. eco-product filtering;
3. category standardisation;
4. price and rating validation;
5. missing-value handling;
6. sustainability attribute extraction;
7. discount calculation;
8. price-tier classification;
9. duplicate checks;
10. analytical feature engineering.

See `DATA_PROVENANCE.md` for responsible-use guidance and `data_dictionary.md` for field definitions.
