# Public Safety

## Sanitization rules used for public proof artifacts

- Remove personal names and demographic fields from manager setup views.
- Remove absolute local filesystem paths and internal machine/user paths.
- Remove or neutralize UUID-like internal run/order identifiers when unnecessary.
- Keep metrics and workflow structures that prove engine capability.

## Why this matters

The repo should demonstrate real operational depth without exposing private operator identity or local environment details.
