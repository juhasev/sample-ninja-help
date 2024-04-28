## Google Sign-In

Google sign-in provides a convenient way for your panelists to register and log in to the Member App. Getting Google sign-in to work requires creating a Google Cloud account. Ultimately, you will obtain the App ID and Secret from the app settings. Google authentication is one of the easiest to set up and literally takes only 5 minutes to do.

https://developers.google.com/identity/sign-in/web/sign-in

Sign in to the Google Cloud or create an account if you don't already have one.

https://console.cloud.google.com/

1) Select **APIs and Services**
2) Select **Credentials**
3) Click on the **Create credentials** button at the top
4) Select **OAuth client ID**
5) Select **Web Application** from the **Application type** pulldown
6) Enter a name such as **SampleNinjaGoogleSignIn**
7) Under **Authorized redirect URIs** click on **ADD URI** button and follow the **Creating the redirect URI** instructions below.
8) Click create and copy **Client ID** and **Client Secret** to Sample Ninja under **Panel Settings -> Integrations -> Google Sign-in**

#### Creating the redirect URI

Copy the base URL in the browser's address bar when logged into Sample Ninja. For example:
```
https://clientname.panelservice.io
```
Then add
```
/auth/google/callback
```
You will end up 
```
https://clientname.panelservice.io/auth/google/callback
```
Enter this URL as **Redirect URI**
