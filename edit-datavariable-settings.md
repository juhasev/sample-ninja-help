## Data variable label
Each variable has it's own unique label. The labels are used to identify the data variable. Sample Ninja data variables can also presented as questions for various locales (ENG-US, SPA-US) and used in both Dynamic Profiling and in the Registration surveys. You must manually supply question text and options text under **QUESTION** tab. You can safely rename the variable label without any impact on the underlaying data or the existing segments, projects or filters.

## Display name
Let's you specify more human readable label for the data variable. For example if you use data variable label **HH_MEMBERS** you could give it a more readable  display name like **Household Members**. The display name is used in the query builder to make queries more readable and understandable by junior **Project Managers**.

## Option labels
Option labels are shown for radio and checkbox questions only.

### Editing option labels
Simply click on the option text to edit it. 

### Adding option labels
Use the **Add option** button to add more options or the trashcan icon to delete them. 

> This option is not available for the system variable or variables belonging to the Standard Questions library.

### Making options exclusive (Checkbox)
> Simply turn the "toggle" switch on to make an option exclusive.

### Creating multiple options at one
Use the **paste options** button to paste a list of options text from Word, Excel or text file.

> If you paste more options than you currently have Sample Ninja will automatically create all the options for you!

### Deleting option labels
Click on the **trashcan** icon, then confirm. The option is removed when you click **UPDATE**.

The confirmation shows how many panelists picked the option, and lists every online or paused project that uses the variable in a survey link, a sample definition or a quota.

Deleting an option removes that answer from every panelist who picked it. If a project pipes the variable into its survey link, the option numbers are also renumbered: every option after the deleted one moves down by one, so panelists who enter the survey afterwards send different numbers than those who entered before. Avoid deleting options while a project using the variable is in field.

> This option is not available for the system variable or variables belonging to the Standard Questions library.

### Re-ordering option labels
You can re-order data variables options by clicking and holding the drag handle. Simply drag the the items in the order you prefer.

> Sample Ninja stores response options with unique ID, which means you can freely change the order without affecting the collected data. Survey links, however, pipe the option's position in the list, so re-ordering changes the numbers sent to the survey. Avoid re-ordering while a project that pipes the variable is in field.
