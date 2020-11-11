## Panelist Imported Select File

The 'Panelist Importer' component let’s you to import panelists (members) to an existing panel or subpanel. Before attempting to import, please ENSURE that the import file...

1. is saved or stored in a CSV (comma delimited) format. Currently, this is the only format supported by the Panelist Importer.
2. contains column for FIRST_NAME, LAST_NAME and EMAIL Data Variables. These variables are mandatory system requirement and therefore need to present in every import file.

## Important: 

BEFORE selecting a file to import, it’s highly recommended that you create a data variable (including answer options) in the ‘Data Variables’ component for each variable in the import file that you intend to import.

It’s further recommended that the name of data variable name in the Data Variables component and the corresponding name of the variable in the import file match, where possible. This will save you a lot time in having to correcting errors, mapping variables or avoid you having to re-start the import process.   

## An overview of the process is shown below:

1. Select file to import 
2. Errors & inspection 
3. Mapping
4. Upload
5. Results

## 1.	Select file to import

Click on the designated area and browse your device for the file you want to import or simply locate the file on your device and drag & drop it into designated area

## 2.	Errors & inspection

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
