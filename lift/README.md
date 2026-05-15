# The Lift — build plan

A civilizational gains record. Part of [Forward Compatible](https://forwardcompatible.org).

The public page is at [/lift.html](../lift.html). The methodology spec is at [/lift/methodology.html](methodology.html).

The Lift is the counterpart record to [The Ledger](../ledger.html) — same architecture, same provenance discipline, inverted lens. The Ledger tracks what states do that needs accountability; The Lift tracks what humanity is building. Both pages run on the same pipeline service.

## What lives in this directory

```
lift/
├── methodology.html       # Public-facing methodology page
├── README.md              # This file
└── data/
    ├── schema.json        # Normalized gain-record schema (the canonical spec)
    ├── sources.json       # Source catalog — 15 sources, ingestion methods, cadence
    ├── heatmap.json       # Country composite progress scores
    ├── timeline.json      # Civilizational gains, 1900–present
    ├── movers.json        # Largest 5-year deltas in progress score
    ├── disputed.json      # Gains where sources disagree, with each claim preserved
    ├── structural.json    # Child mortality, renewables, internet, vaccine coverage panels
    ├── events.json        # Recent gain entries with verification tiers
    └── treaties.json      # Reach of core rights-expansion and protection treaties
```

All JSON files are loaded by `/lift.html` via fetch — editing the JSON updates the page.

## Current status

**Design + scaffolding.** The visualization layer is live with illustrative data. The ingestion pipeline is not yet running — each source connector ships incrementally per the build plan in the methodology page.

## Build order

The order matters. Verification work has to land before scale work, or the record becomes another aggregator. The Lift and The Ledger share connectors where they overlap (e.g., UN treaty deposits, country-year indicators).

1. **World Bank + OWID connectors** (parallel) — two macro-indicator sources with clean APIs. Standing them up together lets the heatmap and structural panels populate from day one.
2. **UN IGME + WHO GHO ingest** — country-year backbone for the healthspan dimension. Annual cron.
3. **UNESCO UIS + ITU ingest** — access dimension: literacy, schooling, internet. Annual cron.
4. **FDA / EMA approval feed** — adjudicated-tier records arrive directly from regulator publication; includes generics and biosimilars where access expansion is the gain.
5. **IUCN Red List + recovery feed** — status changes (especially downlistings) are time-stamped facts. Green Status of Species (added 2021) measures recovery potential.
6. **Magnitude scoring** — automated computation of dot-size and prominence weight, with the rule set published and revisable.
7. **Costs-alongside-gains discipline** — every gain entry has a costs field. Empty is allowed; missing is not.
8. **Public corrections log** — every change writes a queryable row.
9. **Independent governance** — advisory board, published funding sources, refusal of corporate-sponsored gains.

## Where the pipeline will live

Same question as The Ledger, and the answer is the same: **build-step JSON approach for the first six months.** Connectors run on schedule (GitHub Actions cron), output JSON files committed to this repo. The static page reads the JSON directly. Simpler, fully open-source, no operational state.

When data volume exceeds what's reasonable to commit to git, the pipeline migrates to the standalone-service shape — likely on the existing Atlas VPS, leveraging infrastructure already running for other FC work.

## Non-negotiables

- Same lens applied to every gain, including the costs.
- Every claim links to its source. Caveats disclosed when known.
- Disagreement between sources is shown, not hidden.
- Single-source records are tagged, not suppressed.
- Every gain has a costs field — empty is allowed, missing is not.
- Public corrections log records every change.
- No corporate-sponsored gains. Foundation- and reader-supported.

## What this record is not

- **Not a marketing document for any one project, ideology, or government.** A gain is recorded with the same skeptical schema regardless of who claims credit.
- **Not a "progress is inevitable" narrative.** Gains can be reversed (and several on the page have been). The structural panels include backsliding where it occurred.
- **Not in opposition to The Ledger.** Both records are part of the same honest accounting. A government can appear on both pages in the same year for different conduct, and that complexity is the point.

## How to contribute later

(Not yet — the project hasn't opened for external contribution. The schema and source catalog are the public spec; comments and corrections welcome at the contact on the main FC site once that channel is set up.)
