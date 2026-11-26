# Build a document list

Topic: Mapping | Difficulty: Medium | 20 points | webMethods Workbench flow challenge (`challenge.contacts_from_fields:solve`)

## Task

Given `name1`, `email1`, `name2` and `email2`, return `contacts`: a Document List with two entries, each with `name` and `email`.

## Signature

```
INPUTS: name1, email1, name2, email2 (String)
OUTPUTS: contacts (Document List: name, email)
```

## Solution

One MAP step with four links into contacts[0]/name, contacts[0]/email, contacts[1]/name, contacts[1]/email.

## Package contents

`contacts_from_fields.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/contacts_from_fields/solve/`.

All sample tests and the hidden test passed on the site.
