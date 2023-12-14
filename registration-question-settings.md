## Question Settings

### Capturing question data from the URL

Enter the URL parameter name you would like to capture and select if you want to hide this question from the user.

You must use the unique option values for multiple-choice questions. To view the current values, navigate to data variables, edit either radio or checkbox questions, and select **Developer Mode** from the right panel.

### Format examples:

Number: VACATION_COUNT

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
