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

Circuit Flow is being built as the single directed-acyclic-graph dispatcher of the circuit platform. It plans and observes multi-step runs, executes deterministic no-model reference paths, quarantines crashes, re-verifies merged design branches and emits provenance-complete learning records without knowing any board, process design kit or domain solver physics. This checkout contains repository validation tooling and documentation only. Full foundation qualification is in progress. There is no installed flow dispatcher, run-observation recorder, crash-quarantine runner or qualified record schema.

**What does not exist yet:**
- a graph scheduler, branch-merge runner or crash-quarantine engine;
- a learning-record emitter or lineage query tool;
- a registered runtime record schema.

## Boundary

**What this project owns:**

| Record | Scope |
|---|---|
| Run plan | Directed acyclic graph of admitted operations, pinned input digests, pre-bound reference simulation traces, resource reservations, concurrency branches and cancellation rules |
| Run observation | Per-step exit status, resource usage, wall-clock bounds, crash quarantine state, fallback reason (budget exhaustion or service outage) and output digests |
| Design-step learning record | Provenance record of one design or verification step: operator agent, harness digest, generating autonomy envelope, custodied operator-context digest, external-data flags, sealed-split checks and verifier outcomes |

**Static imports:** only Circuit Core. Circuit Flow is imported by Circuit Acceptance, Circuit Manufacturing, Circuit Mixed-Signal and Circuit Workbench.

**Records read without importing domain code:**

| Source | Records consumed |
|---|---|
| Circuit Core | entity references, operation requests, admissions, data-handling profiles, operation profiles, approvals and autonomy envelopes |
| Circuit Technology | technology profile digests as opaque data records |
| Circuit Acceptance | acceptance plans and acceptance reports |
| Circuit Learning | process model inventories and grader bundle specifications |
| Domain, prototyping, lab and manufacturing repositories | operation descriptors and run artefacts as opaque digest-pinned records |
| Evidence Manifest Toolkit | shared evidence manifest envelopes |

**Capability registration and handoffs:** Registers as the platform's single workflow dispatcher with Circuit Core, connects over registered interfaces to Evidence Manifest Toolkit, Experiment Ledger, Neuro Evidence Bench, Bitstream Evidence CI and SYNAPSE-CHANNEL, and serves compiler and studio flow requests.

**Explicit non-claims and operating boundaries:**
- It imports only Circuit Core — zero Circuit Technology or domain-solver packages — and contains no board, process-design-kit or physics code.
- It never trains, fine-tunes or promotes a machine-learning model.
- Every flow executes deterministically on its no-model reference path when no model is promoted or when a model service is unavailable.

## Current tooling

Repository controls inspect:
- metadata and source attribution;
- workflows and dependency alignment;
- native documentation and repository inventory;
- preflight orchestration.

Metadata declares architecture-only maturity with empty implemented domain capability and claim inventories.

- Use the exact environment in [Contributing](CONTRIBUTING.md).
- Full CI and preflight belong in CI or in an explicitly admitted pre-push environment.
- See [Validation](VALIDATION.md) for the maintained validation scope.

## Intended evidence

Every future domain artefact will carry the platform's common provenance envelope, its source and environment digests, its confidentiality compartment and its explicit verification boundary. None of the planned record schemas is registered or qualified by this foundation.

## Documentation and support

Read [Architecture](ARCHITECTURE.md), [support](SUPPORT.md), [security reporting](SECURITY.md) and [citation metadata](CITATION.cff).

**Not claimed:**
- a hosted service, released package or DOI;
- a public CI status;
- a performed simulation, hardware measurement or sign-off verdict.

## Licence

Source is licensed under [AGPL-3.0-or-later](LICENSE). A commercial licence is available through the contact in [NOTICE](NOTICE.md).

![ANULUM](docs/assets/anulum_logo_company.jpg)

![Fortis Studio](docs/assets/fortis_studio_logo.jpg)

## Text and data mining reservation
The rightsholder, Miroslav Šotek (ANULUM), expressly reserves the use of the
works in this repository for text and data mining, including the collection of
this content for, and its use in, training, fine-tuning or evaluating machine
learning and artificial intelligence models, in accordance with Article 4(3) of
Directive (EU) 2019/790 and the national provisions transposing it.

No permission for such use has been granted beyond what the licence in
`LICENSE` grants. This reservation does not change that licence: uses the
licence permits remain permitted on its terms, including its attribution and
share-alike conditions.

Reservation made on 2026-11-22. Requests for permission: contact the
rightsholder through the contact listed in this repository.
