# Build an order number

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.order_number:solve`)

## Task

Given `year` and `sequence`, return `orderNo`: ORD-, the year, a dash, then the sequence padded with zeros to five digits. Example: 2024 and 42 give ORD-2024-00042.

## Signature

```
INPUTS: year (String), sequence (String)
OUTPUTS: orderNo (String)
```

## Solution

1. INVOKE `pub.string:padLeft` on `sequence` with length 5 and padString `0`, giving `seq5`.
2. INVOKE `pub.string:concat` with inString1 `ORD-%year%-` and inString2 `%seq5%`, giving `orderNo`.

## Package contents

`order_number.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/order_number/solve/`.

All sample tests and the hidden test passed on the site.
