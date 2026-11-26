# Build a document

Topic: Mapping | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.build_customer:solve`)

## Task

Given `id` and `name`, return a document `customer` with the fields `id` and `name`.

## Signature

```
INPUTS: id (String), name (String)
OUTPUTS: customer (Document: id, name)
```

## Solution

One MAP step with two links: id -> customer/id, name -> customer/name.

## Package contents

`build_customer.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/build_customer/solve/`.

All sample tests and the hidden test passed on the site.
