## Registration Survey Questions

This is where you control which registration questions are asked and in which order. A registration survey must always include FIRST_NAME, LAST_NAME, and EMAIL, and these three questions cannot be deleted. To add more questions, click the **SELECT QUESTIONS** button. Only data variables that panelists can answer are listed. You can re-order the questions by grabbing the drag handle and moving them around.

Click the pencil icon to edit the data variable behind a question, and the trash icon to remove the question from the survey.

> The pencil icon edits the data variable itself. Changes to its texts, options, and validators apply everywhere that data variable is used, not only in this registration survey.

### How panelists see the survey

- The survey shows one question per screen. Two questions cannot be combined on the same screen.
- The question text is shown exactly as it is entered in the data variable translations. An answer to an earlier question cannot be inserted into the text of a later question.
- A radio or checkbox option cannot have its own text box. To collect an "Other, please specify" answer, add a Text question right after the radio question and give it a condition on the "Other" option (see **Conditional questions** below). The text question is then shown on the next screen, only to panelists who picked "Other". This works only when the radio question has no condition of its own.
- Questions that are not required show a **Skip** button.
- When a panelist uses the **Back** button, the question they return to keeps its answer, but every question they go back past is cleared. For example, if a panelist goes back two screens and then forward again, the question in between is empty and must be answered again.
- After the last question, the panelist creates a password if **Create Password** is enabled, and completes the Google reCaptcha if it is enabled. These steps are shown as grey rows below the questions.

### Conditional questions

A condition shows a question only to panelists who picked certain options in an earlier question.

To add a condition, click the **C** icon on the question. Choose the question the condition depends on (the target question), tick one or more of its options, and click **APPLY**. The question is shown when the panelist picked **any** of the ticked options. To delete a condition, open it again and click **REMOVE CONDITION**.

> For example, you could conditionally ask for more details about pet ownership if a panelist has indicated they own pets. If **ALLERGIES** has a condition on **PETS** with the option "Yes" ticked, the allergy question is shown only to panelists who said they own pets.

These rules apply to conditions:

- The target question must be a Radio or Checkbox question placed above the question you are editing.
- Each question can have one condition, which points to one target question. Several questions can have a condition on the same target question.
- Any type of question can have a condition, for example Text, Number, Date, Radio, or Checkbox.
- Conditions cannot be chained. A question that has a condition cannot be a target question, and a question that is already a target question cannot get a condition.
- FIRST_NAME, LAST_NAME, and EMAIL cannot have a condition. Apart from these three, the first question in the list cannot have a condition either.
- Keep a question with a condition below its target question. When you drag questions, a move that would put any question with a condition above its target question is reverted.

> For example, **INCOME** and **INDUSTRY** can both have a condition on **EDUCATION**. The question order is then EDUCATION first, followed by INCOME and INDUSTRY. Giving INDUSTRY a condition on INCOME while INCOME has a condition on EDUCATION is not possible.

A target question is handled differently from other questions:

- It is made required automatically, and it cannot be made optional while a condition points to it.
- It cannot be deleted while a condition points to it. Remove the condition first.

When a panelist reaches a question with a condition and did not pick any of the ticked options, the question is skipped and its answer is left empty.

Anytime questions are added, please ensure the necessary translation has been supplied. Otherwise, the registration survey is not available for locales without translations.

> Questions that are missing translations are marked with the warning icon.

### Disqualifying and exclusive options (radio & checkbox)

To see the choice options, click on the arrow-down indicator on the left of the question. Click the **D** icon on an option to make it disqualifying. For checkbox questions, click the **E** icon on an option to make it exclusive.

- **Disqualifying options** work for both radio and checkbox questions. A panelist who picks a disqualifying option still answers the remaining questions. At the end, the registration is submitted without the password and reCaptcha steps, and the panelist is shown the **Registration disqualified** landing page. No panelist is created. Disqualifying options are saved for this registration survey only.
- **Exclusive options** work for checkbox questions only. When a panelist ticks an exclusive option, all other options are unticked. When they tick another option, the exclusive option is unticked.

> Exclusive is a setting of the data variable option itself. It applies everywhere that data variable is used, not only in this registration survey.

### Populating questions from URL parameters

Click on the gear icon to modify question settings. Enter the URL parameter name. For example, if you want to populate the GENDER data variable from the URL, enter "g" or "gender" as the URL parameter name. You may also hide the question from the user by toggling **Hide question** on.

- You must enter a URL parameter name before you can hide a question.
- The EMAIL question cannot be hidden.
- Some parameter names are used by the system and cannot be used, for example `source` and `affiliate_id`.

> **IMPORTANT** If you do not hide the question, it will be presented to the user pre-answered. The user can still change the answer. A condition on the question still applies: if the condition is not met, the question is skipped and the value from the URL is not saved.

> **IMPORTANT** If you hide the question and the question is required, the URL parameter becomes mandatory. When the parameter is missing or empty, the registration stops with a red error page that says "URL Param (name) not provided!". If you want to avoid this, you can set the question as not required. FIRST_NAME, LAST_NAME, EMAIL, and target questions of a condition are always required.

> **IMPORTANT** If you hide FIRST_NAME or LAST_NAME, always send its URL parameter. If the value is missing, the registration fails, either at the start with the red error page or when the panelist submits it at the end.

To send a male respondent to your registration survey, the URL would take the following form:

```
https://myinstall.panelservice.io/registration/1/ENG-US?gender=1
```

You must separate URL parameters using the "&" character to add more URL parameters. For example:

```
https://myinstall.panelservice.io/registration/1/ENG-US?gender=1&education=4
```
> The URL parameters must be properly encoded. https://www.w3schools.com/tags/ref_urlencode.ASP

> A missing or empty URL parameter is silently ignored when the question is not hidden, or when it is hidden but not required. Click on the R -icon to toggle required on/off.

> **IMPORTANT** A URL parameter value that is not valid stops the registration with a red error page, even when the question is not hidden and not required. For example, an option ID that does not exist, or a date that is not in the YYYY-MM-DD format.

> In **test mode** (a registration link with the **test** parameter), URL parameter errors do not stop the registration, so you will not see the red error page.

> **IMPORTANT:** If you are bringing in radio and checkbox data, you must use Unique IDs (punch) instead of Option IDs (option order). For checkbox data, separate the Unique IDs with commas, for example `hobbies=3,5,7`. Please visit **Data Variables -> Edit radio/checkbox -> Toggle on developer mode**. Alternatively, you can download **Codebook** from the **Data Variables** list view.

### Localizations
Data variables must be provided with proper localizations when you use data variables as a question. For example, if you have two Sub Panel locales, ENG-US and SPA-US, you must provide localizations for both locales using the pencil icon.

> If you are missing localizations, an orange triangle will show up by the question name. The registration page for a locale with a missing translation shows an error message instead of the survey.

### Answer validation
Sample Ninja includes multiple validators that can be used to validate user-provided input. For example, if you are asking for a zip code, you can set the following validators for the question:

- Minimum length 5
- Maximum length 5
- Numeric characters only

Click the pencil icon and switch to the **VALIDATORS** tab to view validators. This tab contains detailed help on configuring validators.

> Validators, including **Required**, belong to the data variable. They apply everywhere that data variable is used, for example in Dynamic Profiling.

### Password and locale
If **Create Password** is enabled in the settings, Sample Ninja will ask a user to create a password at the end of the registration survey. Similarly, the **LOCALE** data variable is filled automatically with the locale of the registration page.
