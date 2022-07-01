## Postal Code mapping

**SampleNinja** can automatically map **POSTAL_CODE** variables to **CITY**, **REGION**, **DMA** (typically state or province) and **COUNTRY**.

Region values will be full names not abbrevations like TX, CA.

> **DMA** coding is only available to US panelists and will always be stored in the numeric format.

There are multiple ways to configure how things are handled.

### Postal Code
You can configure the update to delete invalid postal codes. This can be handy as you can dynamically profile **POSTAL_CODE** with validation turn on.

> Panels based in United States should use **POSTAL_CODE** variable and not some custom variable like **ZIP_CODE**.

> Postal codes in United Kingdom, Canada and Netherlands will use the short format.

Or alternative you may want to choose "No action" which leaves the **POSTAL_CODE** variable intact.

### CITY, REGION, COUNTRY and DMA

Choose the options which make sense to your panel and do a test run. 

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
- CITY
- OLD_CITY
- REGION
- OLD_REGION
- COUNTRY
- OLD_COUNTRY
- DMA
- OLD_DMA

When the mapping process is completed you will receive an instant notification with high level details about the updated, added and deleted records.

> **IMPORTANT**: Use the "Scan and report only" switch to run a test mapping. It is important that you understand how your data will be changed. For example if you are currently using **REGION** abbreviations, these will be changed from **TX** -> **Texas**. Any project looking for sample in **TX** would no longer find any panelists!

