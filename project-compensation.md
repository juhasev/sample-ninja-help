## Project compensation

### Basic compensation by Sub Panel and LOI
Project compensation is automatically selected from **Sub Panels -> Settings -> Compensation** based on the entered project LOI (Length Of Interview) setting in the project's **Basic Settings** tab.

- Client CPI (This is the sample cost to your client or your revenue)
- Reward completed (Compensation for completed panelists)
- Reward profile (Compensation for screened out or profile panelists)
- Reward quota (Compensation for quota-terminated panelists)
- Net Revenue (which is CPI - cost of reward points)

Use the revenue calculator to apply the correct per-panelist revenue or Client CPI (Cost Per Incidence). You must first enter **Project cost** or **Client CPI** in the **Basic Settings** -tab. Sample Ninja tracks revenue per panelist and can report various metrics like how profitable certain segments coming from various recruitment sources are, and more. Using the Revenue / Client CPI is optional but **highly recommended**.

You may override compensation values on a per-project basis. The reward must be entered in **Reward Points**, while **CPI** is entered in **accounting currency**, such as US dollars or EUR. To edit any value, mouse over the value and click to edit.

> **IMPORTANT!** If you change the project's LOI (Length of Interview), click the apply button to update the **Cost Per Incidence** column.

> If you never reward **profile** or **quota** terminates you can turn these fields off in **Sub Panels -> Settings -> Compensation**

> Accounting currency is specified in the **panel settings**. Choose **settings** from the main menu.

### Multiple compensation tables per data variable
You may optionally add another dimension to the compensation table by using a data variable. You can use any custom radio-type datavariable you have defined in the panel. The base compensation tables are configured under **Sub Panels -> Settings -> Compensation**. If you are interested in using this feature, follow the directions in the sub-panel compensation configuration.

When this feature is enabled, the project compensation table defaults to multiple compensation tables. However, if you want to use Basic Compensation temporarily, simply toggle on **Use basic compensation**. This gives simple compensation for each sub-panel.

When using multiple compensation tables, by default, compensation entries that do not match any panelists based on qualifications are hidden. If you want to view these entries as well, please toggle on **Show unused compensation**.

> **IMPORTANT** When using this feature, you must ensure that all invited panelists have the data variable on which the compensation is based. If a panelist is found to lack the required compensation variable, an error is triggered, and the invitation is skipped for that panelist.
 
> **TIP** If you don't have the compensation variable for all the panelists, add a clause to Qualification that requires that the compensation variable exists. For example, add the condition EXISTS to SPECIALTY (compensation variable).
