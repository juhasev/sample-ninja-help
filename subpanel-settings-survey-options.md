## Survey Options

### Enable registration
This must be turned on to access the registration survey. Otherwise, you will receive a 404 Not Found message.

### Show progress
Use this control to enabled the progress bar in the registration survey.

### Auto fill region details
 You can choose to populate COUNTRY, REGION (state), CITY, and POSTAL_CODE data variables automatically from the detected geo-location.

> Sample Ninja uses an IP-based geolocation provided by https://www.ip-api.com. For example, you wouldn't know a person's exact street address, but you would most likely place them in the right zip code in the correct city. If you collect variables like CITY and POSTAL_CODE during the registration survey, this setting will not override actual answers provided by the registering panelist.

> Please note that mobile customers using Apple's iPhone will have their location masked by default (new Apple 2022 non tracking initiatives), which means the city may differ from the actual city the panelist lives in. Generally speaking, the state-level data can be considered accurate.

### Create password
The registration survey prompts the registering panelist to create a password when enabled. A password is required if your panelists are offered access to the **Member's app** via the built-in app or via **Community API**.

### Use Google reCaptcha
This enables Google's reCaptcha validation, designed to ensure no bots or other suspicious persons can register.

> Sample Ninja recommends you turn reCaptcha on! reCaptcha must be configured in **Panel Settings** -> **Integrations** before it can be used.

### Double Opt-in
If you are double-opting your panelists in another way, you may disable a double opt-in email from being sent.

### Send reminders
You can enable this setting to send email confirmation reminders automatically. The reminders are sent 24 hours after registration if a panelist still needs to confirm their email address.

### Prominent email confirmation info
Provides registering panelists extra information about the confirmation email, like checking their spam folder and whitelisting the sender address. This information is presented in a green info box at the top of the page. This setting is optional; alternatively, you can incorporate your messaging into the **Registration complete** -landing page instead. 

> **Example:** We have sent you a confirmation email! Please check your inbox now to complete your registration!
> - Remember to check your spam folder! Sometimes, emails may be placed there accidentally.
> - Please add email invite@clientname.panelservice.io to your address book so you do not miss any survey opportunities!

> The texts/translations in this box can be edited via the generic sub-panel translations only.

### Disable welcome page
Use this toggle to disable the **Registration Welcome** page altogether for example in cases where you have a pre-screener survey before the **Registration Survey**.

> It is recommended that you use this page to explain what the panel is all about. 

### Disable consent checkboxes
If you handle getting proper user consent some other way you may disable the consent boxes.

> You must have consent to email, and all your panelists must accept the Terms and Conditions and Cookie Policies. If you don't do this, you may violate CCPA and GDPR regulations.
