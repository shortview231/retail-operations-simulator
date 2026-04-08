# Overview

`retail-operations-simulator` is the public baseline for Lucid Vision's retail simulation work.

## What is credible today

- There is an earlier SQL + Python POS simulator foundation
- There is a more ambitious vending-first simulator with documented schema and workflow structure
- The current public repo includes a proof pack that demonstrates launch flow, inventory depth, vendor planning, order state, loadout, and reporting
- The architecture is operational, not just visual: inventory, vendors, machines, and reporting are connected parts of one system story
- SQLite-backed persisted state gives the simulator a stronger systems posture than a throwaway prototype

## What this public repo is showing

The goal of this repository is to make the simulator legible in public without dumping internal project state. It is showing:

- the current simulator direction
- the vending-first workflow shape
- the architectural boundary of the public baseline
- the proof artifacts that demonstrate real operational surfaces

## Why the baseline matters

For a public repo, the value here is not fake completeness. The value is that the simulator already reads like a real operations system: it has multiple workflow surfaces, documented structure, and a visible proof layer that connects inventory, vendor ordering, machine planning, and reporting.

## Why this simulator stands out

- It is built around a vending-route operational model rather than a generic retail abstraction
- It connects inventory, procurement, machine loadout, and reporting into one simulation story
- It presents the simulator as a business decision engine, not just a front-end concept
- It uses SQLite-backed state architecture to make runs and operational changes persistent and inspectable

## Current public boundary

- no internal save files
- no private local machine paths
- no operator-identifying setup data
- no claim that this repo contains the full internal simulator implementation

## Demonstration pack

The public proof pack includes:

- architecture and workflow notes under `docs/`
- eight sanitized simulator screenshots under `screenshots/`
- verification notes explaining what each public artifact proves

This keeps the public repo concrete, reviewable, and honest about current maturity.
