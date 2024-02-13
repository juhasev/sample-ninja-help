## PayPal

PayPal integration enables you to distribute cash rewards to your panelists in a very convenient way. To use PayPal rewards, the user must register a commercial developer account with PayPal.

1) Create a new Application in PayPal and call it something descriptive like **SampleNinja**
2) You grant permission for the Application to use **Payouts** and **Transaction Search**

Once the account API keys have been obtained, click the **configure** button to enter the keys. First, select the appropriate **Environment** and then enter the **Client ID** and **Secret required**. If everything went successfully, you should see the account balance(s) loaded.

> Sometimes, you must contact **PayPal** to enable the **Payouts** API access for the application, as it may be disabled for security reasons. If true, you will likely see **FAILED** transactions in the Redemptions History. If you mouse over the elements, you likely see **AUTHORIZATION_ERROR** in the popup.

> **IMPORTANT!** To distribute PayPal rewards in multiple currencies, you must add the funds in that currency into your account. Sample Ninja does not support currency conversions due to the high fees imposed by PayPal. Once you have multiple currencies on your account, you can select rewards for that currency.

#### Manage Rewards

Select the nominations and currencies you would like to offer. Maximum nomination for USD, GBP, and EUR is 200, others 1000.

#### Disable

Disables PayPal rewards.
