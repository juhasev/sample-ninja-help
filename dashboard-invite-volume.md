## Invitation Volume

This widget shows how many project invitations your panelists receive. It answers a simple question: **are you inviting your panel evenly, or are some panelists being asked far more often than others?**

Over-inviting is one of the quickest ways to wear out a panel. Panelists who are asked too often tend to stop responding, rush through surveys or unsubscribe, which shrinks your panel and weakens your data over time. Use this widget to spot over-inviting early, before it shows up in your response rates and churn.

**Average = invitations sent ÷ panelists** over the selected period (the last 7, 30 or 90 days, or the last 12 months).

For example, say four panelists received 1, 2, 6 and 0 invitations. That is 9 invitations in total:

- Among **invited only**, the average is 9 ÷ 3 = **3.00** and the median is **2**.
- Across the **whole panel**, the average is 9 ÷ 4 = **2.25** and the median is **1.5**.

### What the widget shows

- **Average** — invitations per panelist for the selected period. Longer periods naturally have higher averages, so anything other than 30 days also shows the figure per 30 days. Use that figure to compare periods.
- **Median** — the middle panelist's invitation count. A few heavily invited panelists can pull the average up, but they barely move the median. A large gap between the two means invitations are uneven.
- **Panel reached** — the share of the panel that received at least one invitation during the period.
- **Most invites** — the highest number of invitations any one panelist received. Click the icon next to it to open that panelist. The icon is only shown to users who are allowed to view panelists.
- **Next highest** — the second highest panelist's count. If it is far below the most invites, the top panelist is an outlier worth checking.
- **Chart** — how many panelists received each number of invitations. The same groups are used for every period, so you can compare the shape between periods.
- **Same-day email warning** — an amber line below the chart when any panelist was sent more than one project email on the same day during the last 7 days. It always covers the last 7 days, whichever period you have selected.

Use the settings menu to change the period, to switch between invited only and whole panel, or to show selected sub panels only. The download button exports the figures as a CSV file.

### Invited only or whole panel

- **Invited only** counts just the panelists who received at least one invitation during the period. Use it to see how hard you are working the panelists you actually contact.
- **Whole panel** also includes panelists who received none, shown as the grey **0** column. Use it to see how much of your panel is sitting idle.

The whole panel is your subscribed panelists, plus anyone invited during the period who has since unsubscribed or been blacklisted. Those panelists stay in the count because they did receive the invitations, and over-mailing may be why they left.

The number of invitations and the most invites are the same in both views. Only the average, the median and the chart change.

### What counts as an invitation

- Invitations count **regardless of how they were delivered**: email, push notification or webhook.
- Each panelist counts **once per project**, even if the invitation was resent.
- **Reminders** are not counted.
- **Qualitative projects** count from the moment a panelist is added to the project, even though Sample Ninja sends them nothing. Your team contacts these panelists directly, so the date is when they were added, not when they were contacted.
- Panelists who have been **deleted** from your panel are no longer counted.

### What the same-day email warning counts

- It counts **emails**, so unlike the rest of the widget it includes **reminders**. An invitation and a reminder on the same day will trigger it.
- **Push notifications and webhooks** are not counted, and neither are newsletters or qualitative projects, because none of these create a project email.
- Days are **calendar days in UTC**, so two emails either side of midnight UTC count as separate days.
- It is a warning only. Nothing is held back or blocked, and some panels choose to send this often.

### What it means for panel owners

- **Invitation fatigue.** Panelists who are invited too often stop responding or unsubscribe. Watch the right-hand columns of the chart, and compare the 7 day and 30 day views to spot short bursts.
- **Wasted capacity.** A low panel reached means a large part of your panel is not being used. Those panelists may drift away, and you may be paying to recruit people you already have.
- **Sampling balance.** If a small group receives most of the invitations, your sampling may be favoring the same people. Review your projects' targeting and quotas, as narrow targeting often concentrates invitations on the same panelists.
- **Test accounts.** A most invites figure far above the next highest is often an internal test account rather than a real panelist. Open the panelist to check.

### What it means for sample buyers

- **Respondent quality.** Buyers and auditors often ask how frequently panelists are contacted. Panelists who are invited at a sensible rate tend to be less fatigued and less likely to become professional survey takers.
- **Read it together with other metrics.** Invitation volume is most meaningful next to response rates, churn and panel decay. There is no single "correct" number: it depends on your panel size, how many projects you run and how narrowly they target.

### Unusual values

> **A whole panel average well below 1** is normal for short periods and large panels, as most panelists will not have been invited recently.

> **A median of 0** in the whole panel view means more than half of your panel received no invitations during the period.

> **Long periods can read slightly low** in the whole panel view, because panelists who joined recently had less time to be invited.

> **When filtering by sub panel**, panelists are counted under the sub panel they belong to today, including invitations they received before moving to it.

> **Figures can differ slightly between periods**, because each period is calculated when you first open it and then kept for up to an hour. The widget shows how long ago the figures on screen were calculated. For example, the 7 day figure can briefly show more than the 30 day figure if nearly all recent invitations went out in the last week and more were sent between the two calculations.

> **The refresh button** recalculates the figures on screen and clears the saved figures of every other period, so they are recalculated when you next open them. The 12 month period can take several seconds on large panels.
