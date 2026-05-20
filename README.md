# Epheia trust-anchors

Public trust-anchor bundle for the EPR-1.1 demo. Served at
[`https://trust-anchor.epheia.ai/v1/trust-anchors`](https://trust-anchor.epheia.ai/v1/trust-anchors).

Every change is a signed commit. The history of this repo is the audit
log of every key the public verifier (`verifier.epheia.ai`) has trusted.
Receipts that reference a `kid` no longer present in the latest
`v1/trust-anchors` will fail verification at step 7.

Updates are produced by `deploy/setup.sh` in
[`Vpgx7/epr-chatbot`](https://github.com/Vpgx7/epr-chatbot) and committed
here by the operator. The repo is intentionally one operator-controlled
choke point; the runtime trio cannot push to it.

## Schema

See `epheia_common.types.TrustAnchorBundle` in the demo repo — the same
Pydantic model the verifier uses to parse this file.

## Verification

```bash
curl -sS https://trust-anchor.epheia.ai/v1/trust-anchors | jq .
```
