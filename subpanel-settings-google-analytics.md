## Analytics Platforms

Track every single panelist interaction using your own analytics platforms. Sample Ninja supports both Google Tag Manager (for Google Analytics, Google Ads, etc.) and Meta Pixel (for Meta Ads and event measurement). Tags are executed on all panelist-facing pages, including landing pages, the registration survey, and the member app.

> IMPORTANT!
> Third‑party analytics platforms such as Google Tag Manager and Meta Pixel may not be GDPR or CCPA compliant out of the box and may require additional disclosures and/or consent. We recommend updating your Privacy Policy (landing page) under the section "Information we collect" and gating tags behind consent if required by your jurisdiction.

### Google Tag Manager

#### Setup

Let's say you want to use Google Analytics.

1) First, log in to Google Analytics.
2) Then go to Admin -> Data Collection and Modification -> Data Streams.
3) Next, create a new web stream.
4) Enter your Sample Ninja site base URL as Stream URL, for example https://clientname.panelservice.io
5) Name the stream and hit the Create and Continue button.
6) Edit the new stream and copy the Measurement ID.

Next, we set up a new Google Tag using [Google Tag Manager](https://tagmanager.google.com).

1) Log in to Google Tag Manager
2) Create a new tag
3) Tag configuration -> Select Google Analytics -> Google Tag
4) Enter the Measurement ID you obtained from Google Analytics and paste it into the Tag ID field
5) Choose a trigger: Page View Trigger
6) Save

Copy the GTM code (GTM-XXXXXXXX) from the top toolbar and paste it into **Sub Panels -> Manager -> Settings -> Google Tag**. The tag should now be called on each page (panelist-facing pages).

> **REMEMBER** to publish the container!

### Meta Pixel

Meta Pixel helps you measure conversions, optimize delivery, and build audiences for your Meta campaigns.

#### Create your Meta Pixel ID

1) Go to Meta Events Manager. You can start from the guide: https://www.facebook.com/business/help/952192354843755?id=1205376682832142
2) Click "Connect Data Sources" and choose "Web"
3) Select "Meta Pixel" and click Continue
4) Name your Pixel, optionally enter your website URL, and click Create
5) In Events Manager, open your Pixel and copy the Pixel ID (a numeric value)

#### Add the Pixel ID to Sample Ninja

- Go to **Sub Panels -> Manager -> Settings -> Meta Pixel ID**
- Paste your Meta Pixel ID and save
- The Pixel will be executed on all panelist-facing pages (landing pages, registration survey, and member app)

#### Events and naming

Sample Ninja automatically sends events from both the server‑rendered landing pages and the Member App. You will see the following in Meta Events Manager:

- PageView: fired on page loads (landing pages) and member app route changes
- Lead: fired when a participant starts the registration process
- CompleteRegistration: fired when a participant successfully completes registration (also used for sign up)
- Custom events:
  - welcome: when the registration welcome screen is shown
  - disqualified: when a participant is screened out during the registration

Naming convention
- Standard Meta events are used whenever applicable (PageView, Lead, CompleteRegistration)
- Custom events use snake_case names to match our internal analytics (e.g., welcome, disqualified)

Tip: Use the Meta Pixel Helper browser extension to verify that your Pixel is loaded and events are firing.

**Additional reading**

> Please refer to [Google Tag Manager Help](https://support.google.com/tagmanager) for more information on configuring other services, such as Google Analytics or Google Ads.
>
> [Google Tag Manager & Google Analytics tutorial](https://support.google.com/tagmanager/answer/9442095)
>
> Meta Pixel: Getting Started — https://developers.facebook.com/docs/meta-pixel/get-started
>
> Meta Pixel: Events reference — https://developers.facebook.com/docs/meta-pixel/reference
>
> Meta Business Help Center: Create and set up the Meta Pixel — https://www.facebook.com/business/help/952192354843755
>
> Meta Pixel Helper (troubleshooting) — https://developers.facebook.com/docs/meta-pixel/support/pixel-helper
