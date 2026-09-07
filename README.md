# Exercise BLACK MERIDIAN

**Family first. Small groups. A free kitchen-table tabletop so American households can practice doing what it takes to stay a family — water, medicine, contact, a sharing rule — if a shock hits services at home. This file is an asset to that household. It is not a war staff.**

[Open the dashboard](index.html) · [Read the instruction manual](instruction-manual.html) · [Kitchen-table notes](docs/kitchen-table-notes.md)

![BLACK MERIDIAN — I need to play this game to protect my family](assets/black-meridian-poster.png)

> **Important boundary:** Countries are real. Campaign events, injects, and force bands are invented. This is a publicly discussed Taiwan Strait planning frame for U.S. household continuity. It is not an intelligence product, threat warning, forecast, operational plan, targeting tool, evacuation order, or personal safety guarantee. Do not use it to identify real bases, plants, ships, or hospitals as targets.

## Overview

BLACK MERIDIAN is free. You do not need a war plan. You need a line of people who still drink, take their medicine, and find each other. It combines:

- A **hard wall (Kobayashi Maru):** the war is unwinnable from a kitchen table; the family is winnable with the right mindset
- **Radio dispatches (mile markers):** after each inject, a world bulletin plus whether this table’s plan held, mixed, or failed
- A 90-minute **home-front session** that couples each campaign phase to a civilian effect (comms, medicine, fuel, payments, rumor)
- **Hotspot radios:** Taiwan Strait (most discussed), Canada / northern trade, Mexico / southern trade, and **Homeland worst night** (nightmare as home effects — no landing map, no ethnic armies)
- Group roster by callsign, mutual-aid roles, and a hard cap of three 14-day commitments
- A named Taiwan Strait campaign frame (U.S., PRC, Taiwan, Japan/Philippines/shipping as gray) with invented events
- Tactical commander decision records
- Fog-of-war and adjudication concepts
- Public-source U.S. force-scale context
- Broad regional civilian-resilience planning modules
- Household continuity planning across 72-hour, two-week, and longer recovery horizons
- Browser-local orders, scorecards, household-profile drafts, and session logs

The project is intentionally **operating-system agnostic**. It uses static HTML, CSS, JavaScript, SVG, and JSON files. No installation, package manager, database, external library, or backend service is required.

## Features

### Home-front session (start here)

- 90-minute clock: ethics, baselines, four injects, three commitments
- Group roles: facilitator, households, mutual-aid, information, civil picture
- Callsign roster (no names or addresses)
- Six civilian injects coupled to the Taiwan Strait campaign (H-01–H-06)
- Recommended path H-01, H-03, H-04, H-05
- Hard cap of three 14-day commitments, each requiring a test
- Session-log export

### Fictional campaign dashboard

- Exercise brief and commander’s problem
- Abstract Taiwan Strait schematic (not a targeting map)
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
│   ├── home-front.json        # 90-minute civilian session, coupled injects
│   ├── hotspots.json          # Taiwan / Canada / Mexico / homeland frames
│   ├── radio.json             # Mile-marker dispatches (plan held / partial / failed)
│   ├── us-reality.json        # Public-source U.S. reference data
│   └── us-regions.json        # Broad regional planning modules
└── storage/
    └── README.md              # Suggested location for exported drafts
```

## Recommended workflow

1. Open **Home-front session** and read the ethics list (effects, not targeting).
2. Pick a region and fill household baselines without names or addresses.
3. Add group callsigns to the roster.
4. Run H-01, H-03, H-04, and H-05 (90 minutes). After each inject, each household says stay, move, share, or wait.
5. Record **three** 14-day commitments, each with a test.
6. Export the session log into `storage/`.
7. Optionally run the overseas campaign staff tools (orders, evaluation).
8. Re-run after 14 days and count closed gaps.

## Storage and browser behavior

The dashboard uses browser `localStorage` for draft orders, scorecards, and household-planning entries. These drafts are local to the browser profile and are not automatically shared between computers or browsers.

Use the export buttons to create portable JSON files. Move those files into the repository’s `storage/` directory if desired.

The browser cannot reliably write directly into an arbitrary folder when an HTML file is opened locally. This is why exports are downloaded through the browser first.

## Editing the data

The editable reference files are in `data/`:

- `scenario.json` — Taiwan Strait public-scenario campaign data
- `home-front.json` — 90-minute home-front session and coupled injects
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

- **Names without targeting:** Use real countries so the shock is believable. Keep events invented and effects-only.
- **Separate facts from assumptions:** Public data and scenario assumptions are not the same thing.
- **Model effects, not just force totals:** Civilian outcomes are shaped by power, water, fuel, communications, medical care, transportation, and supply chains.
- **Use multiple horizons:** Immediate continuity, extended disruption, and recovery require different decisions.
- **Preserve uncertainty:** A planning tool should make uncertainty visible instead of disguising it with exact-looking scores.
- **Prefer useful preparation:** Plans for outages, severe weather, smoke, transportation failure, medical interruption, and supply disruption remain useful even when extreme scenarios do not occur.

## Safety and responsible use

This repository should not be used to:

- Identify real-world targets, plants, bases, bridges, or hospitals as attack surfaces
- Produce attack plans or weapons-employment instructions
- Infer that a real-world conflict is imminent
- Replace emergency alerts or instructions from public authorities
- Store personal, medical, financial, or location-sensitive information

For an immediate real-world emergency, follow official alerts and contact local emergency services.

## Project status

**Version:** 0.8  
**Date:** 2026-09-06  
**Format:** Static offline web application  
**Build step:** None required

## License

BLACK MERIDIAN is free for everyone to use, study, modify, and share under the [MIT License](LICENSE).

The license applies to the dashboard, scenario content, documentation, data files, and project artwork included in this repository. See `LICENSE` for the complete text.
