## REDEMPTIONS

The pending redemptions requests need to be manually approved before the panelist get sent their rewards. Select the redemptions using the checkbox on the left and then click the **APPROVE** or **REJECT** button at the bottom of the table. If you want to view the processed redemptions, select the **HISTORY** -tab.

### FILTERING OPTIONS
Use the search field to find any panelist using first name, last name, or email. If you would like to view redemption requests for any given Sub Panel(s), you may do so by clicking the filter icon.

> Use the **REMEMBER FILTER** -button to set this as your default filter i.e. if you only approve redemptions for, let's say Italian Sub Panel.

> This works in either in the **APPROVALS** -tab or the **HISTORY** -tab.

### APPROVALS

This table displays redemption requests from panelists to redeem their points for rewards. Select one or more redemption requests and either choose to **APPROVE SELECTED** or **REJECT SELECTED**. When a reward request is approved, Sample Ninja will execute the redemption with the vendor in the next fifteen minutes.

#### Quality Score
You should pay attention to the panelist’s **Quality Score**, which indicates bad behavior. The quality score ranges from 0 (bad) to 100 (good). Click on the edit panelist button and view the “Quality” -tab. Consider unsubscribing or blacklisting panelists with suspicious or low quality behaviour. 

> If you reject redemption requests, the panelists are fully refunded.

### HISTORY

View historical approvals data and monitor partner statuses. 

> If you mouse over the **info** icon, you will see a popup that contains any reward partner supplied data. This data varies by vendor but can be useful for troubleshooting purposes. Click on the icon to copy all the data.

### Tango Card statuses

**COMPLETE** Transaction was successfully completed

**FAILED** Transaction failed. Redemption cost was refunded to the panelist.

> If you are looking for either refunding or re-sending the panelist's redemption email, you are in the wrong place! Instead, locate the panelist first by going to **panelist manager** and search for the panelist by using name, email, or ID. Click on the panelist name and open the **redemptions** -tab. 

### PayPal Statuses

**SUCCESS** Funds have been credited to the recipient’s account.

**FAILED** This payout request has failed, Redemption cost was refunded to the panelist.

**PENDING** Your payout request was received and will be processed.

**UNCLAIMED** The recipient of this payout does not have a PayPal account. A link to sign up for a PayPal account was sent to the recipient. However, if the recipient does not claim this payout within 30 days, the funds will be returned to your account.

**RETURNED** The recipient has not claimed this payout, so the funds have been returned to your account.

**ON HOLD** This payout request is being reviewed and is on hold.

**BLOCKED** This payout request has been blocked.

**REFUNDED** This payout request was refunded.

**REVERSED** This payout request was reversed.

The following additional errors may also occur while communicating with PayPal

**AUTHORIZATION_ERROR** This error means that your account is not eligible for using PayOuts API. You must have Business Account with PayPal and have requests specifically to allow your account to be used for the **PayOuts** API.

**UNKNOWN** This error can be returned in some rare cases. Most likely cause is that your account keys are not correct or there is some other issue authenticating with **PayPal**. These could include account setup problems like not enabling **PayOuts API** or **Transaction Search**. These two features are required. Contact support@sampleninja.io if in doubt.

### EXPORT REDEMPTIONS
Click on the download button (cloud icon with downwards arrow in the top right corner) and select the date range and desired filters to export redemption information to a CSV file. The default configuration includes all approved redemptions processed for the calendar year.

> Note that the filter works on logic that supports satisfying the filter criteria i.e. if **FAILED**, **APPROVED**, and **PROCESSED** are all selected, the system will only export redemptions that were processed and approved but failed. To show all failed or rejected redemptions, solely tick **FAILED**. To show all approved/completed redemptions, solely tick **APPROVED**. To show redemptions irrespective of status, solely tick **PROCESSED**.

> Toggle on **Export all dates**, to download all redemptions that satisfy the chosen filter criteria i.e. this will include every redemption from the first to the most recent based on the filter criteria. Example - with **Export all dates** toggled on and **PROCESSED** ticked, all processed redemptions will be exported.





