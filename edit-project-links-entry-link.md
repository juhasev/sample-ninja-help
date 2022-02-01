## Survey Link

The survey link defines where panelists are sent after they respond to invitations. Additionally you can pipe panelist ID, data variable data and enable URL security via hashing.

> The default link for new projects points to **Sample Ninja - Test Survey** that can be used in place of an actual survey for testing purposes. When using the test survey you can manually select survey outcome i.e. COMPLETED, QUALITY, QUOTA etc...

## Survey link templates
Templates allow you to pre-define survey link templates for the most common survey platforms that you send sample to. When you define templates you can use place holders for URL parameters that need to be manually replaced. For example most survey platform require that you pass in a survey ID. Let's say that it needs to be placed to **id** -parameter, then you **Base URL** would look like this:

https://surveyplatform.com/survey?id=[ID]

When the template is applied you would only need to change the [ID] with desired target survey ID.

The following pipes are inserted automatically depending on how they are configured
**[pid]** is reserved for Panelist ID
**[hash]** is reserved for the security hash (inserted only when hashing is enabled)
**[PROJECT_ID]** if you use this placeholder it will be automatically be replaced with Sample Ninja project ID.

### Piping data variables to surveys
You can easily pipe data variables simply my selecting the data variables you would like to pipe.

You can fully customized the parameter names to match what you use in the survey. For example if you selected **GENDER** the resulting URL might look like this

https://surveyengine.com?project=343&g=1

#### Piping radio data
Radio data is piped using the **Option ID** number visible when you edit the **Data Variable**. For example piping **EDUCATION** data variable:

https://surveyengine.com?project=[ID]&education=5

#### Piping checkbox data
Sample Ninja pipes check box values as multiple values. For example if your HOBBIES are 1,2,3 the URL would be something like:

https://surveyengine.com?project=[ID]&hobbies=1&hobbies=2&hobbies=3

> Some survey platforms may use alternate formats like hobbies=1,2,3. Please contact support@sampleninja.io if you run into this situation.

#### Piping locale
Every panelist has assigned locale for example ENG-US. If you are running multilingual survey then should pipe data variable **LOCALE** into the survey.

> Some survey platforms may use alternative locales or languages. Please contact support@sampleninja.io if you run into this stuation.

#### Test link and data variable pipes
Sample Ninja will automatically insert random data for all the defined the data variable pipes.

> The inserted data for the Keyword and the Text -variable types is static because there is no way for the test data generator to figure out the real intent of the data variable. For example if you pipe in **CITY** you will see data set as **test_keyword_city**. Similarly for text variable let's call it **DESCRIPTON** you would see data set as **test_text_description**.
 
### Panelist ID
Panelist ID is automatically piped on the URL. You should save the panelist ID along with the survey responses. This important for reconsilidation i.e. if you need to disqualify some participants after survey data has been reviewed. By default the parameter name is **pid** but you may customize this to match the target survey platform.

https://surveyengine.com?project_id=343&pid=4b6c7e1e-2ec3-4cc7-975a-5a523d55248f

If you toggle on **Random test ID** SampleNinja will send random panelist ID to your test survey when testing the survey link. In some cases this makes testing easier especially if duplicate IDs are blocked by the survey software.

### Signing and security
You should always use signing if your target platform supports it. This prevents URL tampering. Sample Ninja supports the following algoritms:

- MD5 
- SHA1 
- SHA256

> If you need additional signing algorithms please contact us and we will consider adding them.

Signing will verify the path and query part of a survey's URL (i.e., not the protocol/host), including the leading slash. Let imagine you have the following URL

https://surveyengine.com/projects?project_id=10&region=2

Signature or hash will be calculate using

/projects?project_id=10&region=2

And appended at the end of the URL using the specified parameter name for example

/projects?project_id=10&region=2&signature=325436AB32C324528800023AB

> Please note that these examples are simplified and we have intentionally omitted panelist ID or **pid** parameter.

