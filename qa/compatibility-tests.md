# 2007 Safari Regression Check

## Visual comparison
- Captured a 320×480 WebKit screenshot of the patched simulator (`current-version.png`) and compared it with the pre-retrofit layout from commit 5a7b128 (`previous-version.png`). Both show four evenly spaced blob rows, matching top-row button spacing, and the fixed info icon in the lower-right corner.

## Interaction parity
- Automated taps on blob key indices 3 → 5 → 10 → 5 yield the text `hltl` in both builds, ensuring center-letter selection matches the 2007 layout.
- A left glide on the first blob key appends `b` in both builds, confirming swipe hysteresis logic remains intact.

_All checks executed in WebKit via Playwright._
