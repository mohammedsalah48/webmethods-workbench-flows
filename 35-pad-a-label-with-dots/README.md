# Pad a label with dots

Topic: Strings | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.dot_leader:solve`)

## Task

A printed report shows each label padded on the right with dots to 12 characters. Given `label`, return `line`. Example: Total gives Total........

## Signature

```
INPUTS: label (String)
OUTPUTS: line (String)
```

## Solution

One INVOKE of `pub.string:padRight` with padString `.` and length 12.

## Package contents

`dot_leader.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/dot_leader/solve/`.

All sample tests and the hidden test passed on the site.
