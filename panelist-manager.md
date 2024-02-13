## Panelist Manager

Find, edit, and perform batch actions on individual or group panelists.

### Locating individual panelist

You can search for individual panelists by their Panelist ID, First Name, Last Name, or any wildcard combination of letters contained within these names, as well as searching by unique panelist ID or email address.

> The search displays the first 100 matches, while the blue box on the right indicates the total number of panelists that match the search string.

#### Add Filter
If you want to use a query filter to find panelists, you can either build a query on the fly or pick an existing query filter you have previously saved in the Query Filters.

#### From list
If you have a list of panelist IDs or email addresses you may paste them into the dialog to find multiple panelists at once.

#### Columns
Click on this button to change the visible columns. You can select any number of data variables.

#### Sort
Select which column to sort by i.e., QUALITY_SCORE, COMPLETED_COUNT, JOIN_DATE.

### Perform Batch action

Click on this button to perform a batch action on the panelists. In term search mode this is only visible when AT LEAST ONE panelist is selected.

> **WARNING!** If you don't select any panelists when using a query filter, the batch action is applied to all the panelists, not just those visible on the screen!

#### Change subscription status

This allows the user to select a new subscription status for the checked panelists.  The choices are **Subscribed, Unsubscribed** or **Blacklisted**.

> **WARNING!** Sample Ninja will automatically delete all data variables for any unsubscribed or blacklisted panelists to comply with GDPR and CPAA while retaining anonymous activity history and system variables for one year. This enables you to retain detailed project statistics, health metrics, and other critical statistics to operate your panel efficiently.

#### Delete panelists

This allows the user to DELETE the selected panelists.    

> **WARNING!** Delete panelist function should only be used when you must wipe out the entire panelist record, including any activity. For all other purposes, you should either unsubscribe or blacklist the panelist. Sample Ninja will automatically delete all data variables for any unsubscribed or blacklisted panelists to comply with GDPR and CPAA while retaining anonymous activity history and system variables for one year. This enables you to keep detailed project statistics, health metrics, and other critical statistics to operate your panel efficiently.

> Blacklisted panelists cannot rejoin the panel, whereas unsubscribed panelists can.

#### Change Sub-panel(s) membership

This allows the user to switch the selected panelists to chosen Sub-Panels.  This is particularly useful if an organization changes how they want to re-structure multiple Sub-panels.

> **IMPORTANT!** The target **sub panel** must contain moved panelists locale(s).

