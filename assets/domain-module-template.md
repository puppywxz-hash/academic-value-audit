# Academic Value Audit Domain Module — Contribution Template

> Copy this file into `references/domains/<domain>.md` within the skill package. Replace every bracketed prompt. Delete optional sections only with a short reason. This is a methods module, not a prewritten verdict about the field.

## Module metadata

- **Module ID:** `[stable-kebab-case-id]`
- **Module version:** `[semver or repository convention]`
- **Compatible core contract:** `[e.g. 1.4; identify required changes]`
- **Scope / trigger:** `[technical areas and claims that should load it]`
- **Out of scope:** `[adjacent topics it must not silently assess]`
- **Contributors and relevant roles:** `[names or handles, roles]`
- **Affiliations / funding / interests:** `[relevant disclosures; write none declared only when confirmed]`
- **Contribution and content license status:** `[confirm the repository license and contributor terms before public inclusion; do not copy copyrighted source text/data without permission]`
- **Last source review:** `[YYYY-MM-DD]`
- **Review state:** `[draft / domain reviewed / source reviewed / behavior tried; define exact meaning]`
- **Change summary:** `[what changed and why]`

## 1. What this module adds to the core audit

State the domain-specific decisions this protocol improves. Do not repeat the core's universal evidence-quality, attribution, two-level value, source independence, or reporting rules. Link to core methods instead.

## 2. Claim types and analysis boundary

| Claim type | Operational definition | Actual endpoint / unit | Typical overreach | Include? |
| --- | --- | --- | --- | --- |
| `[claim]` | `[definition]` | `[observable endpoint]` | `[common invalid inference]` | `[yes / condition]` |

Specify how to distinguish author claims, policy/award criteria, promotional expansions, user hypotheses, and auditor-generated candidate scenarios.

## 3. Domain-specific analytical model

Core 2.0: explain the real bottleneck and why it exists; give a competing explanation and discriminating observation, a strong task-matched baseline, scaling or equivalent domain reasoning, deletion/replacement/completion comparisons, and what evidence changes a funding action. Include both a case where positive engineering evidence defeats an overbroad negative claim and a case where a headline improvement fails to improve the endpoint. State actual trial scope; examples are not preset verdicts.

Describe the minimum field-appropriate model or interpretive framework needed to test consequential claims. Do not force quantitative causality or physical first principles onto fields where another evidentiary method is appropriate:

- **Causal/technical or interpretive chain:** `[input/material → mechanism or reasoning → intermediate evidence → endpoint/interpretation]`
- **Definitions and units:** `[terms, measurement units, denominators]`
- **First-principles constraints:** `[derivation, assumptions and validity range]`
- **Measured parameters that theory cannot supply:** `[real-world data needed]`
- **Competing explanations / counterexamples:** `[how to distinguish them]`
- **Stop rule:** `[when more theoretical depth cannot change the decision]`

## 4. Domain gates and evidence eligibility

Do not state universal numeric cutoffs without an applicable source. Separate legal/standard/customer/process requirements from roadmaps, expert conventions, author targets, and scenario assumptions.

| Requirement / gate | Source class and specific source to retrieve | Version / scope | Test method and denominator | Why required for this task | Eligible as a real-world gate? | Missing/mismatched evidence wording |
| --- | --- | --- | --- | --- | --- | --- |
| `[requirement]` | `[original source]` | `[date / jurisdiction / process / population]` | `[method]` | `[task consequence]` | `[yes / no / conditional]` | `[bounded conclusion]` |

Explain how a threshold can be derived when no direct requirement exists, and what assumptions prevent that derived threshold from being treated as an industry rule.

## 5. Strong alternatives and cross-scale bridges

Name the alternatives that solve the same task at the relevant time and explain what makes them comparable. Specify bridges from:

`[scientific/material result] → [device or method] → [system task] → [real use/adoption] → [net value]`

For every bridge, list the necessary evidence and the stop wording if it is missing. Do not import a future platform's value into the audited work without an evidenced contribution chain.

## 6. Search and source map

| Question | First-party/original records | Independent or countervailing records | Search concepts / aliases / languages | Known blind spots |
| --- | --- | --- | --- | --- |
| `[need / requirement / performance / adoption / costs]` | `[standards, datasets, product or operating records]` | `[independent replications, regulators, users, alternative suppliers]` | `[queries]` | `[paywall, secrecy, data bias]` |

Identify which source types establish experiments, requirements, actual use, payments, safety, or net benefits. Describe shared datasets/teams/consortia and how to de-duplicate them. A source list is not proof that those sources were retrieved or read during a particular audit.

## 7. Domain-specific analysis and calculations

| Model / calculation | Formula or executable procedure | Required inputs + units | Assumptions / validity | Uncertainty and sensitivity | Not suitable when |
| --- | --- | --- | --- | --- | --- |
| `[method]` | `[equation / procedure]` | `[input fields]` | `[conditions]` | `[how to bound]` | `[failure domain]` |

Use observed parameters where available. Tag derived values and scenarios; do not fill unknown quantities with literature averages unless task/population/process compatibility is demonstrated. State whether calculations were actually run.

## 8. Disputes, limitations and common inference traps

- **Disputed propositions:** `[positions and evidence on each side]`
- **Shared assumptions to test:** `[assumptions repeated across otherwise separate groups]`
- **Common promotional / policy misreadings:** `[claim → why invalid → what would establish it]`
- **Evidence that would change the assessment:** `[specific observation/document]`
- **Unresolved limitations of this module:** `[what it cannot decide]`

## 9. Worked cases for method review

Provide at least one affirmative, one negative/limiting, and one ambiguous/boundary example when the domain supports them. Each must show source locations, claim scope, evidence reached, unresolved bridges, and a bounded conclusion. Do not require the auditor to reproduce a preferred ideological or funding verdict.

| Case | Why representative or deliberately nonrepresentative | Original evidence | Key alternative / contrary evidence | What the method should and should not conclude |
| --- | --- | --- | --- | --- |
| `[case]` | `[scope]` | `[source IDs/links]` | `[source IDs/links]` | `[bounded conclusion]` |

## 10. Core interface mapping

- **Claims and judgments:** `[existing core IDs/objects]`
- **Evidence and source relations:** `[existing core objects]`
- **Parameters/calculations/models:** `[existing core objects]`
- **Report placement:** `[existing report section/template]`
- **Proposed contract change, if any:** `[none, or exact field/version migration proposal]`

## 11. Reviewer checklist and dissent log

- [ ] Definitions, test methods, units, denominators, and validity domain are explicit.
- [ ] Every proposed real-world gate has an applicable source and justification.
- [ ] Primary evidence is distinguished from roadmap, review, commentary, and promotion.
- [ ] Independent evidence and shared source/assumption networks are assessed.
- [ ] Strong alternatives, counterexamples, unknowns, and conclusion-flipping evidence are included.
- [ ] Interests and external review limits are disclosed.
- [ ] Core data contracts and report conventions remain compatible or migration is documented.
- [ ] Case review tests evidence boundaries, not agreement with a desired final judgment.

**Reviewer roles and affiliations:** `[roles and relevant interests]`

**Substantive dissent:** `[position, evidence, and what could resolve it]`

**Validation performed:** `[format/source/domain review/behavior trial, exact scope and date; do not say “validated” without specifying what]`
