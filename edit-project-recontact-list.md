### Recontact Identifiers

Paste a list of panelist identifiers to the target "paste" box. Identifiers can be optionally enclosed in quotation marks and be separated with commas. We will automatically clean your list and validate that all the identifiers are in the correct format. Any detected errors will be immediately shown. 

**Please note** that you must paste in the correct identifiers from the right project. **Sample Ninja** will send an invitation to all the panelists pasted in w/o checking if they participated in any projects.

> The correct format for panelist identifiers is 7418ccdb-2607-4e98-8b11-2c53246214f0. If you paste panelist identifiers not found in your panel, the system will ignore them when sending invitations.

> At least one identifier must be valid, or the project will not save.

> You cannot remove identifiers from the project after submitting them. However, you can add more identifiers by pasting more. If you accidentally saved the wrong set of identifiers, could you take the project offline and start over?

### Recontact using match again unique data variables of type (Email, Keyword or Number)

If you are a Health Care panel or Customer Experience (CX), you may store a unique customer ID or NPI (National Provider Identification USA Only) in the data variables. You can use these IDs to find sample by selecting match against data variable values you supply in a CSV file. If the ID number is alphanumeric, you should always use the keyword -type, if numeric, then you can also use the number -type. Never use the text -type as it is analyzed field "Brown Dog" will match both "Brown" and "Dog".

> This feature is only available by uploading a CSV file.

### Passcode Authentication for Surveys

Sample Ninja supports **Passcode** authentication for 'Recontact' projects. Simply create a new 'Recontact' project and under the 'Panelists' tab, the option to upload CSV files containing 'Panelist IDs' + **Passcodes** is now available. CSV files with other columns can also be added. Sample Ninja will ask which columns contain the 'Panelist ID' and the **Passcode**.

Following the above, edit the link under the SURVEY LINK -tab and ensure the "Passcode param name” is set. The survey link templates can also save the configuration for easy access in future projects.

> This feature is only available by uploading a CSV file.

> The **Passcode** must be passed into the survey via a predetermined variable.
