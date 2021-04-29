## Panelist Imported Select File

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

Easiest way to get started is to produce a test import file by clicking **GENERATE TEST IMPORT FILE**. This little tool let's you pick data variables that you would like to import. Just follow the format and you are good to go. 

> **IMPORTANT!** Do not import the file back in unless you are running **SIMULATION MODE**.

## An overview of the process is shown below:

1. Select file to import 
2. Inspection 
3. Mapping
4. Upload
5. Results

## 1.	Select file to import

Click on the designated area and browse your device for the file you want to import or simply locate the file on your device and drag & drop it into the drop zone indicated by a dashed line.

## 2.	Inspection

Here you’ll be able to visually inspect the first 100 records of your CSV file for any obvious errors. At the bottom of this screen you can also change the number records or rows per page shown. 

Once you have completed inspecting your file, you can either click the ‘Restart’ button at the bottom of the page to re-start the import process or click ‘Next let’s map your data’ button to continue.

## 3.	Mapping

The system will attempt to automatically map all variables/ columns in the import file to a variable in the system with the same name, provided that such a variable exists. 
The variables or columns in the import file are shown on the left hand-side of window and the matching variable in the system on the right-hand side.
Where the system cannot auto-map a variable you have the options of either: 

1.	manually mapping to a variable in the system by selecting from the list of available variables in the dropdown list, or 
2.	leaving this variable out in the import by clicking on ‘ignore this column’ button.
If the later is chosen, the variable in question will be skipped and left out from the import. 
Where there are missing values or validation failures a warning message is displayed against the variable in question. For more detailed inspection of the error, simply click on the error text.

## 4.	Upload

You can assign or specify the following before clicking the ‘Upload’ button:
1.	Target sub panel 
2.	 Locale
3.	Recruitment source
4.	Join date

## 5.	Results

The result of the outcome of the upload is displayed here. You can see how many panelists were successfully imported and similarly the number of panelists that couldn’t be imported. 

A download of all panelist that couldn’t be imported is available.
