## Reconcile participants

Reconciling panelists means changing their project (survey) outcome for any reason. Mainly, you would do that to keep the panel up to date on whether your panelists answer truthfully or for other reasons, such as security issues or duplication. Every time you reconcile your panelists, the QUALITY_SCORE variable is adjusted accordingly. This enables you to eliminate accounts that do not make you money or that could compromise your panel's quality reputation.

You can reconcile panelists in 3 different ways:

1) One pass reconciliation. Changes all provided IDs to complete and disqualify all other project panelists. Releases are pending reward points for all qualifying panelists.
2) Change to complete. Only changes provided IDs to complete status.
3) Change to reconciled. Reconcile for any other reason, like dishonest answers. Only provided IDs will be set to RECONCILED status.

Ideally, you would use the “One pass reconcile” mode by providing all the completed panelist IDs. All other panelists not included in the pasted list will be automatically set to status **reconciled**. 

> Reconciling is always recommended as it impacts panelists' QUALITY SCORE variable. This, in turn, lets you eliminate problematic panelists who are frequent offenders.

> When you reconcile panelists, Sample Ninja will automatically email them that their project participation has been rejected due to the quality of answers provided. To edit the contents of this email, go to: **Sub Panels -> Manage -> Email templates  -> Transactional -> Reconciled Notification**.

#### Pasting IDs
The identifier list should only contain panelist identifiers in the UUID format, example:  ```494d4c81-f109-4551-8929-0870d9b79d84``` one per line. Alternatively, the identifiers can be separated by a comma and/or enclosed in quotation marks. Line items that cannot be parsed will be displayed in the errors box. Duplicate identifiers pasted are automatically removed with a warning.

Once submitted, the server will perform a test run and report the number of affected panelists.

1) Disqualified (Reconciled)
2) Promoted to complete
3) No action taken
4) Invalid panelist IDs

The **no action taken** means that 

1) The panelist's current status does not match the statuses on the allowed list.
2) The panelist already has a status you are reconciling to.
3) The panelist never participated in the project you are reconciling

### What does the changing participation status to completed mean?
- You are changing the panelists' project participation status to **COMPLETED**
- Reward points are issued and immediately released from the pending state (on hold) to panelists to use.
- Revenue record is created
- Panelist's participation status is set to COMPLETED
- Quotas are incremented
- QUALITY_SCORE is adjusted up +7 points

> Since the status reporting relies on the Internet connection, sometimes the counts may not match. Using this feature means bringing your panelists to parity with your survey software's completes.

### What does the reconciliation entail?
- You are changing the panelists' project participation status from **STARTED** or **COMPLETED** to **RECONCILED**
- Any earned reward points are rolled back
- Earned revenue is withdrawn
- Panelists' participation status is set to RECONCILED.
- Quotas are decremented if the panelist was completed.
- QUALITY_SCORE is adjusted down -20 points
- Panelists whose status was **COMPLETED** are notified by email that their participation was not approved and their reward points were reverted. Panelists who only **STARTED** are not emailed, as they had no reward to revert.

> You can disqualify panelists using the auto sampling or profiler project types while your project is running! The advanced sampling engine will automatically find replacement panelists and invite them to the project!

> If your survey platform can identify duplicates and participants with quality issues like straight lining, you can use the appropriate exit links to terminate them immediately. See **Project configuration** -> **Exit links** for more details.


