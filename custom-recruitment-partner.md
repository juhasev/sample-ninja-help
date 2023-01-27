## Custom recruitment partner

Enables you to create custom recruitment partners and automatically report conversion back to the partner.

Let's say you have a partner that sends you transaction_id and affiliate_id parameters. The partner want you to report doubled opted in back to https://reporting.gocloud.org.

Since this partner only want to be informed when a user is fully double opt-in you would selected the double opted in URL and enter the following:

```

httpd://reporting.gocloud.org?tid=[transaction_id]&aff_id=[affiliate_id]

```
Sample Ninja will automatically capture all incoming URL parameters with their respective name so you have refer to the in the reporting URLs.

You can report back the following events:

- Registration survey started (user clicks on the start button)
- Registration survey completed (user completes the survey but has not yet been double opted in
- Regisgtration survey double opted in (most comment, a panelist is fully double opted in)
