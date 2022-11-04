## Data Variables

### Magical data variables
Data variables CITY, REGION and COUNTRY are magical as. they can be populated automatically using IP based geolocation, user given location i.e. GPS on mobile devices and or based on the POSTAL_CODE entered. Do not use home grown variables like STATE or PROVINCE, use the built-in REGION variable instead due to its special ability. 

The BIRTH_DATE variable enables the dashboard Age vs. Gender chart can be used to send birthday greeting etc….

### Data variable types
Sample Ninja supports multiple different data variable types for more detailed information on each variable type, click the Create new data variable -button under the Data Variables main menu item. Please note the difference between the text and the keyword data variable types. Almost in all cases you want to use the keyword -data variable.

Data Variables are the basic storage unit for the panelist information you collect. Use the top row boxes to filter data variables by name, group or system designation. See below for more details.

#### Text
Any content saved to a text -type variable is analysed. Records with partial matches are scored and returned in the order of highest matching score first.

#### Keyword
Keyword variables are always matched with exact search term. Use keyword -variable to store unstructured categorical data like city or postal code.

#### Email
Email variables must contain valid email and input is automatically validated when placed in the registration survey or dynamic profiling.

#### Radio
Radio questions can have single multiple answer option selected.

#### Checkbox
Checkbox questions can have multiple answer options selected.

#### Locale
Locale question contain standard locale identifier. System wide validation is automatically applied.

#### Date
Use to store dates. Date values can be searched using ranges. System wide validation is automatically applied.

#### Number
Use to store numeric data. Numbers can be integers, numbers with decimals or floating point values

#### Phone
Store phone numbers using international e164 -standard. System wide phone number validation is automatically applied.

> If you click on the blue **Statistics** -button on each row it will take you into the data variable dashboard.

### System data variables
The system variables track various metrics and provide you additional information you can use when running queries against your panel. There are many useful lifetime counters and other system variables you may want to use to manage your panel better. System Variables include

- INVITED_COUNT
- STARTED_COUNT
- QUALITY_COUNT
- PROFILE_COUNT
- QUOTA_COUNT
- SECURITY_COUNT
- COMPLETED_COUNT
- EMAIL_VALID (Can receive email or is bounced)
- STATUS (Subscribe, Unsubscribe or Blacklisted)
- RESPONSE_RATE (Response rate in the period as configured in the panel settings) 
- REVENUE (Lifetime revenue earned for your panelists)
- SUBSCRIBED_DATE (When a panelist joined your panel)
- UNSUBSCRIBED_DATE (When a panelist left your panel)
- POINTS_BALANCE (Current points balance)
- POINTS_REWARDED (Lifetime points awarded)
- POINTS_REDEEMED (Lifetime points redeemed)

This is not a comprehensive list of the system variables and it is recommended that you view the full list under system variables by selecting the group filter “SYSTEM” to have an idea what is available. 

### Using industry standard variables
You should consider using industry standard variables for B2C panels. Sample Ninja provides the defaults that are Lucid / CINT compatible. When you are using industry standard variables they can be mapped to various sample exchanges with minimal effort. You can create the standard data variables under Data Variables. These are:

- GENDER
- HOBBIES
- ETHNICITY
- RELATIONSHIP
- EMPLOYMENT_STATUS
- EDUCATION
- INCOME
- INDUSTRY

### Data Variable vs. Question
Any data variable in Sample Ninja can be presented as a multilingual question as long as question text and option texts are provided in the languages needed. This enables you to populate the data variables in the Registration Survey as well as in the Dynamic Profiling.

### Importing Data Variables
If you have a lot of variables i.e. you are migrating from an existing panel into Sample Ninja you can import hundreds of data variables by uploading them all at once. In order to do this, you need to provide them in the correctly formatted JSON document. Under the Data Variables you will find import / export buttons. The format is different for each question type and documenting them here is beyond the scope of this document. You can export all different question types for an example file that you can apply to your own variables.

If you need help getting your existing variables imported please contact support@sampleninja.io.

### Managing data variables

#### Filter by Group

Simply choose filter from the top menu.

For example it is possible to create a data variable group such as Demographics, Healthcare, Household etc which allows the ability to filter all the data variables that fit into these particular category.

#### Filter by Class

Allow you to filter by the system class. For example one could find all variables that are flagged **Personally Identifiable (PI)** or variables that community users can write **Community writable**.

> It is possible to filter by using a combination of both **Group** and **Class** at the same time.

#### Reload Screen

Hit the **CIRCLE ARROW** - button at top right corner of the screen to reload all data variables.

#### Create a New Data Variable Group

The sample ninja platform allows you to create variable groups four example you might want to create the group of all the demographic variables or all the healthcare related variables so that it is easier to select these later on.

Firstly, click on the (4 Dot Icon) on the Top Right of the screen, then click on the (+ sign) and name the New group.

Then select all the variable that you wish to assign to that group and click on the **ASSIGN TO GROUP** button on the bottom left.

#### Create a New STANDARD Data Variables

Allows you to create STANDARD Sample Ninja data variables. These standards are based on LUCID's standard questions and offer greater flexibility in terms of buying and selling from exchanges.

#### Create a New Data Variable

Hit the **PLUS** button to create a new data available in you panel database.

After selecting the data variable type, the next step is to **select the base locale**. You can add more locales later on. If your panel only has one locale this selection is done automatically for you.

> Text question types are analyzed! This means that partial matches can be also returned. If this is not what you want use the **Keyword** type instead. For example Sample Ninja uses keyword type for CITY, STATE and POSTAL_CODE.

#### Data Variable Export and Import

**Data Variable Export** - Click on the **Export** button (cloud icon with downwards arrow). From here you can select the Data Variables that you wish to export. On clicking **Done** a downloadable file will be created, which can be accessed from the 'Downloads' section of Sample Ninja.

**Data Variable Import** - Click on the **Import** button (cloud icon with upwards arrow). Here, select the downloadable file that was created during the exporting process. On clicking **Open** your selected Data Variables will be imported into Sample Ninja.

> Locales (selected for the imported Data Variables) must exist in the target panel or the import will fail!
