## Refer Friends

Enable Refer Friends to let your panelists earn extra rewards for inviting friends to join. You have multiple configuration options in terms of how and when the reward payout takes place. You also have control of who is eligible to refer friends, e.g. you may require at least 30 days of panel membership. To start, click on the **Enabled** -toggle to turn the feature on.

When enabled the **Refer Friends** feature writes to system variables **REFERRED_COUNT** and **REFERRED_BY**.

If you are using the built-in registration survey all the referred panelists are clearly marked in **R** -icon in the registration participation log. Click on the icon to see who the referee is.

> All referred friends are automatically tagged with **Refer a friend** -recruitment source. This recruitment source is automatically created for you.

### Configuration options:

Please consider configuring this feature with some time or action-based restrictions to help reduce potential misuse by professional panelists. 

> A professional panelist is a person who is using dirty tactics in an attempt to earn and cash out maximum rewards. Professionals use any tools available to them, including creating multiple accounts, providing false data in surveys to produce maximum completes, or misusing features like **Refer Friends**. 
 
#### Locale selection
Select which locale you want to preview the **Refer Friends** banner in.

#### Default background
Select one of the default backgrounds that come bundled with **SampleNinja**. See below **Upload background image** how to upload your custom background image.

#### Referee Reward
This is the number of reward points paid to the referer when all the configurable settings below are met. Leave as zero for no compensation.

#### Upload background image
The recommended background image size is 900 x 300 pixels. We recommend not placing any text directly on your background image, but let **SampleNinja** overlay the text. This is the minimum requirement if your **Sub Panel** is multilingual. **SimpleNinja** overlays the text using the correct **Locale** and **Language**. You can use **PNG** images to achieve transparency and **SVG** images for indefinite scalability and sharpness on high-resolution screens. 

To upload an alternate image, simply click on the upload icon at the bottom right. 

> **TIP** Use the sliders below to set margins for your text block. You can use the margins to prevent text from overlapping features on the background image. We recommend using the least amount of margins and keeping your messaging short. This is to ensure that all the text fits on mobile phone screens! 

> **LIMITATIONS** You cannot have different images for different locales.

#### Editing texts
Simply, click on the text to edit. The text box supports **Markdown**. Use the slider below the image to adjust the position of the text box. Similarly, click on the button to customize the text for the current locale.

#### Minimum days as member
Controls the minimum number of days a panelist must be subscribed before becoming eligible to refer friends. Leave as zero to disable.

#### Number of completed surveys
Controls how many surveys a referee must complete before the referred panelist is paid out. Leave as zero for an immediate referer compensation.

#### Minimum days between referrals
Controls how often an individual can refer friends. Enter zero to have **Refer Friends** permanently visible.

#### Maximum number of friends to refer
This is the number of friends that can be referred at one time. This setting does not control maximum lifetime referrals.

#### Redirect to registration survey
All traffic from confirming the referral is sent to the registration survey by default. However, if you run your registration survey externally, you can define an alternate redirect URL where the referrals are sent.

The alternate URL will receive the following query parameters:

- **ref** Unique referral ID
- **locale** Locale of the referring panelist
- **source** Recruitment source ID
- **email** Referred email address

> Use these values in your own registration flow. The following values can be passed back to **SampleNinja** when using **Application API** **Register Panelist** -end point.
- **ref** Required for Refer a Friend functionality to work correctly.
- **locale** Pass in using **LOCALE** variable
- **source** Pass in using **RECRUITMENT_SOURCE** variable

> Please note when testing that there is random delay up to 12 hours of sending the **Refer a friend** email out. If the referring panelist's email address matches one of the admin users there will be no delay!
