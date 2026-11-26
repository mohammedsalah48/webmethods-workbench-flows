# Assemble a URL

Topic: Mapping | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.service_url:solve`)

## Task

Given `host`, `port` and `path`, return `url` in the form `http://host:port/path`.

## Signature

```
INPUTS: host, port, path (String)
OUTPUTS: url (String)
```

## Solution

One MAP step: set url = "http://%host%:%port%/%path%".

## Package contents

`service_url.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/service_url/solve/`.

All sample tests and the hidden test passed on the site.
