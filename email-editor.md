## Email editor
Select the email template you would use by using the **selected email template** selector. If you are inviting multiple sub-panel locales, you may select them using **Preview for sub panel** and **Preview for locale** selectors. This enables you to provide customizations for each sub-panel and translations for each locale.

> You may now create multiple email templates in **Sub Panels -> Manage -> Email Templates**.

### Email Subject
Enter the email subject to this field

### Piping data variables
The following data variables can be piped into all emails

- FIRST_NAME
- LAST_NAME
- EMAIL
- POINTS_BALANCE
- PROJECT_ID

Place variable name in square brackets and it will be replaced on the fly i.e. Hello [FIRST_NAME] we have a survey for you! If the data variable is missing, it will be silently removed.

> Please note that test sessions are not tied to an actual panelist; thus, data variable piping is not possible for any test sessions.

### Email sender name
Please type in the email sender name you want the email to appear to be coming from.

### Email body and signature
These use Markdown language, which allows the user to apply formatting like header (###), bolding (\**), bulleted list (-), highlight box (>), etc.

> [Learn more about markdown](https://www.markdownguide.org/basic-syntax/#overview)
