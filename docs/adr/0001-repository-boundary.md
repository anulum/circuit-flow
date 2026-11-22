<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-FLOW — repository foundation
-->

# Decision: keep workflow orchestration domain-blind and import only Circuit Core

## Context

If the workflow scheduler imported process design kits, board definitions or domain simulators, every new specialist domain would force changes in the scheduler and create import cycles with mixed-signal, manufacturing, acceptance and workbench consumers.

## Decision

**What Circuit Flow owns:**
- run plan;
- run observation;
- design-step learning record;

**What it imports:** only Circuit Core. Circuit Flow is imported by Circuit Acceptance, Circuit Manufacturing, Circuit Mixed-Signal and Circuit Workbench.

**Owned elsewhere:**

| Responsibility | Owner |
|---|---|
| contracts, admission and approval kernel | Circuit Core |
| technology and board profiles | Circuit Technology |
| grader bundle specifications and study templates | Circuit Learning |
| sign-off and slot-rights verification | Circuit Acceptance |
| dataset curation, training and model promotion | DIRECTOR-AI |
| sealed holdout and context custody | REMANENTIA |

## Consequences

**What can be qualified now:** repository governance and validation tooling, before domain code exists.

**What it cannot qualify:** unimplemented schemas, solvers, hardware or sign-off verdicts.

**Architectural consequences:**
- Circuit Flow imports only Circuit Core and dispatches domain steps solely through registered operation profiles;
- branch-merge re-verification, crash quarantine, deterministic reference runs and learning-record provenance are enforced once in one dispatcher;
- training and promotion stay cleanly separated in DIRECTOR-AI.
