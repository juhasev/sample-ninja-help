## Custom recruitment partner

Create and configure custom recruitment partners which automatically report conversions back to the partner.

Let's say you have a partner that sends you transaction_id and affiliate_id parameters. The partners wants you to report doubled opted in back to https://reporting.gocloud.org using **tid** and **aff** URL parameters.

Since this partner only want to be informed when a user is fully double opt-in you would use **Registration double opted in reporting URL** and enter the following:

```
httpd://reporting.gocloud.org?tid=[transaction_id]&aff_id=[affiliate_id]
```

Sample Ninja will automatically capture all incoming URL parameters with their respective name so you have refer to the in the reporting URLs, even if they are reported back using different parameter names.

You can report back the following events:

- Registration survey started (user clicks on the start button)
- Registration survey completed (user completes the survey but has not yet been double opted in
- Regisgtration survey double opted in (most comment, a panelist is fully double opted in)

> Not all the partners require all URL. You can simply leave the URLs empty when not needed!
