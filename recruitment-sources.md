## Recruitment Sources

Recruitment sources are used to track of different sources of registration traffic. 

When viewing registration source the **Recruitment Source ID** is indicated in the blue circle, next to the recruitment source's name. This recruitment source ID is always appended to the registration survey URL as **source** query parameter.

```
https://domain.sampleninja.io/registration/1/ENG-CA?source=10
```

> By default all panelist are assigned data variable **RECRUITMENT_SOURCE** = 1.
 
### Creating and editing recruitment sources

Enter the name, cost per conversion and if you are using external recruitment partners select the partner name from the pulldown.

The recruitment partners are configured in **Settings -> Integrations**.

### Tracking recruitment sources in real life

If you are using the built-in registration survey you need to append **source** query param to the URL. Example:

```https://yourcompany.sampleninja.io/registration/1/ENG-US?source=12```

The recruitment source IDs are listed on the each row for each source. Similarly if you are registering panelist using the **Community API** you must supply the correct ID in the **RegisterPanelist** API call.

### Enabling and disabling recruitment sources
By default all recruitment sources are enabled. If you wish to turn one off, then use the **Source ENABLED** / **Source DISABLED** select to do so.

> When recruitment source is disabled any traffic sent from the URL will be terminated immediately.

In order for the recruitment source tracking to work you must supply the **source** parameter on the URL. Example:

```
https://domain.sampleninja.io/registration/1/ENG-CA?source=10
```

### AdBloom recruitment

In order to use **AdBloom** conversion reporting you must first enable it in the **Panel Settings** under **Integrations**. You must have an account with **AdBloom** and know your **Reporting URL** before you can enable the service. This information is available via the **AdBloom** admin interface or from your **AdBloom** representative.

Next create a **recruitment source** and enable **ADBLOOM** integration.

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
In order to use **Everflow** conversion reporting you must first enable it in the **Panel Settings** under **Integrations**. You must have an account with **Everflow** and know your **Reporting URL** before you can enable the service. This information is available via the **Everflow** admin interface or from your **Everflow** representative.

Next create a **recruitment source** and enable **Everflow** integration.

When enabled, the recruitment source ID or **source** and **Everflow** **transaction_id** URL query parameters must be provided. For example, if your standard **Registration Survey** URL looks like this:

```
https://domain.sampleninja.io/registration/1/ENG-CA
```

You need to append all the required parameters and the final URL will look like this:

```
https://domain.sampleninja.io/registration/1/ENG-CA?source=10&transaction_id=a93b5fc7d44234dab8f8
```

### ShareASale Recruitment.
In order to use **ShareASale** conversion reporting you must first enable it in the **Panel Settings** under **Integrations**.

if your standard **Registration Survey** URL looks like this:
```
https://domain.sampleninja.io/registration/1/ENG-US
```

You need to append the **source** parameter to the URL which corresponds to **Recruitment Source ID** assigned for ShareASale. The "sscid" parameter is populated by **ShareASale** and contains click ID. 

```
https://domain.sampleninja.io/registration/1/ENG-CA?source=4&sscid=31k7_182ftf
```

### TUNE Recruitment
In order to use **TUNE** conversion reporting you must first enable it in the **Panel Settings** under **Integrations**. 

Use the **Integration Partner** pulldown and select **TUNE**

When enabled, the recruitment source ID or **source** and TUNE transaction id or **transaction_id** URL query parameters must be provided. For example if your standard **Registration Survey** URL looks like this:
```
https://domain.sampleninja.io/registration/1/ENG-CA
```

You need to append the required parameters and the final URL will look like this:

```
https://domain.sampleninja.io/registration/1/ENG-CA?source=10&transaction_id=935f78f8
```

> **TUNE** must use this URL format for all the redirects they do.

Or for test mode:

```
https://domain.sampleninja.io/registration/1/ENG-CA?source=10&transaction_id=935f78f8&test=true
```
As long as the **registration survey** URL is configured in **TUNE's admin interface** these URL parameters are automatically appended when new recruits land into your registration survey.

> The **source** parameter must be a valid **Recruitment Source ID** and the **Recruitment Source** must have **TUNE** enabled.

> For more information visit https://www.tune.com

### MVF Co-registration
In order to use **MVF** co-registration you must first enable it in the **Panel Settings** under the **Integrations** -tab. You must have an account with **MVF** and know your server to server double opt-in reporting URL.

Use the **Integration Partner** pulldown to select **MVF**.

> For more information visit https://www.mvfglobal.com

When **MVF** is turned on for a **Recruitment Source** Sample Ninja expects 6 URL query parameters to be passed in:

1) **sid** MVF internal user identifier (assigned by MVF)
2) **pix** MVF internal pixel identifier (assigned by MVF)
3) **first** First name collected by MVF -> auto saved as **FIRST_NAME** -data variable.
4) **last**  Last name collected by MVF -> auto saved as **LAST_NAME** -data variable.
5) **gender** Gender collected by MVF -> auto saved as **GENDER** -data variable.
6) **email** Email address collected by MVF -> auto saved as **EMAIL** -data variable.

Let's say you have **Recruitment Source** with **ID 4** with **MVF reporting** enabled. Your base **Registration Survey** URL would look like this:

```
https://client.sampleninja.io/co-registration/mvf/1/ENG-US
```

Next append all the required query parameters to the URL:

```
?source=4&sid=12345&pix=123456&first=John&last=Doe&email=john.doe@sampleninja.io&gender=1
```

> **NOTE** The URL does not point to the registration survey, instead it points to a specific URL for co-registration! This URL is used to server to server communication between **MVF** and **Sample Ninja**

When an API request is received and validation is passed **Sample Ninja** will send a confirmation email as configured under **Sub Panels -> Email Templates -> Co-registration invitation**. When a registering panelist confirms their email, the standard security checks, fingerprinting etc.. will run.

Questions **FIRST_NAME**, **LAST_NAME**, **GENDER** and **EMAIL** are automatically answered when co-registration request is received from **MVF**. **Sample Ninja** will automatically report these as completed registration surveys, so you will have normal registration survey statistics even though these users never took the actual registration survey.

