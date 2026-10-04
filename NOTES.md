# Patch Exercise Notes

## Changes Made
- Fixed SQL condition grouping so archived tasks are excluded and status filtering applies to both title and description matches.
- Added validation for page and pageSize values, including a maximum page size of 100.
- Added graceful handling of invalid task status values.
- Reset pagination to page 1 when search or status filters change.
- Improved request error handling, loading state cleanup, and protection against stale API responses.

## What I Did Not Change
- Kept the existing React component structure and Spring Boot architecture.
- Did not rewrite the database or introduce new dependencies.
- Did not change task sorting or existing API response fields.

## Biggest Remaining Risk
The backend still loads all matching tasks before applying pagination in memory. This may become inefficient as the dataset grows.

## Tools and AI Use
Used ChatGPT for debugging guidance, code review, and explanations. I reviewed the changes and manually tested the API, task listing, search, status filtering, pagination reset, and invalid pagination response. I am responsible for understanding and explaining the submitted changes.
