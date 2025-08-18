# Multiple Survey Starts Limitation

This setting allows administrators to control how often a survey participant (panelist) can start a new survey. It prevents panelists from starting multiple surveys too quickly, ensuring a more controlled and fair survey process.

## How it Works

When this feature is enabled, a minimum time is set between when a panelist can start one survey and then start another.

### Enable Max Delta Time

This toggle switch activates or deactivates the survey start limitation.
*   **On (Blue)**: The limitation is active. Panelists will be subject to the time restriction.
*   **Off (Gray)**: The limitation is inactive. Panelists can start surveys without this specific time restriction.

### Max Delta Time in Seconds Between Survey Starts

This field specifies the minimum amount of time, in seconds, that must pass before a panelist can start a new survey after completing or abandoning a previous one.

The value must be between `0` and `86400` seconds (inclusive).

*   **Example**: If this value is set to `1800` (which equals 30 minutes), a panelist must wait at least 30 minutes after starting one survey before they can start another.

## Panelist Experience

If a panelist tries to start a second survey before the specified "Max Delta Time" has passed, they will see a special page. This page will display a message, which can be customized by an administrator, explaining why they cannot proceed immediately.

On this page, the panelist will also be able to **abandon** their previous survey start.

*   If the panelist chooses to **abandon** the previous survey start, their session for that abandoned survey will be marked as "non-actionable." This means that a particular survey attempt will not be counted or processed further.

This feature helps manage survey participation and prevents unintended multiple entries, ensuring data quality and fair access for all panelists.