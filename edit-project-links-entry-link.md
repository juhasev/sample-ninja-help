## Survey Entry Link

The survey link defines where panelists are sent after they respond to invitations. Additionally you can pipe panelist ID, data variable data and enable URL security via hashing.

> The default link for new projects points to **Sample Ninja - Test Survey** that can be used in place of an actual survey for testing purposes. When using the test survey you can manually select survey outcome i.e. COMPLETED, QUALITY, QUOTA etc...

## Survey Entry Link Templates
Templates allow you to pre-define survey link templates for the most common survey platforms that you send sample to. When you define templates you can use place holders for URL parameters that need to be manually replaced. For example most survey platform require that you pass in a survey ID. Let's say that it needs to be placed to **id** -parameter, then your **Base URL** would look like this:

https://surveyplatform.com/survey?id=[ID]

When the template is applied you would only need to change the [ID] with the desired target survey ID.

The following pipes are inserted automatically:

- **[pid]** variable is for Panelist ID
- **[hash]** variable is for the security hash (inserted only when hashing is enabled)
- **[PROJECT_ID]** variable is automatically be replaced with Sample Ninja project ID)

### Piping Data Variables to Surveys
Data variables can be easily piped using the **Select Data Variables** button to choose the required ones from the available selection.

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


## Signing and security
Signing should always be used if the target platform supports it as this prevents URL tampering. **Sample Ninja** supports the following algoritms:

- MD5 (not recommended)
- SHA1 
- SHA256 (recommended)

> If you need additional signing algorithms please contact us and we will consider adding them

> You must enable hashing for each project by selecting **algorithm**, **hash param name** and enter the **secret** in the **Sample Ninja -> Projects -> Edit Project -> Survey Links -> Edit survey link**. You can template the entry link configuration for future use.

> **IMPORTANT:** If the computed hash does not match you should always return panelist back to Sample Ninja with **security** or **s=sec** status. See   [the help file for exit links](/edit-project-links-exit-links.md) for more information.

## Example hash calculations
These examples use real computed hash values so that you can verify your own hash calculations using the examples.
Signing will verify the path and query part of a survey's URL including the leading slash. Please note that these examples are simplified and we have intentionally omitted panelist ID or **pid** parameter.

### Example A

In this example we are using **SHA-256** algorithm with secret **MySecretPasscode** to verify that URL has not been tampered with.

Survey entry link produced by **Sample Ninja**

```
https://surveyengine.com/projects?project_id=10&region=2&country=US&hash=18f3b4c68014e18a539a80916a937ac61d9a96303cd4f1b66a91c7e7f5afef8f
```

#### Step 1 - Remove protocol, host and hash -parameter:
```
/projects?project_id=10&region=2&country=US
```
#### Step 2 - Sort URL params alphabetically
```
/projects?country=US&project_id=10&region=2
```
#### Step 3 - Append the secret at the end of the URL
```
/projects?country=US&project_id=10&region=2MySecretPasscode
```
#### Step 4 - Calculate hash
Here we use PHP's built-in hash function (https://www.php.net/manual/en/function.hash.php) with secret **MySecretPasscode**
```
$hash = hash($algorithm, $hashableUrl . $secret);
$hash = hash('SHA256','/projects?country=US&project_id=10&region=2MySecretPasscode');

echo $hash; // Outputs 18f3b4c68014e18a539a80916a937ac61d9a96303cd4f1b66a91c7e7f5afef8f
```
#### Step 5 - Verify hash parameter supplied by Sample Ninja matches your calculated hash

### Example B

In this example we are using **SHA-1** algorithm with secret **MySecretPasscode**

Survey entry link:
```
https://surveyengine.com/projects?country=US&project_id=10&region=2&hash=d86cca325d097945e54e8f394d031e10e17e815f
```
#### Step 1 - Remove protocol, host and hash -parameter:
```
/projects?country=US&project_id=10&region=2
```

#### Step 2 - Sort URL params alphabetically
No change here
```
/projects?country=US&project_id=10&region=2
```

#### Step 3 - Append the secret at the end of the URL
```
/projects?country=US&project_id=10&region=2MySecretPasscode
```
#### Step 4 - Calculate hash
```
echo hash('SHA1','/projects?country=US&project_id=10&region=2MySecretPasscode); // PHP example

d86cca325d097945e54e8f394d031e10e17e815f
```

#### Step 5 - Verify hash parameter supplied by Sample Ninja matches your calculated hash

### Example C

In this example we will be using **SHA-256** algorithm with secret **MySecretPasscode** to verify the value hash supplied by **Sample Ninja**

Survey entry link:
```
https://surveyengine.com/projects??country=US&project_id=10&region=2&hash=b4f323675eb1c43223c990e0dbc55fca2cc30401e97cbe47ab4b7a7a7de90613
```
#### Step 1 - Remove protocol, host and hash -parameter
```
/projects?country=US&project_id=10&region=2
```
#### Step 2 - Sort URL params alphabetically
No change here
```
/projects?country=US&project_id=10&region=2
```
#### Step 3 - Append the secret at the end of the URL
```
/projects?country=US&project_id=10&region=2MySecretPasscode
```
#### Step 4 - Calculate hash
```
echo hash('SHA256','/projects?country=US&project_id=10&region=2MySecretPasscode); // PHP example

b4f323675eb1c43223c990e0dbc55fca2cc30401e97cbe47ab4b7a7a7de90613
```
#### Step 5 - Verify hash parameter supplied by Sample Ninja matches your calculated hash
 
### Example D
In this example we are using **SHA-256** algorithm with secret **@$Sup3rS3cur3S3cr3t!!@**

Survey entry link:
```
https://surveyengine.com/projects?p=1435540&r=2&c=US&g=1&hash=93ce7437be0603c5dd244ef31951bac690f367f67b889d26bf5751781385afbc
```

#### Step 1 - Remove protocol, host and hash -parameter
Hashable URL part (params sorted alphabetically)
```
/projects?c=US&g=1&p=1435540&r=2
```
#### Step 2 - Sort URL params alphabetically
No change here
```
/projects?c=US&g=1&p=1435540&r=2
```
#### Step 3 - Append the secret at the end of the URL
```
/projects?c=US&g=1&p=1435540&r=2@$Sup3rS3cur3S3cr3t!!@
```
#### Step 4 - Calculate hash
```
echo hash('SHA256','/projects?c=US&g=1&p=1435540&r=2@$Sup3rS3cur3S3cr3t!!@'); // PHP example

93ce7437be0603c5dd244ef31951bac690f367f67b889d26bf5751781385afbc
```
#### Step 5 - Verify hash parameter supplied by Sample Ninja matches your calculated hash




