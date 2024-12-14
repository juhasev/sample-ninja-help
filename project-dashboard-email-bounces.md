## Bounced emails
Emails can bounce for multiple reasons. This section gives you detailed information about the bounces and their types. A bounce type can be one of the following:

- **Permanent** This means that the email address no longer exists.
- **Transient** The email box may be full, or there may be another temporary issue.
- **Undetermined** The target email server responded with a bounce but did not provide enough information to determine whether the bounce is **Permanent** or **Transient**

Contact support@sampleninja.io if you are unsure how to rectify the situation.

> If you want to download CSV of all bounced emails, click on the top right corner of the window.

> To copy individual panelist IDs, click the round information button on each row.

> All **Permanent** bounces are automatically unsubscribed from the panel. This is because if you keep sending emails to the bounced email addresses, your email reputation will worsen.

### Transient or soft bounces

The transient bounces have multiple subtypes:

- **General** The recipient's email provider sent a general transient bounce. This typically happens when the recipient has set up an "out of the office" automatic reply. This type of soft bounce generally fixes itself. If the bounce resulted from an "out of the office" reply, the soft bounce resolves after the recipient removes the automatic reply.
- **MailboxFull** The recipient mailbox is full and can't accept any more emails. You can send emails to the same recipient later when their mailbox is no longer full.
- **ContentRejected** The recipient mail server doesn't allow the content of the email. You can resolve this type of bounce by modifying the content of your email.

These do not happen with project invitations as you cannot create an email that is too large neither can you add attachments to your emails.

- **MessageTooLarge** The recipient mail server can't accept the email because the file size of the message is too large. You can resolve this bounce by reducing your message size.
- **AttachmentRejected** The email contains an unacceptable attachment. Some email providers block emails with attachments of a certain file type or large attachments. After you remove or modify your email attachments, you can try to send the email to this recipient again.

> **Sample Ninja** does not currently collect information on the sub-types. We are looking to bring support soon.
