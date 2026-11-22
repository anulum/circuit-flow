<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-FLOW — repository foundation
-->

# Repository architecture

## Current executable tooling

**What it contains:** the repository's metadata, source-provenance, workflow, dependency-alignment, documentation, inventory and preflight controls.

**What each control does:** it inspects its fixed, declared local scope.

**What received metadata cannot do:** select another acceptance policy or grant domain authority.

Foundation qualification is in progress.

## Intended domain boundaries

| Record | Responsibility | Required evidence |
| --- | --- | --- |
| Run plan | Directed acyclic graph of admitted operations, pinned input digests, pre-bound reference simulation traces, resource reservations, concurrency branches and cancellation rules | Acyclic dependency check, admission verification and pre-run digest pinning before dispatch |
| Run observation | Per-step exit status, resource usage, wall-clock bounds, crash quarantine state, fallback reason (budget exhaustion or service outage) and output digests | Idempotent new-run recovery on crash and zero silent reuse of partial outputs |
| Design-step learning record | Provenance record of one design or verification step: operator agent, harness digest, generating autonomy envelope, custodied operator-context digest, external-data flags, sealed-split checks and verifier outcomes | Disjointness from sealed held-out bundles, copyleft training exclusion, enclave confinement for secret-bearing captures and seven-cause withdrawal lineage |

## Training-data hygiene and source withdrawal lineage

- **Sealed-split exclusivity and poisoning screens.** Custody refuses any training bundle listing an exact digest present in a sealed held-out evaluation bundle, and structural near-duplicate checks require no near-duplicate detected between held-out and training bundles for the declared kinds of edit, each at a stated lower confidence bound on recall, with edit kinds the check does not cover listed as limits. Poisoning screens cover only the planted poison families on a threshold-separate set, reporting their false-positive rate with an upper confidence bound measured on a declared clean reference set and the share of excluded items for each source.
- **Copyleft and secret exclusions.** Copyleft-quarantined artefacts are never eligible for model training, and secret-bearing captures stay confined to their confidential enclave by default.
- **Seven closed withdrawal causes.** At each custody watermark, transitive lineage queries halt affected datasets and model slots when a source is withdrawn — including expired non-disclosure agreements, poisoned inputs, licence revocations or newly added text-and-data-mining reservations.

## Planned record schemas

- `circuit_flow.run_plan.v1`
- `circuit_flow.run_observation.v1`
- `circuit_flow.design_step_learning_record.v1`

These are planned identifiers. None of them is registered or qualified here.

Read [validation tooling](validation-tooling.md) for the executable repository interfaces.
