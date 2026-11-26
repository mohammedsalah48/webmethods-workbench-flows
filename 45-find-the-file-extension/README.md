# Find the file extension

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.file_extension:solve`)

## Task

Given `fileName`, return `extension`: the text after the last dot. Example: report.final.pdf gives pdf.

## Signature

```
INPUTS: fileName (String)
OUTPUTS: extension (String)
```

## Solution

One INVOKE of `pub.string:replace` with searchString `^.*\.` (everything up to the last dot), useRegex true and an empty replaceString.

## Package contents

`file_extension.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/file_extension/solve/`.

All sample tests and the hidden test passed on the site.
