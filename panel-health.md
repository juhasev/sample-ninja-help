## Health Metrics

### Health score

The panel health score measures how many panelists are invited and completing projects. If the started count is higher than the invited count, the started count is used instead; i.e., you run many projects that do not send invitations at all. The selected period and/or **Sub Panel** filter affects the health score.

> Formula is: invited count OR started count/completed count x 100%

> A low health score is an indication of panelist fatigue or other issues, like panelists not completing enough projects. When panelists are not earning any reward points, they have little reason to start projects or participate in general.

### Quality score

The quality score ranges from 0 to 100. Each time a panelist is returned to Sample Ninja with the status "completed," the quality score is incremented by 10 quality points. The quality score is stored in **QUALITY_SCORE** variable, enabling you to use it in the Business Rules, qualifications, filters, and more.

### Scores

#### Score additions
Each time a panelist is returned to Sample Ninja with the status "completed," the quality score is incremented by +10.

#### Score deductions

- **Is Proxy -10** Panelist is using a public VPN service.
- **Is Hosted -20** Panelist IP address originates from a hosted server. This could be a targeted bot.
- **Is Bot -20** Panelist is detected as a bot.
- **Ip Mismatch -20** Panelist IP address changed in the middle of the project.
- **Duplicate Fingerprint -5** Somebody else has the same exact fingerprint.
- **Fingerprint Mismatch -20** Fingerprints do not match from start to end.
- **Out of Country -5** Panelist is out of the country.
- **Speeding -10** Panelist speeding.
- **Link Manipulation -45** Panelist has potentially engaged in link manipulation.
- **Refer Friend -5** Refer a friend error or potential abuse
- **Quality -7** Returned from survey with status quality
- **Duplicate -5** Returned from survey with status duplicate
- **Security -7** Returned from survey with status security
- **Cookie Deleted -10** Panelist deleted the tracking cookie or used an incognito window
- **Spoofed Location -45** Panelist is attempting to hide their true location
- **Reconciled -20** Panelist has been reconciled for providing inconsistent answers
- **Fraud -45** Panelist is engaged in fraudulent activity

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

Displays percentage values of the total Panellists held within the platform. If you mouse over any of these statuses, it will give the actual number of Panellists.

### Start sources
Displays a pie chart what sources panelists are starting from. Possible values are 

- **Android** (Mobile App)
- **Members** App
- **Invite**
- **Apple iOS** (Mobile App)

This chart can be generated for any time period or sub-panel combination. Simply use the blue filter icon to set desired filters.

### Churn

Displays the number of panelists added and lost due to churn (subscriptions, blacklisting) over time. The periods can be either days, weeks, or months.

### Filter by Sub Panel

Click the blue filter icon in the top-right corner to filter by **Sub Panels** and/or time range.

### Note about caching
We use advanced server-side caching. This cache time is about 2 hours on average. For example, if you deleted 1000 panelists, it would take, on average, two hours for those changes to be reflected on the charts.

