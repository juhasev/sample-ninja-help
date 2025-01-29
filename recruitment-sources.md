## Recruitment Sources

Recruitment sources are used to track different sources of registration traffic. 

### Recruitment source list

The **Recruitment Source ID** is indicated in the blue circle next to the registration source's name when viewing the registration source. This recruitment source ID is always appended to the registration survey URL as **source** query parameter.

```
https://domain.sampleninja.io/registration/1/ENG-CA?source=10
```
If the recruitment source uses **UUID** for identification, a red lock will appear on top of the blue recruitment source ID. Click to copy to the clipboard. Example URL with UUID:

```
https://domain.sampleninja.io/registration/1/ENG-CA?source=5f031c0e-dc5f-4e79-a318-46fa62fd42f9
```

> By default, if the **source** parameter is omitted all panelists are assigned data variable **RECRUITMENT_SOURCE** = 1
 
### Creating and editing recruitment sources

Enter the name and cost per conversion, and if you are using external recruitment partners, select the partner name from the pulldown.

The recruitment partners are configured in **Settings -> Integrations**.

### Tracking recruitment sources in real-life

If you use the built-in registration survey, you need to append the **source** query param to the URL. Example:

```https://yourcompany.sampleninja.io/registration/1/ENG-US?source=12```

The recruitment source IDs are listed on each row for each source. Similarly, if you register a panelist using the **Community API**, you must supply the correct ID in the **RegisterPanelist** API call.

### Appending affiliate ID
Some recruitment partners utilize multiple affiliates. You may track them by passing in **affliate_id** parameter. Example:

```https://yourcompany.sampleninja.io/registration/1/ENG-US?source=12&affiliate_id=zrecruiter12```

### Enabling and disabling recruitment sources
By default, all recruitment sources are enabled. If you wish to turn one off, then use the **Source ENABLED** / **Source DISABLED** select to do so.

> When the recruitment source is disabled, any traffic sent from the URL will be terminated immediately.

For the recruitment source tracking to work, you must supply the **source** parameter on the URL. Example:

```
https://domain.sampleninja.io/registration/1/ENG-CA?source=10
```

### AdBloom recruitment

To use **AdBloom** conversion reporting, you must first enable it in the **Panel Settings** under **Integrations**. You must have an account with **AdBloom** and know your **Reporting URL** before enabling the service. This information is available via the **AdBloom** admin interface or your **AdBloom** representative.

Next, create a **recruitment source** and enable **ADBLOOM** integration.

When enabled, the recruitment source ID or **source** and AdBloom click ID or **cid** URL query parameters must be provided. For example, if your standard **Registration Survey** URL looks like this:

```
https://domain.sampleninja.io/registration/1/ENG-CA
```

You need to append all the required parameters and the final URL will look like this:

```
https://domain.sampleninja.io/registration/1/ENG-US?source=3&cid=a93b5fc7d44234dab8f8
https://domain.sampleninja.io/registration/1/ENG-CA?source=10&cid=a93b5fc7d44234dab8f8
```

### Everflow recruitment
To use **Everflow** conversion reporting you must first enable it in the **Panel Settings** under **Integrations**. You must have an account with **Everflow** and know your **Reporting URL** before enabling the service. This information is available via the **Everflow** admin interface or from your **Everflow** representative.

Next, create a **recruitment source** and enable **Everflow** integration.

When enabled, the recruitment source ID or **source** and **Everflow** **transaction_id** URL query parameters must be provided. For example, if your standard **Registration Survey** URL looks like this:

```
https://domain.sampleninja.io/registration/1/ENG-CA
```

You need to append all the required parameters and the final URL will look like this:

```
https://domain.sampleninja.io/registration/1/ENG-CA?source=10&transaction_id=a93b5fc7d44234dab8f8
```

### ShareASale Recruitment.
To use **ShareASale** conversion reporting, you must first enable it in the **Panel Settings** under **Integrations**.

if your standard **Registration Survey** URL looks like this:
```
https://domain.sampleninja.io/registration/1/ENG-US
```

You need to append the **source** parameter to the URL which corresponds to **Recruitment Source ID** assigned for ShareASale. The "sscid" parameter is populated by **ShareASale** and contains click ID. 

```
https://domain.sampleninja.io/registration/1/ENG-CA?source=4&sscid=31k7_182ftf
```

### TUNE Recruitment
To use **TUNE** conversion reporting you must first enable it in the **Panel Settings** under **Integrations**. 

Use the **Integration Partner** pulldown and select **TUNE**

When enabled, the recruitment source ID or **source** and TUNE transaction ID or **transaction_id** URL query parameters must be provided. For example, if your standard **Registration Survey** URL looks like this:
```
https://domain.sampleninja.io/registration/1/ENG-CA
```

You need to append the required parameters, and the final URL will look like this:

```
https://domain.sampleninja.io/registration/1/ENG-CA?source=10&transaction_id=935f78f8
```

> **TUNE** must use this URL format for all their redirects.

Or for test mode:

```
https://domain.sampleninja.io/registration/1/ENG-CA?source=10&transaction_id=935f78f8&test=true
```
As long as the **registration survey** URL is configured in **TUNE's admin interface** these URL parameters are automatically appended when new recruits land into your registration survey.

> The **source** parameter must be a valid **Recruitment Source ID** and the **Recruitment Source** must have **TUNE** enabled.

> For more information visit https://www.tune.com

