# Worked Example — Microsoft 365 Copilot

A completed assessment, scored **only** from public documentation as it stood on
2 August 2026. It shows a practitioner what an evidenced 2, an asserted 1 and an absent 0
actually look like against a real supplier, and demonstrates that a competent, well
documented vendor still does not score 16.

**Read this first.** A customer's negotiated agreement may differ materially from the
published terms, in either direction. An enterprise agreement may contain switching and
audit commitments that no public page discloses. Nothing here is an allegation of
non-compliance: Microsoft is unusually transparent, and several of the scores below are 2
precisely because the commitment is contractual and locatable. The purpose is to model the
method, not to grade the company. Re-score against the client's own paper before advising.

---

## The scores

| Domain | Score | Basis |
|---|---|---|
| **SD-1** Derived-data title | **2** | Inputs and Output Content are both Customer Data under the Product Terms; Microsoft states it does not own output content, and that customer embeddings are not available to OpenAI ([Microsoft, protecting customer data in the AI era](https://techcommunity.microsoft.com/blog/microsoft-security-blog/faq-protecting-the-data-of-our-commercial-and-public-sector-customers-in-the-ai-/4097231)) |
| **SD-2** Purpose limitation and training | **2** | Prompts, responses, and data accessed through Microsoft Graph are not used to train foundation LLMs, stated in product documentation and carried in the Product Terms and DPA ([Microsoft Learn, data privacy and security for Microsoft 365 Copilot](https://learn.microsoft.com/en-us/microsoft-365/copilot/microsoft-365-copilot-privacy)) |
| **SD-3** Extractability | **2** | A customer-executable bulk path exists: the Graph `getAllEnterpriseInteractions` API returns prompts and responses tenant-wide ([Microsoft Learn, AI interaction history](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/api/ai-services/interaction-export/resources/aiinteractionhistory)), with eDiscovery and Purview as secondary routes |
| **SD-4** Switching and functional equivalence | **0** | No published switching-assistance obligation, transition window, or functional-equivalence statement for the AI service. Absent from public terms — not evidence that none exists in a negotiated agreement, which is exactly why it must be asked |
| **SD-5** Residency and inference jurisdiction | **1** | Residency at rest is contractual and Copilot is an EU Data Boundary service, but see below |
| **SD-6** Substrate and subprocessor transparency | **1** | Model providers are disclosed and changes are announced, but through the message centre rather than as a contractual notice-and-object right |
| **SD-7** Access, logging and audit | **2** | Every interaction writes to the Purview unified audit log as part of Audit (Standard), including which files the system reached into, with bulk export ([Microsoft Learn, audit logs for Copilot](https://learn.microsoft.com/en-us/purview/audit-copilot)) |
| **SD-8** Exit, deletion and survivability | **1** | Retention policy, activity-history deletion and inactive-mailbox handling are documented; independent customer verification that deletion completed across backups and derived stores is not |

**Total 11 of 16 — proceed with conditions.** No veto condition triggered: title is not
captured, training rights are bounded, an independent extraction path exists, and the
inference jurisdiction is disclosed.

---

## Why SD-5 scores 1 and not 2

This is the finding that justifies the whole exercise, and no adoption framework would have
surfaced it.

Microsoft 365 Copilot is an EU Data Boundary service and data at rest stays inside it. But
**flex routing** allows LLM inferencing to occur outside the EU Data Boundary during peak
demand ([Microsoft Learn, flex routing for EU and EFTA](https://learn.microsoft.com/en-us/microsoft-365/copilot/copilot-flex-routing)).
It is a tenant setting, and it is **on by default** — for tenants created after 25 March
2026, and enabled by Microsoft on existing EU and EFTA tenants from 17 April 2026
([changepilot analysis of MC1269223](https://changepilot.cloud/blog/microsoft-365-copilot-flex-routing-eu-data-boundary-mc1269223)).
Separately, Anthropic models available within Copilot experiences are documented as **out of
scope for the EU Data Boundary** and for in-country processing commitments
([Microsoft Learn](https://learn.microsoft.com/en-us/microsoft-365/copilot/microsoft-365-copilot-privacy)).

Three things follow, and each is a general lesson rather than a Microsoft-specific one.

**Residency at rest and inference jurisdiction are different questions.** A vendor can
answer the first truthfully and completely while the second has a different answer. SD-5
asks both deliberately. Question 23 of the
[vendor questionnaire](https://eveglyphdesign.github.io/enterprise-grade-criteria/use/) puts
it in writing.

**A default is not a commitment.** The protection here is real and the control is genuinely
offered — an administrator can switch flex routing off. But it arrived switched on, changing
where inference ran for organisations that had made no decision at all. A control the
supplier may set, and reset, is asserted, not evidenced. That is a 1 by definition, and the
definition is doing useful work.

**Model choice changes the boundary.** A commitment that holds for the vendor's own models
may not hold for a third-party model offered through the same interface. SD-6 exists for
this, and it is why the questionnaire asks which models in the proposal sit outside the
vendor's own residency commitment.

## Where SD-4 scores 0, and what that means

Zero here means absent from public documentation, not refused. Microsoft publishes a great
deal; a switching-assistance obligation with a stated transition window and a cost ceiling
is not among it for this service. Under the EU Data Act, switching charges must fall to zero
from 12 January 2027, which makes this the domain most likely to move between now and then
for every vendor in the market.

Practically: a 0 on SD-4 is not a reason to decline. It is a reason to put questions 17 to
21 in writing and convert the 0 into a 2 by negotiation, before signature, while the buyer
still has leverage. After signature there is no leverage, which is the entire thesis of the
assessment.

## What a practitioner should take from an 11

An 11 is a good score. It comes from a supplier that has published its position, made
several commitments contractual, and built the audit surface. Most proposals a peer will
score will do worse, and many will do worse while claiming more.

The value is not the number. It is that the two soft domains are now identified, specific,
and negotiable — a residency default to be pinned by contract rather than by setting, and a
switching obligation that does not yet exist on paper. That is a two-item negotiation
agenda, produced before signature, from public sources, in an afternoon.

---

## Version and provenance

- **Document ID** EgD-GCF-004 · **Key ID** EgD-KEY-2026-07 · **Version** 1.0
- **Scored** 2 August 2026, from public documentation only. Vendor positions change; verify
  every citation before relying on this in client work.
- **Method** — [EgD-GCF-001, the Global Compliance Framework Assessment](https://eveglyphdesign.github.io/enterprise-grade-criteria/gcf/).
- **Not affiliated with, endorsed by, or reviewed by Microsoft.** Product names belong to
  their owners. Every score is an opinion formed from the cited public sources, offered as
  decision support, not legal advice.

---

© 2026 EVEglyphDesign. All rights reserved. Controlled copy.
*Pour le bien-être du peuple.*
