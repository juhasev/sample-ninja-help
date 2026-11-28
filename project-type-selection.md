## Project types

### Auto Sampling
Auto Sampling is the everyday project type. Sample Ninja picks the participants at random from everybody who matches the qualifications and quotas selected in the project properties. Invitations go out in small waves paced by the project duration and the number of target completes, so the project runs to completion with minimal waste and the panel is not over sampled. This is good for the panelist experience, as your panelists will experience fewer profile and quota terminations. The panel business rules are always obeyed. The maximum number of target completes is 50,000.

### Uploaded Sample
The Uploaded Sample project (formerly called Recontact) invites a list of panelists that you upload. This is handy for recontacts, where you need to invite certain panelists back, for example after survey programming errors or for a follow-up wave. It can also be used whenever you want to invite a group of hand-selected panelists. The maximum number of uploaded panelists is 10,000.

Extra columns in the uploaded CSV file are passed to the survey as URL parameters, and the project can use quotas. Without quotas everybody on the list is invited right away and the panel business rules are not applied. With quotas the list is sampled towards the quota targets and the panel business rules are obeyed.

> **TIP:** If you want to test the invitation flow, the Uploaded Sample project is the easiest way to invite yourself to a project.

### Profiler
The Profiler project is for external surveys that build deeper panelist profiles. It is suitable for cases where **Dynamic Profiling** cannot be used, for example, when you need complex profiling logic that is only possible in advanced survey software. You can bring the collected profiles back to Sample Ninja using the **Panelist Importer**'s update mode.

> **TIP:** Remember to publish profiler projects to anyone who qualifies + add an engagement image under Project Settings -> Member App.
> 
A profiler project has no settings for “target completes” or “end date”. It keeps inviting matching panelists at a steady rate, including those who join the panel later, until you close it. Profiler surveys sample at a constant rate of 400 invitations / h * Sampling Priority set in the project properties. For example, if you set “sampling priority” to 5 then a profiler project will send 400 * 5 = 2000 invitations per hour. The profiler surveys do not trigger out-of-sample warnings because they are by nature out of sample all the time. The panel business rules are always obeyed.

> **TIP:** If you want to invite the entire panel, use the **STATUS** variable and select **Subscribed** in your Project -> Qualifications.

If you are starting a new profiling in an existing panel, consider the profiler survey's impact on the other projects you run. A profiler project can quickly invite your entire panel and thus can steer available sample from your other live projects depending on the established business rules. The default business rules limit how often a panelist can be invited to a project in a given period. See Business Rules under Settings from the main menu.

> **WARNING:**  Do not remove the Activity Filter from the Business Rules! This will most certainly have negative consequences on your panelists, as they may get multiple survey invitations per day. Thus, it is like asking your panelist to press that unsubscribe button.

### Qualitative
The Qualitative project is for focus groups, interviews and other studies that have no survey link. No email invitations are sent, so the project has no invitation, welcome page or survey link settings.

You upload the participants in the same way as in an Uploaded Sample project. Once the project is online they appear in the project's participant list as invited, and you set the status of each one by hand from the participant's menu: **Start interview** first, and then **Complete interview** or one of the terminate options (profile, quota, quality or duplicate).

The reward set in the project's compensation is granted when you mark a participant as completed.
