# Say hello

Topic: Mapping | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.greet:solve`)

## Task

Return a greeting for the caller.

Given `name`, set `greeting` to `Hello, NAME!` with the name inserted.

## Signature

```
INPUTS: name (String)
OUTPUTS: greeting (String)
```

## Solution

Set greeting = "Hello, %name%!" in one MAP step (value substitution on).

## Package contents

`greet.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/greet/solve/`.

All sample tests and the hidden test passed on the site.
