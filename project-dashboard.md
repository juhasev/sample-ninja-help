## Project Dashboard

The project dashboard gives a wealth of statistics about your project.

### Toolbar button at the top right corner
- Use the "Reload" -button to update stale data
- Use "View participant list" -button to quickly browser thru the participants

### Statistics at the top
- **Percentage completed** Shows the % of completed Surveys against the Target completes for that project, if you **MOUSE OVER** this % figure, the report is switched to the actual number of completes.
- **Response Rate** is defined as proportion of the total number of completed / invitations * 100%. 
- **Start Rate** (flip side of **Response Rate**) you see **Start Rate** which is calculated started / invitations * 100%.
- **Indicence Rate %** is calculate starts / (starts + completes) * 100.
- **Estimated Incidence Rate** (flip side of **Incidence Rate**) is directly what is entered in the **Project Settings** -> **Basic Settings** -> **Length of Interview**
- **Length of Interview** Reported using 95% percentile average or 2 standard deviations from mean to remove out liers from the data.
- **Estimated LOI** is directly what is entered in the **Project Settings** -> **Basic Settings** -> **Length of Interview**
- **Target Completes** The total target completes for that Project
- **Rating** This is the average survey rating given by the participants
- **Ratings count** is the number of survey ratings given by the participants

> **Response rate, Incidence Rate and Rating** Take color cues from **Panel Settings** -> **Action Thresholds**

### Project status, name and ID

On this line you see:
- Project status - **Online, Closed, Archived** and **Offline**
- Project name
- Project ID

### Project progress chart

This chart plots the Daily and Hourly project progress for the last 72 hours. If you mouse over over the chart the tooltips will tell you exactly how each bar is composed and what the colors mean.

> You can click and highlight a series of days or hour slots which will zoomed in for more granular analysis.

If you like you can export the chart image or it's data click on **three dots** at top right of the chart.

### Outcome statistic to left of the chart

- **Starts** Total number of Started surveys for the project.
- **Completed** Total number of Completed surveys for the project.
- **Quota terminations** Total number of panelists terminated because of Quotas reached for that criteria. Mouse over to see percent from started.
- **Profile terminations** Total number of panelists terminated because of Profile not being suitable for a particular project. Mouse over to see percent from started.
- **Quality terminations** Total number of panelists terminated due to quality. Mouse over to see percent from started.
- **Duplicate terminations** Total number of panelists terminated due to duplicate. Mouse over to see percent from started.
- **Security terminations** Total number of panelists terminated due to security check like **out of country**. Mouse over to see percent from started.
- **Dropouts** Total number of panelist who dropped out from the survey or did not finish the survey. During a live project "on going survey takers" fall in this bucket so you may see higher than expected rate at the beginning of the survey.

> **TIP** Mouseover the percentage values to see the actual count.

### Statistics under chart  
- **Routed in** Total number of panelists routed into this project from other projects.
- **Routed out** Total number of profile or quota terminated panelists successfully routed to other projects.
- **Number of initiations sent** Shows the total number of email invites.
- **Delivered** shows the % of successfully delivered emails for the project.  If you mouse over, the system will display “Number of Delivered”.
- **Opened** Shows the number of opened invitations. This value is not 100% accurate and should be used for guidance only
- **Bounced** shows the total number of bounced emails from the emails sent in that project. This is colour coded for instant recognition.
  - Over 3.001%= Red
  - Over 1.001-3%= Dark Orange
  - 1% or less = Green  

> If you project exceeds 7% complaint rate then **Sample Ninja** will automatically stops ending sample to your project. This will generate both a project error and notification sent to the project managers.

- **Complaints** shows the number of complain emails sent to the SampleNinja email server with regards to this project. This is color coded for instant recognition:
  - **Over 10 complaints**  Red
  - **Under 1-10% complaints** Dark Orange
  - **No complaints** Green

> If your project exceeds 1% complaint rate then **Sample Ninja** will automatically stop sending sample to your project. Complaints are generated when the recipient flags your email as **SPAM**. This can happen if the recipient doesn't remember signing up or otherwise does recognize your invitation. This will generate both a project error and notification sent to the project managers.

### Redemption Points allocations for Panellists
- **Total Revenue** Total redemption points allocated thus far for this project in the platform.
- **Rewards Issued** Total redemption points allocated thus far for this project issued to Panellists.
- **Gross Revenue** Is the calculation of **Total Revenue** minus **Rewards Issued**
- **Gross Revenue Margin** Display gross revenue margin.
- **Wasted Reward Point Cost** Displays the total cost associated with wasted reward points.

> Wasted Reward Points are accumulated when an overinvite is registered. This could ne indication that you are attempting to field the project too fast.

> Within the **Balancing** segment, keep an eye on the numbers in the quota cells. If these numbers get too high, it means you are trying to complete the project too fast or the quota cells are requiring too many invitations due to a low response rate. This will incur unnecessary cost.
