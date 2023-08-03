## Panelist Manager

### Top statistics
The top row statistics provide basic statistics about the panelist's vitals.

- **Status** Current panelist status -> Subsribed, Unsubscribed or Blacklisted
- **Days in Panel** # of days as panel member. This is calculated from the SUBSCRIBED_DATA data variable.
- **Quality Score** Panelist quality score between 0 (worst) and 100 (best). You can just switch to the quality tab to learn more.
- **Bad experience percent** This is a percentage of panelists getting "profile" or "quota" terminated.
- **Total activities** This is the number of total interactions with the panel. Switch to the "Activity" tab for more.
- **Completed projects** Number of completed projects this panelist has accumulated. Same as COMPLETED_COUNT data variable.
- **Reward points balance** Current reward points balanace. Same as POINTS_BALANCE data variable.
- **Lifetime reward points earned** This is the total reward points earned since joining the panel. Same as POINTS_REWARDED data variable
- **Response rate** The response rate to the email invitations. Same as the RESPONSE_RATE data variable.

### Basics
This box provides basic information about the panelist.

- **Identifier** This is panelist's unique identifier.
- **Email valid** Whether panelist's email address is healthy and the system is able to deliver mail to the panelist's email address
- **Sub Panel** Which sub panel this panelist is member of
- **Locale** Panelist's locale
- **Recruitment Source** Which recruitment source this panelist is coming from.

### Projects
Displays counts of project-related activities
- **Invitations** Number of email invitations sent to this panelist
- **Invitations opened** Number of email invitations the panelist has read
- **Started** Number of project starts
- **Quota** Number of project quota terminations
- **Profile** Number of project profile terminations
- **Quality** Number of project quality terminations (returned to SampleNinja via quality exit link)
- **Duplicate** Number of project duplicate terminations (returned to SampleNinja via duplicate exit link)
- **Security** Number of project security terminations (returned to via security exit link)
- **Reconciled** Number of the time a project manager has reconciled this panelist
- **Completed** Number of project completions

### Unsubscribing or blacklisting
This pulldown lets you unsubscribe or blacklist panelists. If you unsubscribe or blacklist a panelist, their personally identifiable information is erased to comply with regulatory data privacy laws like GDPR (Europe), CCPA (California). This includes name, email, and any custom data variables collected. System variables like INVITED_COUNT and SUBSCRIBED_DATE remain. Anonymous activity history remains for one year. 

### Balance adjustment
This button lets you manually deduct or add reward points to the panelist's balance. Any text entered into the description will be automatically added as a note. Please take a look at the notes tab for more details. This information is not visible to the panelist.

### Reset passwords
Resets the panelist's password by sending a password reset email to the panelist's email address. Panelists can also reset their password from the member app login screen.

### Delete panelist
Wipes out the entire panelist, including their activity history. Please use the unsubscribe or blacklist options to retain activity history records that power your panel's statistics.

> This should be only used for test panelists, never for real panelists! 
