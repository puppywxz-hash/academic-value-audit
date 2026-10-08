# Contributing Domain Modules and Companion Sub-skills

We welcome contributions from researchers, engineers, practitioners, users, and evaluators who can make an audit more specific to a real field. Useful contributions may cover batteries, semiconductors, quantum technologies, medical devices, AI, agriculture, social science, or another well-defined area.

You can contribute in either of two forms:

1. **A drop-in domain module** for the core skill. This is the preferred starting point when specialist knowledge can be expressed as a focused reference loaded only for relevant audits.
2. **A deeper companion sub-skill** with its own `SKILL.md` and field workflow. Use this when the domain needs substantial procedures, calculations, datasets, or recurring outputs beyond a reference module. The sub-skill must state how it relies on the core audit and how its findings map back to the core evidence and decision rules.

## Where to put contributions

- Domain module: `references/domains/<domain>.md`. Start from [`assets/domain-module-template.md`](assets/domain-module-template.md).
- Companion sub-skill proposal: `contrib/skills/<skill-name>/`. Include a `SKILL.md`, any needed `references/` or `assets/`, a short README describing its scope and invocation, and a compatibility note for the core skill version.

Keep the shared principles in the core skill. A sub-skill should add field expertise, not fork the whole audit method or create a competing value score. Do not assume that installing a companion skill automatically loads or inherits the core skill; document any required invocation and bundle/version arrangement.

## What a strong field contribution includes

1. Define the field, claims, tasks, users, and system boundaries it covers—and what it does not cover.
2. Explain the mechanisms, scientific or engineering constraints, and actual bottlenecks that determine task-level performance.
3. Identify the strongest alternatives that solve the same task, including their limits and the conditions under which each is preferable.
4. Bridge laboratory metrics to device, system, production, use, and net outcomes; identify scale-up, reliability, maintenance, and cost constraints.
5. Provide reliable source routes and explain which source types can establish requirements, performance, adoption, costs, or outcomes.
6. Identify recurring misleading metrics, promotional overreach, shared assumptions, practitioner critiques, and relevant failed or discontinued efforts.
7. Provide field-appropriate models or calculations with units, inputs, assumptions, validity limits, sensitivities, and cases where the method should not be used.
8. Include affirmative, limiting, and boundary examples where the field supports them. Show how evidence changes the analysis; do not encode a preferred verdict.
9. State what new evidence could strengthen, weaken, or reverse a conclusion or funding action.
10. Disclose relevant affiliations, funding, technical or commercial interests, and the limits of any expert review.

## Review expectations

Please include the intended domain and limits, source-to-claim links, known disagreements, and at least one worked example showing how the contribution changes the analysis. Keep claims testable and distinguish field consensus from disputed positions. A source list is not proof that a source was read or that its claim is true.

Submissions are reviewed for scope, source traceability, compatibility with the core workflow, usability, and overgeneralization. Depending on available reviewers, review status may be limited; every contribution must state what kind of review it actually received. A module may be useful without being behaviorally validated, but must not imply stronger validation than was performed.

The core report schema and evidence/decision rules should not be changed casually. If a contribution needs a contract change, explain why, identify all affected files, and propose a versioned migration. Keep field-specific thresholds tied to applicable standards, customer requirements, measured process constraints, or explicitly labeled scenarios; never present an unsupported expert convention as a universal industry requirement.

## Sources, copyright, and license

Link to authoritative or primary sources where possible. Cite source versions, dates, sections, and access limits. Do not copy paywalled standards, papers, proprietary datasets, figures, or large passages into a contribution without permission. Prefer bibliographic references, links, and contributor-written method summaries.

By submitting a contribution, you agree that it will be distributed under the repository's MIT License. Include content only when you have the right to contribute it under that license.
