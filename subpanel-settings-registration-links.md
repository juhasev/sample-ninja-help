## Public access URLs

You should use these URLs when you link the registration survey, for example, to your panel's marketing website.

- Click on the **TEST** -button to take the survey in the **test mode**. 
- Click the **URL** to copy it to the clipboard.
- Click on the **REGISTER** -button to register a real panelist.

> The first link indicated with the **globe** -icon is a universal link that automatically detects the user's country and locale. Please be aware that this detection is not 100% reliable as it relies on the user's IP-based geolocation + browser's configured locale. We recommend that you do not use the universal URL, unless you have no other option.

> If you run the survey in test mode, you will see a blue **INFO** button that gives you more information on what is being collected in the background. 

> Please note that the registration survey does not register new panelists or send confirmation emails when run using the **test mode**. 

> Any registration survey link can be turned into test mode simply by appending the **test** parameter at the end of the registration survey URL. Example:
> ```https://mysite.sampleninja.io/registration/1/ENG-US?test```

### Recruitment sources
You can provide the URL's recruitment source ID by providing the **source** parameter on the link. Example:

```https://mysite.sampleninja.io/registration/1/ENG-US?source=1```

Or combined with the test mode.

```https://mysite.sampleninja.io/registration/1/ENG-US?source=1&test```

> Source ID must match the ID of one of the **Recruitment Sources** created. The parameters can be supplied in any order.

### Providing additional data
You can provide the following variables on the URL to prefill and skip.

- first = FIRST_NAME
- last = LAST_NAME
- email = EMAIL

```
https://mysite.sampleninja.io/registration/1/ENG-US?first=John&last=Doe&email=john.doe@example.com
```
> If you want the auto-skip feature to work, we recommend placing these variables at the beginning of your survey.

### Security checks

Be aware that all built-in security checks will be bypassed as long as you are authenticated to the admin application. If you need to test that the appropriate security checks are working, copy the link and paste it into a private window. Different browsers call private windows differently. Refer to the list below if you need help with what to look for. You can also paste the link into another browser not currently authenticated to the admin application.

- Google Chrome **New ingognito window**
- Safari **New private window**
- Edge **New inPrivate window**
