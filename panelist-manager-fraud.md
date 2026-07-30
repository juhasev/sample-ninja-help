## Fraud
The level of fraud is determinated by issuing security events for various reasons. The fraud score is recorded to system variable FRAUD_SCORE and can be used in filtering and queries. Essentially the fraud score increments for any security events and descrements for good behavior.

### Event types

#### IS PROXY
Panelist is using public VPN service or other service that masks users true location.

#### IS HOSTED
Panelist IP address is originating from a hosted server. Servers are typically used
as proxies to hide users true location.

#### IS BOT
Panelist is detected as bot.

#### IP MISMATCH
Panelist IP address changed in the middle of the project.

#### DUPLICATE FINGERPRINT
Duplicate project fingerprint.

#### FINGERPRINT MISMATCH
Project fingerprints do not match from start to end.

#### IS OUT OF COUNTRY
Panelist is out of country.

#### LOCATION
Impossible location change for example LA to New York in 2 hours.

#### LINK MANIPULATION
Panelist has potentially engaged in link manipulation. This security event can triggered if link hash validation fails or panelist completes a project under 5% of estimated project LOI.

#### REFER FRIEND
Refer a friend error or potential abuse. Multiple checks are run for example if we detect that panelist referred themself with a new email or is otherwise attempting to create multiple accounts.

#### SURVEY SECURITY
Returned back from a survey with security status.

#### DUPLICATE
Survey exit duplicate or reconciled as duplicate.

#### COOKIED DELETED
Panelist deleted tracking cookie intentionally or using a incognito window. It is very unsual to delete cookies repetably unless you are trying game the system using ingognito window, virtual machine, residentiual proxy etc... Repeated warning here should not be taken lightly. You may ask yourself when did you delete you cookies last time?

#### STOLEN COOKIE
Panelist device contained cookie that belongs to an another panelist. If you see this security event, it is likely that the panelist has registered multiple accounts to game the system.

#### SPOOFED LOCATION
Panelist is attempting to hide their true location. Sample Ninja runs WebRTC check which in many cases reports back user's true location. WebRTC is enabled by default in all browsers and basically enables you to participate in video conferences. If WebRTC is disabled is very likely the panelist is intentionally trying to hide their through location.

#### LIKELY PROXY
If panelist WebRTC check does not pass then Sample Ninja measures cross ping latency to determine if potential proxy sits in between the user and the requesting IP address. Its worth noting that vast majority of Internet connected devices are always behing NAT and thus cross ping cannot be run. If you see this event then it is very likely panelist is trying to hide their real location using proxy services.

#### COMPLETED, PROFILE and QUOTA
Each time panelist completes project with status "completed","quota" or "profile" the FRAUD score is decreased or healed to reward for good behaviour.

### Which checks are running

Most of the checks above are switched per sub-panel under **Sub panels** -> **Security**, so the
same panelist can be terminated on one sub-panel and let through on another. If you are expecting
an event type and never see it, check that switch first.

Two are worth calling out because operators are often surprised by them:

- **IP MISMATCH** only runs when **IP address** is on for that sub-panel. It is strict: a respondent
  moving between wifi and mobile data changes IP address without any dishonest intent.
- **DUPLICATE FINGERPRINT** only affects the score when **Fingerprint mismatch** is on. With that
  switch off the event is still recorded so you can see it, but no points are taken away.

### Points shown against an event

Each event shows the points that were actually taken away when it was recorded, not the current
configured value for that event type. An event recorded while its check was switched off shows no
deduction.

> Events recorded before this was introduced have no stored value, so they still show the current
> configured points for their event type. If you are reconciling a long history, treat the older
> entries as indicative rather than exact.

A panelist who returns to the same project while still failing the same check is flagged and
redirected again, but is only charged once for that event on that project.
