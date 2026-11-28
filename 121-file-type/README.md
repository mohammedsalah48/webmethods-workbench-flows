# Recognise a file type

Topic: Branching | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.file_type:solve`)

## Task

Given `fileName`, return `type` from its ending, ignoring upper and lower case: `.csv` gives CSV, `.xml` gives XML, `.json` gives JSON, anything else gives UNKNOWN. Example: `Orders.CSV` gives CSV.

## Signature

```
INPUTS: fileName (String)
OUTPUTS: type (String)
```

## Solution

1. INVOKE `pub.string:toLower` on `fileName`, giving `low`, so the ending is compared case-insensitively.
2. One BRANCH step switched on `low`, with regex labels and four MAP children:
   - label `/\.csv$/` sets `type` = CSV
   - label `/\.xml$/` sets `type` = XML
   - label `/\.json$/` sets `type` = JSON
   - label `$default` sets `type` = UNKNOWN

## Package contents

`file_type.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/file_type/`.

All sample tests and all four hidden tests passed on the site.
