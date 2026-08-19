## Sampling Settings

#### Priority among live projects

Normally, you would leave this setting at the default of 5. Sample Ninja samples all projects every 15 minutes following the sampling priority order. If two or more projects compete for the same sample, you can raise this setting to prioritize one project over the others. The lowest priority is 1, and the highest is 10.

> Other project managers' priorities are taken into account as well, so establish a standard for sampling prioritization inside your organization. Setting the priority to the maximum every time defeats the purpose.

> Regardless of the priority, Sample Ninja attempts to finish each project by its end date by adjusting the invitation rate. For profiler projects, the priority instead directly controls the invitation volume per sampling cycle.

#### Invite abandoned after (hours)

This setting controls how long the sampling engine waits for a panelist to respond to an invitation. While an invitation is inside this window, it is counted as an outstanding potential complete — credited against your remaining target and excluded from the response rate — so no unnecessary new invitations are sent. Once the window closes without a response, the invitation is considered abandoned, and the engine sends replacement invitations. The default is 24 hours; the allowed range is 1 to 96 hours.

A short window replaces silent invitations quickly, which suits urgent projects but risks overages. A long window (48+ hours) samples patiently, keeps invitation volume down, and protects your quota allocations.

The window affects only sampling and statistics. A panelist can still participate after their invitation is considered abandoned, as long as the project's target completes has not been reached and their quota cell is not yet full.

> Setting the window shorter than your panelists' natural response time degrades the panelist experience: late responders will land on a "Project full" or "Quota full" page, which lowers future response rates and increases unsubscribe rates. For email-based consumer panels we recommend 24 hours or more; for mobile panels invited through push notifications, a window of a few hours is usually safe.

> The default for new projects can be changed in Settings → Panel Settings → Project Defaults.
