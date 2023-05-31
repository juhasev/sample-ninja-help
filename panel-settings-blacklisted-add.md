## Add Blacklisted Items

To prevent unauthorized access, you can add blacklisted items such as emails and/or IP addresses. 
This allows you to block specific users or sources from accessing surveys.

To add blacklisted items, simply paste a list of emails, IP addresses, or a combination of both. 
Each line represents a new item. 
If you want to add a combination of an email and IP address, separate them with a comma.

Here are some examples:

```text
panelist-one@example.org
panelist-two@example.org,127.0.0.1
192.168.1.1
189.230.120.48,panelist-three@example.com
```

In the above examples, four blacklist items will be added to our system.

---

Once an item is blacklisted, specific actions are taken based on the type of item:

- If a user tries to access a survey using a blacklisted IP address, they will receive a "404 Not Found" page, indicating that the survey is unavailable.
- If a user tries to access a survey using a blacklisted email, they will be automatically redirected to a security page for further verification.

By managing the blacklist, you can enhance the security of your system and protect your surveys from unwanted access.
