# Branch on a field inside a document

Topic: Branching | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.vip_route:solve`)

## Task

Given the document `order`, return `queue`: priority when `order/customer/type` is VIP, otherwise standard.

## Signature

```
INPUTS: order (Document) with id (String) and customer (Document, type String)
OUTPUTS: queue (String)
```

## Solution

One BRANCH step switched on the pipeline path `order/customer/type`, with two MAP children:

- label `VIP` sets `queue` = priority
- label `$default` sets `queue` = standard

## Package contents

`vip_route.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/vip_route/`.

All sample tests and both hidden tests passed on the site.
