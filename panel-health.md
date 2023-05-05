## Health Metrics

### Health score

The panel health score measures how many panelist are invited and completing projects. If the started count than the invited count then started count is used instead i.e. you run a lot of projects that do not send invitations our at all. The selected period and/or **Sub Panel** filter affects the health score.

> Formula is: invited count OR started count / completed count x 100%

> Low health score is indication of panelist fatigue or other issues like panelists are not completing enough projects. When panelist are not earning any rewards points they have little reason to start projects or participate in general.

### Quality score

The quality score can be between 0 and 100. Each time panelist is returned to Sample Ninja with the status "completed," the quality score is incremented +10. The quality score is stored in **QUALITY_SCORE** variable enabling you to use it in the Business Rules, qualifications, filters and more.

### Scores

#### Score deductions
- **isProxy** -5 (Public VPN service)
- **isHosted** -20 (Proxy or origination from a known server)
- **isBot** -20
- **ipMismatch** -20
- **duplicateFingerprint** -5 (Duplicate fingerprint)
- **fingerprintMismatch** -20 (Fingerprint from start survey does not match fingerprint at the end)
- **isOutOfCountry** -5
- **speeding** -10 (Speeding threshold triggered, configurable in the panel settings)
- **linkManipulation** -45 (Panelist completed project so fast that most likely the exit link was altered)
- **quality** -20 (Reconciled or returned from a survey with quality status)
- **duplicate** -7 (Duplicate respondent)
- **security** -45 (Returned from a survey with security status)

> Please note that The Average Quality Score is calculated using panelists that have at least one completed interview. This keeps the average quality score more realistic as you only really care about panelists who are actually completing surveys.

> Always reconcile your projects to keep the Qualify Score accurate! Similarly, try to always set the LOI or Length Of Interview as accurately as you can, as going forward, speeding will decrease panelist's the quality score. You can control speeding threshold percents in **Settings -> Speeding Threshold**.

> You can easily find all panelists whose the Quality Score has fallen too low, similarly you can automatically exclude panelists with low-quality score by adjusting your panel's **Business Rules**.

### Active vs. Engaged

Displays the percentage breakdown of the total the number of Panelists who are defined as **ACTIVE** or **ENGAGED**. An active panelist is somebody you have invited and they have started at least one survey in the past N days. An engaged panelist is somebody you have actually completed surveys in the past N days. You should think of that metric from the panelist experience point of view. Ideally all of your panelists are engaged and earning rewards which ultimetely means they are less likely to leave.

By mousing over the chart you will see the actual counts and percentages.

> What is an active or an engaged panelist? You define that in the Settings -> Basic settings and click anywhere on the **Active Panelist** or **Engages Panelist** box. Use the **Query Builder** to define your own criteria and remember to use **Filters** to impose restrictions like how often can somebody be invited.

### By status

Displays percentage breakdown of the total the number of Panellists who are defined as **Subscribed, Unsubscribed** or **Blacklisted** within the Platform.  By mousing over the chart, it automatically opens up the chosen segment and displays the percentage that fulfil that criteria (and displays the actual number of panellists in that segment in brackets. 

> Sample Ninja will automatically remove ubsubscribed and blacklisted panelists from your panelist withing 12 months. When somebody unsubscribes or gets blacklisted we will delete their variable data within 4 hours but save their activity for 12 months to retain correct reporting for projects and other features.

### Panel Utilization
The panel utilization displays chart of panelist activity along with statistics how you are using your panelists. 

#### Utilization
Percentage of panelists have been invited to at least one project.

#### Started
Percentage of panelists have started at least one project.

#### Profile
Percentage of panelists have profile terminated at least once.

#### Quota
Percentage of panelists have quota terminated at least once.

#### Security
Percentage of panelists have security terminated at least once.

#### Completed
Percentage of panelists have completed at least one project.

> To look at a different time range click on the filter button in the top right corner.

### By activity

Displays percentage values of the total Panellists held within the platform. If you mouse over any of these statuses it will give the actual number of Panellists.

### Churn

Displays number of panelist added and lost due to churn (unsubscriptions) over time period. The periods can be either days, weeks or months.

> Please note that blacklisted panelists are not included in this, only panelists that **unsubscribe** on their own will.

### Filter by Sub Panel

Click on the blue filter -icon on the top right corner to filter by **Sub Panels** and or time range.

### Note about caching
> We use advanced caching on the server side. This cache time is on average about 2 hours. For example if you deleted 1000 panelists it would takes on average two hours for those changed to be reflected on the charts.

