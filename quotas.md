### Sample Quota Balancing

By setting quotas you can control more precisely how your sample is balanced. Using balacingquotas is optional.

#### Target completes

The target completes fields displays # of completes setup in the basic settings page. 

> Please note that modying **target completes** here affects your project **target completes** defined in the basic settings tab.

#### Select variables

Next select variables that you would like to use. Quotas can be created from any **radio** or **date** -question. The date -question type must categorized into ranges before it can be used (or to be visible).

#### Use percent values

Click on the "percent %" button to enable divisions by percent.

#### Balance

Use the balance button to quickly evenly balance all the cells using total number of completes needed.

#### Run feasibility

Runs a quick feasibility check on each cell based on the average response rate for those qualying for the cell. The resulting multiplier tells you how many times can you fill the quota cell. In the other words you have an indication how likely are able to fullfill the quota cell. Sample Ninja by default consider multiple of #3 sufficient. Anything else will be flagged and colored from yellow thru orange to red. To see the defails bring you mouse over the **multiplier box**. 

- Details include:
-- Invitations needed
-- Availability
-- Average response rate for this cell

#### Turning quotas off

Turning quotas off is not recommended unless the availability for cell is zero. If you want to disable cell with non zero availability you should do some in the  **Qualifications** instead. If you turn a quota cell off then the sampling engine will discard any panelists it finds that belong to the disabled bucket. This may have negative effect on the sampling efficiency.

#### Turning enforcing off

You can relax any quota cell to allow overrage. This means that a panelist can to start a survey even if quota is full. This may be helpful in situation where target quotas not known or there are multiple sample vendors supplying sample. Needless to say if you can do this then do it as it will provide better overall experience for your panelists.

