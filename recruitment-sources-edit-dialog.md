### Edit recruitment source

Enter the name and cost per conversion in **reward points**. For example if $1 equals to 100 points and your recruitment cost is 50c you would enter 50 as the cost per conversion.

#### Enabling and disabling recruitment sources
By default all recruitment sources are enabled. If you wish to turn one off then use the **enabled** toggle to do so.

> When recruitment source is disabled any traffic sent from the URL will be terminated immediately.

In order for the recruitment source tracking to work you must supply the **source** parameter on the URL. Example:

```
https://yourdomain.sampleninja.io/registration/1/ENG-CA?source=10
```

#### Tune Integration

Toggle **TUNE Enabled** if you need the recruitment survey to send conversion data back to Tune.

> For more information visit https://www.tune.com

When enabled the **transaction_id** parameter must be provided along with the **source** parameter. Example:

```
https://yourdomain.sampleninja.io/registration/1/ENG-CA?source=10&transaction_id=935f78f8-066b-4c8f-b0a1-dd0421d0a3c6
```

