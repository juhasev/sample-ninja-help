## Registration Survey Questions

This is where you control which registration questions are asked and in which order. A registration survey must always include FIRST_NAME, LAST_NAME, and EMAIL. To select more questions, click on **SELECT QUESTIONS** button. You can re-order the questions simply by grabbing the drag handle and moving them around. You can also EDIT and DELETE questions directly from here.

### Conditional Questions

Registration surveys now support ‘Radio’ -question-based conditional logic. 

Insert question conditions by clicking the **C** -icon on each question and then choosing the applicable data variable from the popup menu. 

> For example, you could conditionally ask for more details about pet ownership if a panelist has indicated they own pets. 

If the condition is satisfied, the question will be displayed to the registering panelist.

> Taking the above example, if there is a data variable such as **ALLERGIES** which has been conditionally linked to the variable of **PETS**, the question regarding allergies will be shown when a panelist has stated they own pets.

There are no limitations to the number of conditions that can be added, i.e., one question can have multiple conditions, and similarly, each subsequent question can have a condition. Questions can still be dragged and dropped in any order. However, please keep in mind that a conditional question cannot come before the question it is linked to.

> Using the following as an example; **INCOME** and **INDUSTRY** can both be conditionally linked to **EDUCATION** or **INCOME** can be conditionally linked to **EDUCATION** and **INDUSTRY** can be conditionally linked to **INCOME**. The question order in both scenarios would be education > income > industry. Both the question for income and the question for industry would appear before the question for education.

At this stage, conditions can only be applied to ‘Radio’ based questions. So while ‘Text,’ ‘Keyword,’ ‘Number,’ etc data variables can be conditionally linked to ‘Radio’ data variables, the aforementioned variables can not be conditionally linked with other variable types. 

> For example, **COUNTRY** (Keyword) can be conditionally linked to **EDUCATION** (Radio), but this would not work in reverse. Similarly, **PHONE** (Number) cannot be conditionally linked to **FIRST_NAME** (Text), nor would this work vice versa.

Anytime questions are added, ensure the necessary question translation has been supplied. Otherwise, the registration survey may become unavailable for some locales. 

> Questions that are missing translations are marked with the warning icon.

### Trap questions
You can designate any question as a trap question. The trap question could be something like that:

Which flavored drinks have you consumed in the past year? Please read the answer options carefully and select only the items that apply.
- Coca Cola
- Gatorade
- RC Cola (disqualify)
- Dr. Pepper
- Coords Heavy (disqualify)
- Budweiser
- Engine Coolant (disqualify)
- Red Bull
- Discoteque Energy Drink (disqualify)
- Red Wine
- Water
- Cool Juice (disqualify)
- Rockstar
- Anthrax Liquor (disqualify)
- Monster
- Chocolate milk
- Rocky Mountain Urine (disqualify)
- Clorox (disqualify)
- Star Dollar Coffee (disqualify)
- Diet Pepsi
- Urine Light XL (disqualify)
- Fanta
- Glass Cleaner (disqualify)
- Mountain Dew
- Restroom Delight (disqualify)
- Sprite or Diet Sprite
- Gym Sweat Seltzer (disqualify)
- Poisonous Juice (disqualify)
- Dunkin Donuts Coffee
- Sunny Delight
- Alaskan Orange Juice (disqualify)
- Florida's Best
- Diesel (disqualify)
- Break Fluid DOT 4.0 (disqualify)
- None of the above (Exclusive) (disqualify)

### Choice options (radio & checkbox)
You can designate options as disqualifying factors for both radio and checkbox. In addition, you can specify exclusive options for the checkbox question type. Click to the down arrow to expand and see the multiple choice options.

### Localizations
Data variables must be provided with proper localizations when you use data variables as a question. For example, if you have two Sub Panel locales, ENG-US and SPA-US, you must provide localizations for both locales using the **EDIT** button.

> If you are missing localizations, an orange triangle will show up by the question name.

### Answer Validation
Sample Ninja includes multiple validators that can be used to validate user-provided input. For example, if you are asking for a zipcode, you can set the following validators for the question:

- Minimum length 5
- Maximum length 5
- Numeric characters only

Click **EDIT** button and switch to **VALIDATORS** tab to view validators. This tab contains mode detailed help on how to configure validators.

> All questions in the registration survey are automatically required. So, you don't need to set up **REQUIRED** validator. Similarly, any email and date-type data variables are automatically validated.

### Password and Locale
If **Create Password** is enabled in the settings, Sample Ninja will ask a user to create a password at the registration survey. Similarly, **LOCALE** data variable is automatically detected and populated.
