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

#### FAKE EMAIL
Email does not resemble name, initials or birthdate.

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
