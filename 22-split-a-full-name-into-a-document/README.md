# Split a full name into a document

Topic: Mapping | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.split_name_doc:solve`)

## Task

Given `fullName`, a first name and a last name separated by one space, return a document `person` with `first` and `last`.

## Signature

```
INPUTS: fullName (String)
OUTPUTS: person (Document: first, last)
```

## Solution

An INVOKE of `pub.string:tokenize` with fullName linked to inString. Its output mapping links valueList[0] to person/first and valueList[1] to person/last.

## Package contents

`split_name_doc.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/split_name_doc/solve/`.

All sample tests and the hidden test passed on the site.
