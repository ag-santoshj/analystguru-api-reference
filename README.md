# AnalystGuru API Reference

This repository contains **reference documentation and sample responses for AnalystGuru’s partner‑facing APIs**.

The goal of this repo is to help brokerages, platforms, and integration teams quickly understand:

* what kinds of APIs AnalystGuru provides
* what data these APIs return
* how that data can be interpreted and used

This is a **reference and evaluation repository**. It is intentionally sample‑driven and does not contain production endpoints, authentication details, or proprietary implementation logic.

---

## What you will find here

The repository is organised by API, with each API documented independently.

```
apis/
  └── <api-name>/
       ├── README.md        # What the API does and how to read its data
       └── samples/         # Sample JSON responses
```

Each API folder typically contains:

* a short README explaining the purpose of the API
* one or more sample JSON responses
* (optionally) a lightweight OpenAPI specification

---

## Currently available APIs

### Analyst Sentiment & Recommendation History

Provides a structured, time‑based view of how research analysts have covered a stock over the last year, including:

* daily analyst sentiment snapshots
* analyst‑level recommendation journeys
* coverage depth and action distribution

This API is designed to power stock detail pages, analyst consensus views, and sentiment visualisations.

See: `apis/analyst-sentiment/`

---

## How to use this repository

This repository is best used as:

* a **technical reference** during partner evaluation
* a **shared artifact** for internal discussions (engineering, product, leadership)
* a **starting point** for integration planning

Partners are encouraged to:

* review the README for an API
* inspect the sample responses
* discuss integration requirements based on the data shape and semantics

---

## What this repository does not include

To keep this repository safe and broadly shareable, it does not include:

* production API URLs
* authentication or access mechanisms
* rate limits or commercial terms
* internal scoring algorithms

These details are shared separately during active engagements.

---

## Notes

* All data shown in samples is illustrative
* APIs expose **data, not investment advice**
* Interpretation and presentation are left to consuming platforms

---

For questions or partnership discussions, please reach out to the AnalystGuru team.
