# Analyst Sentiment & Recommendation History API (Sample)

## What this data is about

This API provides a **structured history of analyst recommendations for a stock over the last one year**.

Instead of raw research notes or PDFs, the data shows:

* how analysts have viewed the stock over time
* how their recommendations evolved
* what the overall analyst sentiment looked like on each day

The intent is to help broker platforms **display analyst consensus, trends, and conviction** in a clear and data-driven way.

---

## How to read the response

Each response is organised into four main sections.

---

## 1. `stock`

Basic stock identification details:

* ISIN
* exchange symbol
* company name
* exchange

This allows the response to be used directly on a stock detail page.

---

## 2. `coverage_summary`

A quick snapshot of analyst coverage during the period:

* date range covered
* total number of recommendations
* number of distinct analysts
* distribution of BUY / HOLD / SELL calls

This section answers, at a glance:

> “Is this stock actively covered, and is the coverage meaningful?”

---

## 3. `sentiment_timeline`

This is the **core signal**.

It shows **one entry per date**, representing the **end-of-day analyst sentiment** after all recommendations made on that day.

For each date:

* `buy / hold / sell`
  Number of analysts holding each stance as of that day
* `unweighted_score`
  Simple consensus score
  (BUY = +1, HOLD = 0, SELL = −1)
* `weighted_score`
  Same score, but weighted by each analyst’s historical performance score (AEI)

This allows platforms to:

* plot sentiment trends over time
* highlight strengthening or weakening conviction
* show divergence or convergence of analyst opinion

---

## 4. `analyst_journeys`

This section shows how **each individual analyst’s view evolved over time**.

For each analyst:

* only meaningful changes are shown (not every minor revision)
* action changes and target price revisions are captured
* the analyst’s historical score (AEI) is included

This enables:

* analyst-level timelines
* consistency vs flip-flop analysis
* credibility-aware interpretation of recommendations

---

## How this data can be used

Broker platforms can use this data to:

* display **analyst sentiment trends** on stock pages
* show **consensus strength** alongside price charts
* highlight **recent changes in analyst opinion**
* compare **individual analyst journeys**
* build visualizations without parsing research PDFs
* power both **retail-facing UI** and **internal analytics**

The API provides **data, not advice** - interpretation and presentation are left to the consuming platform.

---

## Notes

* All sentiment is derived from published analyst recommendations
* Data reflects historical analyst behavior, not future predictions
* The same data can be consumed as raw history or as aggregated views
