# Architecture

## Current system shape

The internal retail simulator evidence supports a layered story:

1. a lightweight SQL + Python POS simulator used as a portfolio-friendly proof of process design
2. a more ambitious vending-first retail simulator with a documented SQLite schema registry and supporting scripts

## Existing implementation truths

- The vending-first project tracks simulator runs, days, inventory, vendors, assortments, sales, money ledger entries, events, and staffing foundations
- The current schema registry explicitly treats the simulator as Phase 1 of a broader operations model
- The next internal steps documented in the schema registry focus on stronger staffing effects, scheduling policy, and UI workflow support

## Public baseline boundary

The first export should describe the simulator architecture and current maturity rather than claim a polished public product. Any future public examples should be derived from safe schema or fixture-level material.
