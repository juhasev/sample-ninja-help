### Uploaded Sample Identifiers

Paste a list of panelist identifiers to the target "paste" box. Identifiers can be optionally enclosed in quotation marks and be separated with commas. We will automatically clean your list and validate that all the identifiers are in the correct format. Any detected errors will be immediately shown. 

**Please note** that you must paste in the correct identifiers from the right project. **Sample Ninja** will send an invitation to all the panelists pasted in w/o checking if they participated in any projects.

> The correct format for panelist identifiers is 7418ccdb-2607-4e98-8b11-2c53246214f0. If you paste panelist identifiers not found in your panel, the system will ignore them when sending invitations.

> At least one identifier must be valid, or the project will not save.

> You cannot remove identifiers from the project after submitting them. However, you can add more identifiers by pasting more. If you accidentally saved the wrong set of identifiers, could you take the project offline and start over?

### Matching panelists against unique data variables of type (Email, Keyword, or Number)

If you are a Health Care panel or Customer Experience (CX), you may store a unique customer ID or NPI (National Provider Identification USA Only) in the data variables. You can use these IDs to find sample by selecting match against data variable values you supply in a CSV file. If the ID number is alphanumeric, you should always use the keyword -type. If numeric, then you can also use the number -type. Never use the text -type as it is analyzed field "Brown Dog" will match both "Brown" and "Dog."

> This feature is only available by uploading a CSV file.

### Passing CSV columns to the survey

An 'Uploaded Sample' CSV file can carry more columns than the one that identifies the panelist. After you have selected the 'Panelist ID' column (or the column to match against a data variable), Sample Ninja lists the remaining columns. Every column you leave ticked is added to each panelist's survey link as a URL parameter. The column header is used as the parameter name and the cell is used as the value.

For example, a file with the columns **panelist**, **region** and **wave** sends each panelist to the survey with their own values:

```
https://mysurvey.com?id=58d477ce-a23f-420c-a148-816dddf024af&session=610fbafb-e875-43d4-8534-a8a35a5a7aa2&region=EU&wave=2
```

- Column headers may contain letters, numbers, dashes and underscores, and cannot be a number alone. Columns with other headers are shown but cannot be selected, so rename them in the file first.
- A column cannot use a parameter name the survey link already sends, such as the Panelist ID, session or hash parameter, or a data variable parameter.
- If a panelist has no value in a column, that parameter is left off their link.
- A project can have up to 20 uploaded parameters, and each value can be up to 255 characters long.
- Values are kept exactly as they are in the file, so leading zeros (for example in zip codes or passcodes) are preserved.
- The uploaded parameters are included when the survey link is hashed.
- Uploading another CSV file with different columns adds those columns to the project. Values of panelists that were already saved cannot be changed.

The **URL PARAMS** column of the panelist list shows how many values each panelist has; hover over the number to see them. The values are also shown in the project participants list and in the participant export, one column per parameter.

> This feature is only available for 'Uploaded Sample' projects and by uploading a CSV file.

### Passcode Authentication for Surveys

A **Passcode** is uploaded like any other column. Name the column after the URL parameter your survey expects the **Passcode** in, for example **code**, and leave it ticked when Sample Ninja lists the columns. Each panelist is then sent to the survey with their own **Passcode** in that parameter.

> There is no separate 'Passcode param name' setting any more. Projects created before this change keep sending their **Passcodes** in the parameter that was configured for them.

### Testing a survey that needs a passcode or other uploaded values

Test panelists are not in the uploaded sample, so they have no values for the uploaded columns. When you click **TEST SURVEY** on the SURVEY REDIRECTS -tab, Sample Ninja asks for a value for each uploaded column, the **Passcode** column included. The values you enter are sent to the survey exactly as they would be for a real panelist. Any value you leave empty is not sent.

> Save the project after uploading a CSV file before you test, otherwise the new columns are not known to the test link.

### Using quotas with an uploaded sample

An 'Uploaded Sample' project can use quotas in the same way as an auto sampling project. After you have uploaded your list of panelists, open the QUOTAS -tab, turn on **Enable quotas** and select the variables you want to balance on.

- Without quotas, everybody on the uploaded list is invited and the **Target completes** is the size of the list.
- With quotas, panelists are invited from the uploaded list in waves, towards the quota targets. Only panelists on your list are ever invited.
- With quotas you set the **Target completes** yourself on the BASIC SETTINGS -tab. It is usually lower than the size of the list, for example 500 completes out of 5,000 uploaded panelists.
- With quotas the **Sampling settings** on the BASIC SETTINGS -tab apply: the sampling priority against other projects, and the hours until an unanswered invite is considered abandoned and replaced. Without quotas they are not used, because everybody on the list is invited right away.
- **RUN FEASIBILITY** counts the panelists inside your uploaded list, so you can see whether the list has enough people for each quota. As with auto sampling projects, you can choose to apply the panel business rules to the count.
- Panelists on the list who have no answer for a quota variable cannot be placed in a quota and are not invited.
- With quotas, the panel business rules and the quiet period apply to the uploaded list, the same as in an auto sampling project. A panelist on the list who does not pass the business rules is not invited.

> If the list runs out of panelists for a quota before its target is met, review the quotas or upload more panelists. Sample Ninja raises a sampling alert on the project when this stalls it.

