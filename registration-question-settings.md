## Question Settings

### Capturing question data from the URL

Enter the URL parameter name you would like to capture and select if you want to hide this question from the user.

You must use the unique option values for multiple-choice questions. To view the current values, navigate to data variables, edit either radio or checkbox questions, and select **Developer Mode** from the right panel.

> You cannot hide "EMAIL" question from the user. This is because the email address goes through server-side validations like is the email address blacklisted.

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

Let's add the third URL Param: **bday** Data Variable: **BIRTHDATE** (date)

```
https://sampleninja.app/registration/1/ENG-US?scr_id=123456&gender=1&hobbies=3,5,7&bday=1982-10-25
```
