### Webhook URL
If you would like to call a webhook instead of sending invitation emails, enter a URL here to call. The request type is POST, and it contains a payload about the panelist, project, and the original email config + along with translations.

Using a token is optional. If supplied, it will be added to the **Authorization** header. The token enables you to secure access to the endpoint you are calling.

> You toggle on **Disable email invitations** in the project settings before the webhook will fire.

