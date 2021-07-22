## Panelist Importer

Panelist Importer let’s you to import panelists (members) to an existing panel or subpanel from a CSV file.

You must have FIRST_NAME, LAST_NAME and EMAIL columns in your CSV file. Technically you cannot import into any data variables that are not owned by the system with the exception of

- POINTS_BALANCE
- LOCALE
- SUBSCRIBED_DATE
- EMAIL_CONFIRMED
- RECRUITMENT_SOURCE

> You can view a list of importable variables in **Data Variables** but selecting **Registration / Import writable** -class.

> **RECRUITMENT_SOURCE** must be one of the defined under **Recruitment Sources** menu item.

> **BIRTH_DATE** variable is automatically checked against **minimum age to join** settings found in the **Sub Panel settings**.

> **LOCALE** must exists in the targeted sub panel or line will fail. Locales must be specified in format **ENG-US**.

## Getting started with your own import

The easiest way to get started is to produce a test import file by clicking **GENERATE TEST IMPORT FILE**. This little tool let's you pick data variables that you would like to import. When you prepare your own import file simply follow the test import file format.

> **IMPORTANT!** Do not import the file back in unless your panel is in the **SIMULATION MODE**. This is indicated on the application top toolbar with label **SIMULATION**

## Preparing your own data file

### Blank / NULL / unknown values
If a panelist doesn't have value for example BIRTH_DATE you may leave the value blank. If the target variable type is **checkbox** then all columns must be left blank. For example:

```
FIRST_NAME,LAST_NAME,EMAIL,BIRTH_DATE,BREXIT:Yes,BREXIT:No
John,Doe,john@sampleninja.io,1980-01-01,0,1                    <-- GOOD LINE
Lisa,Doe,lisa@sampleninja.io,,1,0                              <-- BIRTH DATE BLANK
Jack,Doe,jack@sampleninja.io,1966-04-12,,                      <-- BLANK CHECKBOX
```

### Data formats
The importer access only values in the international formats

#### Text
In SampleNinja the text variables are tokenized and analyzed allowing you to store various kind of text data if desired.

For example if you store: "Brown lazy dog" you could then later search for matches like "Brown dog". This may not be what you want and if you need to match the whole term you should use the **Keyword** data variable type instead.

#### Date
All dates must be imported in format 2021-07-22 or YYYY-MM-DD.

#### Phone
All phone numbers must be in the international format for example US number (512) 670-4444 needs to be converted to +15126564444.

#### Checkbox
Checkbox columns must be noted with target variable name followed by the option label. Checked options are noted with 1 and unchecked options are noted with 0. For example:

```
BREXIT:yes,BREXIT:no
1,0
```

#### Radio
Data values must correspond to option number i.e. GENDER -> Male -> 1

### Data type detection and how it affects mapping

The importer scans each column and attempt to discover the CSV data type and the potential target data variable types. The detection runs in the following order: 

```javascript
[
    {
        csvDataType: 'Date',
        targetVariableTypes: ['date']
    },
    {
        csvDataType: 'Phone',
        targetVariableTypes: ['phone', 'keyword']
    },
    {
        csvDataType: 'Integer',
        targetVariableTypes: ['radio', 'checkbox', 'number', 'keyword', 'text']
    },
    {
        csvDataType: 'Numeric',
        targetVariableTypes: ['number', 'keyword', 'text'],
    },
    {
        csvDataType: 'Email',
        targetVariableTypes: ['email', 'keyword'],
    },
    {
        csvDataType: 'Locale',
        targetVariableTypes: ['locale', 'keyword']
    },
    {
        csvDataType: 'ZipCode',
        targetVariableTypes: ['keyword', 'number'],
    },
    {
        csvDataType: 'String',
        targetVariableTypes: ['text', 'keyword'],
    }
]
```
This generates list of potential target variable types and if the target data variable **LABEL** matches the **CSV COLUMN HEADER** then the imported will map the CSV column to the data variable automatically. 

> If you don't see your variable listed under the mapping selection then either the data is provided in the wrong format or the data variable you are trying to map to is using a wrong type. Please verify your data format and the desired target variable type.

## Using the importer

### 1.	Select file to import

Click on the designated area and select a file to import or simply locate the file on your device and drag & drop it into the drop zone indicated by a dashed line.

### 2.	Inspection

Here you’ll be able to visually inspect the first 100 records of your CSV file for any obvious errors. At the bottom of this screen you can also change the number records or rows per page shown. 

Once you have completed inspecting your file, you can either click the **Restart** button at the bottom of the page to re-start the import process or click **Next let’s map your data** -button to continue.

### 3.	Mapping

The system will attempt to automatically map all columns in the import file to a variables in the system with the same names, provided that such a variable exists. The variables or columns in the import file are shown on the left hand-side of window and the matching variable in the system on the right-hand side.

If the system cannot auto-map a variable you have the options of either: 

1.	Manually mapping to a variable in the system by selecting from the list of available variables in the dropdown list, or 
2.	Leaving this variable out in the import by clicking on **ignore this column** button.

If the later is chosen, the variable in question will be skipped and left out from the import. 
Where there are missing values or validation failures a warning message is displayed against the variable in question. For more detailed inspection of the error, simply click on the error text.

### 4.	Upload

You can assign or specify the following before clicking the **Upload** button:

1.	Target sub panel 
2.	Locale
3.	Recruitment source
4.	Subscribed date

> You can provide **LOCALE**, **RECRUITMENT_SOURCE** and **SUBSCRIBED_DATE** for each individual panelists if desired. If the importer encounters any blank or missing values then the values you selected here will be used. You may also omit these columns completely from your CSV file.

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
