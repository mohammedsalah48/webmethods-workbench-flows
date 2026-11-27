# Map an HTTP method to an action

Topic: Branching | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.method_action:solve`)

## Task

Given `method`, return `action`: GET gives read, POST gives create, PUT gives update, DELETE gives delete, anything else gives unsupported.

## Signature

```
INPUTS: method (String)
OUTPUTS: action (String)
```

## Solution

One BRANCH step switched on `method` with MAP children: `GET` = read, `POST` = create, `PUT` = update, `DELETE` = delete, `$default` = unsupported.

## Package contents

`method_action.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/method_action/solve/`.

All sample tests and all four hidden tests passed on the site.
