## Reconcile participants

You can reconcile panelists in 3 different ways:

1) One pass reconcile. Changes all provided IDs to complete and disqualify all other project panelists.
2) Reconcile to complete. Only changes provided IDs to complete status.
3) Reconcile to quality or duplicate. Only changes provided IDs to the selected status.

You can now use the “One pass reconcile” mode by providing all the completed panelist IDs. All other panelists not included in the pasted lists will be automatically reconciled to status **reconciled**. Additionally, you can provide additional instructions on which statuses should be reconciled to promoted to **completes**. For example, you may want to exclude **SampleNinja** issued statuses like "quota" or “security.”

You can also reconcile specific panelists to completed by using the “Reconcile to complete” mode or, like before, disqualify them for quality or duplication using the “Reconcile to disqualified” mode.

#### Pasting IDs
The identifier list should only contain panelist identifiers in the format ```494d4c81-f109-4551-8929-0870d9b79d84``` one per line. Alternatively, the identifiers can be separated by a comma and/or enclosed in quotation marks. Line items that cannot be parsed will be displayed in the errors box. Duplicate identifiers pasted are automatically removed with a warning.

Once submitted, the server will perform a test run and report back the number of panelists affected

1) Disqualified 
2) Promoted to complete
3) No action taken
4) Invalid panelist IDs

The **no action taken** means that 

1) The panelist's current status does not match the statuses on the allowed list (when reconciling to complete).
2) The panelist's current status is not final in the project like invited or opened, started (when reconciling to disqualified)
3) The panelist already has a status you are reconciling to.

You are likely reconciling the wrong project if you get many invalid panelist IDs! Or it could also be possible that those panelists need to have **started** status in the project.

### What does the disqualification process do?

**RECONCILE TO COMPLETE**
- Reward points are issued
- Revenue record is created
- QUALITY_SCORE is adjusted up
- Quotas are incremented
- Any quality, security, or duplicate flags are removed, and QUALITY_SCORE is adjusted up

**RECONCILE TO DISQUALIFIED**
- Earned rewards for the project points are set to zero
- Earned revenue for the project is set to zero
- Panelists are issued quality or duplicate flag
- QUALITY_SCORE is adjusted down
- Quotas are decremented

> You can disqualify panelists while your project is running! **Sample Ninja's Sampling Engine** will automatically find replacement panelists and invite them to the project!

> If your survey platform can identify duplicates and participants with quality issues like straight lining, you can use the appropriate exit links to terminate them immediately. See **Project configuration** -> **Exit links** for more details.


