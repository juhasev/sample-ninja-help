## Verisoul security checks

The Verisoul security checks use Verisoul's device and network intelligence to stop fraud, fake
accounts and bots that the standard security checks may miss. They run when a panelist registers
and when a panelist opens a project link. Each check is set per sub-panel.

> The Verisoul security checks are available in Sample Ninja, but they are not active on your panel
> by default. To activate them, please contact our sales team.

## Turning the checks on

All Verisoul checks are off by default, also on existing sub-panels. To use them on a sub-panel:

- Turn on the switch in the toolbar of the **Verisoul security checks** card. This switch enables
  or disables all Verisoul checks for the sub-panel at once.
- Click each check you want to use. A green shield means the check is active, a red shield means it
  is off.

> You need both. With the toolbar switch on but no check selected, Verisoul does not run. With
> checks selected but the toolbar switch off, Verisoul does not run either.

The Verisoul checks run in addition to the standard security checks. Turning a Verisoul check on or
off never changes a standard check. For example, **Proxy, VPN & Tor** and the standard **Public VPN**
check are independent of each other.

## Pricing

> During the free beta period the Verisoul checks cost nothing. When billing starts, each Verisoul
> call is paid from your service credits under **Settings -> Service Credits**. There is one call per
> registration and one per project entry, however many checks are turned on. If your credits run
> out, the Verisoul checks stop and only the standard checks run.

## What happens when a check fails

**At registration**, the registration is rejected before the panelist account is created, and the
panelist is shown the **Registration disqualified** landing page. The rejected registrations and
their reasons appear in the **Verisoul Rejections** chart on the registration survey dashboard.

**At project entry**, the panelist is shown the **Failed security check** landing page. A security
event is recorded against the panelist for that project and their quality score is reduced. A
panelist who returns to the same project while still failing the same check is redirected again,
but is only charged once for that event.

> If Verisoul cannot be reached, the panelist is let through and only the standard checks apply.

## The checks

All checks run at registration and at project entry, except **Account authenticity**, which runs at
registration only.

### Fraud

Checks the panelist for recent fraudulent activity and IP addresses associated with fraud.

### Spoofed location

Checks whether the panelist is hiding or faking their true location through a spoofed IP address
or location spoofing.

### Impossible travel

Checks whether the panelist's location history shows travel between sessions that is not possible.

### Hosted or corporate VPN

Checks whether the panelist's IP address comes from a data centre or a hosted server.

> As with the standard **Hosted server detected** check, respondents on a B2B panel often connect
> through a corporate network that looks like a hosted server. Consider leaving this off for B2B
> panels.

### Bot

Checks whether the panelist's session shows automated or bot behaviour.

### Device risk

Checks whether the panelist's device shows elevated risk signals.

### Device / network mismatch

Checks whether the panelist's device signals do not match their network profile.

### Proxy, VPN & Tor

Detects connections through a proxy, a VPN or the Tor network, using Verisoul's device and network
intelligence. This is separate from the standard **Public VPN** check.

### Account authenticity

At registration, rejects accounts that Verisoul judges fake or suspicious, and email addresses that
are disposable or invalid.

### Duplicate account

Detects when the same person operates several accounts on the panel.

### Linked accounts

Detects when a panelist account is linked to other accounts on the panel through shared devices,
networks or identifiers.

> Several people in one household or office can share a device or a network. On panels where that
> is common, consider leaving **Duplicate account** and **Linked accounts** off.

> See **Panelist manager** -> **Fraud** for the full list of security event types, and
> **Panelist manager** -> **Quality** for how the quality score is built up.
