# Architecture

## System shape

The simulator is organized around persistent operating state and connected workflow stages rather than disconnected screens.

Core areas include:

1. scenario and run state
2. inventory and replenishment
3. vendor and catalog planning
4. order tracking
5. machine slot and depth planning
6. reporting and decision review

## Simulation state

Scenario state is persisted so an operating run can be initialized, continued, and advanced over time. This supports repeatable scenarios and makes state changes inspectable.

## Inventory model

Inventory is represented with product-level availability and depth so it can support fill-gap analysis, replenishment decisions, and downstream machine planning.

## Vendor model

Vendor and catalog structures represent sourcing as an explicit part of the workflow rather than an assumed background step.

## Order pipeline

Purchasing moves from planning through order creation and current-order tracking. This provides a reviewable path between sourcing decisions and downstream inventory effects.

## Machine loadout

Machine state is represented at the slot and depth level, supporting product-placement and replenishment decisions.

## Reporting

Reporting surfaces summarize current scenario state across operational, personnel, and business views. The reporting layer is intended for decision review, not only presentation.

## Design principles

- persist meaningful state
- make workflow stages explicit
- keep example data inspectable
- separate operational logic from presentation
- document assumptions and boundaries
- use sanitized examples for public demonstration
