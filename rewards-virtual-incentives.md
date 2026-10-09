## Virtual Incentives

Whether you already have an account with Virtual Incentives or you are entirely new, please email Virtual Incentives at support@virtualincentives.com or visit www.virtualincentives.com/sampleninja for more information. An account representative will provide you with credentials and custom catalog programs compatible with **Sample Ninja**.

To start issuing rewards, click the configure button and paste the username and password provided by Virtual Incentives (these are different from your Virtual Incentives login; these are Virtual Incentives API credentials). Then, in the next step, select the programs you'd like to use with Sample Ninja.

> **NOTE** The program names must begin with an SN_ prefix. This allows you to have separate reporting for SampleNinja Virtual Incentives programs and your existing programs.

#### Testing
You can test the redemptions using the "Sandbox" or "Production" account. This should be done in the staging environment.

> Do not use the sandbox account in production to prevent accidentally offering "fake" rewards to your panelists.

#### IP Whitelisting

Virtual Incentives require that all connecting servers are IP whitelisted. If you encounter random errors, ensure your account whitelists the following Sample Ninja IP addresses.

```
3.135.136.57,3.149.61.67,3.20.110.34,18.220.252.20,3.140.62.214,3.139.253.68,18.190.230.163,18.227.57.42,3.130.42.149,3.132.6.13,3.133.255.106,3.138.161.51,3.138.252.4,3.18.143.74,3.20.135.79,3.21.14.86
```

> Login to Virtual Incentives Admin Panel. Select the API tab from the top menu, then click on Whitelist and paste the IPs to both the Development and Production IP whitelists. Please ensure that there are no line breaks or spaces when pasting.

#### Manage Rewards

In the Virtual Incentives world, you subscribe to a catalog that is tailored to you. If you want to customize your catalog, you need to contact your representative at Virtual Incentives. 

Each card in the catalog comes with the amounts Virtual Incentives accepts for it: either a list of fixed values (for example 25, 50 and 100 USD) or a range (for example 5 to 1,000 AUD). When you add a card, you can only save an amount Virtual Incentives offers. Any other amount is rejected, and the message lists the amounts that are valid.

#### Catalog Updates

Virtual Incentives can change the amounts of a card at any time, for example by raising the minimum value. Sample Ninja downloads your catalog again once a day and checks every reward you offer against it. You can also run the same update at any time with the **Reload catalog** button in **Manage Rewards**.

When an amount you offer is **no longer available**, or Virtual Incentives removes the card from your catalog:

- The reward is hidden from your panelists, so nobody can redeem it.
- The reward stays in your list with the **EXPIRED** label. Hover over the label to see what Virtual Incentives offers now.
- Users with the **Rewards Manager** role receive a notification in the app and by email.

To keep offering the card, delete the expired amount and add one that Virtual Incentives still offers. If Virtual Incentives makes the amount available again, the reward becomes visible to panelists automatically, unless you had hidden it yourself.

When the amounts of a card **change but the amounts you offer are still valid** (for example a card moves from fixed values to a range), your rewards stay as they are. Users with the **Rewards Manager** role receive a notification that lists the new amounts, so you can decide whether to add new values.

> A redemption that is waiting for approval when its amount stops being available is marked as failed when it is processed, and no order is placed with Virtual Incentives.

#### W9 / 1099 Tax Reporting

For US-based panelists, Sample Ninja can submit Virtual Incentives reward orders as W9-eligible, so Virtual Incentives can collect and track the tax information needed for 1099 reporting.

> This is configured per panel and is enabled by Sample Ninja on request. If your panel needs W9 / 1099 handling for US recipients, contact Sample Ninja support to turn it on. Panels without it submit no tax information, and non-US panelists are never affected.

#### Disable

Disables Virtual Incentives completely.
