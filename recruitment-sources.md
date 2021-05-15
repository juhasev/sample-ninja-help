# Recruitment Sources

Recruitment sources can be used to keep track ofdifferent recruitment sources, their effectiveness and costs. By default all panelist are assigned RECRUITMENT_SOURCE = 1.

To edit the **cost per conversion**, click on any recruitment source name to edit. If you disable a recruitment source it will no longer accept any recruits.

## Create new recruitment sources

Click on the plus -icon to add a new recruitment source.

## Tracking recruitment sources in real life

If you are using the built-in registration survey you need to append &source=[ID] to the URL to capture the recruitment source. Example:

```https://yourcompany.sampleninja.io/registration/1/ENG-US?source=12```

The recruitment source IDs are listed on the each row for each source. Similarly if you are registering panelist using the Community API you must supply the correct ID in the **RegisterPanelist** API call.

> If you do not append any recruitment source the default source (1) will be used.
