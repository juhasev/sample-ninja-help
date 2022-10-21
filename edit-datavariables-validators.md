## Validators

Validators are used when a question is presented to the user for example in **Dynamic Profiling** or in the built-in **Registration Survey**. Different validators are available for some questions, some questions don't need validators at all for example email -data variable type is automatically validated.

> **WARNING** It is possible to create validators that don't have any overlap, therefore question cannot be answered at all! Always test your validators using the **TEST VALIDATORS** -button!

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

#### Min value
Minimum value, can be used with number -data variable type

#### Max value
Maximum value, can be used with number -data variable type

#### Range
Numeric range, can be used with number -data variable type

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

Examples:

Regular expression to validate US postal code
```
^[0-9]{5}$
```

Regular expression to validate Canadian postal code
```
^[A-Za-z]\d[A-Za-z][ -]?\d[A-Za-z]\d$
```

> Vist Regexr.com to learn and test your regular expressions: https://regexr.com/

### Preview question
Click on the **TEST VALIDATORS** -button to preview the question with the current validators. There you can quickly test the combination of validators selected are working as intended.

> In the preview dialog you can select any Sub Panel and Locale to preview question with. You can only select from sub panels that are compatible with the data variable in terms of translations and locale.


