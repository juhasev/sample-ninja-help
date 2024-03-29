## Email template editor
Use the email template editor to customize the content and appearance of your email templates with ease. 

### Configuration settings

#### Template
Specify the template name and the groups this template should belong to. Please use the drop-down menu to view translations for another language and locale.

#### Elements
The element configuration contains various options that can be enabled or disabled when needed. We recommend using all of them for the most professional-looking emails.

#### Preview
This is the live preview of the email. You may click on the different elements to modify them. If you want to send the template to yourself, please click the **EMAIL TO ME** button.

**Subject and sender**

> Always vary the subject in all your emails. This is the first thing the email recipients see. You may use Unicode characters like smileys in the subject.

#### Settings
These let you control the logo alignment and the element colors. The font color is automatically selected based on the background color (white or black).

#### Font
Emails have limited font support across different operating systems like PCs, Macs, iPhones, etc... We have picked up generally supported font stacks that can be used with emails. Alternatively you may upload a completely custom font to be used. 

### Sections (top to down)

The email is divided into sections. Each section can be edited by clicking on it. 

All multiline sections use Markdown, read more here: [Markdown basics](https://www.markdownguide.org/basic-syntax/#overview)

> NOTE: Logo can only be changed in the sub-panel settings!

#### Logo section
This logo is always inherited from the sub-panel logo. To change, you must change the sub-panel logo.

#### Engagement image section
Use the engagement image to keep your invitation looking unique by utilizing different images in each email template. If this area is not visible please ensure that the **Elements** selection on the left you have **Engagement Image** toggled on.

#### Content section
This section contains the greeting and body of the email. You may use markdown elements in this section. Click on the text to edit.

#### Action button section
This section contains an action button, and in terms of project invitations and reminders, it may also contain the **Visit member app button** if the built-in Member App is enabled. You must enable **Member App Action Button** in the **Elements** configuration on the left side of the screen. You may use markdown elements in this section. Click on the text to edit.

#### Signature section
This section should contain a personal signature from the project manager. You may use markdown elements in this section. Click on the text to edit.

#### Project information section
The project information section is only visible for project invitations or reminders. The reward line will be hidden if the project does not offer any reward.

#### Notice section
This box contains specific disclaimers and notices that you'd like to repeat in all emails. 

Examples:

- Terms of use
- Privacy policy
- Unsubscribe link

You may use markdown elements in this section. Click on the text to edit. 

> **IMPORTANT!** Any modification to this section applies to all the email templates!

#### Footer section
This section usually contains the copyright text and terms of use. You may choose to use **Footer** alone or combine it with the **Notice** section above it.

You may use markdown elements in this section. Click on the text to edit. 

> **IMPORTANT!** Any modification to this section applies to all the email templates!

### Personalization

The following variables can be piped into all emails

- FIRST_NAME
- LAST_NAME
- EMAIL
- POINTS_BALANCE
- PROJECT_ID

Place variable name in square brackets and it will be replaced on the fly i.e. 

```Hello [FIRST_NAME] we have a survey for you!```

If the data variable is missing, it will be silently removed.
