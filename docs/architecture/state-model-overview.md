# State Model Overview

This document gives a compact public-safe view of the simulator's state structure without publishing the full internal schema.

## Core state areas

- **run state**: identifies the active scenario and day progression
- **storeroom inventory**: tracks on-hand product depth and replenishment pressure
- **vendor planning**: represents supplier-facing catalog and ordering decisions
- **current order state**: tracks draft or active procurement actions
- **machine state**: represents slot/depth loadout for route machines
- **report state**: summarizes the operational picture for review surfaces

## State relationships

`run state -> storeroom inventory -> vendor planning -> current order -> machine state -> reports`

## Why this artifact exists

The repo already includes screenshots and architecture notes. This file gives one more concrete layer: a quick state-model summary that helps reviewers understand how the simulator is organized as a system rather than a collection of isolated screens.
