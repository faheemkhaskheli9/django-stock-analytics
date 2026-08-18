# Architecture Notes: Stock Market Analytics Web Application

## Pipeline

```text
Market Data APIs -> Django Backend (ETL + Models) -> PostgreSQL -> Web Dashboard (Charts, News, Fundamentals)
```

## Components

- OHLCV data display
- Dividends and splits tracking
- Financial statements
- Stock charts
- News aggregation
- Sentiment overlay
- Company profile pages
- Historical analytics

## Design Notes

- Keep provider/model choices swappable behind interfaces (see `multi-llm-router`
  and similar projects in this portfolio for the general pattern).
- Prefer configuration-driven pipelines (YAML/JSON in `configs/`) over hardcoded
  parameters so experiments are reproducible.
