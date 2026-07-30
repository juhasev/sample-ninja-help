## reCaptcha by Google
reCAPTCHA uses an advanced risk analysis engine and adaptive challenges to keep malicious 
software from engaging in abusive activities on your website. Meanwhile, legitimate users will 
be able to login, make purchases, view pages, or create accounts and fake users will be blocked.

[Read more about reCaptcha](https://www.google.com/recaptcha/about)

> Sample Ninja recommends that you always use reCaptcha validation. When enabled it will be used 
> during the built-in registration survey as well as with all password reset requests.

### Where it is used

Once enabled, reCaptcha protects every place a panelist can create an account or set a password:

- The registration survey, when **Use Google reCaptcha** is on for that registration survey
- Password reset, both from the link in a reset email and through the member's app
- Setting a password for the first time, from the link in a create-password email and through the
  member's app
- The member's app sign-in check that decides whether a password is required

> The registration survey has its own switch under **Sub panels** -> **Registration survey** ->
> **Survey options**. The password screens follow this integration: if reCaptcha is enabled here,
> they use it.

### Creating an account
In order to use reCaptcha you must create an individual or a corporate account. 

> If you are operating a very large panel then we recommend you get commercial subscription allowing you to do unlimted reCaptcha validations. 

Once you have signed to the dashboard you must create a new site. Use the following settings

- reCaptcha type: v2 Checkbox
- Domain, enter the top level domain name you are using. The default is sampleninja.io.
- Check "Verify the origin of reCAPTCHA solutions"
- Check "Send alerts to owners"

### If reCaptcha cannot be reached

If Google's verification service cannot be reached, registrations and password requests are allowed
through without being checked, rather than being refused. This is deliberate: a problem at Google's
end would otherwise stop every genuine registration for as long as it lasted.

> The trade-off is that while Google is unreachable, every screen listed above has no bot protection
> at all: registration, both password reset paths, both create-password paths and the member's app
> password check. These outages are recorded as errors and raised to your error monitoring, so the
> gap is visible and you can see how long it lasted.

> Only an unreachable verifier is waved through. A wrong, expired or already-used answer is still
> rejected exactly as before.

> If you see a burst of registrations that look automated, check whether it lines up with a
> reCaptcha outage in that period before assuming the check was misconfigured.
