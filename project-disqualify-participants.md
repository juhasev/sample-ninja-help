## Reconcile participants

Reconciling panelists means you want to change their project (survey) outcome for any reason. Mainly, you would do that to keep the panel up to date on how honest your panelists are; they answer truthfully or for other reasons like security issues or being duplicated. Every time you reconcile your panelists, the QUALITY_SCORE variable is adjusted up or down. This enables you to eliminate accounts that do not make you money or are potentially problems for your panel's reputation in terms of quality.

You can reconcile panelists in 3 different ways:

1) One pass reconcile. Changes all provided IDs to complete and disqualify all other project panelists. Releases are pending reward points for all qualifying panelists.
2) Change to complete. Only changes provided IDs to complete status.
3) Change to reconciled. Reconcile for any other reason, like dishonest answers. Only provided IDs will be set to RECONCILED status.
4) Mark project reconciled will release all the pending reward points for all panelists.

Ideally yo,u would use the “One pass reconcile” mode by providing all the completed panelist IDs. However, for a longer running projects, it is may not be feasible. All other panelists not included in the pasted lists will be automatically reconciled to status **reconciled**. Additionally, you can provide additional instructions on which statuses should be reconciled to promoted to **completes**. For example, you may want to exclude **SampleNinja** issued statuses like "quota" or “security.”

You can also reconcile specific panelists to completed by using the “Reconcile to complete” mode or, like before, disqualify them for quality or duplication using the “Reconcile to disqualified” mode.

> Reconciling is always recommended as it impacts panelists' QUALITY SCORE variable. This, in turn, lets you eliminate problematic panelists who are frequent offenders.

#### Pasting IDs
The identifier list should only contain panelist identifiers in the UUID format, example:  ```494d4c81-f109-4551-8929-0870d9b79d84``` one per line. Alternatively, the identifiers can be separated by a comma and/or enclosed in quotation marks. Line items that cannot be parsed will be displayed in the errors box. Duplicate identifiers pasted are automatically removed with a warning.

Once submitted, the server will perform a test run and report the number of affected panelists.

1) Disqualified (Reconciled)
2) Promoted to complete
3) No action taken
4) Invalid panelist IDs

The **no action taken** means that 

1) The panelist's current status does not match the statuses on the allowed list (when reconciling to complete).
2) The panelist's current status is not final in the project like invited or opened, started (when reconciling to disqualified)
3) The panelist already has a status you are reconciling to.

If you get many invalid panelist IDs, you are likely reconciling the wrong project! It is also possible that those panelists need to have a **started** status in the project.

### What does the reconciling to completed mean?
- Reward points are issued and immediately released from the pending state (on hold) to panelists to use.
- Revenue record is created
- Panelist's participation status is set to COMPLETED
- Quotas are incremented
- QUALITY_SCORE is adjusted up +7 points

> Since the status reporting relies on the Internet connection, sometimes the counts may not match. Using this feature means bringing your panelists to parity with your survey software's completes.

### What does the reconciled entail?
- The reward points are widthdrawn (deleted)
- Earned revenue is withdrawn (deleted)
- Panelists' participation status is set to RECONCILED.
- Quotas are decremented if the panelist was completed.
- QUALITY_SCORE is adjusted down -20 points

> You can disqualify panelists using the auto sampling or profiler project types while your project is running! The advanced sampling engine will automatically find replacement panelists and invite them to the project!

> If your survey platform can identify duplicates and participants with quality issues like straight lining, you can use the appropriate exit links to terminate them immediately. See **Project configuration** -> **Exit links** for more details.


