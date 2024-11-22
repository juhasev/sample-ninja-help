### Webhook URLs

Webhook calls are made from server to server and use the POST request type. If the call fails for any reason, it will be retried five times once per hour. You should always return HTTP STATUS 200 when the call succeeds. You may supply a token, which enables you to secure access to the endpoint you are calling.

> Using a token is optional. If supplied, it will be added to the **Authorization** header.

#### Invited webbook
If you would like to call a webhook instead of sending invitation emails, enter a URL here to call. The payload contains panelist, project, original email config, and translations.

> **WARNING** This will disable all project email invitations!

#### Email confirmed webhook
This is your best friend if you want to trigger a webhook call when panelists confirm their email. The request type is POST, and the payload includes panelist ID, panelist data variables, and sub-panel info.

