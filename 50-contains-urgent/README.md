# Detect an urgent subject

Topic: Strings | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.contains_urgent:solve`)

## Task

Given `subject`, return `urgent`: true when the subject contains the word urgent in any mix of upper and lower case, otherwise false.

## Signature

```
INPUTS: subject (String)
OUTPUTS: urgent (String)
```

## Solution

Three INVOKE steps: `pub.string:toLower`, then `pub.string:replace` mapping `.*urgent.*` to `true`, then a second `pub.string:replace` mapping anything that is not exactly `true` to `false`.

## Package contents

`contains_urgent.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/contains_urgent/solve/`.

All sample tests and the hidden tests passed on the site.
