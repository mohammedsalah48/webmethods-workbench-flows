# Perimeter of a rectangle

Topic: Math | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.perimeter:solve`)

## Task

Given whole numbers `width` and `height`, return `perimeter` = 2 × (width + height).

## Signature

```
INPUTS: width (String), height (String)
OUTPUTS: perimeter (String)
```

## Solution

1. INVOKE `pub.math:addInts` with num1 = `width`, num2 = `height`, giving `s`.
2. INVOKE `pub.math:multiplyInts` with num1 = `s`, num2 = 2, giving `perimeter`.

## Package contents

`perimeter.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/perimeter/solve/`.

All sample tests and the hidden test passed on the site.
