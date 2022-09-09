## Panelist Importer

Panelist Importer let’s you to import new panelists to your panel from a CSV file or you can use the importer to update existing panelist profiles.

### When importing new panelists
You must have column **EMAIL**, **FIRST_NAME** and **LAST_NAME** columns in your CSV file. Sample Ninja's **system variables** cannot be written to with the exception of:

```
- POINTS_BALANCE      <-- Allows you to bring in the existing points balance
- LOCALE              <-- Allows you to set locale if you existing panel contains multiple locales
- SUBSCRIBED_DATE     <-- Set the actual subscribed date when the panelist signed up
- RECRUITMENT_SOURCE  <-- Allows you to specify recruitment source ID
```

The first column should always be **EMAIL**.

> You can view a list of importable variables in **Data Variables** by selecting **Registration / Import writable** from the **Filter by class** select at the top right corner.

> **RECRUITMENT_SOURCE** must be one of the choices defined under **Recruitment Sources** menu item.

> **BIRTH_DATE** variable is automatically checked against **minimum age to join** settings found in the **Sub Panel settings**.

> **LOCALE** must be in format ENG-US for US English or SPA-US for US Spanish. For the complete list of locales visit **Locales** from the main menu. 

### Importing STATE or PROVINCE
**Sample Ninja** has magic variable called **REGION** and it should be used for states and provinces instead of using home grown **STATE** or **PROVINCE** variables. The magical **REGION** can be automapped using IP address location or **POSTAL_CODE** to **REGION** mapping.

### When updating panelists

Your CSV file should have column **IDENTIFIER** as the first column and that should contain an existing panelist ID. When updating please switch on "Update existing panelists" -toggle.

> You cannot update any system variables i.e. **POINTS_BALANCE** or **LOCALE**.

## Getting started with your import

### When importing panelists
The easiest way to get started is to produce a test import file by clicking **GENERATE TEST IMPORT FILE**. This little tool let's you pick data variables that you would like to import. When you prepare your own import file simply follow the test import file format.

> **IMPORTANT!** Do not import the file back in unless your panel is in the **SIMULATION MODE**. This is indicated on the application top toolbar with label **SIMULATION**.

### When updating panelists
You can export your existing panelists to a CSV file by using the **Panelist Manager** where you use any query filter to find the segment you need and select which data variables you need to export.

## Preparing your own data file

### Cleaning your data
It is imperative that you spend significant time cleaning up your import file. **Sample Ninja** uses strict validation on all values and prevents you from importing garbage in your database. For example if you have previously collected car make and have values like:

- Toyota
- toyota
- tyoota

In your data file these will be all considered different car makes in **Sample Ninja** when stored to the keyword type -variable. In additional you should make sure your value set does not contain other garbage like values that read NULL.

Pay attention to the values that are stored as Keywords in **Sample Ninja**. Examples:

```
POSTAL_CODE: 45455   <-- OK
POSTAL_CODE: 4546    <-- Invalid US postal CODE
POSTAL_CODE: A1A 1A1 <-- OK Canada
POSTAL_CODE: A2B2C1  <-- Invalid Canada
POSTAL_CODE: a1a 1a1 <-- Should be upper case
REGION: Texas        <-- OK
REGION: TX           <-- Use full keywords not abbreviations
CITY: los angeles    <-- Capitalization incorrect
CITY: NULL         <-- Do not use NULL values, leave values blank instead
```

### CSV Headers
Always use CSV headers that match the target variable name. **Sample Ninja** can automatically map these to your variables. Makes life easier!

### Minimum requirements
When importing new panelist variables **FIRST_NAME**, **LAST_NAME** and **EMAIL** are always required. When updating panelists **IDENTIFIER** is always required.

### Blank / NULL / unknown values
If a panelist doesn't have a value, (for example BIRTH_DATE), you may leave the value blank. If the target variable type is **checkbox** then all columns must be left blank. For example:

```
FIRST_NAME,LAST_NAME,EMAIL,BIRTH_DATE,COLORS:blue,COLORS:Brown,COLORS:Red
John,Doe,john@sampleninja.io,1980-01-01,0,1,1                              <-- OK ALL VALUES SUPPLIED
Lisa,Doe,lisa@sampleninja.io,,1,0,1                                        <-- OK BIRTH DATE OMITTED
Jack,Doe,jack@sampleninja.io,1966-04-12,,,                                 <-- OK CHECKBOX OMITTED
Jack,Doe,jack@sampleninja.io,1966-04-12,,,1                                <-- BAD, ALL CHECKBOX COLUMNS MUST BE PRESENT
```

### Data formats

#### Text
In SampleNinja the text variables are tokenized and analyzed allowing you to store various kind of text data if desired.

For example if you store: "Brown lazy dog" you could then later search for matches like "Brown dog". This may not be what you want and if you need to match the whole term you should use the **Keyword** data variable type instead.

#### Keyword
The keyword variable type requires exact match when searching. This variable type is the best choice for things like Car Make & Model, City, Region etc... Keyword is case sensitive.

#### Date
All dates must be imported in the international format i.e. **2021-07-22** or **YYYY-MM-DD**. As an incorrect example, if you use the US date notation 7/31/1976, this will not be detected as a date and you will not be able to map it to **Date** -data variable type.

#### Phone
All phone numbers must also be in the international format. For example, US number (512) 670-4444 needs to be converted to +15126564444. If you are storing a phone number for reference only and don't plan to use SMS functions then you can also use the **Keyword** type.

#### Checkbox
Checkbox columns must be noted with target variable name followed by the option label. Checked options are noted with 1 and unchecked options are noted with 0. For example:

```
BREXIT:yes,BREXIT:no
 1,0

```

#### Radio
Data values must correspond to option number i.e. GENDER -> Male -> 1. You can see the option values by editing the data variable in question.

#### Locale
Locale must exist in the targeted sub panel or line will fail. Locales must be specified in the correct format i.e. **ENG-US**. In additional your target **Sub Panel** must have the locale enabled.

### Excel Data Formatting
In order for Sample Ninja to correctly map data, certain variables needed to be formatted into a specific data type in Excel. These are shown below:

```
Sample Ninja Data Variable  |    Excel Data Format
-----------------------------|------------------------
            Date             |    Date as 2021-07-23
            Phone            |    Text as +12345678912
            Checkbox         |    Number (No Decimals)
            Radio            |    Number (No Decimals)
 All Other Data Variables    |    Text
 
```


## Using the importer

### 1.	Select file to import

Click on the designated area and select a file to import. Or simply locate the file on your device and drag & drop it into the drop zone (indicated by a dashed line).

### 2.	Inspection

Here you’ll be able to visually inspect the first 100 records of your CSV file for any obvious errors. At the bottom of this screen you can also change the number records or rows per page shown. 

Once you have completed inspecting your file, you can either click the **Restart** button at the bottom of the page to re-start the import process or click **Next let’s map your data** -button to continue.

### 3.	Mapping

The system will attempt to automatically map all columns in the import file to a variables in the system with the same names, provided that such a variable exists. The variables or columns in the import file are shown on the left hand-side of window and the matching variable in the system on the right-hand side.

If the system cannot auto-map a variable you have the options of either: 

1.	Manually mapping to a variable in the system by selecting from the list of available variables in the dropdown list, or 
2.	Leaving this variable out in the import by clicking on **ignore this column** button.

If the later is chosen, the variable in question will be skipped and left out from the import. 
Where there are missing values or validation failures, a warning message is displayed against the variable in question. For a more detailed inspection of the error, simply click on the error text.

### 4.	Upload

You can assign or specify the following before clicking the **Upload** button:

1.	Target sub panel 
2.	Locale
3.	Recruitment source
4.	Subscribed date

> You can provide **LOCALE**, **RECRUITMENT_SOURCE** and **SUBSCRIBED_DATE** for each individual panelists if desired. If the importer encounters any blank or missing values then the values you selected here will be used. You may also omit these columns completely from your CSV file.

### 5.	Results

The result of the outcome of the upload is displayed here. You can see how many panelists were successfully imported and similarly the number of panelists that couldn’t be imported. Any errors are highlighted in red. If you mouse over the error items you will see more details description of the error.

If your import contains any errors, the system will automatically generate a results file containing all the CSV lines with errors and explanations on how to fix. This file is automatically placed in your downloads. Select **Downloads** from the main menu to go to downloads or click on the **Downloads** -button in the importer results screen. 

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
