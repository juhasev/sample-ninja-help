### Facebook authentication

You'll need to obtain Facebook credentials and create a Facebook app. In return, Facebook will provide the credentials you enter to **Sample Ninja**. Before you begin, you should create **Meta Business Portfolio**. More info below:

https://www.facebook.com/business/help/1710077379203657?id=180505742745347

Start the process by clicking "Log In" on the page below.

https://developers.facebook.com/products/facebook-login

The Facebook authentication is very simple to configure.

1) Once logged in click **Create App** button.
2) Next, select **Authenticate and request data from users with Facebook Login**
3) Select **Not building a game**
4) Provide app name, contact email, and link to your **Meta Business Portfolio**
5) Go to the app settings and supply Valid OAuth Redirect URIs

#### Creating the redirect URI

The base URL you see in the browser's address bar when logged into Sample Ninja. For example:
```
https://clientname.panelservice.io
```
Then add
```
/auth/facebook/callback
```
You end up 
```
https://clientname.panelservice.io/auth/facebook/callback
```
Accept the defaults to all the other settings and save.

### Permissions
You must enable both **email** and **public_profile** in the **Permissions**

> Don't hesitate to contact support at support@sampleninja.io if you need assistance.

### Business verifications
Next, complete the business verification.
https://www.facebook.com/business/help/2058515294227817?id=180505742745347

### App review
Complete the app review and answer all the questions.

### Submit your app for approval
This process can take up to 10 days to complete.
