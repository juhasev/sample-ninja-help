## Dynamic Profiling

With **Dynamic Profiling**, **Data Variables** are automatically populated without having to resort to additional update surveys. Dynamic Profiling activates every time panelists get terminated (profile, quota) or come back as completed from a survey project. **Dynamic Profiling** can also be enabled in the **Member App** settings.

### Top row master settings and answer frequency

#### Settings
Control whether **Dynamic Profiling** is included in the **Sub Panel**, adjust the compensation for each question and set daily question limits.

> Make sure that the daily question limit is set correctly and so that the **Minimum points to redeem** -setting is higher than a panelist's daily maximum earnings from answering Dynamic Profiling questions. The reason is simple: you do not want panelists to create an account and walk out with rewards without completing a single survey. The **Minimum points to redeem** -setting can be adjusted in each **Sub Panel's** settings.

#### Answer Frequency
General indicator of the answer frequency for the selected period.

### Toolbar

#### Show unused
Displays all data variables, otherwise we display only variable that are been used in the projects or are enabled for Dynamic Profiling. 

#### Search
Use this field to quickly find a data variable by using its label or name.

#### Filter by group
Only should data variables assigned to a single group

#### Time period filter (blue filter icon)
Click on the filter button to set a time limit for how far back the system should look in terms of Data Variable usage / usage frequency / answers provided.

#### Reload
Click on the reload button to refresh data

### Data Variables list columns

#### Name
This column displays the variable name and whether dynamic profiling has been enabled.

#### Settings
This column indicates:
- Priority of Dynamic Profiling.
- Refresh interval (ask question again).
- Any warnings such as missing translations.

#### Usage in Projects
This tab displays all variables that are being used in either **Project Qualifications** or in **Sample Balancing**. The list by default is sorted by the most frequently used variable. The frequency is indicated as a progress bar which is calculated comparing the variable to the most used variable. The X multiplier indicates how many projects have used this variable in the selected reporting period.

#### Hydration
This column displays the current hydration percent in percent % out of the subscribed **Sub Panel** members. The selected time period filter has no impact on hydration.

#### Actions

##### Settings
Click on the gear icon to bring up **Dynamic Profiling Settings** for the variable. You can control whether dynamic profiling is enabled, priority and whether the answer should be periodically refreshed.

##### Conditions
Use this button to display Dynamic Profiling question condionally. See section below for details:

##### Additional actions
Click on **dots** -button to display additional actions for each **Data Variable**. The Edit variable button conveniently allows for any missing translation/s to be added to the variables. Data Variable statistics can also be pulled from this menu without having to go back **Data Variables**.

### Displaying questions conditionally
You may want to display some questions conditionally. For example let's imagine we have 3 dependant questions:

1) Car ownership
- Yes
- No

2) What is the model of the car?
- Toyota
- Ford
- Kia
- Etc

3) Annual miles driven?
- less than 50,000 miles
- more than 50,000 miles

If you click on the "C" -button on the question (2) row, you can set condition when to display the question (2). Next, select question (1) "Car ownership" from the menu and then checking "Yes" -option. In order to display question (3) conditionally, you would repeat the same operation.

> The follow up questions are prioritized to display immediately after the parent questions. However, due to daily question limit this may not always be the case. For example questions A & B may be asked and then followed up by question C the next day. Therefore you should set an identical priority for the follow up questions as for the parent question.

### Limitations
- You can only target **Radio** -type questions in your conditions at the moment.
- You cannot target questions that already contain conditions as this would result into a nested conditional structure which is not currently supported.
- You cannot place conditions on questions that are already used in conditions in the other questions. The same reason as above.

> If you turn off dynamic profiling for a question that is used to conditionally display other questions a warning will be produced. If you abort no changes will be made, but if you proceed conditions on the other questions will be automatically removed.
