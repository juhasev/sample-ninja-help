## Action thresholds

### Send notifications when **response rate** falls under configured % 
The system will automatically notify the project manager and the assistant manager (if selected) when **Response Rate** has fallen below the configured percentage.

>**Response rate** is calculated using **completed / invited * 100%**

### Send notifications when **start rate** falls under configured % 
The system will automatically notify the project manager and the assistant manager (if selected) when **Start Rate** has fallen below the configured percentage. The following projects prequisites must be met. A project has been sampling at least 4 hours or has minimum of 100 starts.

> **Start rate** is calculated using **started / invited * 100%**

### Send notifications when **incidence rate** is less than % of estimated.
The system will automatically notify the project manager and the assistant manager (if selected) when the measured incidence rate is less than % of the estimated value. The estimated value can be provided for each project. The following projects prequisites must be met. A project has at least 50 completes or has been sampling at least 4 hours.

> **Incidence rate** is calculated using **started / start + terminated * 100%**.

### Send notification when survey rating falls under
The system will automatically notify the project managers if survey rating fall under the configured score here. The following projects prequisites must be met. A project has at least 10 ratings submitted.

### Flag speeders when length of interview is less than % of expected
This settings tells the system when to consider someone a speeder. If you project's LOI (Length Of Interview) is 10 miunutes and you have set this setting to 70% this would mean than anybody with actual LOI under 7 minutes would be flagged.

> If you are logged in you get these notifications pushed to the application otherwise an email will be sent instead.

> Please note that the project **email notification** - setting must be turned on to receive an email notifications!
