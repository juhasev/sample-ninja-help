## Registration Statistics

Registration statistics are available if you are using the built in Registration Survey. Each Sub Panel has their own registration survey. To configure registration survey for a Sub Panel please find the Registration Survey tab in the Sub Panel Settings.

If you have at least one registration survey active you can select it from the top pulldown to view statistics.

> The registration statistics are limited for the past 30 days. You can use the **JOIN_DATE**, **EMAIL_VALID**, **EMAIL_CONFIRMED** - data variables to filter, slice and dice any given period in various other features throughout the application. The email delivery statistics are not stored for more than 30 days and cannot be use in filtering or in segments. The **EMAIL_VALID** variable indicates whether your email is valid, meaning we have recorded successfull delivery at least once. If panelist email bounces the **EMAIL_VALID** variable will be set to NO.

### Top row statistics
Statistics include number of new panelists, conversion rate, surveys started and completed. Additionally we also include statistics for confirmation (double opt-in) emails in form of delivered, opened and bounced counts. 

> Conversion rate is calculated from started surveys, using simple formula **Number of new panelists** / **Number of started surveys** * 100.

### Registration activity chart
This chart displays stacked totals that are indicative how many surveys are started, pending email confirmation and new panelists. The pending confirmation email count and the new panelists counts are substracted from the started. You can mouse over each column on the chart to view details.
