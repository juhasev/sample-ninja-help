## Security

The standard security checks decide who is allowed to take part in your projects. They run
automatically when a panelist opens a project link and again when they return from the survey.
Each check is set per sub-panel, so a consumer panel and a B2B panel can use different rules.

Click any item to switch it on or off. A green shield means the check is active, a red shield
means it is off.

> All checks except **Block disposable emails** are on by default. Leave them on unless you have a
> specific reason to relax one, and read the notes below first, because a few of them terminate
> genuine panelists in situations you may not expect.

### Public VPN

Terminates panelists using a proxy or a public VPN service to hide their real IP address and
country. Rejected panelists are shown the **Proxy check failed** landing page.

> Country detection depends on this check. If you switch **Public VPN** off, **Out of country** will
> no longer work reliably, because a panelist can simply appear to be somewhere else.

### Hosted server detected

Terminates requests coming from hosted servers. Those are typically running automated bots or a
private or corporate VPN.

> Safe to switch on for a consumer panel. We recommend leaving it **off** for B2B panels, where
> respondents often connect through a corporate network that looks like a hosted server.

> **This and Public VPN overlap.** Many addresses are reported as both a proxy and a data centre, so
> switching off only one of them will not stop the flags. A panelist coming through a cloud-hosted
> corporate VPN is usually caught by both. If you want to admit those panelists, turn **both** off.
> The event recorded against the panelist tells you which check fired, so check that before deciding
> which switch to change. There is more detail on this in the registration reports help.

### Out of country

Every panelist goes through an IP country check. If they are outside the countries configured in
the sub-panel locales, or outside their own locale, they are terminated and shown the
**Outside country** landing page.

### IP address

Enforces that a panelist starts and finishes a project from the same IP address. If the address
changes part-way through, the panelist is terminated and shown the **Security check failed**
landing page.

> This is the check most likely to affect real panelists, so consider your audience before leaving
> it on. A mobile respondent moving between wifi and mobile data, a laptop that reconnects, or a
> home connection that is issued a new address mid-survey will all change IP address without any
> dishonest intent. It is strict by design: switch it off if you see genuine respondents being
> rejected for **Security check failed** and their sessions look otherwise normal.

### Fingerprint mismatch

Enforces that a panelist starts and finishes a project on the same device. Rejected panelists are
shown the **Security check failed** landing page.

> This switch also governs whether duplicate device detection affects the quality score. With it
> off, a panelist who shares a device fingerprint and network with another panelist on the same
> project is still recorded, but no points are taken away. That matters on panels where several
> people legitimately share one household or office connection.

### Bot detected

Terminates bots, crawlers, page scrapers, search engines and other automated traffic you do not
want in your panel.

### Flag cookie deletions

Flags panelists who repeatedly delete their tracking cookie. Ordinary respondents rarely clear
cookies, so frequent deletions are a strong fraud signal. This check flags rather than terminates.

### Block disposable emails

Blocks disposable email addresses, also called burner or temporary addresses, from registering
through the registration survey or the Application API. Off by default.

> Disposable addresses are a common tool for people trying to hold several accounts on one panel.

## How these checks affect the quality score

A check that fails records a security event against the panelist for that project, and that event
reduces the panelist's quality score. A panelist who returns to the same project while still
failing the same check is flagged and redirected again, but is only charged once for that event.

Each event listed on a panelist's **Security events** shows the points that were actually taken
away at the time. If a check was switched off for that sub-panel, the event is still recorded for
your visibility but shows no deduction.

> See **Panelist manager** -> **Fraud** for the full list of event types, and
> **Panelist manager** -> **Quality** for how the quality score is built up.

## Switching a check off

Turning a check off stops three things for that sub-panel: the panelist is no longer terminated,
they are no longer sent to the matching landing page, and no points are taken from their quality
score.

> Switching a check off does not remove security events that were already recorded, and it does not
> restore points that were already deducted.
