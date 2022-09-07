### Error reporting options
Choose how the errors will be handled.

#### Skip and report lines with errors
The importer will produce an error file containing the entire line where the error occured alogn with error message. The error report will be placed in the **Downloads**. This allows you to fix errors manually and re-upload the error report file, yes it is re-importable CSV!

#### Abort on any error
The importer will abort on the first error it encounters. This maybe a good choice especially when you are updating data. This prevents the importer from updating everybody with incorrect data should there be some fundamental issue with the CSV file. For example if you importing ETHNICITY and let's say normal range of values is 1 to 16. If line 12 contains value of 17 the importer will stop on this line till you can resolve the issue.
