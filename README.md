# Retail Operations Simulator

A public portfolio project demonstrating how retail and vending operations can be modeled as connected workflows rather than isolated dashboards.

## What the project demonstrates

The simulator focuses on operational decisions across:

- storeroom inventory
- vendor planning
- purchasing and current orders
- machine slot and loadout planning
- persistent scenario state
- operational reporting

The project is intentionally scoped as a portfolio case study. It presents the architecture, example data, and proof artifacts needed to evaluate the design without publishing private operating data or unrelated internal systems.

## System flow

```text
scenario setup
  -> storeroom inventory
  -> vendor planning
  -> order tracking
  -> machine loadout
  -> operational reports
```

## Engineering approach

### Persistent state

The simulator models an ongoing operating scenario rather than a collection of static screens. SQLite-backed state supports repeatable scenario progression and makes operational changes inspectable over time.

### Inventory model

Inventory is represented at the product and on-hand level so the system can support fill-gap analysis, replenishment decisions, and downstream machine loadout planning.

### Vendor and ordering workflow

Vendor catalogs and ordering steps connect purchasing decisions with expected inbound inventory. Drafting and current-order views make the purchasing workflow reviewable instead of treating procurement as an invisible background process.

### Machine loadout planning

Machine state is represented with slot-level product and depth information, supporting more realistic placement and replenishment decisions.

### Reporting

Reporting surfaces summarize the current scenario across operational, personnel, and business-facing views. The emphasis is on decision support and workflow visibility rather than decorative dashboarding.

## Proof artifacts

The repository includes a curated demonstration set:

- launch and scenario-flow examples
- storeroom operations
- inventory depth and fill-gap examples
- vendor workspace and catalog examples
- current-order tracking
- machine loadout planning
- reporting summaries
- public-safe sample JSON state
- verification documentation linking examples to modeled behavior

## Repository structure

```text
retail-operations-simulator/
├── docs/          # Architecture, flow, schema, and verification notes
├── examples/      # Public-safe sample state and reporting data
├── screenshots/   # Demonstration surfaces
└── README.md
```

## Skills demonstrated

- Python and SQL-oriented system design
- relational and state modeling
- SQLite-backed persistence
- operations workflow analysis
- inventory and procurement modeling
- business reporting
- schema documentation
- testable sample-state design
- technical communication

## Public-data boundary

This repository contains only portfolio-safe examples and documentation. It does not contain real customer records, private operator data, credentials, personal financial data, or private production system configuration.

## Portfolio positioning

This project is best read as evidence of business-systems thinking: translating a real operating process into state, workflow stages, data structures, and decision-support surfaces while keeping the design understandable and testable.