### Project name
This can be any name (any alphanumeric or Special characters between 5 and 150 characters long). This is an internal name and was never disclosed to the participants.

### Public name
An optional panelist-facing name for the project, up to 150 characters. Internal project names often carry client references, cost codes, or version tags you would rather keep in-house. When a **Public name** is set, it is used where panelists see the project:

- The **Member App** activity timeline, alongside a chip showing the Sample Ninja project ID.
- Any email template using the **[public-project-name]** variable.

Leave the field empty, and everything behaves as before.

> The **[public-project-name]** variable is replaced with blank text when no public name is set, it does not fall back to the internal name. Review the templates where you use it, starting with the **Reward points awarded** template in **Sub Panels -> Manage -> Email Templates -> Transactional**.

### Project status
This controls project fielding status. 

#### ONLINE
Select **online** to start fielding the project. The project will start fielding automatically at the configured **start date and time**. 

#### PAUSED
Select **paused** if you want to stop sampling for the project for any reason. The existing invitees can still normally complete the project.

#### OFFLINE
Use the **OFFLINE** status to take the project temporarily offline. When in **OFFLINE** no new respondents can start the survey, however any interviews in progress are allowed to finish normally. 

#### CLOSED
Use the **closed** mode to close the project permanently. In **closed** mode, anybody currently in progress can finish normally. 

#### ARCHIVED
When the project is **ARCHIVED**, no more respondents can start or complete the project.

> **IMPORTANT** You should never archive a project right after closing it, as interviews might still be in progress!

> Sample Ninja will automatically archive any **CLOSED** projects after 1 month. 

#### Target Completes
The total number of survey completes that the project needs to achieve.

#### Soft launch completes
This enables you to automatically pause the project when a specified number of soft launch completions has been reached. After reviewing the survey answers, simply set the project back online.

#### Length of interview
Estimated length of interview in minutes. The length of the interview will be displayed to the participants if you have configured your email invitation template to display the **Project Info Box**. The default project email templates are configurable for each sub-panel under **Sub Panels**.

#### Estimated Incidence rate
This is provided for reference purposes and can be left empty. Sample Ninja will send automatic alerts if the estimated incidence rate deviates from the configured % of the actual incidence rate. 

#### Cost Per Incidence
Enter the **Cost per Incidence** or **CPI**. This is the revenue figure you make for each completed panelist. The project's **total cost** field will be automatically updated based on the entered **CPI** and **Target Completes** or if you know the project's **Total Cost** but know **CPI** enter that to the **Cost per Incidence** field instead. This will automatically calculate **CPI** for you.

> See the **compensation** -tab for more details and revenue calculation example.

#### Project cost
Enter the actual cost to your end client using accounting currency, i.e., USD, EUR, etc... Sample Ninja uses this value to calculate **Cost per Incidence** or revenue per completed. Sample Ninja keeps track of revenue per panelist. Alternatively, you may use the **Cost Per Incidence** field. Both fields update each other based on the **Target Completes**

> See the **Compensation** -tab for more details and revenue calculation example.
