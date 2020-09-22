## Business Rules
Business Rules are applied automatically to all project samples. You should always make sure that you have system variables such as STATUS, EMAIL_VALID and EMAIL_CONFIRMED included in the business rules. You may additionally apply filter such as not been invited in 7 days. Of course you can also include you custom data variables that fit your business case as well.

### STATUS
This variable indicated panelist's subscription status which can be either Subscribed, Unsubscribed or Blacklisted.

### EMAIL_VALID
This variable indicated that email address has no delivery issues. You should never attempt to deliver people EMAIL_VALID set to no because this will cause additional bounces and start effecting email reputation.

### EMAIL_CONFIRMED
This variable indicates that the panelist was double opted in and that the email address has been confirmed by the panelist.
