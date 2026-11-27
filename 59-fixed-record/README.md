# Build a fixed-width record

Topic: Strings | Difficulty: Hard | 40 points | webMethods Workbench flow challenge (`challenge.fixed_record:solve`)

## Task

A legacy system reads fixed-width lines. Given `name` and `amount`, return `record`: name padded on the right with spaces to 10 characters, then amount padded on the left with zeros to 8 characters. Example: Mona and 1250 give `Mona      00001250`.

## Signature

```
INPUTS: name, amount (String)
OUTPUTS: record (String)
```

## Solution

Three INVOKE steps: `pub.string:padRight` (length 10, padString a space), `pub.string:padLeft` (length 8, padString 0), then `pub.string:concat` joins the two fields.

## Package contents

`fixed_record.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/fixed_record/solve/`.

All sample tests and the hidden tests passed on the site.
