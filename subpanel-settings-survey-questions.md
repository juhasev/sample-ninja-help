## Registration Survey Questions

This is where you control which registration questions are asked and in which order. A registration survey must always include FIRST_NAME, LAST_NAME, and EMAIL. To select more questions, click on **SELECT QUESTIONS** button. You can re-order the questions simply by grabbing the drag handle and moving them around. You can also EDIT and DELETE questions directly from here.

### Conditional questions

Registration surveys now support ‘Radio’ -question-based conditional logic. 

Insert question conditions by clicking the **C** -icon on each question and then choosing the applicable data variable from the popup menu. 

> For example, you could conditionally ask for more details about pet ownership if a panelist has indicated they own pets. 

The question will be displayed to the registering panelist if the condition is satisfied.

> Taking the above example, if a data variable such as **ALLERGIES** has been conditionally linked to the variable of **PETS**, the allergy question will be shown when a panelist has stated they own pets.

The number of conditions that can be added is unlimited. One question can have multiple conditions, and similarly, each subsequent question can have a condition. Questions can still be dragged and dropped in any order. However, please remember that a conditional question cannot come before the question it is linked to.

> Using the following as an example; **INCOME** and **INDUSTRY** can both be conditionally linked to **EDUCATION** or **INCOME** can be conditionally linked to **EDUCATION** and **INDUSTRY** can be conditionally linked to **INCOME**. The question order in both scenarios would be education > income > industry. Both the question for income and the question for industry would appear before the question for education.

At this stage, conditions can only be applied to ‘Radio’ based questions. So while ‘Text,’ ‘Keyword,’ ‘Number,’ etc data variables can be conditionally linked to ‘Radio’ data variables, the aforementioned variables can not be conditionally linked with other variable types. 

> For example, **COUNTRY** (Keyword) can be conditionally linked to **EDUCATION** (Radio), but this would not work in reverse. Similarly, **PHONE** (Number) cannot be conditionally linked to **FIRST_NAME** (Text), nor would this work vice versa.

Anytime questions are added, please ensure the necessary translation has been supplied. Otherwise, the registration survey may become unavailable for locales without translations. 

> Questions that are missing translations are marked with the warning icon.

### Disqualifying and exclusive options (radio & checkbox)
To see the choice options, click on the arrow-down indicator. You can designate options as disqualifying factors for both radio and checkbox. In addition, you can specify exclusive options for the checkbox question type.

### Populating questions from URL parameters
Click on the gear icon to modify question settings. Enter the URL parameter name. For example, if you want to populate the GENDER data variable from the URL, enter "g" or "gender" as the URL parameter name. You may also hide the question from the user by toggling **Hide question** on.

> **IMPORTANT** If you do not hide the question, it will be presented to the user pre-answered.

> **IMPORTANT** If you hide the question, it becomes a mandatory URL parameter if the question is required. Any missing parameters lead to a hard stop and a red screen. Please make sure that if you pass data in, you always have a value for the URL parameters. Sending empty or NULL values will lead to a hard error. If you want to avoid hard errors, you can set the question as not required.
 
To send a male respondent to your registration survey, the URL would take the following form:

```
https://myinstall.panelservice.io/registration/1/ENG-US?gender=1
```

You must separate URL parameters using the "&" character to add more URL parameters. For example:

```
https://myinstall.panelservice.io/registration/1/ENG-US?gender=1&education=4
```
> The URL parameters must be properly encoded. https://www.w3schools.com/tags/ref_urlencode.ASP

> A missing URL parameter is silently ignored if you do not require an answer to the question. Click on the R -icon to toggle on/off.

> **IMPORTANT:** If you are bringing in radio and checkbox data, you must use Unique IDs (punch) instead of Option IDs (option order). Please visit **Data Variables -> Edit radio/checkbox -> Toggle on developer mode**. Alternatively, you can download **Codebook** from the **Data Variables** list view.

### Localizations
Data variables must be provided with proper localizations when you use data variables as a question. For example, if you have two Sub Panel locales, ENG-US and SPA-US, you must provide localizations for both locales using the **EDIT** button.

> If you are missing localizations, an orange triangle will show up by the question name.

### Answer validation
Sample Ninja includes multiple validators that can be used to validate user-provided input. For example, if you are asking for a zip code, you can set the following validators for the question:

- Minimum length 5
- Maximum length 5
- Numeric characters only

Click the **EDIT** button and switch to the **VALIDATORS** tab to view validators. This tab contains detailed help on configuring validators.

### Password and locale
If **Create Password** is enabled in the settings, Sample Ninja will ask a user to create a password at the registration survey. Similarly, **LOCALE** data variable is automatically detected and populated.
