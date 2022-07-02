## Postal Code mapping

This feature lets you request automatic **POSTAL_CODE** mapping to **CITY**, **REGION** (typically state or province), **COUNTRY** and **DMA**.

> **IMPORTANT**: Use the "Scan and report only" switch to run a test mapping. In this mode no data is changed but **SampleNinja** will produce a detailed CSV how the data would be changed. It is important that you understand how your data will be changed. For example if you are currently using appreviation in the **REGION** variable, these will be changed from **"TX"** -> **"Texas"**. Any project looking for sample in **REGION** **"TX"** would no longer find any panelists!

> **DMA** coding is only available to US panelists and will always stored in the numeric format. You must also create **DMA** variable by visiting **Data Variables** and by clicking on the **STANDARD** button and then selecting **DMA** to create it.

### Postal Code

You can configure **SampleNinja** to delete invalid postal codes by selecting option **"Remove invalid postal codes"**. This can be handy as you can dynamically profile **POSTAL_CODE** with automatic postal code validation turned on to ensure you are collecting only valid codes going forward.

Or alternatively you may want to choose **"No action"** which leaves the **POSTAL_CODE** variable intact.

> Your panel should **ALWAYS** use the **POSTAL_CODE** and the **REGION** variables. If you are using some home grown variables like **ZIP_CODE**, **STATE** or **PROVINCE** the automatic features / validation will not be available. Please contact support@sampleninja.io for information how to migrate to **POSTAL_CODE** and **REGION**.

> **IMPORTANT** Postal codes in **United Kingdom, Canada and Netherlands** will use the short format. If a long format portal code is found it will be automatically converted to the short format.

### CITY, REGION, COUNTRY and DMA

Choose the options which make sense to your panel and do a test run by toggling on "Scan and report" (default). When ready to update your panelists toggle "Scan and report" off to apply the changes.

#### Overwrite
This option will overwrite existing values if the new value is different. This can be handy if your existing values have differences in spellling like "United States" vs "US".

#### Add missing only
This option will add missing values only.

#### No action
No action, variable will not be mapped

### Notification & results

**SampleNinja** will produce detailed CSV file that contains

- PANELIST_ID
- POSTAL_CODE
- OLD_POSTAL_CODE
- CITY
- OLD_CITY
- REGION
- OLD_REGION
- COUNTRY
- OLD_COUNTRY
- DMA
- OLD_DMA

When the mapping process is completed you will receive an instant notification with the high level details about the updated, added and deleted records by each LOCALE you **Sub Panel** contains.

