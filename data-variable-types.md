## Data variable types

Sample Ninja offers multiple flexible data variable types that can be used to collect and store profiling data. It is important to understand the difference and use the correct type.

### Text 
As the name implies this type stores text, however it is important to realize that the text is analysed. For example if you store the following phrase: **Brown lady fox** all words are analyzed and can be queried independently. For example you could simply search for **fox** and this would produce a match. Each match is given match score based on well it matches analyzed words. Results are always returned highest score first.

> Text question type can be used to store documents up to 2000 characters in lenght.

### Keyword
Keyword data variable can be any text. Keyword is always matched with exact match and is not analyzed like the **text** -type. Keyword type is best suited to storing unstructured categorial data like name of city, name of brand, zipcodes, DMAs, SKUs etc...

### Number
Number data variable type stores integers or decimal numbers. Numeric values can queried using range, greater than, lesser than logic.

### Radio
Radio data variables store a single categorial value.

### Checkbox
Checkbox data variables store multiple categorial values.

### Email
Email question can only store a valid email address.

### Date
Date question store dates.

### Phone
Phone question stores phone numbers using international country code prefix notation. 

### Locale
Locale stores user's locale. Locales follow ISO format
