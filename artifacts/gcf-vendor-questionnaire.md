# Vendor Questionnaire

Forty-one questions to put to a supplier in writing, ordered by control domain. Send it as
a document and require a written response. The questionnaire is phrased so that an evasive
answer is visible as an evasion: each question asks for a document, a clause, or a
demonstrable artifact, and none can be satisfied by a link to a trust centre.

**How to use it.** Send Part A before the vendor's proposal is final. Score the returned
answers with the [scoring workbook](https://eveglyphdesign.github.io/enterprise-grade-criteria/use/EVEglyphDesign_GCF_Scoring_Workbook.xlsx) against the
eight control domains in
[EgD-GCF-001](https://eveglyphdesign.github.io/enterprise-grade-criteria/gcf/). An answer
that points to a marketing page or a policy statement is **asserted** and scores 1. Only a
contractual commitment, a named clause, or an artifact the buyer can test is **evidenced**
and scores 2. Silence is 0.

**One instruction to the vendor, at the top of the covering note.** *Where the answer is a
contractual commitment, cite the agreement and clause number. Where it is a product
behaviour, cite the documentation and its date. Where the answer is "not currently
offered", say so plainly — an accurate no is more useful to us than an ambiguous yes, and
will not by itself disqualify the proposal.*

That last sentence matters. It converts the questionnaire from an interrogation into a
disclosure exercise, and it removes the vendor's incentive to blur. A supplier who answers
"no" to four questions and "yes, clause 8.3" to the rest is a better counterparty than one
who answers "yes" to everything without a citation.

---

## Part A — the questions

### SD-1 Derived-data title

1. Who holds title to embeddings, vector representations, and indices generated from our
   data? Cite the clause.
2. Who holds title to a model fine-tuned or customised on our data, and to the weights
   produced by that process?
3. Who holds title to structure your service extracts from our unstructured content —
   entities, relationships, classifications, summaries?
4. On termination, are the artifacts in questions 1 to 3 delivered to us, deleted, or
   retained by you? State which, per artifact type.
5. Does your agreement grant you any licence over our inputs or outputs that survives
   termination? Quote it.

### SD-2 Purpose limitation and training use

6. Are our data, prompts, outputs, or derived artifacts used to train, fine-tune, evaluate,
   or improve any model that serves another customer? Cite the contractual prohibition, not
   the policy page.
7. Is that commitment identical across every tier and product name you have proposed to us,
   including any consumer-branded or free tier our staff may reach?
8. Does human review of our content occur for abuse monitoring, quality, or safety, and can
   it be disabled contractually?
9. If any of the above requires a configuration setting rather than a contract term, name
   the setting, its default, and who can change it.
10. What notice do we receive if a default in question 9 changes?

### SD-3 Extractability

11. Describe the export path by which we obtain a complete, timestamped, full-text copy of
    our prompts, outputs, and derived artifacts.
12. Can we execute that export ourselves, without raising a support request or engaging
    your professional services?
13. What licence, role, or add-on is required to execute it, and does it survive
    non-renewal for the period we need to leave?
14. In what format, and does the format preserve the relationships between records rather
    than flattening them?
15. What is the largest export you have delivered to a customer of our size, and how long
    did it take end to end?
16. Is there a rate limit, record cap, or retention horizon that would make a complete
    export impossible?

### SD-4 Switching and functional equivalence

17. What switching assistance are you contractually obliged to provide, and for how many
    days after notice?
18. What do you charge for it? State the amount, and whether it exceeds the cost you
    directly incur.
19. Do you assert compliance with the EU Data Act switching provisions, and are you aware
    that switching charges must fall to zero from 12 January 2027?
20. Which functions of the proposed service have a documented equivalent on another
    platform, and which are proprietary such that leaving means losing them?
21. What is the minimum term, and what happens to our data during any wind-down period?

### SD-5 Residency, transfer and lawful access

22. Where does our data rest? Name the countries, not the region marketing name.
23. Where does **inference** run? This is a separate question from question 22, and we
    require a separate answer.
24. Under what conditions can inference be routed outside the stated boundary — capacity,
    failover, feature availability, model selection — and is any such routing on by default?
25. Which models in your proposal are outside your own residency commitment?
26. Which legal entity processes our data, in which jurisdiction, and to which government
    access regimes is that entity subject?
27. What is your notification obligation to us if you receive a lawful access demand, and
    what are the exceptions to it?

### SD-6 Substrate and subprocessor transparency

28. Which model or models serve this proposal, from which provider, hosted on whose
    infrastructure?
29. What notice do we receive before the model, its provider, or its hosting location
    changes, and can we object?
30. Provide the current subprocessor list and the mechanism by which we are notified of
    additions.
31. If a model is deprecated, what is the notice period and the migration obligation?

### SD-7 Access, logging and audit

32. Are logs of every interaction — prompt, response, and the resources the system reached
    into — available to us and exportable in bulk?
33. Are logs of **your personnel's** access to our data available to us, and can we require
    approval before such access occurs?
34. What is the log retention period, and can we extend it?
35. Provide your most recent independent attestation and identify precisely which services
    are in scope. Confirm in writing whether the AI service proposed to us is inside that
    scope or outside it.
36. Do we have a contractual right to audit, and under what conditions?

### SD-8 Exit, deletion and survivability

37. On termination, how long do we retain access for extraction purposes?
38. Describe the deletion process, its completion timeframe, and how we verify it occurred.
39. What is retained after deletion — backups, logs, telemetry, derived artifacts — and for
    how long?
40. Will you provide a certificate of deletion, and is that obligation contractual?
41. If you are acquired, merged, or exit this market, what happens to our data and to the
    commitments above?

---

## Part B — reading the answers

Three patterns recur and each has a specific meaning.

**The tier shift.** The answer is true of the enterprise product and untrue of the
consumer-branded product with the same name. Question 7 exists to force this into the open.
If the answer to question 7 is anything other than an unqualified yes, treat every other
answer as scoped to a single tier and establish which one.

**The setting that is not a term.** The protection exists, but as a configuration default
the vendor can change without amending the contract. Questions 9 and 10 exist to catch it.
A default is not a commitment. It scores 1.

**The attestation with the wrong scope.** A certification covers the platform, and the AI
service sits outside its boundary. Question 35 is deliberately blunt for this reason: it
asks the vendor to state the exclusion themselves, in writing, which is materially harder
than allowing an assumption to stand.

A vendor who answers all forty-one plainly has told you what you are buying. A vendor who
will not answer question 23, question 33, or question 35 has also told you something, and
it should be recorded in the scoring sheet as a 0 rather than left as an open item.

---

## Version and provenance

- **Document ID** EgD-GCF-003 · **Key ID** EgD-KEY-2026-07 · **Version** 1.0
- **Companion to** [EgD-GCF-001, the Global Compliance Framework Assessment](https://eveglyphdesign.github.io/enterprise-grade-criteria/gcf/),
  whose eight control domains this questionnaire operationalises.
- **Licence** — practitioners may use this with their own clients, unmodified, with
  attribution to EVEglyphDesign. See the
  [practitioner licence](https://eveglyphdesign.github.io/enterprise-grade-criteria/use/).
- **Use and limits** — a decision-support instrument, not legal advice. Counsel should
  review any contractual position taken in reliance on it.

---

© 2026 EVEglyphDesign. All rights reserved. Controlled copy.
*Pour le bien-être du peuple.*
