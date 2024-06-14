## Email editor
Select the email template you would use using the **selected email template** selector. If you invite multiple sub-panel locales, you may choose them using **Preview for sub panel** and **Preview for locale** selectors. This enables you to provide customizations for each sub-panel and translations for each locale.

> You may now create multiple email templates in **Sub Panels -> Manage -> Email Templates**.

### Email Subject
Enter the email subject to this field

> The email subject is the first thing the recipient sees. Always use different subject lines to keep your email more engaging.

### Email preview text
Some email clients can display preview text. Do not enter important information as preview text as the recipient may not see it.

### Personalizing content
The following substitution variables can be inserted into all emails

- FIRST_NAME
- LAST_NAME
- EMAIL
- POINTS_BALANCE (Current reward points balance)
- PROJECT_ID (Current project ID, for example, when contacting support)

Place the variable name in square brackets and it will be replaced on the fly i.e. 

```
Hello [FIRST_NAME] we have a survey for you!
```
If the data variable is missing, it will be silently removed.

### Email logo
The email logo is automatically inherited from the sub-panel settings. If you don't see the logo, please verify your email templates and make sure the logo is enabled. Also, make sure that the sub-panel contains the uploaded logo.

### Engagement image
We recommend using engagement images with all emails to keep each looking different and original.

### Email body and signature
Email body and signature use Markdown language, which allows the user to apply formatting like header (###), bolding (\**), bulleted list (-), highlight box (>), etc.

> [Learn more about markdown](https://www.markdownguide.org/basic-syntax/#overview)

### Sending test email
You may send a test email by clicking the **EMAIL TO ME** button.

