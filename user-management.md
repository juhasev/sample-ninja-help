## User Management

### Creating new users
At the top of the screen, you have a **PLUS** button to invite more users as well as a **CLOCK** icon that allows you to view any pending invitations. Creating a user is simple, simply enter the user's full name and email address along with the roles the user should have. Sample Ninja will then send an invitation for the user to join.

> Please note that all user invitations expire after 7 days. You can re-invite the user to join again.

> Only users with the Admin role can invite other users!

### Roles
Sample Ninja comes pre-loaded with various roles you would expect to find in most panels. By clicking the roles button, you can customize which roles each user has and view the individual permissions for each role.

> Only users with the Admin role can assign roles to the users!

> If you would like to create a custom role you can do so by clicking the roles tab and then click on **PLUS** icon.

### Login audit
Contains a complete audit trail of user logins. The list contains important information, such as IP address, location, and whether 2-factor authentication was successful. Use the search box to find a specific user by email or IP address.

### Login audit
The **LOGIN AUDIT** tab keeps a trail of login attempts made to your panel's admin console. Each entry records when the attempt happened, who attempted it, the IP address and approximate location it came from, whether the password was correct, whether the second factor succeeded (and whether it was verified by SMS code or by a trusted device), and the overall outcome. Failed two-factor attempts are kept permanently, so repeated verification failures on an account are always visible. You can search the trail by email address or IP address.

> The location is derived from the IP address and may be empty when it cannot be determined reliably.

> Attempts blocked by rate limiting are rejected before credentials are checked and do not appear in the list.

> Access to the login audit is controlled by the **View login audit** permission. Administrators have it by default, and you can grant it to any custom role, including a read-only role for someone who should review the trail without being able to manage user accounts.
