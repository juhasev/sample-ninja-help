## Question Settings

### Capturing question data from the URL

Enter the URL parameter name you would like to capture and select if you want to hide this question from the user.

You must use the unique option values for multiple-choice questions. To view the current values, navigate to data variables, edit either radio or checkbox questions, and select **Developer Mode** from the right panel. For checkbox questions, separate the values with commas.

> You cannot hide "EMAIL" question from the user. This is because the email address goes through server-side validations like is the email address blacklisted.

> You must enter a URL parameter name before you can hide the question.

> Some parameter names are used by the system and cannot be used, for example `source` and `affiliate_id`.

#### What the user sees

- **Question not hidden:** the question is shown pre-answered with the value from the URL, and the user can change it. If the parameter is missing, the question is asked normally.
- **Question hidden and required:** the parameter is mandatory. If it is missing or empty, the registration stops with a red error page that says "URL Param (name) not provided!".
- **Question hidden and not required:** if the parameter is missing or empty, the question is skipped and left unanswered.

> A condition on the question still applies. If the condition is not met, the question is skipped and the value from the URL is not saved.

> If you hide FIRST_NAME or LAST_NAME, always send its URL parameter. If the value is missing, the registration fails, either at the start with the red error page or when the panelist submits it at the end.

> A value that is not valid stops the registration with a red error page, whether the question is hidden or not. For example, an option value that does not exist, or a date that is not in the YYYY-MM-DD format.

> In **test mode** (a registration link with the **test** parameter), URL parameter errors do not stop the registration, so you will not see the red error page.

#### Example use case.

Capture metadata from the pre-screener survey without displaying that information to the user.

Let's add the first URL Param: **scr_id** Data Variable: **SCREENER_ID** (numeric)

```
https://sampleninja.app/registration/1/ENG-US?scr_id=123456
```

Let's add the second URL Param: **gender** Data Variable: **GENDER** (radio)

```
https://sampleninja.app/registration/1/ENG-US?scr_id=123456&gender=1
```

Let's add the third URL Param: **hobbies** Data Variable: **HOBBIES** (checkbox)

```
https://sampleninja.app/registration/1/ENG-US?scr_id=123456&gender=1&hobbies=3,5,7
```

Let's add the fourth URL Param: **bday** Data Variable: **BIRTHDATE** (date)

```
https://sampleninja.app/registration/1/ENG-US?scr_id=123456&gender=1&hobbies=3,5,7&bday=1982-10-25
```
