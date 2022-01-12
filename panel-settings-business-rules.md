## Business Rules
Business Rules are applied automatically to all the projects you or anyone creates in Sample Ninja. You should always make sure that you have system variables such as **STATUS**, **EMAIL_VALID** and **EMAIL_CONFIRMED** included in the business rules. You may additionally apply various activity filters. By default Sample Ninja includes a filter that excludes anybody who has been invited in the past week (7 days). This prevents you from over utilizing your panel which tends to lead into higher unsubscription rates. You are free to include your own custom data variables that fit your business needs as well i.e PERSON_VERIFIED = "yes".

> Business rules do not apply to recontacts or reminders. 

### STATUS
This variable indicates panelist's subscription status which can be either **Subscribed, Unsubscribed or Blacklisted**.

### EMAIL_VALID
This variable indicates that email address has delivery issues. You should never attempt to send invitations to panelists which have EMAIL_VALID set to NO because this will cause additional bounces and start effecting the email reputation and ultimately delivability.

### EMAIL_CONFIRMED
This variable indicates that the panelist was double opted in and that the email address has been confirmed by the panelist.
