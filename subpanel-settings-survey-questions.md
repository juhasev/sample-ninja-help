## Registration Survey Questions

This is where you control which registration questions are asked and in which order. A registration survey must always include FIRST_NAME, LAST_NAME and EMAIL. To select more questions click on **SELECT QUESTIONS** button. You can re-order the questions simply by grabbing the drag handle and moving them around. You can also EDIT and DELETE questions directly from here.

### Conditional Questions

Registration surveys now support ‘Radio’ -question based conditional logic. 

Simply insert question conditions by clicking the **C** -icon on each question and then choosing the applicable data variable from the pop up menu. 

> As an example, you could conditionally ask more details about pet ownership if a panelist has indicated they own pets. 

If the condition is satisfied then the question will be displayed to the registering panelist.

> Taking the above example, if there is a data variable such as **ALLERGIES** which has been conditionally linked to the variable of **PETS**; then when a panelist has stated they own pets, the question regarding allergies will be shown.

There are no limitations to the number of conditions that can be added i.e. one question can have multiple conditions and similarly each subsequent question can have a condition. Questions can still be dragged and dropped in any order, however please note that a conditional question cannot come before the question it is linked to.

> Using the following as an example; **INCOME** and **INDUSTRY** can both be conditionally linked to **EDUCATION** or **INCOME** can be conditionally linked to **EDUCATION** and **INDUSTRY** can be conditionally linked to **INCOME**. In both these scenarios the question order would be education > income > industry. Neither the question for income nor the question for industry would appear before the question for education.

At this stage conditions can only be applied to ‘Radio’ based questions. So while ‘Text’, ‘Keyword’, ‘Number’ etc data variables can be conditionally linked to ‘Radio’ data variables, currently the aforementioned variables can not be conditionally linked with other variable types. 

> For example, **COUNTRY** (Keyword) can be conditionally linked to **EDUCATION** (Radio) but this would not work in reverse. Similarly, **PHONE** (Number) cannot be conditionally linked to **FIRST_NAME** (Text), nor would this work vice versa.

Anytime questions are added, ensure that the necessary question translation has been supplied, otherwise the registration survey may become unavailable for some locales. 

> Questions that are missing translations are marked with the warning icon.

### Localizations
When you use data variables as question they must be provided proper localizations. For example if you have two Sub Panel locales ENG-US, SPA-US you must provide localizations for both locales using the **EDIT** button.

> If you are missing localizations an orange triagle will show up by the question name.

### Answer Validation
Sample Ninja includes multiple validators that can be used validating user provided input. For example if you are asking for zip code you can setup the following validators for the question:

- Minimum length 5
- Maximum length 5
- Numeric characters only

Click **EDIT** button and switch to **VALIDATORS** tab views validators. This tab contains mode detailed help how to configure validators.

> All questions in the registration survey are automatically required, therefore there is no need to setup **REQUIRED** validator. Similary any email and date -type data variables are automatically validated.

### Password and Locale
Sample Ninja will always ask user to create a secure password at the end of the registration survey. Similarly **LOCALE** data variable is automatically detected and populated.
