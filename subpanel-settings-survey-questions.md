## Registration survey questions

This is where you control which registration questions are asked in which order. A registration survey must always include FIRST_NAME, LAST_NAME and EMAIL. To select more questions click on **SELECT QUESTIONS** button. You can reorder the questions simply by grabbing the drag handle and moving them around. You can also EDIT and DELETE questions directly from here.

### Localizations
When you use data variables as question they must be provided proper localizations. For example if you have two Sub Panel locales ENG-US, SPA-US you must provide localizations for both locales using the **EDIT** button.

> If you are missing localizations an orange triagle will show up by the question name.

### Answer validation
Sample Ninja includes multiple validators that can be used validating user provided input. For example if you are asking for zip code you can setup the following validators for the question:

- Minimum lenght 5
- Maximum length 5
- Numeric characters only

Click **EDIT** button and switch to **VALIDATORS** tab enable validators.

> All questions in the registration survey are automatically required, therefore there is no need to setup **REQUIRED** validator. Similarly if you asking for **EMAIL** Sample Ninja will validate that automatically.

### Password and locale
Sample Ninja will always ask user to create a secure password at the end of the registration survey. Similarly **LOCALE** data variable is automatically detected and populated.
