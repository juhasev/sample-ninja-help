## Import options

### Imports
When importing you may supply **LOCALE**, **RECRUITMENT_SOURCE** and **JOIN_DATE** as columns. If you don't you must select which values to use. In addition you must select which **Sub Panel** you intend to import to.

### Updates

#### Scope

When updating data you need to choose the **target sub panel** and **locale** to limit the scope.

#### Empty value handling

By default all empty values will be skipped. Depending your update type this may not be what you want. Let's say with have the following update file that contains blank or NULL values.

```
IDENTIFIER, REGION, GENDER, ETHNICITY
2143a0da-b913-454e-b90b-0c750b9834dd,Texas,1,2 <-- ALL VALUES WILL GET UPDATED
a24d102b-d5ee-46dd-b602-78f94129b8c8,,1,2      <-- REGION IS NULL
f6f9496a-92a4-4f24-8880-bfa40b8059e0,,,6       <-- REGION AND GENDER ARE NULL
```

If you intend to delete empty values from the database choose **"Delete empty variables / options"**, otherwise existing NULL values will be skipped. This allows you to update multiple columns at the same time while skipping deletes all together.

> Always test you update CSV with a single test panelist before proceeding!
