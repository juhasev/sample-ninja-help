## Registration Surveys URLs

- Click on the **TEST** -button to take the survey in the **test mode**. 
- Click the **URL** to copy it to the clipboard.
- Click on the **REGISTER** -button to register a real panelist.

> The first link indicated with the **globe** -icon is a universal link that detects the user's country and locale automatically.

> If you run the survey in the test mode then you will see a blue **INFO** button which gives you more information on what is being collected in the background. 

> Please note that the registration survey does not register new panelists or send confirmation emails when run using the **test mode**. 

> Any registration survey link can be turned into test mode simply by appending **test** parameter at the end of registration survey URL. Example:
> ```https://mysite.sampleninja.io/registration/1/ENG-US?test```

### Recruitment sources
You can provide the recruitment source ID on the URL by providing **source** parameter on the link. Example:

```https://mysite.sampleninja.io/registration/1/ENG-US?source=1```

Or combined with the test mode

```https://mysite.sampleninja.io/registration/1/ENG-US?source=1&test```

> Source ID must match the ID of one of the **Recruitment Sources** created. The parameters can be supplied in any order.

### Providing additional data
You can provide the following variables on the url to prefill and skip.

- first = FIRST_NAME
- last = LAST_NAME
- email = EMAIL

```
https://mysite.sampleninja.io/registration/1/ENG-US?first=John&last=Doe&email=john.doe@example.com
```
> If you want to auto skip feature to work we recommend that you place these variables at the beginning your survey.

### Security checks

Be aware that all built-in security checks will be by-passed as long as you are authenticated to the admin application. If you need to test that the appropriate security checks are working, simply copy the link and paste it into a private window. Different browsers call the private windows differently. Refer to the list below if unsure what to look for. You can also paste the link into another browser that is not currently authenticated to the admin application.

- Google Chrome **New ingognito window**
- Safari **New private window**
- Edge **New inPrivate window**
