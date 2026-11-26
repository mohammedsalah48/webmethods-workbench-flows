# Build an address

Topic: Mapping | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.address_label:solve`)

## Task

Given `street`, `city` and `zip`, return:

- `address`: a document with those three fields
- `label`: one line in the form `street, city zip`

## Signature

```
INPUTS: street, city, zip (String)
OUTPUTS: address (Document: street, city, zip), label (String)
```

## Solution

One MAP step: links street/city/zip -> address/street, address/city, address/zip, and set label = "%street%, %city% %zip%".

## Package contents

`address_label.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/address_label/solve/`.

All sample tests and the hidden test passed on the site.
