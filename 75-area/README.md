# Area of a room

Topic: Math | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.area:solve`)

## Task

Given whole numbers `width` and `length`, return `area` = width × length.

## Signature

```
INPUTS: width (String), length (String)
OUTPUTS: area (String)
```

## Solution

One INVOKE of `pub.math:multiplyInts` with num1 = `width` and num2 = `length`; value maps to `area`.

## Package contents

`area.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/area/solve/`.

All sample tests and the hidden test passed on the site.
