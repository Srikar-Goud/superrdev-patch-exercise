# Notes

## Summary of changes
- Fixed SQL search filtering so archived tasks are excluded and status filtering applies correctly.
- Removed artificial `Thread.sleep()` latency from search requests.
- Moved pagination from application memory to database-level pagination.
- Fixed frontend loading and error state handling.
- Reset pagination when search or status filters change.
- Added validation for invalid page and pageSize values.

## What I chose not to change
I did not add search debouncing, request cancellation, broader refactoring, or changes to reference SQL files because they were outside the highest-priority fixes and the exercise was timeboxed.

## Biggest remaining risk
The application could benefit from more automated tests, especially for search combinations, pagination edge cases, and rapid successive requests.

## Tools / AI used
Used VS Code, Maven, browser/API testing, Git/GitHub, and ChatGPT for code review, bug identification, prioritization, and implementation guidance. I reviewed and tested the changes before committing them.