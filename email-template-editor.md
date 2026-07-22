## Email template editor
Use the email template editor to customize the content and appearance of your email templates with ease. 

### Template
Specify the template name and the groups this template should belong to. Please use the drop-down menu to view translations for other languages and locales.

### Elements
The element configuration includes options that can be enabled or disabled as needed. We recommend using all of them for the most professional-looking emails.

### Preview
This is the live preview of the email. You may click on the different elements to modify them. If you want to send the template to yourself, please click the **EMAIL TO ME** button.

#### Email Subject
This is the first thing the email recipients see. You may use Unicode characters like smileys in the subject.

> The email subject is the first thing the recipient sees. Always use different subject lines to keep your email more engaging.

#### Email pre-header
An email pre-header is the short summary text that follows the subject line when an email is viewed in the inbox. It's like a sneak peek into your content. It can provide additional context and nudge recipients to open your email. Pre-headers can also enhance engagement with your content by offering valuable information right off the bat. For instance, if you're running a special survey, mentioning it in the pre-header can entice those interested.

- Keep it concise and mobile-friendly. Most email clients display around 50 characters of the preheader, so edit yours to fit. If you need to go over this length, ensure your primary message is clear, even if cut off.

- Entice your audience. Give readers a reason to click. Tease the content, offer value, or create urgency.

- Complements your subject line. Your pre-header should add context to your subject line, not just repeat it.

#### Sender name
The sender name can be your panel's name or the project manager's name.

> Always use a name that the panelist will recognize!

### Settings
These let you control the logo alignment and the element colors. The font color is automatically selected based on the background color (white or black).

#### Font
Emails have limited font support across different operating systems like PCs, Macs, iPhones, etc.. We have selected generally supported font stacks for use in emails. Alternatively, you may upload a custom font to use. 

> Remember that you can use Emoji characters in the subject, preheader, and message body to spice things up. <a href="https://apps.timwhitlock.info/emoji/tables/unicode" target="_blank">Full list of Emojis</a>

### Sections (top to down)

The email is divided into sections. Each section can be edited by clicking on it. 

All multiline sections use Markdown, read more here: [Markdown basics](https://www.markdownguide.org/basic-syntax/#overview)

> **NOTE:** Logo can only be changed in the sub-panel settings!

#### Logo section
This logo is always inherited from the sub-panel logo. To change, you must change the sub-panel logo.

#### Engagement image section
Use the engagement image to keep your invitation looking unique by utilizing different images in each email template. If this area is not visible, please ensure that the **Elements** selection on the left has **Engagement Image** toggled on.

#### Content section
This section contains the greeting and body of the email. You may use markdown elements in this section. Click on the text to edit.

#### Action button section
This section contains an action button, and, for project invitations and reminders, it may also include the **Visit member app button** if the built-in Member App is enabled. You must enable **Member App Action Button** in the **Elements** configuration on the left side of the screen. You may use markdown elements in this section. Click on the text to edit.

#### Signature section
This section should contain a personal signature from the project manager. You may use markdown elements in this section. Click on the text to edit.

#### Project information section
The project information section is only visible for project invitations or reminders. The reward line will be hidden if the project offers no rewards.

#### Bottom body
The bottom body is disabled by default, but can be used to add additional information.

#### Notice section
This box contains specific disclaimers and notices you'd like to repeat in all emails. 

Examples and how they are inserted into the markdown:

- **Privacy policy** [privacy_policy_name:Click here to view privacy policy]
- **Cookie policy** [cookie_policy_name:Click here to view cookie policy]
- **Terms of use** [terms_policy_name:Click here to view terms of use]
- **Extra policy** [extra_policy_name:Click here to view extra policy]
- **Unsubscribe link** [unsubscribe_link_text:Click here]

You may use markdown elements in this section. Click on the text to edit. 

> **IMPORTANT!** Any modification to this section applies to all the email templates!

#### Unsubscribe from project reminders
You may use the following tag to offer a link-based approach for unsubscribing from the project reminders. The example below will produce a link that reads "Click here to unsubscribe from reminders".
```
[unsubscribe_project_url:Click here to unsubscribe from reminders]
```
This tag works in the signature, notice, or footer sections.

#### Footer section
This section usually contains the copyright text and terms of use. You may use **Footer** alone or combine it with the **Notice** section above it.

You may use markdown elements in this section. Click on the text to edit. 

> **IMPORTANT!** Any modification to this section applies to all the email templates!

### Personalization

The most commonly used data variables are those related to personalization.

- **[FIRST_NAME]**
- **[LAST_NAME]**
- **[POINTS_BALANCE]**

You may pipe variables into email templates by referring to them with their variable names in square brackets. For example:

```Hello [FIRST_NAME], we have a survey for you! Your balance is [POINTS_BALANCE]```

If the panelist does not have a value for the data variable, it will be silently removed from the final email.

#### Project email-related variables that you may use

- **[project-id]** The Sample Ninja project ID
- **[duration]** The LOI of the project
- **[reward-points]** The reward for the project
- **[public-project-name]** The public project name specified in the project settings
