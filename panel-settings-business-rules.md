## Business Rules
Business Rules are applied automatically to all sample pulls. You should always make sure that you have system variables such as STATUS, EMAIL_VALID and EMAIL_CONFIRMED included in the business rules. You may additionally apply various activity filters. By default Sample Ninja includes filter that excludes anybody who has been invited in the past week (7 days). This prevents over utilizing your panel which leads to higher unsubscrition rates because you are sending too frequent emails. However, the business rules are ignored in the second change routing and available surveys with in the Community Portal. Of course you can also include you custom data variables that fit your business case as well.

### STATUS
This variable indicates panelist's subscription status which can be either **Subscribed, Unsubscribed or Blacklisted**.

### EMAIL_VALID
This variable indicates that email address has no delivery issues. You should never attempt to deliver people EMAIL_VALID set to no because this will cause additional bounces and start effecting email your reputation.

### EMAIL_CONFIRMED
This variable indicates that the panelist was double opted in and that the email address has been confirmed by the panelist.
