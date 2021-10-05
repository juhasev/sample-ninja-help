## Edit recruitment source

Enter the name and cost per conversion in **reward points**. For example if $1 equals to 100 points and your recruitment cost is 50c you would enter 50 as the cost per conversion.

### Enabling and disabling recruitment sources
By default all recruitment sources are enabled. If you wish to turn one off then use the **Source ENABLED** / **Source DISABLED** select to do so.

> When recruitment source is disabled any traffic sent from the URL will be terminated immediately.

In order for the recruitment source tracking to work you must supply the **source** parameter on the URL. Example:

```
https://domain.sampleninja.io/registration/1/ENG-CA?source=10
```

### Tune Integration

Use the pulldown to enable conversion reporting back to Tune. 

> For more information visit https://www.tune.com

When enabled the **transaction_id** parameter must be provided along with the **source** parameter. Example:

```
https://domain.sampleninja.io/registration/1/ENG-CA?source=10&transaction_id=935f78f8
```

Or for test mode:

```
https://domain.sampleninja.io/registration/1/ENG-CA?source=10&transaction_id=935f78f8&test=true
```


> For developer documentation please visit [Getting started with the JavaScript SDK](https://developers.tune.com/javascript-sdk/getting-started-with-the-javascript-sdk)

### MVF Integration

Use the **Integration Partner** to report conversion back to MVF.

? For more information visit https://www.mvfglobal.com

When enabled Sample Ninja expects 6 URL parameters to be passed:

1) **sid** MVF internal user identifier
2) **pip** MVF internal job identifier
3) **first** First name collected by MVF
4) **last**  Last name collected by MVF
5) **gender** Gender collected by MVF (male (1) or female (2))
6) **email** Email address collected by MVF

Let's say you have **Recruitment Source** with 4 with MVF integration enabled. Now your **Registration Survey** URL would look like this:

```
https://sampleninja.app/registration/1/ENG-US?source=4&sid=12345&did=123456&first=John&last=Doe&email=john.doe@sampleninja.io
```

> Variable data that is not in valid format will be silently ignored and users are automatically asked to fill in questions again.
