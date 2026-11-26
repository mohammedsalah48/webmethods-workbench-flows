# Convert between two document shapes

Topic: Mapping | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.rename_in_doc:solve`)

## Task

Given the document `in` with fields `fname` and `lname`, return the document `person` with fields `firstName` and `lastName`.

Extra rule: `person` must be the only variable left in the pipeline.

## Signature

```
INPUTS: in (Document: fname, lname)
OUTPUTS: person (Document: firstName, lastName)
```

## Solution

One MAP step: links in/fname -> person/firstName and in/lname -> person/lastName, then drop `in`.

## Package contents

`rename_in_doc.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/rename_in_doc/solve/`.

All sample tests and the hidden test passed on the site.
