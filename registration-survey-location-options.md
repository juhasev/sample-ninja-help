## Auto fill region variables
SampleNinja can automatically fill the location data variables using either **IP address** location or based **POSTAL_CODE** variable.

### Auto fill using POSTAL_CODE variable

You must add "POSTAL_CODE" variable to your registration survey and based on the postal code the following variables can be populated automatically

- CITY
- REGION (i.e. state or province)
- COUNTRY
- DMA (Designated Market Area, US only)
 
> **IMPORTANT**: If you enable this option **POSTAL_CODE** question is automatically validated using https://www.geocodes.org database. This validation varies based on the country and we recommend you test this feature for countries other than United States and Canada.
 
### Auto fill using IP location

SampleNinja will automatically capture user's location using IP API https://ip-api.com.

The following variables can be populated automatically

- POSTAL_CODE
- CITY
- REGION (i.e. state or province)
- COUNTRY
- DMA (Designated Market Area, US only)

> **PLEASE NOTE**: IP location capture is fairly accurate but can vary on mobile phones like Apple's iPhone. Apple is actively obfuscation mobile location thus is can considered accurate at REGION level. We are actively working on a solution that allows us to ask for the mobile location coordinates.
