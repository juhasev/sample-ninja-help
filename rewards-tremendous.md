## Tremendous

Tremendous lets you reward panelists with merchant gift cards, prepaid Visa cards, PayPal payouts, bank transfers and charity donations across 200+ countries and dozens of currencies. Rewards are delivered by Tremendous directly to the panelist's email address, so there is nothing extra for you to send.

If you do not have a Tremendous account yet, visit www.tremendous.com to create one.

#### Before You Start

You will need:

1. A Tremendous account with a funded balance (**Tremendous dashboard → Billing**). Rewards are paid from this pre-funded balance.
2. An API key, created in the Tremendous dashboard under **Team settings → Developers → API keys**.

> Keep your API key secret. Anyone holding the key can send rewards from your balance. The key is stored encrypted and is never displayed again after saving — if you lose it, create a new one in the Tremendous dashboard and update the configuration.

#### Configure

1. Click the **Configure** button on the Tremendous card.
2. Select the environment: **Sandbox (testing)** or **Live (production)**.
3. Paste your API key and click **Save**.
4. Click **Enable** to make Tremendous rewards available to your panelists.

Saving the configuration automatically downloads the Tremendous product catalog in the background. This normally takes under a minute.

To change the environment or replace the API key later, open Configure again and flip the **Replace credentials** switch. Leaving the switch off keeps your stored key unchanged.

#### Testing (Sandbox)

Sandbox mode connects to the Tremendous "testflight" environment where orders never draw real funds. The testflight environment is completely separate from your live account — create a separate account and API key at **testflight.tremendous.com**.

> Do not use the sandbox mode in production. Sandbox rewards are not real and panelists would receive nothing of value.

#### Manage Rewards

Click **Manage Rewards** to open the catalog:

- The **Catalog** tab lists every product available to your Tremendous account. Use the search field and the country selector to narrow the list. Click **Select** on a product to choose the denominations (card values) you want to offer, or add a custom value within the product's allowed range.
- The **Rewards** tab shows what your panelists currently see. From here, you can review, inspect (description and legal disclosure), and delete individual reward values.

Each product defines which countries, currencies, and value ranges it supports. Panelists are only shown rewards matching their local currency.

The catalog refreshes automatically once a day. If Tremendous retires a product, the related rewards are removed from your offering automatically.

#### How Redemptions Work

1. A panelist redeems a Tremendous reward in the member app. Points are deducted immediately.
2. The redemption waits for approval in **Redemption Approvals** (like any other partner).
3. Once approved, the system places the order with Tremendous within a few minutes.
4. Tremendous emails the reward to the panelist's registered email address. The panelist picks how to receive the value if the product allows choices.

The email sender name, logo, and colors can be customized in your Tremendous dashboard.

#### Balance

The figure shown on the Tremendous card is the available amount of your pre-funded Tremendous balance. Pending top-ups are not included until Tremendous clears them.

If the balance runs out, affected redemptions are **soft-failed**: the panelist keeps their redemption, administrators are notified, and the redemption can be retried from the Redemptions screen after you top up your account. After three failed attempts, the redemption is refunded to the panelist automatically.

#### Resending a Reward

If a panelist reports a missing reward email, open **Redemptions**, locate the redemption, and click **Resend**. Tremendous re-delivers the reward to the original recipient's email address.

> Tip: ask the panelist to check their spam folder first — reward emails occasionally end up there.

#### Troubleshooting

- **"Failed to retrieve balance"** on the Tremendous card — the API key is invalid, was revoked, or belongs to the wrong environment (sandbox key with Live mode selected, or vice versa). Re-check the configuration.
- **Catalog is empty** — the initial download may still be running; use the refresh button in the catalog dialog. If it stays empty, verify the API key.
- **Redemptions stuck in soft-failed state** — usually an empty balance or a temporary Tremendous outage. The notification you received names the cause and the fix. Retry from the Redemptions screen once resolved.
- **Order shows PENDING** — the order is awaiting settlement or a manual approval rule configured in your Tremendous dashboard. The system checks pending orders every few minutes and completes them automatically. For fully automatic processing, disable order approvals in the Tremendous dashboard (**Team settings → Approvals**).

#### Disable

Disables Tremendous completely. Your panelists can no longer see or request Tremendous rewards, and approved Tremendous redemptions will not be processed until you re-enable the integration. Your configuration and reward selection are kept.
