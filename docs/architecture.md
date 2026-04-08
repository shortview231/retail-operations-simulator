# Architecture

## Current system shape

The internal retail simulator evidence supports a layered story:

1. a lightweight SQL + Python POS simulator used as a portfolio-friendly proof of process design
2. a more ambitious vending-first retail simulator with a documented SQLite schema registry and supporting scripts

## Existing implementation truths

- The vending-first project tracks simulator runs, days, inventory, vendors, assortments, sales, money ledger entries, events, and staffing foundations
- The current schema registry explicitly treats the simulator as Phase 1 of a broader operations model
- The next internal steps documented in the schema registry focus on stronger staffing effects, scheduling policy, and UI workflow support

## Engine components

### Simulation engine

The simulator is organized around persisted run state and day progression. That matters because it lets the system behave like an ongoing operation instead of a one-off dashboard or static mock flow.

### Inventory model

Inventory is represented as an operating layer with on-hand depth, fill-gap visibility, and downstream loadout consequences. It is not just a list of products; it is part of the decision surface.

### Vendor model

The vendor layer captures supplier-facing planning, catalog views, and ordering workflows. This gives the simulator a stronger procurement dimension than a simple POS-style demo.

### Order pipeline

Catalog planning, draft order construction, and current-order tracking form a connected order pipeline. This makes purchasing behavior visible and reviewable as part of the simulator design.

### Machine loadout engine

Machine state is modeled at the slot/depth level, which supports realistic replenishment and product placement thinking. That level of detail is a core part of what makes the simulator vending-first.

### Reporting engine

Reporting surfaces summarize operational, personnel, and business state from the current simulation context. This helps the simulator read as a workflow and decision system, not just an interface study.

## Public baseline boundary

The first export should describe the simulator architecture and current maturity rather than claim a polished public product. Any future public examples should be derived from safe schema or fixture-level material.
