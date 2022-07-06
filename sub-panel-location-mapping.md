## Postal Code Mapping

This feature allow for automatic **POSTAL_CODE** mapping to **CITY**, **REGION** (typically state or province), **COUNTRY** and **DMA**.

> **IMPORTANT**: Use the "Scan and report only" switch to run a test mapping. In this mode, no data is changed but **SampleNinja** will produce a detailed CSV of how the data would be changed. It is important to understand how the data will be changed. For example, if abbreviation is currently being used for the **REGION** variable, these will be changed from **"TX"** -> **"Texas"**. Any project looking for sample in **REGION** **"TX"** would no longer find any panelists!

> **DMA** coding is only available to US panelists and will always stored in the numeric format. A **DMA** variable must also be created by visiting **Data Variables** and by clicking on the **STANDARD** button and then selecting **DMA** to create it.

### Postal Code

**SampleNinja** can be comfigured to delete invalid postal codes by selecting option **"Remove invalid postal codes"**. This can be useful as **POSTAL_CODE** can be dynamically profiled with automatic postal code validation turned on to ensure only valid codes are collected going forward.

Or alternatively **"No action"** can be chosen, which leaves the existing **POSTAL_CODE** values intact.

> A panel should **ALWAYS** use the **POSTAL_CODE** and the **REGION** variables. If home grown variables like **ZIP_CODE**, **STATE** or **PROVINCE** are used, the automatic features / validation will not be available. Please contact support@sampleninja.io for information on how to migrate to **POSTAL_CODE** and **REGION**.

> **IMPORTANT** Postal codes in **United Kingdom, Canada and Netherlands** will use the short format. If a long format portal code is found it will be automatically converted to the short format.

### CITY, REGION, COUNTRY and DMA

Choose the options which make sense for the panel in question and do a test run by toggling on "Scan and report" (default). When ready to update the panelists, toggle off "Scan and report" to apply the changes.

#### Overwrite
This option will overwrite the existing value if the new value is different. This can be useful if existing values have differences in spellling like "United States" vs "US" or "London" vs "Lonson". It is imperative that all records are clean. It would be possible for a project manager to accidentally target "Lonson" while meaning to target "London"! 

#### Add missing only
This option will add missing values only.

#### No action
Take no action, variable will not be mapped. 

### Notification & results

**SampleNinja** will produce a detailed CSV file that contains the following columns. 

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

> If "No action" is chosen for any of the target variables, then the variable will be omitted from the report as no changes will be made.

> When the mapping process is completed an instant notification will be sent with high level details about the updated, added and deleted records by each **LOCALE** contained in the **Sub Panel**.

