# Retail Operations Simulator

Public-facing baseline for a real retail operations simulation system with a documented vending-first engine and a public-safe proof pack.

This repository is intentionally honest about scope. It does not pretend to be the entire internal simulator build. It exists to show the current architecture, operating model, and proof artifacts in a public-safe form that hiring managers, collaborators, and clients can evaluate quickly.

## Why This Matters

Retail simulation is only useful if it can represent actual operational decisions, not just static dashboards or toy screens. This repo is meant to show a system-builder approach to that problem:

- inventory, ordering, and machine loadout treated as connected workflows
- simulation state modeled through SQLite-backed operational structures
- a proof layer that demonstrates launch flow, storeroom ops, vendor planning, and reporting
- a public boundary that keeps private operator details and internal save data out of the repo

## What Exists Today

- An earlier SQL + Python POS simulator portfolio project
- An active vending-first retail simulator project inside Lucid Vision
- A documented Phase 1 schema registry for the vending simulator
- Existing setup and run scripts for simulator database and run-loop support
- A public-safe 8-shot proof pack covering launch flow, storeroom operations, ordering, loadout, and reports

## Compact System Flow

`manager setup -> storeroom inventory -> vendor planning -> current order -> machine loadout -> reports`

The current public baseline shows how the simulator moves from bootstrap and inventory state through vendor ordering and machine planning into operational reporting surfaces.

## Proof Layer

- `screenshots/01-launch-surface-demo.svg` shows run bootstrap and continue flow
- `screenshots/02-storeroom-ops-demo.svg` shows the central operations surface
- `screenshots/03-inventory-depth-demo.svg` shows product-level inventory depth and fill-gap logic
- `screenshots/04-vendor-workspace-overview-demo.svg` shows vendor workspace state
- `screenshots/05-vendor-catalog-demo.svg` shows catalog planning and draft-order actions
- `screenshots/06-current-order-demo.svg` shows current order totals and in-transit tracking
- `screenshots/07-machine-loadout-demo.svg` shows machine slot planning and depth updates
- `screenshots/08-reports-summary-demo.svg` shows operations, personnel, and business reporting surfaces
- `docs/verification.md` maps each artifact to the simulator behavior it validates

## Public Positioning

This repo is strongest when read as a credible engineering baseline:

- it documents a real simulator direction without overstating polish
- it shows operational depth across multiple surfaces instead of a single mock screen
- it keeps the scope honest: proof, architecture, and public-safe documentation rather than an internal code dump
- it preserves the connection between simulation design and business workflow

## What This Repo Does Not Claim

- It is not the full internal Lucid Vision simulator codebase
- It does not publish internal save files or operational data
- It does not expose private local paths or operator-identifying setup details
- It does not claim the public repo is the complete finished simulator product

## Source of Truth

The current working materials live inside `~/Desktop/Projects/Lucid_Vision`.

## Recommended GitHub Metadata

- Description: `Public baseline for a retail operations simulator with vending-first workflow docs, proof artifacts, and architecture notes.`
- Website: `https://shortview231.github.io/`
- Topics: `retail-simulator`, `operations`, `sqlite`, `simulation`, `inventory`, `vending`, `workflow`, `proof-pack`
