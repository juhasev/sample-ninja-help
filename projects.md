## Projects

Create, manage, and track the progress of all projects within the system. Click the **PLUS** -icon at the top right corner to create a new project. To view all projects in the calendar, click on the **CALENDAR** -icon.

> Sample Ninja will automatically archive any projects that are **CLOSED** and older than 30 days. After that, they appear under the **ARCHIVED** tab.

The screen is kept uncluttered by default by applying the **Responsible for** filter. You can change the filtering by adding or removing additional filters.

### Search

The search functionality searches thru **ID**, **name**, **external project reference**, and **external billing reference**. Clear any filters before searching; otherwise, you may not see the results.

> **PLEASE NOTE** that the search will only search thru the active projects. If you need to search for archived projects, please switch to the **ARCHIVED PROJECTS** -tab.

### Projects table

Some columns are sortable. Simply click on the table headers to change the sort order.

#### ID

Simply indicates project ID.

#### PRIORITY

If you have an urgent project where you anticipate running out of sample the priority setting is your new friend. The sampling process is always carried out in the priority order. Normally when you do not anticipate any sample shortfalls, you can leave the priority setting to the default of five (5). Maximum priority is 10, so 5 falls in the middle ground as indicated as **dot**. Lower or higher priorities are indicated with **arrow** -icons pointing either up or down. 

> The sampling engine always attempts to complete all projects regardless of the priority setting. The sampling engine uses the priority setting to determine in order to sample from the currently available panelist pool.

#### NAME
This is the internal project name. This name is never disclosed to the panelists.

#### ERROR INDICATOR
Something may have gone wrong if you see an error indicator on your project. Click on the error indicator to see the details. 

> If you clear all the errors, the error indicator will disappear but will come back if any consequent sampling errors occur.

#### PROGRESS

The overall progress of the project. 

> Progress is calculated by **completed interviews** / **target completes** * 100%.

#### STATUS

Status can be changed simply by clicking each row's **STATUS** indicator.

#### Online
Select **online** to start fielding the project. The project will begin fielding automatically at the configured **start date and time**. 

#### Offline
Use the **offline** status to take the project temporarily offline. When **offline**, no new respondents can start the survey. However, any interviews in progress are allowed to finish normally. 

#### Closed
Use the **closed** mode to close the study permanently. In **closed** mode, anybody currently taking in progress can finish usually. 

#### Archived
When the project is **archived**, no more respondents are allowed to start or complete it.

> **IMPORTANT** You should never archive a project right after closing it, as interviews might still be in progress!

> Sample Ninja will automatically archive any **closed** projects after 1 month. 

#### DASHBOARD

There are TWO dashboards available for each project.

- **Project Dashboard** - Allows the user to explore granular statistics on the activity around that particular project.  
- **Map of Respondents** - Allow the user to see the geographic representation of Survey Starts.  

Click on the blue icons on each row to access these features.

#### RESPONSE RATE

Project response rate percentage.

The response rate has a color indicator of either **Green, Amber, or Red**. The red color indicator is triggered when **Send notification when response rate % falls under** -setting limit has been met in the **PANEL SETTINGS**.

> Response rate is calculated using **completes / invitations * 100%**.

#### INCIDENCE RATE
Displays the project's current incidence rate. The indicator is color-coded based on the difference between the estimated incidence compared and the actual incidence rate. The incidence indicator stays **green** as long as your true incidence > estimated incidence and gradually goes thru **amber** to **red**. The red status is based on the incidence rate threshold setup in **the panel settings**.

> Incidence rate is calculated using **completes / (completes + terminated) * 100%**.

#### RATING

This is an average survey rating score on a scale of 1 - 10. Survey ratings are collected at the end of each interview and is voluntary to panelists. The rating functionality is on by default but can be turned off in the **PANEL SETTINGS** if desired.

The rating is color coded and can either be **Green, Amber and Red**. The red color indicator is triggered when **Send notification when survey rating falls under** -setting limit has been met in the **PANEL SETTINGS**.

#### CALENDAR

Indicates when the projects are running. 

> The calendar feature is there to help you to spread your panel usage evenly so you don't have periods where you may fall short of sample. Ramming all the projects on the same day can quickly lead to a sample shortfall after business rules are applied.

> **IMPORTANT**: Calendar by default displays projects you are responsible for. Remove the **responsible** filter if you want to display all the projects panel wide in the calendar.

#### ACTIONS 

Click on the triple dot at the end of each row button to see available project actions.

**View participants** - View participants.
**Disqualify** - Batch disqualifies participants by providing a list of panelists' IDs.
**Clone** - Clone project.
**Delete** - Delete project.

> You can only delete projects without participants. Consider archiving the project to make it "disappear" from your view.
