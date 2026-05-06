## Bounced emails
Emails can bounce for multiple reasons. This section gives you detailed information about the bounces and their types. A bounce type can be one of the following:

- **Permanent** This means that the email address no longer exists.
- **Transient** The email box may be full, or there may be another temporary issue.
- **Undetermined** The target email server responded with a bounce but did not provide enough information to determine whether the bounce is **Permanent** or **Transient**

> If you want to download a CSV of all bounced emails, click on the top right corner of the window.

> To copy individual panelist IDs, click the round information button on each row.

### Permanent bounces

All panelists with **Permanent** bounces are automatically unsubscribed from the panel. This is because if you keep sending emails to the bounced email addresses, your email reputation will worsen. Permanent bounces are normal, but should be way under < 1%. 

> The sampling engine will stop automatically if you exceed a 7% bounce rate. You must contact support@sampleninja.io and talk with us.

If you run into this issue, there is something badly wrong with the imported panelists. Typically, these are:

- Your migrated panelist database is too old
- The uploaded panelists are not double-opted in
- You are migrating from another panel system that did not handle bounce processing at all.

> Consider using third-party tools to remedy the situation, like [Zero Bounce](https://www.zerobounce.net), or worst case scenario, run all your panelists through the **Registration Survey** in **Sample Ninja** and reach out to them using a third-party marketing tool like **Mail Chimp** or **Constant Contact**.

Please contact support@sampleninja.io if you are unsure how to rectify the situation.

> The EMAIL_VALID data variable is automatically set to "No" for these panelists to prevent subsequent email sends, which would affect your email reputation.

### Transient or soft bounces

The transient bounces have multiple subtypes:

- **General** The recipient's email provider sent a general transient bounce. This typically happens when the recipient has set up an "out of the office" automatic reply. This type of soft bounce generally resolves on its own. If the bounce resulted from an "out of the office" reply, the soft bounce resolves after the recipient removes the automatic reply.
- **MailboxFull** The recipient's mailbox is full and can't accept any more emails. You can send emails to the same recipient later when their mailbox is no longer full.
- **ContentRejected** The recipient's mail server doesn't allow the content of the email. You can resolve this type of bounce by modifying your email content.

These do not happen with project invitations, as you cannot create an email that is too large, nor can you add attachments.

- **MessageTooLarge** The recipient mail server can't accept the email because the file size of the message is too large. You can resolve this bounce by reducing the size of your message.
- **AttachmentRejected** The email contains an unacceptable attachment. Some email providers block emails with attachments of a certain file type or large attachments. After you remove or modify your email attachments, you can try to send the email to this recipient again.

> **Sample Ninja** does not currently collect information on the sub-types. We are looking to bring support soon.
