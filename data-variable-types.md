## Data variable types

Sample Ninja offers multiple flexible data variable types that can be used to collect and store profiling data. It is important to understand the difference and use the correct type.

### About Text -variable type 
As the name implies this type stores text, however it is important to realize that the text is analysed. For example if you store the following phrase: **Brown lady fox** all words are analyzed and can be queried independently. For example you could simply search for **fox** and this would produce a match. Each match is given match score based on well it matches analyzed words. Results are always returned highest score first.

> Text question type can be used to store documents up to 2000 characters in lenght.
