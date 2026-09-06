# State Model Overview

This document gives a compact view of the simulator's state structure.

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

The repository includes screenshots and architecture notes. This state-model summary gives reviewers a concise view of how the simulator is organized as a connected system rather than a collection of isolated screens.
