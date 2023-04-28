## Quality Score (BETA)

The quality events are used to calculate a quality score between 0 and 100 for each panelist. The quality score is recorded to the system variable **QUALITY_SCORE** and can be used in filtering and queries. Essentially the quality score decrements for bad behaviors and increments for good behavior.

### Event types

#### Quality
A quality event is triggered if the panelist is reconciled in a project or returned to Sample Ninja with the status "quality." You should always reconcile for your projects to catch repeat offenders easily.

#### Speeding
A speeding event is triggered when a panelist completes a survey too fast. The speeding threshold is set in the panel settings. Suppose we have a project where the estimated LOI is set to 10 minutes. If the speeding threshold is set to 50%, any panelist who completes the project in under 5 minutes will be flagged. If a panelist completes the project in less than 1% of the LOI the panelist flagged with **Link Manipulation** event.

#### Completed, profile or quota
Each time panelist is returned to Sample Ninja with the status "completed," the quality score is incremented +10.

### Scores

#### Score deductions
- **isProxy** -5 (Public VPN service)
- **isHosted** -20 (Proxy or origination from a known server)
- **isBot** -20
- **ipMismatch** -20
- **duplicateFingerprint** -5 (Duplicate fingerprint)
- **fingerprintMismatch** -20 (Fingerprint from start survey does not match fingerprint at the end)
- **isOutOfCountry** -5
- **speeding** -10 (Speeding threshold triggered, configurable in the panel settings)
- **linkManipulation** -45 (Panelist completed project so fast that most likely the exit link was altered)
- **quality** -20 (Reconciled or returned from a survey with quality status)
- **duplicate** -7 (Duplicate respondent)
- **security** -45 (Returned from a survey with security status)

> Always reconcile your projects to keep the **QUALITY_SCORE** accurate! Similarly, try to always set the LOI or Length Of Interview as accurately as you can, as going forward, speeding will decrease panelist's the quality score. You can control speeding threshold percents in **Settings -> Speeding Threshold**.

> You can easily find all panelists whose QUALITY_SCORE has fallen too low, similarly you can automatically exclude panelists with low-quality score by adjusting your panel's **Business Rules**.
