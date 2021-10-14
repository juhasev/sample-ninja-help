## Dashboard

Registration statistics are available if you are using the built in Registration Survey. Each Sub Panel has their own registration survey. To configure registration survey for a Sub Panel please find the Registration Survey tab in the Sub Panel Settings.

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

> **IMPORTANT**: If your panel is B2B we recommend that you allow corporate VPNs. For example almost all the Health Care Panels will have panelists like physicians / doctors accessing the system through a corporate VPN. The reported geo location will be around the facilities your client operates. Any employee can remote in but the location will be reported as the facility address.

> **WARNING** If you allow any VPNs (Virtual Private Network), hosted server runnig VPN to access your community / projects your location IP accuracy is no longer reliable.

Additionally we scan for email addresses that you have already blacklisted. SampleNinja also maintains a blacklist list for email domains that are known to be bad actors. Contact support@sampleninja.io if you would like to contribute to our blacklisted domain collection. 

> Only if we all team up we make the future of research better. Your contribution is appreciated.

To recoup you registration will be rejected if you

- Provide an email address that is blacklisted
- Provide an email address that contains a domain name that is blacklisted

## Sources tab
Provides details which recruitment sources are the most active in the past month.
> These values are recorded using everybody visiting the registration survey.

## Devices tab
Provides information of all devices visiting the registration survey.

> These values are recorded using everybody visiting the registration survey.
