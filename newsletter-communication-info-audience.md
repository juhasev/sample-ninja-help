# How to Use Audience Selection & Query Filters

The Audience Selection feature helps you create targeted groups of people from your subpanel for sending newsletters and communications. Think of it as a smart way to find exactly the right people to receive your message.

## Understanding the Interface

The Audience Selection tool is made up of three main screens that work together:

### Screen 1: Audience Selection Overview
This is where you see your current filter settings and can access the query builder. You'll see:
- **Current filters**: Displays what criteria you've set (like "STATUS includes Subscribed")
- **"SELECT QUERY FILTER" button**: Opens the saved filters menu

### Screen 2: Select Query Filter Dialog
This popup helps you choose from pre-made filters:
- **MY QUERY FILTERS tab**: Shows filters you've created and saved
- **SHARED QUERY FILTERS tab**: Shows filters others have shared with you
- **Search box**: Lets you search through available filters by name

### Screen 3: Query Builder
This is where you create and customize your audience criteria:
- **Match count and execution time**: Shows results in real-time
- **Filter conditions**: Where you set your criteria (like STATUS, location, etc.)
- **ADD CONDITION** and **ADD SUB GROUP** buttons**: For building complex filters

## Step-by-Step Guide

### Creating Your First Audience Filter

#### Step 1: Access the Query Builder
1. Clink in the middle of the Audience Selection screen to open the Query Builder
2. Add a condition or a sub group. You can modify this by clicking on the dropdown menus:
   - **Field**: Choose what aspect to filter by (status, location, age, etc.)
   - **Condition**: Choose how to match (includes, excludes, equals, etc.)
   - **Value**: Enter or select the specific value you want

#### Step 2: Add More Conditions (Optional)
- Click **"ADD CONDITION"** to add another filter rule
- Click **"ADD SUB GROUP"** to create complex logic (like "this AND that, OR something else")
- Watch the match count update in real-time as you add conditions

#### Step 3: Review Your Results
- Check the **match count** (like "20,093") to see how many people match your criteria
- Note the **execution time** (like "24 ms") - this shows how quickly the system found matches
- If the number seems too high or too low, adjust your conditions

### Using Your Audience Filter

#### For Immediate Use
1. Once you're satisfied with your match count, you can use this audience right away
2. Look for an **"UPDATE"** button to apply your filter
3. Your audience is now ready for sending newsletters or communications

## Best Practices

### Start Simple
- Begin with basic criteria like subscription status
- Add more conditions gradually to narrow your audience
- Watch how the match count changes with each addition

### Test Your Filters
- Always review the match count before using a filter
- If you get too few matches, remove some conditions
- If you get too many, add more specific criteria

### Monitor Performance
- Pay attention to execution time - very slow filters might need optimization
- If a filter takes too long, try simplifying the conditions

## Common Scenarios

### Monthly Newsletter
**Goal**: Send to all active subscribers
**Filter**: STATUS includes "Subscribed"

### Regional Announcement
**Goal**: Target specific geographic area
**Filters**: 
- STATUS includes "Subscribed"
- REGION equals "[Your Target Region]"

### Re-engagement Campaign
**Goal**: Target less active members
**Filters**:
- STATUS includes "Subscribed" 
- LAST_LOGIN older than "60 days"

### New Member Welcome Series
**Goal**: Target recently joined members
**Filters**:
- STATUS includes "Subscribed"
- REGISTRATION_DATE within "Last 7 days"

## Troubleshooting

### Match count seems wrong
- Double-check your filter conditions
- Make sure you're using "includes" vs "equals" correctly
- Verify that your criteria make logical sense together

### Filter runs slowly
- Simplify your conditions if possible
- Avoid overly complex sub-groups unless necessary
- Consider if you really need all the conditions you've set

## Tips for Success

- **Start broad, then narrow**: Begin with basic criteria and add specifics
- **Test before sending**: Always verify your audience size makes sense

Remember: The goal is to reach the right people with the right message. Take time to build your audience filters thoughtfully, and they'll serve you well for all your future communications.