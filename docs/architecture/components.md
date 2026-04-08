# Architecture Components

This note expands the top-level architecture summary into the main engine areas already reflected by the current public proof pack and documented simulator foundations.

## Simulation engine

The simulator is run-oriented. It keeps enough state to initialize, continue, and advance an operational scenario rather than resetting to a disconnected screen state.

## Inventory model

The inventory layer focuses on depth, availability, and replenishment implications. That makes inventory part of the simulation's decision logic instead of a passive reference table.

## Vendor model

Vendor workspaces and catalog browsing represent supplier relationships as an active planning surface. The simulator treats sourcing choices as part of the operational loop.

## Order pipeline

Order behavior moves through planning, draft creation, and current-order tracking. This creates a reviewable path between supplier selection and downstream inventory or machine impact.

## Machine loadout engine

Machine loadout is modeled at the slot/depth level, which gives the simulator a more realistic replenishment and placement layer than a generic stock transfer view.

## Reporting engine

The reporting surfaces collect current simulation state into business, personnel, and operations views so the simulator can support decision review as well as state mutation.
