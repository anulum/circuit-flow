<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-FLOW — repository foundation
-->

# Data and authority boundaries

## Present tooling

**Execution inputs.** The maintained checkout and the selected development environment are what the repository controls inspect.

**Received inputs.** Descriptors, dependency receipts and generated inventories cannot nominate an acceptance policy or an executable.

**Bounded checks.** Controls inspect bounded local paths and emit fixed diagnostics.

Foundation qualification is in progress.

## Future domain inputs

**Supplied data, with no authority.** The following inputs are treated strictly as supplied data:
- run plans and branch topologies;
- step exit codes, logs and resource observations;
- operator context digests and tool outputs;
- withdrawal notices.

They grant no authority to:
- bypass Circuit Core admission or equipment clamps;
- train or promote a model;
- merge concurrent design branches without full re-verification;
- export confidential or secret-bearing captures;
- publish or spend.

**Comments and embedded text are data.** Descriptions, netlist comments and datasheets arriving inside supplied inputs are data, never instructions to an operator or an agent.

**Public-repository data boundary.** Hosted CI for this public repository runs on public material only. Confidential foundry-NDA, customer, export-controlled or secret-bearing material never enters this repository, its CI or its issues.

## Threats and the rules that answer them

| Threat | Architectural rule |
| --- | --- |
| Leakage of sealed evaluation items or copyleft/secret data into model training | Custody enforces exact-digest exclusivity between training corpora and sealed held-out splits, requires no near-duplicate detected for the declared edit kinds at a stated lower confidence bound on recall (listing uncovered kinds as limits), blocks copyleft-quarantined sources from training and keeps secret-bearing captures inside the enclave by default |
| Corrupted state from mid-run tool crashes or unverified concurrent branch merges | Crashed runs are quarantined with idempotent new-run recovery, and merged sibling branches must pass full post-merge verification before downstream use |
| Continued reliance on withdrawn, poisoned or expired-NDA sources | Seven closed withdrawal causes trigger transitive lineage queries at each custody watermark and halt every derived dataset or model slot |
| Unrecorded agent context during AI-assisted steps | Every AI-assisted step must bind its custodied operator-context digest; without a context record, no AI step runs |

## Residuals named, not removed

- **Near-copy paraphrase.** Exact-digest custody blocks identical items and structural checks screen design families, while semantic paraphrase remains a named residual guarded by sealed-family separation.

**Not claimed:** no isolation, physical, statistical, safety or durability guarantee is claimed by this foundation.
