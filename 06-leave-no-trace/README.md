# Leave no trace

Topic: Mapping | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.leave_no_trace:solve`)

## Task

Given `firstName` and `lastName`, return `fullName` (first name, one space, last name).

Extra rule: when the service ends, `fullName` must be the only variable in the pipeline. Inputs and working variables must be dropped.

## Signature

```
INPUTS: firstName (String), lastName (String)
OUTPUTS: fullName (String)
```

## Solution

One MAP step: set fullName = "%firstName% %lastName%", then drop firstName and lastName.

## Package contents

`leave_no_trace.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/leave_no_trace/solve/`.

All sample tests and the hidden test passed on the site.
