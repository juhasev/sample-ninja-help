### Google Tag

Track every single panelist interaction using your own Google Tag. Google Tag can be used with various Google services, including Google Adwords and Google Analytics. Google Tag is executed on all panelist-facing pages, including all the landing pages, the registration survey, and the member app.

> **IMPORTANT!** Google Tag may not be **GDPR** or **CCPA** compliant and may require additional disclosures when used. We recommend disclosing in the **Privacy Policy** landing page in the section **Information we collect**

### Setup

Let's say you want to use Google Analytics. 

1) First, log in to Google Analytics.
2) Then Go to Admin -> Data Collection and Modification -> Data Streams.
3) Next, create a new web stream.
4) Enter your Sample Ninja site base URL as Stream URL, for example https://clientname.panelservice.io
5) Name the stream and hit the Create and Continue button.
6) Edit the new stream and copy the Measurent ID.

Next, we set up a new Google Tag using [Google Tag Manager](https://tagmanager.google.com).

1) Login to the Google Tag Manager
2) Create a new tag
3) Tag configuration -> Select Google Analytics -> Google Tag
4) Enter the Measurent ID you obtained from Google Analytics and paste it into the Tag ID field.
5) Choose a trigger Page View Trigger
6) Save

Copy the GTM code (GTM-XXXXXXXX) from the top toolbar and paste it into **Sub Panels -> Manager -> Settings -> Google Tag**. The tag should now be called on each page (panelist-facing pages).

> Please refer to [Google Tag Manager Help](https://support.google.com/tagmanager) for more information on configuring other services, such as Google Analytics or Google Adwords. 

> [Google Tag Manager & Google Analytics tutorial](https://support.google.com/tagmanager/answer/9442095) 
