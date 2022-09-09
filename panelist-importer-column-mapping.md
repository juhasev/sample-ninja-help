## Column Mapping

In this screen you map your CSV columns to the data variables. If you used column headers names that match your data variables names then the mapping should be done automatically for you.

### What to when auto mapping fails

If you don't see your variable listed under the mapping selection then either the CSV data is provided in the wrong format or the data variable is does not exists or is created using wrong type. For example, if the CSV data type is detected as **String** -type you would be unable to map it to a **Radio** data variable type with requires integer values 1 - n. 

If this happens, first verify your data format and the desired target variable types! See the **HELP** in the first screen (file selection, drop page) for details how to format your data file.

> **TIP**: Don't forget to scroll down when you look for variables. If you have a lot of variables, you can simply type in the variable name in selection field to narrow down the data variable list!

### Column value errors

**Sample Ninja** performs a basic column value validation on the fly. This is no means 100% comprehensive validation but it gives you an idea of obvious errors in CSV file. For example if you attempt to import value "A" to a **radio** data variable type this will be flagged automatically. In these cases you can you replace invalid values with NULL and you can still proceed with the import / update or alternatively you can fix the values in the CSV import file and try again.

> **TIP**: Sample Ninja allows you to do a **TEST RUN** in which no values will be inserted or updated in the database. The test run will perform in depth validation of CSV file. If you can do test run without any errors then that is a good indicator that you ready! The **TEST RUN** is selected in the next screen after all the mapping have been completed.

## How the auto mapper works?

### Data type detection and how it affects mapping

The importer scans each column and attempts to discover the column's data type and the potential target data variable types. The detection runs in the following order: 

#### When detected CSV value contains

- date -> target variables offered are date -type
- phone -> target variables offered are phone or keyword -type
- integer -> target variables offered are radio, checkbox, number, keyword and text -type.
- number -> target variables offered are number, keyword and text -type.
- email -> target variables offered are keyword -type
- locale -> target variables offered are keyword -type
- string -> target variables offered are text and keyword -type

When the auto mapper has discovered suitable target variable types for a CSV column, it then tries to use Fuzzy logic to match **CSV COLUMN HEADER** to **DATA VARIABLE LABEL**. If the names are similar then the column mapper should select the target variable automatically.

> **TIP** If you supply date in the incorrect format then **Sample Ninja** will not detect it as date but rather sting thus you cannot map invalid dates to date -variable types. To see the correct formatting of all types, please read the help file in the first screen how to format your CSV file correctly.
