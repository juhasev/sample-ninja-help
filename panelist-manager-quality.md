## Quality Events (BETA)

The quality events are used to calculate quality score between 0 and 100 for each panelist. The quality score is recorded to system variable **QUALITY_SCORE** and can be used in filtering and queries. Essentially the quality score decrements for bad behavious and increments for good behavior.

### Event types

#### Quality
Quality event is triggered if panelist is re-conciled in a project or returned back to Sample Ninja with status "quality". You should always reconcile for your projects so you can catch repeat offenders easily.

#### Speeding
Speeding event is triggered when panelist completes a survey too fast. The speeding threshold is set in the panel settings. Let's imagine we have a project where estimated LOI is set to 10 minutes. If the speeding threshold is set to 50% then any panelist who completes the project under 5 minutes would be flagged.

#### Completed, profile or quota
Each time panelist is returned back to Sample Ninja with status "completed", "quota" or "profile" the quality score is incremented.

### Scores
**isProxy** -5
**isHosted** -20
**isBot** -20
**ipMismatch** -20
**duplicateFingerprint** -5
**fingerprintMismatch** -20
**isOutOfCountry** -5
**speeding** -10
**location** -100
**linkManipulation** -45
**supplierDuplicate** -5
**referFriend** -5
**fakeEmail** -20
**quality** -20
**duplicate** -7
**security** -45
**cookieDeleted** -20
**spoofedLocation** -45
**completed** +5
**profile** +10
**quota** +10
