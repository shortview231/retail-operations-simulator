# Overview

`retail-operations-simulator` is the outward-facing baseline for Lucid Vision's retail simulation work.

## Current evidence

- POS portfolio project summary: # SQL + Python POS Simulator (Portfolio) A fictional retail company simulator using SQLite + Python with a basic POS GUI. ## Features - SQLite schema and seed data for products, customers, orders, and order_items - Python data layer for sales operations and...
- Vending simulator schema summary: # Phase 1 Schema Registry This registry defines the SQLite schema for the first runnable vending simulator slice. ## Database Location - SQLite DB: `sim/data/phase1_vending.sqlite` - Schema file: `sim/schema/phase1_vending.sql` - Setup script: `scripts/setup_phase1_db.py` - Registry exports: `data/csv/phase1_table_r...

## Truthful public framing

The repo should be presented as a retail-simulation foundation with a strong vending-first internal slice already documented. The initial public baseline stays docs-first so the public repo matches what is actually stable and reviewable today.
