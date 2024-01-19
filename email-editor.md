## Email editor
Use **preview for subpanel** and **preview for locate** controls to switch between different subpanels and locales and provide customizations for each.

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

> The defaults can be configured under **Sub Panels** and **Email Templates**

### Email body and signature

These use Markdown language, which allows the user to apply formatting like header (###), bolding (\**), bulleted list (-), highlight box (>), etc.

> (https://www.markdownguide.org/basic-syntax/#overview)
