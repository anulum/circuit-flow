<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-FLOW — repository foundation
-->

# Circuit Flow

Circuit Flow is being built as the single directed-acyclic-graph dispatcher of the circuit platform. It plans and observes multi-step runs, executes deterministic no-model reference paths, quarantines crashes, re-verifies merged design branches and emits provenance-complete learning records without knowing any board, process design kit or domain solver physics. Its current executable surface is repository validation tooling. It has no installed flow dispatcher, run-observation recorder, crash-quarantine runner or qualified record schema.

Read [Architecture](ARCHITECTURE.md), [validation tooling](validation-tooling.md), [data boundaries](THREAT_MODEL.md) and the [repository boundary decision](adr/0001-repository-boundary.md).
