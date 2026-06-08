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

Sample Ninja automatically sends events from both the panelist‑facing pages (landing pages, registration survey, email‑confirmed page) and the Member App. Standard Meta events are used wherever one applies — so Meta's built‑in optimization and reporting work out of the box — and everything else is sent as a custom event.

**Conversion: successful registration → `CompleteRegistration`**

`CompleteRegistration` is the event that marks a *successful* registration. **When it fires depends on the registration method:**

- **Social flow:** fired immediately after the panelist finishes the survey. The social login already proves the identity, so registration is complete at that point.
- **Password flow:** fired when the panelist opens the **email confirmation link**. Registration is only complete once the email address is confirmed, so `CompleteRegistration` is *not* sent when the survey is submitted — at that stage the account still needs confirming.

In the password flow you will therefore see `CompleteRegistration` only **after** the confirmation link is opened, not when the survey is sent.

**`PageView`**

Fired on every panelist‑facing page (landing pages, registration survey, email‑confirmed page, and the Member App).

**Custom events (milestones, not conversions)**

These mark steps along the funnel. They are **not** registration completions — do not use `complete` as your success metric; use `CompleteRegistration` for that.

- `welcome` — the survey's initial welcome step
- `start` — the panelist begins the survey/registration. Also sent as the standard Meta `Lead` event.
- `complete` — the registration **survey was submitted**. A milestone only ("the form was sent"); in the password flow the account is **not yet confirmed** when this fires.
- `email_confirmation_sent` — password flow only: the confirmation email has just been sent
- `disqualified` — the participant was screened out during registration (fires on its own; no conversion)

**Event parameters and data policy**
- `registration_method` is included on the relevant events (`password` or `social`)
- No PII (such as email) is sent

**Naming convention**
- Standard Meta events are used whenever applicable: `PageView`, `Lead` (via `start`), and `CompleteRegistration` (via `sign_up`)
- Custom events use short lowercase names; multi‑word events use snake_case to match our internal analytics (e.g., `welcome`, `start`, `complete`, `email_confirmation_sent`, `disqualified`)

#### Why don't I see `CompleteRegistration` in the password flow?

In the password flow, `CompleteRegistration` fires on the **email‑confirmation page**, in whatever browser opens the confirmation link. Seeing `PageView`, `Lead`, `complete` and `email_confirmation_sent` but **not** `CompleteRegistration` almost always means the confirmation page never got a chance to send the Pixel. Check the following:

- **Open the confirmation link in a full browser**, not an email app's built‑in viewer. Links are often opened in an in‑app webview or a privacy browser where the Meta Pixel is blocked — the email still confirms in Sample Ninja, but the event never reaches Meta.
- **Ad/tracking blockers** and Safari/iOS tracking protection can block the Pixel on that page. Re‑test in a clean browser with no blockers.
- **Verify on the page itself:** after clicking the link, open the email‑confirmed page and use the **Meta Pixel Helper** there to confirm the Pixel loads and `CompleteRegistration` fires.

Because the earlier `complete` and `email_confirmation_sent` events happen during the uninterrupted survey session, they show up reliably; the confirmation click is a separate navigation, which is why it is the most common place for the Pixel to be missed.

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
