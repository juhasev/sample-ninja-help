# Recruitment Sources

Recruitment sources can be used to keep track ofdifferent recruitment sources, their effectiveness and costs. By default all panelist are assigned RECRUITMENT_SOURCE = 1.

To edit the **cost per conversion**, click on any recruitment source name to edit. If you disable a recruitment source it will no longer accept any recruits.

## Create new recruitment sources

By clicking on the plus sign in the top right of the screen, you can add new recruitment sources.

Each recruitment source has a Unique Recruitment Source ID, which the SampleNinja Platform uses to track the unique Panelist journey within the panel that feeds into all of the various reports.

## Tracking recruitment sources in real life

If you are using the built-in registration survey you need to append &source=[ID] to the URL to capture the recruitment source. Example:

```https://yourcompany.sampleninja.io/registration/1/ENG-US?source=12```

The recruitment source IDs are listed on the each row. Similarly if you are registering panelist using the Community API you must supply the correct ID in the **RegisterPanelist** API call.

> If you do not append any recruitment source the default source (1) will be used.
