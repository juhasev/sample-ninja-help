## Dashboard

Registration statistics are available if you are using the built-in Registration Survey. Each Sub Panel has their own registration survey. To configure registration survey for a Sub Panel please find the Registration Survey tab in the Sub Panel Settings.

If you have at least one registration survey active you can select it from the top pulldown to view statistics.

> The registration statistics are limited for the past month. You can use the **JOIN_DATE**, **EMAIL_VALID**, **EMAIL_CONFIRMED** - data variables to filter, slice and dice any given period in various other features throughout the application. The email delivery statistics are not stored for more than 30 days and cannot be use in filtering or in segments. The **EMAIL_VALID** variable indicates whether your email is valid, meaning we have recorded successfull delivery at least once. If panelist email bounces the **EMAIL_VALID** variable will be set to NO.

> Click on the **View Activity** button at the top to view indivual registration sessions.

### Top row statistics
Statistics include number of new panelists, conversion rate, survey rejections, surveys started and completed. Additionally we also include statistics for confirmation (double opt-in) emails in form of delivered, opened and bounced counts. 

> Conversion rate is calculated from started surveys, using simple formula **Number of new panelists** / **Number of started surveys** * 100.

### Registration failures pie chart

SampleNinja can reject registration for variety of reasons:

- Is out of country (Configurable Sub Panel Settings -> Security)
- Is using public VPN (Configurable Sub Panel Settings -> Security)
- Is using corporate VPN (Configurable Sub Panel Settings -> Security)
- Is bot (Configurable Sub Panel Settings -> Security)
- Email address's domain cannot accept email (missing MX or Mail Exchange record)
- Duplicate (Machine fingerprint matches exatly some body else, these are not blocked but review is recommended)
- Email address provided produces a permanent bounce (email does not exist)

Some of the security features can be turned on/off in the **Sub Panel -> Security** settings. 

> **IMPORTANT**: If your panel is B2B we recommend that you allow corporate VPNs. For example almost all the Health Care Panels will have panelists like physicians / doctors accessing the system through a corporate VPN during the work hours. The reported GEO location will be reported as the physical location of the facility like a hospital. If off work you would be seeing networks like you would expect i.e. in US you would see something like Spectrum, AT&T, Google or Comcast or maybe even Elon Musk's StarLink. If in doubt inspect the "network name and operator" under the info icon in the individual registration stats to give you a clue if the panelist is real or suspicious. Seeign something like China Telecom could be a red flag.

> **WARNING** If you allow any VPNs (Virtual Private Networks), hosted servers runnig VPN to access your community / projects your location accuracy is no longer reliable. A user accessing the Internet throught a VPN service can originate from from **Iran** or any other country including **North Korea** and pretend to originate which ever country to VPN user chooses. There is no way to detect this automatically.

Additionally we scan for email addresses that you have already blacklisted. SampleNinja also maintains a blacklist list for email domains that are known to be bad actors. In sort the registering folks may also be terminated if they:

- Provide an email address that is blacklisted
- Provide an email address that contains a domain name that is blacklisted

Contact support@sampleninja.io if you would like to contribute to our blacklisted domain collection. 

### Filtering
Click on the **filter** -icon top right to open up the filter menu. You can select time range to look at the statistics and/or select individual recruitment sources to compare how the different sources are performing. 

### Sources tab
Provides details which recruitment sources are the most active in the past month.
> These values are recorded using everybody visiting the registration survey.

### Devices tab
Provides information of all devices visiting the registration survey.

> These values are recorded using everybody visiting the registration survey.
