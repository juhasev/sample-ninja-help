### Creating and editing recruitment sources

Enter the name and cost per conversion. Select the partner name from the pulldown if you are using the built-in external recruitment partners.

> The recruitment partners are configured in **Settings -> Integrations**.

Choose how you want to identify the source. Select from one of the options:

#### ID 
This is a numeric ID you append to the registration survey URL, for example:

```
https://yourcompany.panelservice.io/registration/1/ENG-US?source=12
```
In the list view, this ID is indicated in the blue circle.

> This is the system default, and only **ID** is accepted when this mode is selected.

#### UUID
This is an alphanumeric identifier (UUID) that is hard to guess. Example URL:

```
https://domain.sampleninja.io/registration/1/ENG-CA?source=5f031c0e-dc5f-4e79-a318-46fa62fd42f9
```

Sources using UUID are indicated with a red lock in the list view. You can copy the UUID to the clipboard by clicked the blue ID circle.

> In this mode only valid **UUID** value are accepted.

#### Hybrid
In this mode, both numeric ID and UUID are accepted.
