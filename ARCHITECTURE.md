<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-FLOW — repository foundation
-->

# Architecture

## Current executable surface

The checkout contains:
- repository validation tooling;
- dedicated tests;
- workflow definitions;
- native documentation.

No domain component of Circuit Flow is implemented yet. The metadata keeps domain capabilities, claims and qualified record formats empty.

## Intended data flow

1. **Request and flow planning** assemble an acyclic run plan from admitted operation profiles, resource reservations and pre-pinned design/reference digests.
2. **Deterministic no-model execution** runs the declared deterministic reference path so every release and baseline comparison has a complete non-AI run.
3. **Branch merges and crash recovery** quarantine any crashed tool working tree and require full post-merge re-verification whenever concurrent sibling design branches join.
4. **Learning-record emission** writes provenance records for curated dataset intake only when data-compartment, copyleft-quarantine, sealed-holdout disjointness and operator-context custody checks pass.

## Ownership

**This project owns** the planned Circuit Flow records and boundary rules.

**Owned elsewhere:**

| Responsibility | Owner |
|---|---|
| contracts, admission and approval kernel | Circuit Core |
| technology and board profiles | Circuit Technology |
| grader bundle specifications and study templates | Circuit Learning |
| sign-off and slot-rights verification | Circuit Acceptance |
| dataset curation, training and model promotion | DIRECTOR-AI |
| sealed holdout and context custody | REMANENTIA |

## Interpretation

- **Orchestration.** A completed run observation records tool execution; sign-off belongs to Circuit Acceptance.
- **Near-duplicates.** Structural screening reduces but cannot eliminate semantic paraphrase.

Read [the documentation architecture](docs/ARCHITECTURE.md) for the planned records, domain rules and schema identifiers.
