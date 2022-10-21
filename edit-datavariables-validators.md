## Validators

Validators are used when a question is presented to the user for example in **Dynamic Profiling** or in the built-in **Registration Survey**. Different validators are available for some questions, some questions don't need validators at all for example email -data variable type is automatically validated.

#### Required 
When question answer is required user must answer the quested, otherwise user can skip the question in **Dynamic Profiling**

#### Minimum length
Minimum length, can be used with text, keyword or number -data variable types.

#### Maximum length
Maximum length, can be used with text, keyword or number -data variable types.

#### Alphabetic characters only
Only alphabetic created A-Z are accepted

#### Alphabetic or Numeric characters only
Only aplhabetic and numeric characters are allowed example: SN2022 (valid) SN 2022 (invalid)

#### Number
Any numeric value including values with decimals

#### Integer
Value must be an integer. No decimals are allowed

#### Min checks
This validation applies to checkbox -data variable only.

#### Max checks
This validation applies to checkbox -data variable only.

#### Min date
Start of the allowed age range

#### Max date
End of the allowed age range

#### Regular Expression Validation (advanced)
Enter a custom regular expression to validate the field value

For example if you like to validate US postal code the regular expression would be
```
^[0-9]{5}$
```
Vist Regexr.com to test your more complex regular expressions:

> https://regexr.com/

### Preview question
Click on the **TEST VALIDATOR** -button to preview the question with the current validator. This is a quick way to test that the validator is working properly. 

> In the preview dialog you can select any Sub Panel and Locale to preview question with. You can only select from sub panels that are compatible with the data variable in terms of translations and locale.


