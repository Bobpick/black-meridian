# Exercise BLACK MERIDIAN

**A portable, offline HTML dashboard for a fictional professional campaign simulation and civilian resilience planning.**

[Open the dashboard](index.html) · [Read the instruction manual](instruction-manual.html)

![BLACK MERIDIAN — I need to play this game to protect my family](assets/black-meridian-poster.png)

> **Important boundary:** BLACK MERIDIAN is a fictional synthetic exercise. Its countries, forces, geography, campaign events, and military decisions are invented. The U.S. reference layer uses public aggregate information for context. This project is not an intelligence product, threat warning, operational plan, targeting tool, evacuation order, or personal safety guarantee.

## Overview

BLACK MERIDIAN is designed to help users explore difficult decisions under uncertainty. It combines:

- A fictional high-end conventional campaign simulation
- Tactical commander decision records
- Fog-of-war and adjudication concepts
- Public-source U.S. force-scale context
- Broad regional civilian-resilience planning modules
- Household continuity planning across 72-hour, two-week, and longer recovery horizons
- Browser-local orders, scorecards, and household-profile drafts

The project is intentionally **operating-system agnostic**. It uses static HTML, CSS, JavaScript, SVG, and JSON files. No installation, package manager, database, external library, or backend service is required.

## Features

### Fictional campaign dashboard

- Exercise brief and commander’s problem
- Abstract fictional theater schematic
- Five-phase campaign timeline from D-10 through D+45
- Blue, Red, and Gray force-posture summaries
- Fog-of-war and adjudication model
- Inject library with phase filters
- Facilitator-note toggle
- Tactical order-writing form
- Campaign evaluation scorecard
- Print-friendly layout

### U.S. public-source reality layer

The dashboard provides a clearly separated reference layer containing:

- FY2026 authorized active-component end-strength context
- FY2026 Selected Reserve context
- FEMA National Risk Index references
- Ready.gov household continuity guidance
- CISA communications-resilience concepts

These figures are treated as **national context**, not as local readiness, deployment status, or a prediction of civilian outcomes.

### Regional planner

The regional planner includes broad planning archetypes for:

1. Pacific Northwest
2. California & Great Basin
3. Southwest
4. Rockies & High Plains
5. Great Plains & Midwest
6. Gulf Coast & Southeast
7. Mid-Atlantic & Northeast
8. Alaska
9. Hawaii & Pacific territories

Each module includes:

- Primary and secondary hazard categories
- Critical infrastructure dependencies
- First-72-hour planning prompts
- Days-4-to-14 continuity prompts
- Weeks-to-months recovery prompts
- Local-source validation guidance

### Household resilience planner

The planner can record non-sensitive planning fields such as:

- Household size
- Water and food duration
- Medication and medical continuity
- Alternate communications
- Out-of-area contact
- Shelter or relocation plan
- Transportation fallback
- Dependent and pet needs
- Documents and financial backups

It generates a **planning gap list**, not a probability score or safety prediction. Do not enter names, addresses, account numbers, medical record numbers, or other sensitive identifiers.

## Quick start

### Option 1: Open locally

1. Download or clone this repository.
2. Open `index.html` in a modern browser.
3. Use the navigation on the left to explore the dashboard.
4. Open `instruction-manual.html` for the full operating guide.

### Option 2: Use GitHub Pages

This is a static site and can be hosted with GitHub Pages:

1. Push the repository to GitHub.
2. Open the repository’s **Settings**.
3. Select **Pages**.
4. Choose the main branch and repository root as the publishing source.
5. Open the generated Pages URL.

No build step is required.

## Repository structure

```text
black-meridian/
├── index.html                 # Main offline dashboard
├── instruction-manual.html    # Operator and household-planning manual
├── README.md                  # Project documentation
├── LICENSE                    # MIT License
├── assets/
│   ├── black-meridian-hero.png    # Background artwork
│   ├── black-meridian-poster.png  # Typography-complete project graphic
│   └── black-meridian-poster.svg  # Scalable version of the graphic
├── data/
│   ├── scenario.json          # Fictional campaign source data
│   ├── us-reality.json        # Public-source U.S. reference data
│   └── us-regions.json        # Broad regional planning modules
└── storage/
    └── README.md              # Suggested location for exported drafts
```

## Recommended workflow

1. Read the scope and limitations in the instruction manual.
2. Review the **Exercise brief**.
3. Review the **U.S. reality layer** without treating force totals as deployable strength.
4. Open **Regional planner** and select the closest planning region.
5. Complete the household baseline using non-sensitive information.
6. Review the resulting planning gaps.
7. Use **Orders & logs** to record assumptions and decisions.
8. Use **Evaluation** to record lessons and after-action observations.
9. Export important drafts and move them into `storage/`.
10. Validate broad assumptions with official local, state, tribal, and federal sources.

## Storage and browser behavior

The dashboard uses browser `localStorage` for draft orders, scorecards, and household-planning entries. These drafts are local to the browser profile and are not automatically shared between computers or browsers.

Use the export buttons to create portable JSON files. Move those files into the repository’s `storage/` directory if desired.

The browser cannot reliably write directly into an arbitrary folder when an HTML file is opened locally. This is why exports are downloaded through the browser first.

## Editing the data

The editable reference files are in `data/`:

- `scenario.json` — fictional campaign data
- `us-reality.json` — public-source U.S. context
- `us-regions.json` — regional planning modules

The dashboard embeds its data so it can operate offline and through GitHub Pages without a server-side API. If you edit a JSON source file, update the corresponding embedded JSON block in `index.html` before publishing the change.

When changing public-source figures:

1. Record the source URL.
2. Record the publication or update date.
3. Distinguish authorization, readiness, availability, and deployment status.
4. Use ranges or confidence labels when exact values are not available.
5. Recheck local official sources before using the result for household decisions.

## Public sources

The current public-source layer links to:

- [Congressional Research Service — FY2026 NDAA: Active Component End-Strength](https://www.congress.gov/crs-product/IN12651)
- [Congressional Research Service — FY2026 NDAA: Reserve Component End-Strength](https://www.congress.gov/crs-product/IN12652)
- [FEMA National Risk Index Data](https://www.fema.gov/about/openfema/data-sets/national-risk-index-data)
- [Ready.gov](https://www.ready.gov/)
- [Ready.gov — Build a Kit](https://www.ready.gov/kit)
- [CISA — Public Safety Communications Resiliency](https://www.cisa.gov/news-events/news/public-safety-communications-resiliency-ten-keys-obtaining-resilient-local-access-network)
- [National Weather Service](https://www.weather.gov/)
- [USGS Natural Hazards](https://www.usgs.gov/natural-hazards)

These links are starting points. Local emergency-management agencies, utilities, public-health agencies, transportation agencies, and tribal authorities should be treated as the most relevant sources for local planning.

## Design principles

- **Fiction before false precision:** The military campaign is fictional and deliberately abstract.
- **Separate facts from assumptions:** Public data and scenario assumptions are not the same thing.
- **Model effects, not just force totals:** Civilian outcomes are shaped by power, water, fuel, communications, medical care, transportation, and supply chains.
- **Use multiple horizons:** Immediate continuity, extended disruption, and recovery require different decisions.
- **Preserve uncertainty:** A planning tool should make uncertainty visible instead of disguising it with exact-looking scores.
- **Prefer useful preparation:** Plans for outages, severe weather, smoke, transportation failure, medical interruption, and supply disruption remain useful even when extreme scenarios do not occur.

## Safety and responsible use

This repository should not be used to:

- Identify real-world targets or vulnerabilities
- Produce attack plans or weapons-employment instructions
- Infer that a real-world conflict is imminent
- Replace emergency alerts or instructions from public authorities
- Store personal, medical, financial, or location-sensitive information

For an immediate real-world emergency, follow official alerts and contact local emergency services.

## Project status

**Version:** 0.1-draft  
**Date:** 2026-09-06  
**Format:** Static offline web application  
**Build step:** None required

## License

BLACK MERIDIAN is free for everyone to use, study, modify, and share under the [MIT License](LICENSE).

The license applies to the dashboard, scenario content, documentation, data files, and project artwork included in this repository. See `LICENSE` for the complete text.
