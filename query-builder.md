## Query builder

### Basic use
Build and query your panel. First, select the match operation, which defaults to **Match all of the following**, which is basically the ```AND``` group. If you need ```OR``` group, select **Match at least one of the following**.

Next, select the variable you would like to query. **Match** operation is automatically selected, but other options may also be available depending on the data variable type. Use the **exists** to determine if the data variable has data.

> To reduce clutter on the screen use the **Compact** toggle to get rid of the ```AND``` and ```OR``` -labels.

#### OR groups
If you need to add ```OR``` condition click on the **Add sub group** button. Select some variables and if any one them matches the entire group is considered **TRUE**

### Business Rules
If you click on the business rules box, you can toggle business rules on / off to see their impact on your segment.

> You cannot permanently turn off the business rules in projects. Projects will automatically turn business rules back on when saved.

If you need to modify or review your business rules, you can do so by visiting **Panel Settings** > **Business Rules** -tab.

### Query Filter settings
These settings only show when editing/creating query filters in **Query Filters**.

#### Share with the team
This setting makes your segment / designated filter available for the other team members to run and copy. The other team members cannot make changes to your Query Filters.

> **IMPORTANT**: The system makes a copy of the Query Filter when used in a project. Therefore, any modifications to the original Query Filter have no impact on your project.
