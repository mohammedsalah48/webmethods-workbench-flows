# Read a fixed-width record

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.parse_record:solve`)

## Task

Given `record`, a 13-character line, return three values: `id` characters 1 to 3, `code` characters 4 to 8 with surrounding spaces removed, `qty` characters 9 to 13. Example: A01WIDG 00012 gives A01, WIDG and 00012.

## Signature

```
INPUTS: record (String)
OUTPUTS: id, code, qty (String)
```

## Solution

Four INVOKE steps: three `pub.string:substring` calls (beginIndex/endIndex 0-3, 3-8 and 8-13) and a `pub.string:trim` on the middle field.

## Package contents

`parse_record.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/parse_record/solve/`.

All sample tests and the hidden tests passed on the site.
