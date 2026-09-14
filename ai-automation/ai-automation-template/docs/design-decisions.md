# Design Decisions

## Goal

The system is designed to reduce the time spent manually searching for relevant jobs while keeping the final decision in human hands.

## Key decisions

- Use a broad first-pass research stage before filtering.
- Normalize data into a consistent schema before ranking.
- Deduplicate jobs before writing them to the job log.
- Use candidate context for relevance scoring.
- Keep job logs as the operational source of truth.

## Trade-offs

This design favors automation and reliability over one-off custom scraping logic.
