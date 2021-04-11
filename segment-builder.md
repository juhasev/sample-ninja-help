## Query builder

### Basic use
Build and query your panel. First select the match operation which defaults to **Match all of the following** which is basically ```AND``` group. If you need ```OR``` group select **Match at least one of the folllowing**.

Next select the variable you would like to query. **Match** operation is automatically selected but depending on the data variable type other options may be available as well. Use the **exists** to find out if the data variable has data.

> To reduce clutter on the screen use the **Compact** toggle to get rid of the ```AND``` and ```OR``` -labels.

### OR groups
If you need to add ```OR``` condition click on the **Add sub group** button. Select some variables and if any one them matches the entire group is considered **TRUE**

### Business rules
If you click on the business rules box you can toggle business rules on / off to see their impact on your segment.

> You cannot permanently turn off the business rules off in projects. Projects will automatically turn business rules back on when saved.

### Segment settings
These settings only show if you are editing actual segment.

#### Designated filter
If you enable this it simply means this segment is intended to be as a filter in other application features like **Panelist manager**. It also means that business rules should not be applied automatically (in most cases) however if desired business rules can toggled back on. When a segment is designated as filter, it becomes available throughout the application features that use filtering. 

> Please note that segments with **designated filter** toggled off will note show in the filter selection.

#### Share with the team
This setting makes your segment / designated filter available for the other team members to run and copy. The other team members cannot make changes to your segment.

> **IMPORTANT**: The system makes a copy of the segment when used in a project. Therefore any modifications to the original segment has no impact on your project.
