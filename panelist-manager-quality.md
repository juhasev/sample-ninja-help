## Quality Score 

The quality events are used to calculate a quality score between 0 and 100 for each panelist. The quality score is recorded to the system variable **QUALITY_SCORE** and can be used in filtering and queries. Essentially the quality score decrements for bad behaviors and increments for good behavior.

> Consider using **Research Defender** to cut down panel fraud, especially if you operate a B2C panel with registration available on the Internet.

### Event types

#### Quality
A quality event is triggered if the panelist is reconciled in a project or returned to Sample Ninja with the status "quality." You should always reconcile your projects to catch repeat offenders easily.

#### Speeding
A speeding event is triggered when a panelist completes a survey too fast. The speeding threshold is set in the panel settings. Suppose we have a project where the estimated LOI is set to 10 minutes. If the speeding threshold is set to 50%, any panelist who completes the project in under 5 minutes will be flagged. If a panelist completes the project in less than 1% of the LOI the panelist is flagged with **Link Manipulation** event.

### Scores

#### Score additions
Each time a panelist is returned to Sample Ninja with the status "completed," the quality score is incremented by +10.

#### Score deductions

- **Is Proxy -10** Panelist is using a public VPN service.
- **Is Hosted -20** Panelist IP address originates from a hosted server. This could be a targeted bot.
- **Is Bot -20** Panelist is detected as a bot.
- **Ip Mismatch -20** Panelist IP address changed in the middle of the project.
- **Duplicate Fingerprint -5** Somebody else has the same exact fingerprint.
- **Fingerprint Mismatch -20** Fingerprints do not match from start to end.
- **Out of Country -5** Panelist is out of the country.
- **Speeding -10** Panelist speeding.
- **Link Manipulation -45** Panelist has potentially engaged in link manipulation.
- **Refer Friend -5** Refer a friend error or potential abuse
- **Quality -7** Returned from survey with status quality
- **Duplicate -5** Returned from survey with status duplicate
- **Security -7** Returned from survey with status security
- **Cookie Deleted -10** Panelist deleted the tracking cookie or used an incognito window
- **Spoofed Location -45** Panelist is attempting to hide their true location
- **Reconciled -20** Panelist has been reconciled for providing inconsistent answers
- **Fraud -45** Panelist is engaged in fraudulent activity

> Always reconcile your projects to keep the **QUALITY_SCORE** accurate! Similarly, try to always set the LOI or Length of the interview as accurately as you can, as going forward, speeding will decrease panelist's the quality score. You can control speeding threshold percents in **Settings -> Speeding Threshold**.

> You can easily find all panelists whose QUALITY_SCORE has fallen too low, similarly you can automatically exclude panelists with low-quality scores by adjusting your panel's **Business Rules**.
