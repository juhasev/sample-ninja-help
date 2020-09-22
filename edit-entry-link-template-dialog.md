# Entry link templates

Templates allow you to define entry link for your target interview platform

For example you may define template for the survey engine you use all the time. When you define template URLs you can use place holders that need to be manually replaced for each project you run. For example you base URL could look like this:

>`https://surveyengine.com?project=[ID]`

## Piping data variables to surveys

You can easily pipe data variables to survey simply my selecting the data variables you would like to pipe.

You can fully customized the parameter names to match what you use in the survey. The default parameter name is the data variable name. For example if you selected GENDER the resulting URL might look like this

>`https://surveyengine.com?project_id=343&gender=1`

If you customize parameter name to just letter "g" the URL would look like this


>`https://surveyengine.com?project_id=343&g=1`

## Panelist ID

Panelist ID is automatically placed on the URL. You need to be able to save this value along with the survey responses if you need to able to match panelists to their survey answers i.e. to more detailed data analysis. By default the parameter name is `PID` but you may customize this to match the target platform.

>`https://surveyengine.com?project_id=343&pid=4b6c7e1e-2ec3-4cc7-975a-5a523d55248f`

## Signing and security
You should always use signing if your target platform supports it. This prevents URL tampering. Sample Ninja supports

`MD5` `SHA1` `SHA256` signing algorithms.

If you need additional signing algorithms please contact us and we will consider adding them

Signing will verify the path and query part of a survey's URL (i.e., not the protocol/host), including the leading slash. Let imagine you have the following URL

>`https://surveyengine.com/projects?project_id=10&region=2`

Signature or hash will be calculate using

>`/projects?project_id=10&region=2`

And appended at the end of the URL using the specified parameter name for example

>`/projects?project_id=10&region=2&signature=325436AB32C324528800023AB`

Please note that these examples are simplified and we have intentionally omitted `PANELIST_ID` or `PID` parameter.