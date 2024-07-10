## Health Metrics

### Health score

The panel health score measures how many panelists are invited and completing projects. If the started count is than the invited count, then started count is used instead, i.e., you run a lot of projects that do not send invitations our at all. The selected period and/or **Sub Panel** filter affects the health score.

> Formula is: invited count OR started count/completed count x 100%

> Low health score is an indication of panelist fatigue or other issues like panelists not completing enough projects. When panelists are not earning any reward points, they have little reason to start projects or participate in general.

### Quality score

The quality score can be between 0 and 100. Each time panelist is returned to Sample Ninja with the status "completed," the quality score is incremented by 10 quality points. The quality score is stored in **QUALITY_SCORE** variable, enabling you to use it in the Business Rules, qualifications, filters, and more.

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

> Always reconcile your projects to keep the **QUALITY_SCORE** accurate! In the same way, try to always set the LOI or Length of the interview as accurately as you can, as going forward, speeding will decrease a panelist's quality score. You can control speeding threshold percents in **Settings -> Speeding Threshold**.

> The Average Quality Score is calculated using panelists with at least one completed interview. This keeps the average quality score more realistic as you only really care about panelists who are actually completing surveys.

> You can easily find all panelists whose quality Score has fallen too low. Similarly, you can automatically exclude panelists with low-quality scores by adjusting your panel's **Business Rules**.

### Active vs. Engaged

Displays the percentage breakdown of the total number of Panelists who are defined as **ACTIVE** or **ENGAGED**. An active panelist is somebody you have invited, and they have started at least one survey in the past N days. An engaged panelist is somebody you have completed surveys in the past N days. You should think of that metric from the panelist experience point of view. Ideally, all of your panelists are engaged and earning rewards, which ultimetely means they are less likely to leave.

You will see the actual counts and percentages by mousing over the chart.

> What is an active or an engaged panelist? You define that in the Settings -> Basic settings and click anywhere on the **Active Panelist** or **Engages Panelist** box. Use the **Query Builder** to define your own criteria, and remember to use **Filters** to impose restrictions like how often somebody can be invited.

### By status

Displays percentage breakdown of the total number of Panellists defined as **Subscribed, Unsubscribed** or **Blacklisted** within the Platform.  By mousing over the chart, it automatically opens up the chosen segment. It displays the percentage that fulfills that criteria (and the actual number of panelists in that segment in brackets. 

> Sample Ninja will automatically remove unsubscribed and blacklisted panelists from your panelist within 12 months. When somebody unsubscribes or gets blacklisted, we will delete their variable data within 4 hours but save their activity for 12 months to retain correct reporting for projects and other features.

### Reward Points on Hold

The chart displays a timeline of reward points issued for Projects vs. what portion is currently held. The points are held for any projects that have the reconcile toggle turned on (default). You must manually reconcile the project or mark it as reconciled so the held reward points disappear from the chart. The idea of the chart is to display the panel manager a view of the held reward points over a date interval. Consider reconciling projects more quickly if you see long hold times for the held reward points. Generally speaking, panelists do not want to wait too long for their earned reward points to become available.
Click on the sum button to see the totals.

> The reporting period is always the past six weeks.

### Panel Utilization
The panel utilization displays a chart of panelist activity and statistics on how you use your panelists. 

#### Utilization
Percentage of panelists have been invited to at least one project.

#### Started
Percentage of panelists have started at least one project.

#### Profile
A percentage of panelists have profile terminated at least once.

#### Quota
Percentage of panelists have quota terminated at least once.

#### Security
Percentage of panelists have security terminated at least once.

#### Completed
Percentage of panelists who have completed at least one project.

> To look at a different time range, click the filter button in the top right corner.

### By Activity

Displays percentage values of the total Panellists held within the platform. If you mouse over any of these statuses, it will give the actual number of Panellists.

### Churn

Displays the number of panelists added and lost due to churn (subscriptions, blacklisting) over time. The periods can be either days, weeks, or months.

### Filter by Sub Panel

Click on the blue filter -icon on the top right corner to filter by **Sub Panels** and or time range.

### Note about caching
> We use advanced caching on the server side. This cache time is on average about 2 hours. For example if you deleted 1000 panelists it would takes on average two hours for those changed to be reflected on the charts.

