# Format an invoice number

Topic: Strings | Difficulty: Easy | 10 points | webMethods Workbench flow challenge (`challenge.invoice_number:solve`)

## Task

Invoice numbers are printed as INV- followed by the number padded with zeros to six digits. Given `number`, return `invoiceNo`. Example: 42 becomes INV-000042.

## Signature

```
INPUTS: number (String)
OUTPUTS: invoiceNo (String)
```

## Solution

Two INVOKE steps: `pub.string:padLeft` (number to inString, padString 0, length 6, value to padded), then `pub.string:concat` (inString1 `INV-`, inString2 `%padded%`, value to invoiceNo).

## Package contents

`invoice_number.zip` is the Integration Server package exported from the Workbench Flow simulator (package `WorkbenchFlows` 1.0): `manifest.v3` and the service files `node.ndf` and `flow.xml` under `ns/challenge/invoice_number/solve/`.

All sample tests and the hidden test passed on the site.
