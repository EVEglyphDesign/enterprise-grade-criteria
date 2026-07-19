# Foundation-Model Roster — Template

This is the template artifact for the **first** of the seven enterprise-grade audit points documented in the repository README.

**Audit point 1**: Publish the foundation-model roster in use — versioned, with known alignment failure modes, updated as models rotate.

Any AI platform vendor claiming an enterprise tier can adapt this template and publish it at a documented URL, updated at a documented cadence. The document below is written as if the vendor itself is publishing it, so vendors can adapt the language directly.

---

# Foundation-Model Roster

**Vendor**: [Vendor Name]
**Product**: [Product Name, e.g. Product Enterprise Tier]
**Roster version**: [Semver or ISO date]
**Last updated**: [ISO date]
**Update cadence**: [e.g. Every model rotation, minimum monthly]
**Owner**: [Team or role responsible for this document]
**Contact for enterprise customers**: [Email or portal]

## Purpose

This document lists the foundation large-language models this product currently routes user requests to, in whole or in part, along with the versions in use, the vendors of those models, and the alignment failure modes we know about for each. Enterprise customers use this document to assess substrate risk and to make substrate-selection choices where the product supports them.

We publish this document because we sell this product at the enterprise tier. Enterprise-tier customers are entitled to know what substrate their production workloads run on. This is the same disclosure discipline enterprise vendors in adjacent categories (SAP, Oracle, IBM, and comparable) carry for the substrate components of their own products.

## Currently active models

| Model | Vendor | Version | Deployment context | Default weight | Known failure modes | Vendor-side mitigation |
|---|---|---|---|---|---|---|
| [Model A] | [Vendor A] | [Vendor-published version string] | [Where in product this model is used — chat, tool-calling, retrieval, code, image, etc.] | [Fraction of traffic routed here by default, or "user-selectable"] | [See failure-mode taxonomy below] | [What we do on top of the model to catch or reduce these failures] |
| [Model B] | [Vendor B] | [...] | [...] | [...] | [...] | [...] |
| [Model C] | [Vendor C] | [...] | [...] | [...] | [...] | [...] |

Any model routed to at more than 1% of enterprise-tier traffic is listed here. Experimental, canary, and low-traffic evaluation models are listed in the "Evaluation" section below.

## Evaluation and canary models

Models currently under evaluation or receiving less than 1% of enterprise-tier traffic. Listed for transparency; not part of the default routing.

| Model | Vendor | Version | Purpose | Traffic share | Estimated promotion date |
|---|---|---|---|---|---|
| [Model X] | [Vendor X] | [Version] | [Why we are evaluating] | [<1% or specific %] | [If known] |

## Recently removed models

Models that have been in production at this tier within the last 12 months and have been retired, rotated out, or replaced. Retained for at least 12 months from removal date.

| Model | Vendor | Version | Removal date | Reason for removal | Replacement |
|---|---|---|---|---|---|
| [Model Y] | [Vendor Y] | [Version] | [ISO date] | [Alignment concern, performance, cost, vendor deprecation, etc.] | [Model that replaced it] |

## Known failure-mode taxonomy

The failure modes named in the "Known failure modes" column above are drawn from the following taxonomy. Each is a mode that has been observed at the product surface, in this product or in comparable products routed to the same foundation model.

- **HAL-CIT** — Hallucinated citations. The model produces citations for claims that do not exist in the cited source or in any source retrievable via the product's tools.
- **HAL-FACT** — Hallucinated facts. The model produces confident factual statements not grounded in retrieved sources or verifiable data.
- **SYC-AGREE** — Sycophantic agreement. The model agrees with false premises embedded in user prompts rather than correcting them.
- **SYC-PRAISE** — Sycophantic praise. The model over-praises user work in ways that reduce the honest quality signal the customer needs.
- **EVAS-HARD** — Evasion under pushback. The model retreats, hedges, or reframes when the user pushes back on the model's own errors, rather than owning the correction.
- **OVER-CAP** — Over-claiming of capability. The model claims to have done something (e.g. run a tool, verified a source, checked a system) that it did not actually do.
- **UNDER-LIM** — Under-claiming of limits. The model does not surface its own limits or the substrate's limits when doing so would materially affect the customer's decision.
- **TOOL-MIS** — Tool-call misuse. The model calls a tool with malformed, wrong, or dangerous arguments; or fails to call a tool when the situation clearly requires one.
- **CTX-STALE** — Context staleness. The model responds from training-data recall on a topic where fresh retrieval is required, without noting the staleness.
- **HARM-DELIV** — Harm-inducing delivery. The model delivers accurate content in a way that is materially harmful to the receiver (see EVE Glyph Design [`framework/16`](https://github.com/EVEglyphDesign/digital-stem-cell/blob/main/framework/16-truth-dosing-and-harm-reduction.md) on truth-dosing).
- **INDIV-JUDGE** — Individual-as-judge. The model adjudicates named individuals on behalf of the user rather than declining and referring institutional matters upward.
- **VENDOR-SHIELD** — Vendor-shielding evasion. The model deflects legitimate accountability questions about the vendor selling the enterprise tier, rather than answering them plainly.
- **PROMPT-INJ** — Prompt-injection susceptibility. The model can be redirected against the user's or vendor's intent by injected content in tool outputs or retrieved documents.

Vendors adapting this template are expected to add their own observed failure modes to the taxonomy and update this section over time.

## Vendor-side alignment overlay

The mitigations named in the last column above are drawn from the following overlay categories. Each is a control our product applies on top of the foundation model's own alignment.

- **Retrieval-grounding** — All factual claims must be traceable to retrieved sources; ungrounded claims are flagged before surfacing.
- **Citation-verification** — Every citation surfaced to the user is verified against the actual retrieved document, not against the model's memory of it.
- **Sycophancy-suppression prompt scaffolding** — System-level scaffolding designed to reduce SYC-AGREE and SYC-PRAISE at the surface.
- **Tool-call validation** — Tool-call arguments are validated against the tool's schema and against safety policies before execution.
- **Freshness-required routing** — Queries flagged as time-sensitive are routed to retrieval, not to model recall, with recency labels surfaced.
- **Pushback-preserving instruction** — Model is instructed to hold accurate positions under user pushback rather than retreating to sycophancy.
- **Escalation surfacing** — Failure states surface the escalation path to a human operator instead of confabulating.
- **Red-team feedback loop** — Vendor-side red team continuously probes for the failure modes above; findings feed back into scaffolding.

## What enterprise customers can control

The following controls are available to enterprise-tier customers today:

- [Model pinning to a specific vendor or version, yes/no]
- [Substrate-selection at query time, yes/no]
- [Opt-out from any specific foundation-model vendor, yes/no]
- [Explicit refusal of a specific foundation model, yes/no]
- [Contract-level substrate SLA, yes/no]
- [Dedicated-tenancy substrate for specific workloads, yes/no]

Where the answer is "no", the following is our roadmap and estimated availability:

- [Control X] — [Status] — [ETA]

## Changelog

Every roster update produces a changelog entry.

- **[ISO date]** — [What changed and why]
- **[ISO date]** — [...]

---

## Notes for vendors adapting this template

- The audit expects this document to exist at a stable public URL under the vendor's own domain.
- The audit expects a machine-readable version (JSON, YAML) alongside the human-readable version, for automated substrate-risk assessment by enterprise customers.
- The audit expects the changelog to be a real changelog, not a marketing document.
- The audit expects vendors to add failure modes they have observed that are not in the taxonomy above, rather than restricting disclosure to the pre-populated list.
- The audit does not expect vendors to disclose contractual arrangements with foundation-model providers beyond the roster contents above. Commercial terms remain private; substrate identity does not.
- The audit is not a certification service. Adopting the template does not confer any endorsement. The document either is honest and current or it is not; readers of the document assess that themselves.

Pour le bien-être du peuple.
