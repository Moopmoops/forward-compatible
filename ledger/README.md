# The Ledger — build plan

A civilizational accountability record. Part of [Forward Compatible](https://forwardcompatible.org).

The public page is at [/ledger.html](../ledger.html). The methodology spec is at [/ledger/methodology.html](methodology.html).

## What lives in this directory

```
ledger/
├── methodology.html       # Public-facing methodology page
├── README.md              # This file
└── data/
    ├── schema.json        # Normalized event schema (the canonical spec)
    ├── sources.json       # Source catalog — 15 sources, ingestion methods, cadence
    ├── heatmap.json       # Country rights composite scores
    ├── timeline.json      # Historical mass-violence events, 1885–present
    ├── movers.json        # Largest 5-year deltas in composite score
    ├── disputed.json      # Events where sources disagree, with each claim preserved
    ├── structural.json    # Sanctions, arms, surveillance, environmental harm panels
    ├── events.json        # Recent ledger entries with verification tiers
    └── treaties.json      # Treaty ratification gaps for core rights instruments
```

All JSON files are loaded by `/ledger.html` via fetch — editing the JSON updates the page.

## Current status

**Design + scaffolding.** The visualization layer is live with illustrative data. The ingestion pipeline is not yet running — each source connector ships incrementally per the build plan in the methodology page.

## Build order

The order matters. Verification work has to land before scale work, or the ledger becomes another aggregator.

1. **ACLED + UCDP connectors** (parallel) — two event-level sources with clean APIs. Standing them up together lets cross-source agreement scoring run from day one.
2. **V-Dem + HRMI annual ingest** — country-year backbone for heatmap and movers. Quarterly cron.
3. **Entity resolution layer** — actor and location canonicalization. Mistakes here propagate everywhere; this has to be solid before scaling sources.
4. **HRW + Amnesty narrative extraction** — structured scrape + LLM extraction; reviewer-in-loop for calibration.
5. **Disagreement scoring** — automated computation of dispute tier when sources diverge >50%.
6. **Structural-harms connectors** — SIPRI, Citizen Lab, EJAtlas, OFAC sanctions.
7. **Public corrections log** — every change writes a queryable row.
8. **Independent governance** — advisory board, published funding sources.

## Where the pipeline will live

Open question. Two reasonable shapes:

**A. Standalone service.** Python workers per source, Postgres for normalized records, public read-only API. The static GitHub Pages site fetches from this API. Most flexible; most operational overhead.

**B. Build-step approach.** Connectors run on schedule (GitHub Actions cron), output JSON files committed to this repo. The static page reads the JSON directly. Simpler, fully open-source, no operational state.

Leaning toward (B) for the first six months — until the data volume exceeds what's reasonable to commit to git. The point of build-step JSON is that the entire record is auditable in the git history, which is a strong property for an accountability record.

## Non-negotiables

- Same lens applied to every state, including the home country and its allies.
- Every claim links to its source. Bias disclosed when known.
- Disagreement between sources is shown, not hidden.
- Single-source records are tagged, not suppressed.
- Public corrections log records every change.
- No government funding. Funding sources published.

## How to contribute later

(Not yet — the project hasn't opened for external contribution. The schema and source catalog are the public spec; comments and corrections welcome at the contact on the main FC site once that channel is set up.)
