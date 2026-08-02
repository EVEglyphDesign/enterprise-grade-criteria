# What We Check Before You Sign

## The problem

Your vendor's AI proposal has been assessed for security, for cost, and for fit. It has
almost certainly not been assessed for **who ends up holding what** — the part that cannot
be fixed after signature.

An AI system does not merely store your data. It derives new things from it: embeddings,
indices, extracted structure, tuned weights, a semantic map of how your organisation works.
Those artifacts are often worth more than the source records, and are usually silent in the
contract. Silence resolves in favour of whoever holds the infrastructure.

## What we do

We score the proposal against eight control domains, on evidence, before signature.

| | Domain | The question it answers |
|---|---|---|
| **SD-1** | Derived-data title | Who owns what the system makes from your data? |
| **SD-2** | Purpose limitation | Can your data train something that serves a competitor? |
| **SD-3** | Extractability | Can you get everything out, yourself, in full? |
| **SD-4** | Switching | What does leaving cost, and what breaks? |
| **SD-5** | Residency and inference | Where does your data rest — and where does the thinking happen? |
| **SD-6** | Substrate transparency | Whose model, on whose hardware, and who tells you when it changes? |
| **SD-7** | Access and audit | Who touched what, and can you prove it? |
| **SD-8** | Exit and deletion | When you go, does it actually go with you? |

Each domain scores 0, 1 or 2. **2** is evidenced — a clause you can cite or a capability we
can test. **1** is asserted — the vendor says so, on a page it can edit tomorrow. **0** is
absent. A trust-centre page never scores above 1, and that rule is what makes the total mean
something. Four findings override the total outright: the vendor takes title to derived
artifacts, claims unbounded training rights, offers no independent extraction path, or will
not say where inference runs.

## What you get

A completed sixteen-point sheet with every score sourced, a written questionnaire the vendor
must answer on the record, and a ranked list of the clauses to change. For the board: not
*we think this is fine*, but *we asked forty-one questions, here is what came back, and here
is what we are doing about the gaps*.

## What it is not, and why now

It is not a security review; you have one. It is not a verdict on the vendor's competence —
good suppliers score well and still show gaps, because the gaps sit in what nobody thought
to ask. It is not legal advice: your counsel sets the contractual position.

Every one of the eight domains is negotiable while the vendor is selling, and none of them
afterwards. The cost of asking is a fortnight. The cost of not asking is discovered at
renewal, when *can we leave* turns out to have been settled two years earlier by a clause
nobody read.

- **EgD-GCF-005** · v1.0 · method: [EgD-GCF-001, the Global Compliance Framework Assessment](https://eveglyphdesign.github.io/enterprise-grade-criteria/gcf/) · [worked example](https://eveglyphdesign.github.io/enterprise-grade-criteria/use/) · practitioners may hand this to clients unmodified, with attribution to EVEglyphDesign. Decision support, not legal advice.

---

© 2026 EVEglyphDesign. All rights reserved. Controlled copy.
*Pour le bien-être du peuple.*
