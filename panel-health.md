## Health Metrics

### Health score

The **Health score** is a single number from 0 to 100 that tells you how healthy your panel is. It combines five measurements, each scored from 0 to 100, and shows which of them is holding the panel back.

The gauge is red below 30, yellow from 30 to 70 and green above 70.

#### What it measures

- **Activity** (25% of the score) — the share of subscribed panelists who started a project in the last 90 days. 35% or more scores 100.
- **Responsiveness** (20%) — the share of the panelists you invited in the last 90 days who started a project. 10% or less scores 0, 55% or more scores 100.
- **Reachability** (20%) — the share of subscribed panelists whose email address has not bounced. 92% or less scores 0, 99% or more scores 100.
- **Quality** (20%) — the share of the panelists who started a project in the last 90 days and have a quality score below 70. 40% or more scores 0, 5% or less scores 100.
- **Growth** (15%) — panelists who joined minus those who unsubscribed or were blacklisted in the last 90 days, as a share of subscribed panelists. A panel that stays the same size scores 50, 5% growth or more scores 100, a loss of 5% or more scores 0.

Hover over a row to see the measured value behind its score.

#### Main issue

When the lowest of the five scores is below 70 it is shown as the **Main issue**. That is the first thing to work on:

- **Activity** or **Responsiveness** — panelists are not taking part. Look at how often they are invited, how relevant the projects are and what they earn.
- **Reachability** — too many emails bounce. See the Annual Decay section below for what to do with bounced-email panelists.
- **Quality** — many of your active panelists have collected security, duplicate or quality flags. Review them in the Panelist Manager.
- **Growth** — more panelists leave than join. Check recruitment and the Churn widget.

#### Good to know

- The score always looks at the last 90 days. The report period you select on this page does not change it, so the number always means the same thing. The sub-panel filter does apply.
- A measurement is left out when there is too little data to trust it: Responsiveness when fewer than 100 panelists were invited, Quality when fewer than 100 panelists started a project. It is shown as **n/a** and the other measurements make up the whole score.
- When nobody was invited and nobody started a project in the last 90 days, the page shows **No fieldwork in the last 90 days** and no score. An idle panel cannot be measured.
- The score is also stored once a day, so the **Quality & Health** tab of the time series chart shows how it develops. The history starts on the day the score was introduced.

> **Tip:** Large panels usually score lower on Activity and Responsiveness than small ones, because a smaller share of a large panel is needed for each project. Compare a panel with its own history first.

### Quality score

The quality score ranges from 0 to 100. Each time a panelist is returned to Sample Ninja with the status "completed," the quality score is incremented by 10 quality points. The quality score is stored in **QUALITY_SCORE** variable, enabling you to use it in the Business Rules, qualifications, filters, and more.

### Scores

#### Score additions
Each time a panelist is returned to Sample Ninja with the status "completed," the quality score is incremented by +10.

#### Score deductions

- **Is Proxy -10** Panelist is using a public VPN service.
- **Is Hosted -20** Panelist IP address originates from a hosted server. This could be a targeted bot.
- **Is Bot -20** Panelist is detected as a bot.
- **Duplicate Fingerprint -5** Somebody else has the same exact fingerprint.
- **Fingerprint Mismatch -20** Fingerprints do not match from start to end.
- **Out of Country -5** Panelist is out of the country.
- **Speeding -10** Panelist speeding.
- **Link Manipulation -45** Panelist has potentially engaged in link manipulation.
- **Quality -7** Returned from survey with status quality
- **Duplicate -5** Returned from survey with status duplicate
- **Security -7** Returned from survey with status security
- **Cookie Deleted -10** Panelist deleted the tracking cookie or used an incognito window
- **Reconciled -20** Panelist has been reconciled for providing inconsistent answers

> Always reconcile your projects to keep the **QUALITY_SCORE** accurate! In the same way, try to always set the LOI or Length of the interview as accurately as you can, as going forward, speeding will decrease a panelist's quality score. You can control speeding threshold percentages in **Settings -> Speeding Threshold**.

> The Average Quality Score is calculated using panelists with at least one completed interview. This keeps the average quality score more realistic as you only really care about panelists who are actually completing surveys.

> You can easily find all panelists whose quality Score has fallen too low. Similarly, you can automatically exclude panelists with low-quality scores by adjusting your panel's **Business Rules**.

### Active vs. Engaged

Displays the percentage breakdown of the total number of Panelists who are defined as **ACTIVE** or **ENGAGED**. An active panelist is someone you have invited who has started at least one survey in the past N days. An engaged panelist is somebody you have completed surveys in the past N days. You should think of that metric from the panelist's experience point of view. Ideally, all of your panelists are engaged and earning rewards, which ultimately means they are less likely to leave.

You will see the actual counts and percentages when you mouse over the chart.

> What is an active or an engaged panelist? You define that in Settings -> Basic settings, then click anywhere on the **Active Panelist** or **Engages Panelist** box. Use the **Query Builder** to define your own criteria, and remember to use **Filters** to impose restrictions, such as how often someone can be invited.

### By status

Displays percentage breakdown of the total number of Panellists defined as **Subscribed, Unsubscribed** or **Blacklisted** within the Platform.  Mousing over the chart automatically opens up the chosen segment. It displays the percentage that fulfills that criteria (and the actual number of panelists in that segment in brackets. 

> Sample Ninja will automatically remove unsubscribed and blacklisted panelists from your panel within 12 months. When someone unsubscribes or is blacklisted, we will delete their variable data within 4 hours, but retain their activity for 12 months to ensure accurate reporting for projects and other features.

### Panel Utilization
The panel utilization displays a chart of panelist activity and statistics on how you use your panelists. 

#### Utilization
The percentage of panelists who have been invited to at least one project.

#### Started
The percentage of panelists who have started at least one project.

#### Profile
A percentage of panelists have profile terminated at least once.

#### Quota
The percentage of panelists who have had their quota terminated at least once.

#### Security
The percentage of panelists has had security terminated at least once.

#### Completed
Percentage of panelists who have completed at least one project.

> To look at a different time range, click the filter button in the top right corner.

### By Activity

Displays percentage values for the total Panelists on the platform. If you mouse over any of these statuses, it will give the actual number of Panelists.

### Start sources
Displays a pie chart what sources panelists are starting from. Possible values are 

- **Android** (Mobile App)
- **Members** App
- **Invite**
- **Apple iOS** (Mobile App)

This chart can be generated for any time period or sub-panel combination. Simply use the blue filter icon to set desired filters.

### Churn

Displays the number of panelists added and lost due to churn (subscriptions, blacklisting) over time. The periods can be either days, weeks, or months.

### Annual Decay

The **Annual Decay** widget shows how many panelists your panel has effectively lost — the "decay" of your active, reachable audience. It gives you a quick, at-a-glance view of panel attrition so you can keep your panel healthy and your reachable sample size accurate.

#### What it shows

The chart breaks the lost panelists down into three categories:

- **Bounced email** — Subscribed panelists whose email address is no longer valid (their mail has bounced). They are still subscribed, but you can no longer reach them by email.
- **Unsubscribed** — Panelists who have opted out and asked to stop receiving communications.
- **Blacklisted** — Panelists who have been blocked or removed from the panel and are no longer eligible to participate.

Each slice of the pie represents one of these categories. Hover over a slice to see both the exact count and its share of the total decay.

#### Why it matters

Every panelist in these three buckets is someone you can no longer invite or who can no longer respond. Watching these numbers over time helps you:

- **Gauge panel health** — a growing decay total signals that your reachable audience is shrinking.
- **Spot deliverability problems** — a rising *Bounced email* slice points to data-quality or email-hygiene issues worth investigating.
- **Understand opt-out trends** — a climbing *Unsubscribed* slice can indicate over-mailing or messaging that isn't resonating.
- **Plan recruitment** — knowing how fast you lose panelists helps you recruit enough new members to stay ahead of attrition.

#### Filtering and refreshing

- When sub-panel filtering is available, the figures can be scoped to the specific sub-panels you select, so you can compare decay across different segments of your panel.
- The numbers are cached for performance. Use the widget's **refresh** button to force an up-to-the-moment recalculation.

> **Tip:** If the widget shows *Insufficient data*, it simply means no decayed panelists were found for the current selection — a healthy sign.

### Filter by Sub Panel

Click the blue filter icon in the top-right corner to filter by **Sub Panels** and/or time range.

### Note about caching
We use advanced server-side caching. This cache time is about 2 hours on average. For example, if you deleted 1000 panelists, it would take, on average, two hours for those changes to be reflected on the charts.
