## Optional features

Here are the optional settings and what they do:

#### Use Google's reCaptcha
Use Google reCaptcha to detect all non-humans when logging in.

> You should always configure the Google Recaptcha for additional security.

#### Display logo in the toolbar
Whether to display the logo in the Member App's toolbar.

#### Display reward points in the toolbar
Display panelists' reward points in the Member App toolbar.

#### Show next-tier rewards
This keeps the rewards page populated with next-tier rewards available if more points are earned. For example, if a panelist has accumulated $15 worth of reward points, the panelist would see all the rewards with values $5, $10, and $20 (the next tier above the current balance). The panelists would see all the $5 rewards if they had zero balance as opposed to seeing nothing.

> Enabling this setting is recommended. This also enables panelists to see "future rewards" on their rewards page that are not yet available based on the balance alone. This encourages further participation.
  
#### Show footer on all pages
Displays the configured landing page footer on all Member App pages. When turned off, the footer is only displayed on the login screen. To edit the footer, visit **Sub Panels -> Manage -> Landing Pages**, edit any landing page, and change the footer. The footer is shared among all landing pages, including the Member App.

#### Allow panelists to create a password at login
This enables seamless panel migration from an existing panel. Because the passwords are one-way encrypted, it is impossible to read the existing passwords and migrate them over. If a panelist attempts to log in to the member app without a password, an email will be sent to ask them to create one.

#### Veriff ID verification
Enables Veriff ID verification before a panelist can redeem any rewards. Panelists must perform ID verification once per year. To enable Veriff on the panel level go to **Settings -> Integrations -> Veriff** from the main menu.

#### Enable Adverizing ID
When toggled on **OpinionNinja**, the mobile app asks for permission from the user to save the Advertising ID to the **ADVERTISING_ID** data variable. If you are not tracking panelists across multiple sites, do not enable this setting, as it causes an additional prompt for all iOS users.

#### API access only
Turning this setting on will disable access to the built-in member app while allowing API access from a custom community.

