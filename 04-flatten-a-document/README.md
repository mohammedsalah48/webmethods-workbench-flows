# Flatten a document

Topic: Mapping | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.flatten_order:solve`)

## Task

Given the document `order`, return two plain values: `orderId` from `order/id` and `customerName` from `order/customer/name`.

## Signature

```
INPUTS: order (Document: id, customer{name})
OUTPUTS: orderId (String), customerName (String)
```

## Solution

One MAP step with two links: order/id -> orderId, order/customer/name -> customerName.

## Package contents

`flatten_order.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/flatten_order/solve/`.

All sample tests and the hidden test passed on the site.
