### LinkedIn Sign-in

LinkedIn sign-in provides a convenient and passwordless way for your panelists to register and log in to the Member App. Getting LinkedIn authentication requires creating a new app and linking it to the business account you may already have. In the end, you will obtain the Client ID and Client Secret from the app settings.

https://learn.microsoft.com/en-us/linkedin/consumer/integrations/self-serve/sign-in-with-linkedin-v2

Once the app has been created, you can obtain the **Client ID and Client Secret** under the **Auth** tab. You must enter **Authorized redirect URL**

#### Creating the Authorized redirect URL

Copy the base URL in the browser's address bar when logged into Sample Ninja. For example:
```
https://clientname.panelservice.io
```
Then, add the following to the base URL.
```
/auth/linkedin-openid/callback
```
You will end up 
```
https://clientname.panelservice.io/auth/linkedin-openid/callback
```

Enter this URL as **Authorized redirect URL**
