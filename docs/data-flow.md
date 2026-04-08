# Data Flow

## Public-safe system story

The retail simulator models a vending-route operation against a SQLite-backed engine. Simulation state moves through controlled manager setup, inventory/vendor planning, route machine loadout, and reporting layers.

## High-level stages

1. Initialize or continue a manager run from persisted save state.
2. Build storeroom inventory by vendor contracts and catalog planning.
3. Draft and place vendor orders with case-level constraints.
4. Track pending deliveries, received stock, and on-hand counts.
5. Load route machines by slot/depth with product-specific constraints.
6. Advance simulation day and update route, inventory, and finance events.
7. View operations/personnel/business reporting snapshots from current state.

## Public boundary

- Proof screenshots are sanitized and path-neutral.
- No private local filesystem paths are published.
- No demographic/personally identifying inputs are published.
