## Survey Entry Link

The survey link defines where the panelists are sent to after they respond to the invitation. Additionally you can pipe data and enable URL security via hashing.

Templates allow you to define entry link templates for the most common survey platform that you send sample to.

For example you may define template for the survey platform that you use all the time. When you define template URLs you can use place holders that need to be manually replaced for each project you run. For example your base URL could look like this:

https://decipher.com?project=[ID]

> The default link for new projects points to Sample Ninja **Test Survey** that can be used in place of actual survey for testing purposes.

### Piping data variables to surveys
You can easily pipe data variables simply my selecting the data variables you would like to pipe.

You can fully customized the parameter names to match what you use in the survey. For example if you selected GENDER the resulting URL might look like this

https://surveyengine.com?project_id=343&g=1

If you customize parameter name to just letter "gender" the URL would look like this

https://surveyengine.com?project_id=343&gender=1

#### Piping checkbox values
Sample Ninja pipes check box values as multiple values. For example if your HOBBIES are 1,2,3 the URL would be something like:

https://surveyengine.com?project=[ID]&hobbies=1&hobbies=2&hobbies=3

> Some survey platform may use alternate formats like hobbies=1,2,3. Please contact support@sampleninja.io if you run into this situation.

#### Test link and data variable pipes
Sample Ninja will automatically insert random data for all the defined the data variable pipes.

> The inserted data for the Keyword and the Text -variable types is static because there is no way for the test data generator to figure out the real intent of the data variable. For example if you pipe in **CITY** you will see data set as **test_keyword_city**). Similarly for text variable let's call it **DESCRIPTON** you would see data set as ***test_text_description**.

#### Piping locale
Every panelist has assigned locale for example ENG-US. If you are running multilingual survey then should pipe data variable **LOCALE** into the survey.

> Some survey platforms may use alternative locales or languages. Please contact support@sampleninja.io if you run into this stuation.

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

