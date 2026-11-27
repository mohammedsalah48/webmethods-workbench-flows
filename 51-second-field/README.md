# Read the second field of a record

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.second_field:solve`)

## Task

Given `line` with fields separated by `;`, return `second`: the second field. Example: A12;Widget;4 gives Widget.

## Signature

```
INPUTS: line (String)
OUTPUTS: second (String)
```

## Solution

One INVOKE of `pub.string:replace` with searchString `^[^;]*;([^;]*).*$`, useRegex true and replaceString `$1`, keeping only the text between the first and second semicolons.

## Package contents

`second_field.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/second_field/solve/`.

All sample tests and the hidden tests passed on the site.
