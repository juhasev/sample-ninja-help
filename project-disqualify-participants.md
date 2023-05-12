### Reconcile participants

You can reconcile panelists in 3 different ways:

1) One pass reconcile
2) Reconcile to complete. Only changed provided IDs to complete -status.
3) Reconcile to quality or duplicate. Only changes provided ISs to duplicate -status.

You can now use the “One pass reconcile” mode by providing all the completed panelist IDs. In this mode, anybody else not included in the completes will get automatically reconciled. For these reason you must select **Disqualification reason**. Additionally, you can provide additional instructions on which statuses should be reconciled to promoted to **completes**. For example, you may want to exclude **SampleNinja** issued statuses like "quota" or “security.”

You can also reconcile specific panelists to completed by using the “Reconcile to complete” mode or, like before, disqualify them for quality or duplication using the “Reconcile to disqualified” mode.

#### Pasting IDs
The identifier list should only contain panelist identifiers in the format ```494d4c81-f109-4551-8929-0870d9b79d84``` one per line. Optionally the identifiers can be separated by a comma and/or be enclosed in quotation marks. Line items that cannot be parsed will be displayed in the errors box. Duplicate identifiers pasted are automatically removed with a warning.

Once submitted, the server will perform a test run and report back the number of panelits affected

1) disqualified 
2) promoted to complete
3) no action taken
4) invalid panelist IDs

If you get many invalid panelist IDs, you are likely reconciling the wrong project! Or it could also be possible that those panelists do not have **started** status in the project.

The no action taken simply means that 

1) Panelist's current status not match the statuses on allowed list (when reconciled to complete).
2) Panelist already has a status you are reconciling to.

### What does the disqualification process do?

**RECONCILE TO COMPLETE**
- Reward points are issued
- Revenue record is created
- QUALITY_SCORE is adjusted up
- Quotas are incremented
- Any quality or duplicate flags are removed, and QUALITY_SCORE is adjusted up

**RECONCILE TO DISQUALIFIED**
- Earned rewards for the project points are set to zero
- Earned revenue for the project is set to zero
- Panelists are issued quality or duplicate flag
- QUALITY_SCORE is adjusted down
- Quotas are decremented

> You can disqualify panelists while your project is running! **Sample Ninja's Sampling Engine** will automatically find replacement panelists and invite them to the project!

> If your survey platform can identify duplicates and participants with quality issues like straight lining, you can use the appropriate exit links to terminate them immediately. See **Project configuration** -> **Exit links** for more details.


