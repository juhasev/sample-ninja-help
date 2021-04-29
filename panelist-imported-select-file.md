## Panelist Importer

Panelist Importer let’s you to import panelists (members) to an existing panel or subpanel from a CSV file.

You must have FIRST_NAME, LAST_NAME and EMAIL columns in your CSV file. Technically you cannot import into any data variables that are not owned by the system with the exception of

- POINTS_BALANCE
- LOCALE
- SUBSCRIBED_DATE
- EMAIL_CONFIRMED
- RECRUITMENT_SOURCE

These values cannot be modified once imported!

> You can view a list of importer writable variables in **Data Variables** but selecting **Registration / Import writable** as class

> **RECRUITMENT_SOURCE** must be one of the defined under **Recruitment Sources** menu item.

> If you import BIRTH_DATE variable the system will automatically check it against **minimum age to join** settings found in the **Sub Panel settings**.

## Getting started with your own import

The easiest way to get started is to produce a test import file by clicking **GENERATE TEST IMPORT FILE**. This little tool let's you pick data variables that you would like to import. When you prepare your own import file simply follow the test import file format.

> **IMPORTANT!** Do not import the file back in unless your panel is in the **SIMULATION MODE**. This is indicated on the application top toolbar with label **SIMULATION**

### Import process

1. Select file to import 
2. Inspection 
3. Mapping
4. Upload
5. Results

### 1.	Select file to import

Click on the designated area and select a file to import or simply locate the file on your device and drag & drop it into the drop zone indicated by a dashed line.

### 2.	Inspection

Here you’ll be able to visually inspect the first 100 records of your CSV file for any obvious errors. At the bottom of this screen you can also change the number records or rows per page shown. 

Once you have completed inspecting your file, you can either click the ‘Restart’ button at the bottom of the page to re-start the import process or click ‘Next let’s map your data’ button to continue.

### 3.	Mapping

The system will attempt to automatically map all variables/ columns in the import file to a variable in the system with the same name, provided that such a variable exists. 
The variables or columns in the import file are shown on the left hand-side of window and the matching variable in the system on the right-hand side.
Where the system cannot auto-map a variable you have the options of either: 

1.	manually mapping to a variable in the system by selecting from the list of available variables in the dropdown list, or 
2.	leaving this variable out in the import by clicking on ‘ignore this column’ button.
If the later is chosen, the variable in question will be skipped and left out from the import. 
Where there are missing values or validation failures a warning message is displayed against the variable in question. For more detailed inspection of the error, simply click on the error text.

### 4.	Upload

You can assign or specify the following before clicking the ‘Upload’ button:
1.	Target sub panel 
2.	Locale
3.	Recruitment source
4.	Join date

> You can provide LOCALE, RECRUITMENT_SOURCE and SUBSCRIBED_DATE variables for each individual panelists. If the importer encounters any blank or missing values then the default values provided will be used.

### 5.	Results

The result of the outcome of the upload is displayed here. You can see how many panelists were successfully imported and similarly the number of panelists that couldn’t be imported. Any errors are highlighted in red. If you mouse over the error items you will see more details description of the error.

If you import contains any errors the system will automatically generate an results file containing all the CSV lines with errors and explanation how to fix. This file is automatically placed in your downloads. Select **Downloads** from the main menu to go to downloads or click on the **Downloads** -button in the importer results screen. 

> Use the results file to iteratively fix issues. Download the file and fix the indicated issues. You can re-import the results file with the error comments in place!

Example results file:

```csv
"BIRTH_DATE","EMAIL","FIRST_NAME","LAST_NAME","RECRUITMENT_SOURCE","POINTS_BALANCE"
# BIRTH_DATE: Panelist does not meet the minimum age requirement to join
# RECRUITMENT_SOURCE: Valid values are 1,2,3,5
"2021-03-23","john@hotmail.com","Jailyn","Preston",6,2000
# EMAIL: Skipped existing panelist
"1980-03-29","doe@hotmail.com","Charity","Paige",2,1000
```
