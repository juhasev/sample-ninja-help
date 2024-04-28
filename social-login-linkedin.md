### LinkedIn Authentication
LinkedIn authentication provides a convenient way for you panelists to register and log in to the Member App. Getting LinkedIn authentication requires creating a new app. You must link the app to the business account you may already have. At the end, you will obtain the Client ID and Client Secret from the app settings

https://learn.microsoft.com/en-us/linkedin/consumer/integrations/self-serve/sign-in-with-linkedin-v2

Once the app has been created, you can obtain the **Client ID and Client Secret** under the **Auth** tab. You must enter **Authorized redirect URL**

```
https://clientname.panelservice.io/auth/linkedin-openid/callback
```

Replace the hostname with your own, which you see when logged in to the Sample Ninja, in the browser's URL bar.
