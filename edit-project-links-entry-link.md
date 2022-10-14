## Survey Entry Link

The survey link defines where panelists are sent after they respond to invitations. Additionally you can pipe panelist ID, data variable data and enable URL security via hashing.

> The default link for new projects points to **Sample Ninja - Test Survey** that can be used in place of an actual survey for testing purposes. When using the test survey you can manually select survey outcome i.e. COMPLETED, QUALITY, QUOTA etc...

## Survey Entry Link Templates
Templates allow you to pre-define survey link templates for the most common survey platforms that you send sample to. When you define templates you can use place holders for URL parameters that need to be manually replaced. For example most survey platform require that you pass in a survey ID. Let's say that it needs to be placed to **id** -parameter, then your **Base URL** would look like this:

https://surveyplatform.com/survey?id=[ID]

When the template is applied you would only need to change the [ID] with the desired target survey ID.

The following pipes are inserted automatically depending on how they are configured:

**[pid]** is reserved for Panelist ID.
**[hash]** is reserved for the security hash (inserted only when hashing is enabled).
**[PROJECT_ID]** if you use this placeholder it will be automatically be replaced with Sample Ninja project ID.

### Piping Data Variables to Surveys
Data variables can be easily piped using the 'Select Data Variables' button to choose the required ones from the available selection.

Parameter names can be fully customized to match what is used in the survey. For example if **GENDER** is selected, the resulting URL might look like this:

https://surveyengine.com?project=343&g=1

#### Piping Radio Data
Radio data is piped using the **Option ID** number visible when you edit the **Data Variable**. For example, piping the **EDUCATION** data variable would possibly show the URL as:

https://surveyengine.com?project=[ID]&education=5

#### Piping Checkbox Data
Sample Ninja pipes check box values as multiple values. For example, if using the **HOBBIES** data variable with values 1,2,3 the URL would be something like:

https://surveyengine.com?project=[ID]&hobbies=1&hobbies=2&hobbies=3

> Some survey platforms may use alternate formats like hobbies=1,2,3. Please contact support@sampleninja.io if you run into this situation.

#### Piping Locale
Every panelist has an assigned locale, for example ENG-US. If a multilingual survey is being run, then the **LOCALE** data variable should be piped into the survey.

> Some survey platforms may use alternative locales or languages. Please contact support@sampleninja.io if you run into this stuation.

#### Test Link and Data Variable Pipes
Sample Ninja will automatically insert random data for all the defined data variable pipes.

> The inserted data for the Keyword and the Text -variable types is static because there is no way for the test data generator to figure out the real intent of the data variable. For example if **CITY** is piped in, the data set will show as **test_keyword_city**. Similarly for the text variable, if the example **DESCRIPTON** is used, data set would show as **test_text_description**.
 
### Panelist ID
Panelist ID is automatically piped in the URL. You should save the panelist ID along with the survey responses. This is important for reconsilidation i.e. if you need to disqualify some participants after the survey data has been reviewed. By default the parameter name is **pid** but you may customize this to match the target survey platform.

https://surveyengine.com?project_id=343&pid=4b6c7e1e-2ec3-4cc7-975a-5a523d55248f

If **Random test ID** is toggled on, Sample Ninja will send random panelist ID to the test survey when testing the survey link. In some cases this makes testing easier especially if duplicate IDs are blocked by the survey software.

### Signing and security
Signing should always be used if the target platform supports it as this prevents URL tampering. Sample Ninja supports the following algoritms:

- MD5 (not recommended)
- SHA1 
- SHA256 (recommended)

> If you need additional signing algorithms please contact us and we will consider adding them.

### Example survey redirect link (from SampleNinja)
Signing will verify the path and query part of a survey's URL (i.e. not the protocol/host), including the leading slash. 

Using the following URL as an example:

https://surveyengine.com/projects?project_id=10&region=2&country=US

#### Step 1 - Remove protocol and host:

/projects?project_id=10&region=2&country=US

#### Step 2 - Sort URL params alphabetically

/projects?country=US&project_id=10&region=2

#### Step 3 - Calculate hash appending the secret

PHP example using built-in hash function (https://www.php.net/manual/en/function.hash.php) with secret **MySecretPasscode**

```
$hash = hash($algorithm, $hashableUrl . $secret)
$hash = hash('SHA256','/projects?country=US&project_id=10&region=2MySecretPasscode');
```

#### Step 4 - Verify hash parameter

When you receive link you must verify that the Sample Ninja supplied hash is correct. These examples use real hash and you can use these to verify your own hash calculations.

Example: Hash result using **SHA-1** algorithm with secret **MySecretPasscode**

Hashed URL part
```
/projects?country=US&project_id=10&region=2
```
Computed hash:
```
d86cca325d097945e54e8f394d031e10e17e815f
```

Example: Hash result using **SHA-256** algorithm with secret **MySecretPasscode**

Hashed URL part
```
/projects?country=US&project_id=10&region=2
```

Computed hash:
```
b4f323675eb1c43223c990e0dbc55fca2cc30401e97cbe47ab4b7a7a7de90613
```

> You can configure what the **hash** -parameter name in both incoming and outgoing links via Sample Ninja UI -> Edit project -> Survey Links
> The **secret** is entered in the Sample Ninja UI -> Edit project -> Survey Links
> Please note that these examples are simplified and we have intentionally omitted panelist ID or **pid** parameter.

### Example survey exit link (redirect back to SampleNinja)
To make the exit link and the resulting hash more complex, we have added optional panelist ID to the link (id -param). You may used some other parameter as well, the only reserved parameters are "s" for status and "session" for session ID. 

```
https://yourcompany.panelservice.io/p/exit?s=c&id=9bb379a3-7831-4a55-8036-085aeff18790
```

#### Step 1 - Remove protocol and host:

/p/exit?s=c&id=9bb379a3-7831-4a55-8036-085aeff18790

#### Step 2 - Sort URL params alphabetically

/p/exit?id=9bb379a3-7831-4a55-8036-085aeff18790&s=c

#### Step 3 - Append calculated hash to the exit link

Example result using **SHA-1** algorithm with secret **MySecretPasscode**
```
https://yourcompany.panelservice.io/p/exit?id=9bb379a3-7831-4a55-8036-085aeff18790&s=c&hash=17637eac2a8bbd056bb31b19a31768846474b5fa
```

Example result using **SHA-256** algorithm with secret **MySecretPasscode**
```
https://yourcompany.panelservice.io/p/exit?id=9bb379a3-7831-4a55-8036-085aeff18790&s=c&hash=f9c2db85f0d4644b4f8e187bea2bd2c62d4aa216af5f42c4c4a4b9b153bc1bd0
```



