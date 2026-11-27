# Turn a name around

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.reverse_name:solve`)

## Task

Given `listed` in the form `Last, First`, return `natural` in the form `First Last`. Example: Adel, Mona gives Mona Adel.

## Signature

```
INPUTS: listed (String)
OUTPUTS: natural (String)
```

## Solution

One INVOKE of `pub.string:replace` with searchString `^([^,]*),\s*(.*)$`, useRegex true and replaceString `$2 $1`, swapping the parts around the comma.

## Package contents

`reverse_name.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/reverse_name/solve/`.

All sample tests and the hidden tests passed on the site.
