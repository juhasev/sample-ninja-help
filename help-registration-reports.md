## Dashboard

Registration statistics are available if you are using the built-in Registration Survey. Each Sub Panel has its registration survey. To configure registration survey for a Sub Panel, please find the Registration Survey tab in the Sub Panel Settings.

If you have at least one registration survey active, you can select it from the top pulldown to view statistics.

> The registration statistics are limited for the past month. You can use the **JOIN_DATE**, **EMAIL_VALID**, **EMAIL_CONFIRMED** - data variables to filter, slice, and dice any given period in various other features throughout the application. The email delivery statistics are not stored for more than 30 days and cannot be used in filtering or in segments. The **EMAIL_VALID** variable indicates whether your email is valid, meaning we have recorded successful delivery at least once. If panelist email bounces, the **EMAIL_VALID** variable will be set to NO.

> Click on the **View Activity** button at the top to view individual registration sessions.

### Top-row statistics
Statistics include the number of new panelists, conversion rate, survey rejections, and surveys started and completed. Additionally, we also have statistics for confirmation (double opt-in or DOI) emails in the form of delivered, reminded, opened, bounced, and complained counts.

> Reminders are sent out automatically after 24 hours if a registering panelist has not confirmed their email address. To enable sending reminders, please visit **Sub Panels** -> **Registration Survey** -settings by clicking on the **gear** icon in the Registration Survey box.

> Conversion rate is calculated from started surveys, using a simple formula **Number of new panelists** / **Number of started surveys** * 100%

### Rejections pie chart

SampleNinja can reject a registration for a variety of reasons:

- Is out of country (Configurable Sub Panel Settings -> Security)
- Is using public VPN (Configurable Sub Panel Settings -> Security)
- Is using corporate VPN (Configurable Sub Panel Settings -> Security)
- Is bot (Configurable Sub Panel Settings -> Security)
- Email address's domain cannot accept email (missing MX or Mail Exchange record)
- Duplicate (Machine fingerprint matches exatly some body else, these are not blocked but review is recommended)
- Email address provided produces a permanent bounce (email does not exist)

Some security features can be turned on/off in the **Sub Panel -> Security** settings. 

### Research Defender

If configured and enabled, you will see this pie chart. You can click on each pie slice on this chart to see more information about each rejection. 

> **IMPORTANT**: If your panel is B2B we recommend that you allow corporate VPNs. For example, almost all the Health Care Panels will have panelists like physicians/doctors accessing the system through a corporate VPN during work hours. The GEO location will be reported as the facility's physical location, like a hospital. If off work, you would be seeing networks like you would expect, i.e., in the US, you would see something like Spectrum, AT&T, Google, Comcast, or maybe even Elon Musk's StarLink. If in doubt, inspect the "network name and operator" under the info icon in the individual registration stats to determine if the panelist is real or suspicious. Seeing something like China Telecom could be a red flag.

> **WARNING** If you allow any VPNs (Virtual Private Networks), or hosted servers running VPN to access your community/projects, your location accuracy is no longer reliable. A user accessing the Internet through a VPN service can originate from **Iran** or any other country, including **North Korea**, and pretend to originate whichever country the VPN user chooses. There is no way to detect this automatically.

Additionally, we scan for email addresses that you have already blacklisted. SampleNinja also maintains a blacklist list of email domains known to be bad actors. In sort the registering folks may also be terminated if they:

- Provide an email address that is blacklisted
- Provide an email address that contains a domain name that is blacklisted

Contact support@sampleninja.io if you would like to contribute to our blacklisted domain collection. 

### Filtering
Click the **filter** -icon on the top right to open the filter menu. You can select a time range to look at the statistics and/or select individual recruitment sources to compare how the different sources perform. 

### View participant list
Click on the **View Participants** -button on the top right of the screen.

### Sources tab
Provides details on which recruitment sources are the most active in the past month.

> Source statistics are calculated using all registration surveys starts.

### Devices tab
Provides device information of all the registered and confirmed panelists.
