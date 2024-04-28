## Microsoft Sign-in

Microsoft authentication provides a convenient way for your panelists to register and log in to the Member App. Getting Microsoft authentication to work requires creating an Azure account. At the end, you will obtain the App ID and App Secret from the app settings. Microsoft authentication is one of the easiest to set up and literally takes only 5 minutes to do. There is no need to submit any company verification documents. The Azure base account works and is completely free.

https://www.azure.com

When you log in to Azure, find **App registration** (under Identities) or type **App Registrations** to the search bar.

1) Click on **New registration**
2) Select the supported account types (you may select business accounts only or optionally allow personal accounts)
3) Configure the redirect URI

#### Creating the redirect URI

Select **Web** from the dropdown. The base URL you see in the browser's address bar when logged into Sample Ninja. For example:
```
https://clientname.panelservice.io
```
Then add
```
/auth/microsoft/callback
```
You end up 
```
https://clientname.panelservice.io/auth/microsoft/callback
```
Accept the defaults to all the other settings and save. Copy the **Application (client) ID** and paste it into the **Client ID** field in Sample Ninja.

#### Create client secret

Click on **Add a certificate or secret** link and then click **New client secret** button. Enter a description like "SampleNinjaSecret" and select 24 months expiration.

Next, copy the **value** field and enter that into the Sample Ninja as **Client Secret**. Remember to enable **Microsoft Social Authentication** in Sample Ninja. Click save, and you're done.

> **NOTE** Put the expiration date in your calendar, as you must rotate the secret every two years.

> Please visit the **Sub Panels** and edit settings for each sub-panel you want to enable Microsoft sign-in.
