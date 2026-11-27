# Price a line with a discount

Topic: Math | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.net_line:solve`)

## Task

Given whole numbers `price`, `quantity` and `discount`, return `net` = price × quantity − discount.

## Signature

```
INPUTS: price (String), quantity (String), discount (String)
OUTPUTS: net (String)
```

## Solution

1. INVOKE `pub.math:multiplyInts` with num1 = `price`, num2 = `quantity`, giving `pq`.
2. INVOKE `pub.math:subtractInts` with num1 = `pq`, num2 = `discount`, giving `net`.

## Package contents

`net_line.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/net_line/solve/`.

All sample tests and the hidden test passed on the site.
