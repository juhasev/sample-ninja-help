## Transactions

Displays the panelist's reward point transaction ledger. Every event that adds or removes reward points writes an entry here, making the ledger the source of truth for the balances shown on the panelist screens. Entries are listed newest first and loaded one page at a time, so the balance shown on each row is correct on every page.

### Dashboard Cards

**Reward Points Balance** - The current balance, including points that are still pending.

**Pending Reward Points** - Points that have been credited but are on hold. This card is only shown when the panelist has pending points.

**Reward Points Available** - The balance the panelist can redeem right now, i.e. the balance minus pending points.

### Column Names

**ID** - The unique ID of the ledger entry.

**Type** - What produced the entry, e.g. Project, Redemption, Refund, Balance Adjustment, Data Variable (Dynamic Profiling), Referred Friend or Import Balance.

**Type ID** - The ID of the related record, e.g. the project or redemption ID. Shows N/A when there is no related record, for example, for an imported balance.

**Name / Reference** - The name of the related record, such as the project name or the reward that was redeemed. For manual balance adjustments, the reference entered by the user is shown instead.

**Reward Points** - Points added (positive) or deducted (negative) by this entry. A yellow currency icon after the amount marks pending points; hover over it for an explanation.

**Balance** - The panelist's balance right after this entry was recorded. Reading the column from the bottom up shows how the balance developed over time, and the newest entry always matches the Reward Points Balance card.

**Created** - When the entry was recorded, shown in your local time.

#### Pending reward points

Projects with **Hold reward points** enabled credit the reward as pending when a panelist completes the survey. Pending points count towards the balance but cannot be redeemed until the project is reconciled and the points are manually released. If a completion is reconciled as invalid, a negative entry reverses the pending credit.

> The reload button on the right refreshes the list, for example, after adjusting the balance on the Dashboard tab. The cards and the panelist profile are refreshed together using the reload button in the page header.
