# The Lift — build plan

A civilizational gains record. What humanity is building, with costs honestly listed alongside every gain.

The public page is at [/lift.html](../lift.html). The methodology spec is at [/lift/methodology.html](methodology.html).

## What lives in this directory

```
lift/
├── methodology.html       # Public-facing methodology page
├── README.md              # This file
└── data/
    ├── schema.json        # Normalized gain-record schema (the canonical spec)
    ├── sources.json       # Source catalog — 15 sources, ingestion methods, cadence
    ├── heatmap.json       # Country composite progress scores
    ├── timeline.json      # Civilizational gains across recorded history
    ├── movers.json        # Largest 5-year deltas in progress score
    ├── disputed.json      # Gains where sources disagree, with each claim preserved
    ├── structural.json    # 17 indicators across 6 domains
    ├── events.json        # Recent gain entries with verification tiers
    └── treaties.json      # Reach of core rights-expansion and protection treaties
```

All JSON files are loaded by `/lift.html` via fetch — editing the JSON updates the page.

## Current status

**Design + scaffolding.** The visualization layer is live with illustrative data. The ingestion pipeline is not yet running — each source connector ships incrementally per the build plan in the methodology page.

## Build order

The order matters. Verification work has to land before scale work, or the record becomes another aggregator.

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

**Build-step JSON approach for the first six months.** Connectors run on schedule (GitHub Actions cron), output JSON files committed to this repo. The static page reads the JSON directly. Simpler, fully open-source, no operational state.

When data volume exceeds what's reasonable to commit to git, the pipeline migrates to a standalone-service shape.

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

## How to contribute later

(Not yet — the project hasn't opened for external contribution. The schema and source catalog are the public spec; comments and corrections welcome once the contact channel is set up.)
