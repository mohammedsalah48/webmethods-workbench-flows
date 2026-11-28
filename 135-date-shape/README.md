# Check a date format

Topic: Validation | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.date_shape:solve`)

## Task

Given `date`, return `valid`: true when it has the form YYYY-MM-DD (four digits, dash, two digits, dash, two digits), otherwise false. The service must not fail.

## Signature

```
INPUTS: date (String)
OUTPUTS: valid (String)
```

## Solution

One BRANCH step switched on `date`:

- regex label `/^[0-9]{4}-[0-9]{2}-[0-9]{2}$/` sets `valid` = true
- label `$default` sets `valid` = false

## Package contents

`date_shape.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/date_shape/`.

All sample tests and all three hidden tests passed on the site.
