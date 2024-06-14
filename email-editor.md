## Email editor
Select the email template you would use using the **selected email template** selector. If you invite multiple sub-panel locales, you may choose them using **Preview for sub panel** and **Preview for locale** selectors. This enables you to provide customizations for each sub-panel and translations for each locale.

> You may now create multiple email templates in **Sub Panels -> Manage -> Email Templates**.

### Email Subject
Enter the email subject to this field

> The email subject is the first thing the recipient sees. Always use different subject lines to keep your email more engaging.

### Email pre-header
An email pre-header is the short summary text that follows the subject line when an email is viewed in the inbox. It's like a sneak peek into your content. It can provide additional context and nudge recipients to open your email. Pre-headers can also enhance engagement with your content by offering valuable information right off the bat. For instance, if you're running a special survey, mentioning it in the pre-header can entice those interested.

- Keep it concise and mobile-friendly. Most email clients display around 50 characters of the preheader, so edit yours to fit. If you need to go over this length, ensure your primary message is clear, even if cut off.

- Entice your audience. Give readers a reason to click. Tease the content, offer value, or create urgency.

- Complement your subject line. Your pre-header should add context to your subject line, not just repeat it.

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

