## ID Check

**ID Check** verifies the identity of new panelists when they register. It is powered by **Verisoul**. The panelist takes a photo of a government-issued identity document and a selfie, and Verisoul checks that the document is genuine and that the person in the selfie matches it.

> **ID Check is available in Sample Ninja, but it is not active on your panel by default. To activate it, please contact our sales team.**

#### How it works

When **ID Check** is turned on for a registration survey, the panelist starts the ID check after confirming their email address. If the sub-panel does not use double opt-in, or the panelist registers with a social login, the ID check starts right after the registration survey.

The registration is completed only when the ID check is approved. The possible results are:

- **Approved**: the registration is completed as usual.
- **Approved, but suspicious**: the registration is completed, and the panelist gets a security flag.
- **Needs another try**: the photos could not be read or the selfie check failed. The panelist can start the check again.
- **Declined**: the document was judged fake. The registration is not completed, and the panelist gets a security flag.

Panelists who passed the check have a shield icon after their name in the **Panelist Manager**.

#### While the check is not finished

Until the ID check is approved, the registration shows **ID pending** in **Registration activity**, and a declined check shows **ID declined**. A registration is shown as **Confirmed** only after the check is approved.

These actions also wait for the approval instead of the email confirmation:

- The **Email confirmed webhook** call.
- The conversion report to your recruitment partner.
- The referral reward of the panelist who invited them.

A panelist who left the ID check can finish it later by clicking the confirmation link in their email again. When **Send reminders** is on in **Survey options**, they also receive one **ID check reminder** email 24 hours after their last attempt. You can edit it in **Sub Panels -> Manage -> Email Templates -> Transactional -> ID check reminder**.

#### Landing pages

ID Check adds four landing pages to each sub-panel, which you can edit and translate like any other landing page:

- **ID check in progress**: shown while the result is being checked.
- **ID check needs another try**: shown when the panelist must repeat the check.
- **ID check declined**: shown when the identity could not be verified.
- **ID check unavailable**: shown when the check cannot start, for example during a service outage.

#### How to enable ID Check

Once ID Check has been activated on your panel by our sales team:

- Purchase service credits under **Settings -> Service Credits**. Each ID check is paid from your service credits.
- In **Sub Panels**, open the registration survey of the sub-panel you want to protect and turn on **ID Check** under **Survey options**.

> Each check is priced at **$0.20**. A check is charged when it reaches a final result, so declined, abandoned, and repeated checks are charged too.

#### Validity

An approved ID check is valid for 365 days by default. You can change this under **Settings -> Basic settings -> ID verification validity**.
