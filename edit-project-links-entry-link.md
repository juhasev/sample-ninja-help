## Survey entry redirects

The survey entry redirects define where panelists are sent after they respond to invitations. This is typically a survey platform, but can be any other system. In the basic form you should always send:

1) Panelist ID (required to reconcile)
2) Session ID (provides additional safe guard and make hashing more secure)

Additionally, data variable data and enable URL security via hashing.

> The default redirect for new projects points to **Sample Ninja - Test Survey** that can be used instead of an actual survey for testing purposes. When using the test survey, you can manually select the desired outcome, i.e., COMPLETED, QUALITY, QUOTA, etc...

### Settings

- Base URL: Enter the base URL for the survey platform you intend to use.
- Panelist ID param name: Enter the parameter name you want to use, passing **Panelist ID** to the survey platform. (This parameter is automatically inserted.)
- Hash algorithm: Select which hashing algorithm is used to tamper-proof redirects.
- Hash secret: Secret used to compute the hash verification code. This must match the target platform's shared secret.
- Session param name: Defines URL param name for passing the session into the survey.
- Use random panelist ID to test: Select yes if your survey platform requires using unique panelist IDs when testing.
- Passcode param name: This option is only visible for **Re-contact** projects and is used to pass in an uploaded passcode automatically.


## Templates

Templates allow you to pre-define survey entry and exit redirects URL, hashing, and parameter names for the most common survey platforms that you send sample to. When you regularly send to a specific target platform, this can be a real timesaver. Templates allow you to define everything needed for the target platform, including the hash URL of the target platform, hashing algorithm, hashing secret, and parameter names. 

- To create a template from the current project's redirect settings, click on **TEMPLATE CURRENT** button.
- To select and/or manage existing templates, click **SELECT FROM TEMPLATES** button.

> We recommend using the redirect templates, as you can be done configuring redirects literally with a couple of clicks!

When you define templates, you can use placeholders for URL parameters that need to be manually replaced. For example, most survey platforms require that you pass in a survey ID. Let's say that it needs to be placed to **survey_id** -parameter, then your **Base URL** would look like this:

https://surveyplatform.com/survey?survey_id=[SURVEY_ID]

When the template is applied, you only need to change the [SURVEY ID] with the desired target survey ID.

The following pipes are inserted automatically:

- **[id]** variable is for Panelist ID
- **[hash]** variable is for the security hash (inserted only when hashing is enabled)
- **[PROJECT_ID]** variable is automatically be replaced with Sample Ninja project ID)


### Passing variable data to surveys
Data variables can be easily passed using the **Select Data Variables** button to choose the required ones from the available selection.

Parameter names can be fully customized to match what is used in the survey. For example, if **GENDER** is selected, the resulting URL might look like this:

https://surveyengine.com?project=343&g=1

#### Sending Date data to a survey
Dates are passed in ISO dates like 2023-01-26. Optionally you may pass any date variable as age by enabling the "Cast to Age" toggle. A typical use case would be to pass in **BIRTH_DATE** as age.

#### Sending Radio data to a survey
Radio data is piped using the **Option ID** number visible when you edit the **Data Variable**. For example, piping the **EDUCATION** data variable would possibly show the URL as:

https://surveyengine.com?project=[ID]&education=5

#### Sending Checkbox data to a survey
Sample Ninja pipes check box values as multiple values. For example, if using the **HOBBIES** data variable with values 1,2,3 then the URL would be something like this:

https://surveyengine.com?project=[ID]&hobbies=1&hobbies=2&hobbies=3

> Some survey platforms may use alternate formats like hobbies=1,2,3. To accomplish this, enable **Pipe checkbox values as string** toggle.

#### Sending Locale -variable to a survey
Every panelist has an assigned locale, for example, ENG-US. If a multilingual survey is being run, then the **LOCALE** data variable should be piped into the survey.

> Some survey platforms may use alternative locales or languages. Please reach out to support @ sampleninja.io if you run into this situation.

#### Test and send variable data
Sample Ninja will automatically insert random data for all the defined data variable pipes.

> The inserted data for the Keyword and the Text -variable types are static because there is no way for the test data generator to figure out the real intent of the data variable. For example, if **CITY** is piped in, the data set will show as **test_keyword_city**. Similarly, if the example **DESCRIPTION** is used for the text variable, the data set would show as **test_text_description**.
 
### Panelist ID
Panelist ID is automatically piped in the URL and is mandatory. You do not have to define and insert this manually, but instead, you configure your survey entry link param name, and **SampleNinja** will take care of the rest for you. Please save the panelist ID along with the survey responses. This is important when you reconcile participants after reviewing the survey data. By default, the parameter name is **pid**, but you may customize this to match the target survey platform.

```
https://surveyengine.com?pid=343&pid=4b6c7e1e-2ec3-4cc7-975a-5a523d55248f
```

If **Random test ID** is toggled on, Sample Ninja will send a random panelist ID to the test survey when testing the survey link. Sometimes, this makes testing easier, especially if the survey software blocks duplicate IDs.

### Session ID
Sample Ninja now supports projects passing session ID into surveys. When redirected back to Sample Ninja from a survey, the session ID provides backup in case a panelist’s session cannot be found for any reason. This method provides another safeguard so that panelists get compensated. The survey exit redirects become more secure when the session ID is in the URL with hashing enabled.

> It is highly recommended that hashing is enabled, especially when using session ID!

Having session ID available is useful as some survey platforms/exchanges require session ID for deduplication purposes. You may have previously combined project ID + panelist ID to make a unique session key. Now, you can simply use the session ID without doing this.

All manually created projects and redirect exit links now include session ID by default! Sample Ninja will append the "session" parameter to the survey URL, and you will then capture the value in your survey software. When the panelist completes the survey, you will append the session ID to the exit URL to Sample Ninja along with the status code (i.e. completes, profile, quota, etc.).

> Remember to upgrade your project links as soon as possible! Session ID will become mandatory at a later date.

> API projects must be modified to take advantage of this new feature. Please reach out to support @ sampleninja.io for details.


## Signing and security
Signing should always be used if the target platform supports it, as this prevents URL tampering. **Sample Ninja** supports the following algorithms:

The Full URL hashing algorithms: (Recommended)

- SHA256 Full URL (recommended)
- SHA1 Full URL (recommended)
- MD5 Full URL (weak security)

Legacy algorithms: (Not recommended, challenging to program)

- SHA256 Legacy
- SHA1 Legacy 
- MD5 Legacy (weak security)

> The Legacy hash algorithms use URL path + params, while the Full URL hashing uses the entire URL, including protocol and hostname. In addition, the Full URL hashing is more straightforward to implement as no parameter sorting is required.
  
> If you need additional signing algorithms, please contact us, and we will consider adding them.

> You must enable hashing for each project by selecting **algorithm**, **hash param name** and enter the **secret** in the **Sample Ninja -> Projects -> Edit Project -> Survey Links -> Edit survey link**. You can template the entry link configuration for future use.

> **IMPORTANT:** If the computed hash does not match, you should always return the panelist to Sample Ninja with **security** or **s=sec** status. See   [the help file for exit links](/edit-project-links-exit-links.md) for more information.


## Example hash calculations
These examples use actual computed hash values so that you can verify your hash calculations using the examples below. These examples are simplified, and we have deliberately omitted the panelist ID or **pid** parameter.

### Example A (SHA1 Full URL)

In this example, we use the **SHA-1 Full URL** algorithm with secret **MySecretPasscode** to verify that the URL has not been tampered with.

#### Step 1 - Append the secret at the end of the URL
```
https://surveyengine.com/projects?country=US&project_id=10&region=2MySecretPasscode
```
#### Step 2

Calculate hash PHP example:

echo hash('SHA256','https://surveyengine.com/projects?country=US&project_id=10&region=2MySecretPasscode');

ff61ef98ba1eba7c5bc0607b0ef354b79aed2c23e9c1a85507a1886dacf15acb

#### Step 3 - Verify
Verify that the hash parameter supplied by Sample Ninja matches your calculated hash

### Example B (SHA256 Legacy)

In this example, we use the **SHA-256** algorithm with secret **MySecretPasscode** to verify that the URL has not been tampered with.

Survey entry link produced by **Sample Ninja**

```
https://surveyengine.com/projects?project_id=10&region=2&country=US&hash=18f3b4c68014e18a539a80916a937ac61d9a96303cd4f1b66a91c7e7f5afef8f
```

#### Step 1 - Remove protocol, host, and hash -parameter:
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
#### Step 4 - Calculate the hash
Here, we use PHP's built-in hash function (https://www.php.net/manual/en/function.hash.php) with secret **MySecretPasscode**
```
echo hash('SHA256','/projects?country=US&project_id=10&region=2MySecretPasscode');

18f3b4c68014e18a539a80916a937ac61d9a96303cd4f1b66a91c7e7f5afef8f
```
#### Step 5 - Verify
Verify that the hash parameter supplied by Sample Ninja matches your calculated hash

### Example C (SHA-256 Legacy)

In this example we are using **SHA-1** algorithm with secret **MySecretPasscode**

Survey entry link:
```
https://surveyengine.com/projects?country=US&project_id=10&region=2&hash=d86cca325d097945e54e8f394d031e10e17e815f
```
#### Step 1 - Remove protocol, host, and hash -parameter:
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
#### Step 4 - Calculate the hash
```
echo hash('SHA1','/projects?country=US&project_id=10&region=2MySecretPasscode); // PHP example

d86cca325d097945e54e8f394d031e10e17e815f
```

#### Step 5 - Verify
Verify that the hash parameter supplied by Sample Ninja matches your calculated hash

### Example D (SHA-256 Legacy)

In this example, we will be using **SHA-256** algorithm with secret **MySecretPasscode** to verify the value hash supplied by **Sample Ninja**

Survey entry link:
```
https://surveyengine.com/projects??country=US&project_id=10&region=2&hash=b4f323675eb1c43223c990e0dbc55fca2cc30401e97cbe47ab4b7a7a7de90613
```
#### Step 1 - Remove protocol, host, and hash -parameter
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
#### Step 4 - Calculate the hash
```
echo hash('SHA256','/projects?country=US&project_id=10&region=2MySecretPasscode); // PHP example

b4f323675eb1c43223c990e0dbc55fca2cc30401e97cbe47ab4b7a7a7de90613
```
#### Step 5 - Verify
Verify hash parameter supplied by Sample Ninja matches your calculated hash
 
### Example D (SHA-256 Legacy with secure secret)
In this example we are using **SHA-256** algorithm with secret **@$Sup3rS3cur3S3cr3t!!@**

Survey entry link:
```
https://surveyengine.com/projects?p=1435540&r=2&c=US&g=1&hash=93ce7437be0603c5dd244ef31951bac690f367f67b889d26bf5751781385afbc
```

#### Step 1 - Remove protocol, host, and hash -parameter
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
#### Step 4 - Calculate the hash
```
echo hash('SHA256','/projects?c=US&g=1&p=1435540&r=2@$Sup3rS3cur3S3cr3t!!@'); // PHP example

93ce7437be0603c5dd244ef31951bac690f367f67b889d26bf5751781385afbc
```
#### Step 5 - Verify
Verify hash parameter supplied by Sample Ninja matches your calculated hash.





