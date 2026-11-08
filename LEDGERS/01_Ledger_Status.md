# Ledger Status

**Project:** `K_PRIVAIT`  
**Tier:** TIER_6_SECURITY_EVAL  
**Identity:** Upstream `microsoft/presidio` @ `d4ccc6bcb6b6` (MIT)

## Chain state

| Fact | Value |
| --- | --- |
| Upstream | `microsoft/presidio` |
| Commit | `d4ccc6bcb6b6a7144336fe93b7839e61e251301b` |
| Upstream licence | MIT |
| Licence class | permissive |
| Clone size | 153.34 MB |
| Ledger | 0 blocks, chain verified |
| Current TRL | NOT YET MEASURED |
| Post-optimisation TRL | NOT YET MEASURED |
| II budget cap | 1500.0 IIU |
| Verified upstream edits | 1 |

- Blocks: **0**
- Head digest: `None`
- Chain verification: **verified**

## Independent verification

The chain is verifiable without trusting this project's tooling:

```
anticloud ledger verify
anticloud ledger export > ledger.jsonl
```

Each block carries the previous block's digest, so removing or reordering an
entry invalidates every block after it. That property is the reason the
ledger can stand in for a claim of what happened.
