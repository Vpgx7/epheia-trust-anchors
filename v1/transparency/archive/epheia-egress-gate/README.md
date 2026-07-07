# Retired log: epheia-egress-gate (cloud era)

This log was operated by the cloud-hosted egress gate and was RETIRED when receipt
issuance moved into the measured-boot appliance (2026-07). Its final published state is
preserved here unmodified — the append-only history remains auditable.

The successor log is `epheia-appliance-gate` (STH key kid `epheia-appliance-log-1`,
pinned in v1/trust-anchors since generation 80). It is a NEW log starting at tree_size 0,
not a continuation: the publisher refuses to append across a log-identity change, so this
archival move is the explicit, visible transition — never an in-place overwrite.
