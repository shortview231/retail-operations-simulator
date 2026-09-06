# Domain Model

The simulator uses a compact domain model to connect operational state across the workflow.

## Core domains

- runs and days
- products and assortments
- storeroom inventory
- vendors and catalogs
- purchase orders and order state
- machine slots and machine loadout
- sales and ledger context
- events and staffing context

## Why this matters

The model is broad enough to represent a persistent retail operating loop rather than a single isolated workflow. Inventory, procurement, machine planning, and reporting can therefore be reasoned about as related state instead of separate screens.
