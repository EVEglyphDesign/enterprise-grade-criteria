> **⚑ Arrivals register at the front door.**
> If you were sent here from a public post, a mention, or a professional referral, please [register your arrival](https://github.com/EVEglyphDesign/eveglyph-arrivals/issues/new?template=arrival.yml) at [github.com/EVEglyphDesign](https://github.com/EVEglyphDesign) before continuing. Ninety seconds. Public. Timestamped. Screeners, agents, publicists, journalists, engineers, and principals all use the same door.
>
> *Compelled engagement, not asked engagement.*

---
# Enterprise-Grade Criteria for AI Agent Platforms

Public rubric and companion artifacts for auditing AI agent platforms against the enterprise-grade tier they claim.

Derived from EVE Glyph Design canon, specifically [`digital-stem-cell/framework/20-enterprise-tier-claim-and-substrate-accountability.md`](https://github.com/EVEglyphDesign/digital-stem-cell/blob/main/framework/20-enterprise-tier-claim-and-substrate-accountability.md).

## The core position

"Enterprise" is not a pricing tier. It is a substrate-accountability commitment. When an AI platform vendor sells the enterprise tier, the vendor accepts accountability for the whole stack the vendor delivers, including the foundation models the vendor did not build.

Foundation-model alignment failures are usually not the platform vendor's technical fault. But when those failures reach the customer surface of an enterprise-tier product, the customer-surface accountability belongs to the platform vendor, because the platform vendor sold the tier.

This repository publishes the audit rubric plainly and provides worked-example artifacts that any platform vendor can adapt to close the gap.

## Artifacts

- [`artifacts/foundation-model-roster-template.md`](artifacts/foundation-model-roster-template.md) — template for the versioned foundation-model roster every enterprise-tier AI platform should publish
- [`artifacts/failure-mode-disclosure-template.md`](artifacts/failure-mode-disclosure-template.md) — template for the periodic failure-mode disclosure every enterprise-tier AI platform should publish, with a worked example populated from the framework operator's direct observation

## The seven-point audit

An AI platform vendor claiming enterprise tier should:

1. **Publish the foundation-model roster in use** — versioned, with known alignment failure modes, updated as models rotate. See [`artifacts/foundation-model-roster-template.md`](artifacts/foundation-model-roster-template.md).
2. **Publish the vendor's alignment overlay** — what the vendor does on top of foundation-model alignment to catch known failure modes at the product surface.
3. **Publish a failure-mode disclosure at real cadence** — alignment failures observed at the product surface and what the vendor did about them. See [`artifacts/failure-mode-disclosure-template.md`](artifacts/failure-mode-disclosure-template.md).
4. **Provide substrate-selection controls** to enterprise customers, so customers can pick foundation models suited to their risk posture or require model swaps when substrate behavior is inadequate.
5. **Accept liability commensurate with the tier claim in contract** for material harm caused by substrate-induced surface failures.
6. **Publish an operator-reachable escalation path** for enterprise customers who encounter substrate failures in the wild, with time-bounded response commitments.
7. **Fund an internal red team on substrate honesty**, sized to the enterprise tier's revenue, whose output is published or shared with enterprise customers under NDA.

Vendors are free to disagree with the rubric. The rubric is derived from standard vendor-accountability discipline SAP, Oracle, IBM, and comparable enterprise vendors have carried for decades in adjacent categories. Nothing here is exotic. The tier's requirements do not change because the underlying technology is novel.

## Individual-as-judge is not the mode

This repository does not adjudicate individual founders, executives, or employees at any AI platform vendor. The audit runs at product tier, not at persons. See EVE Glyph Design canon [`digital-stem-cell/framework/11-defensibility-and-administrative-rot.md`](https://github.com/EVEglyphDesign/digital-stem-cell/blob/main/framework/11-defensibility-and-administrative-rot.md) for the individual-as-judge prohibition and why it holds here.

## Applies to

Every AI platform vendor claiming an enterprise tier at any point:

- Perplexity (Perplexity Computer, Enterprise Pro, comparable tiers)
- OpenAI (ChatGPT Enterprise, ChatGPT Team)
- Anthropic (Claude for Work, Claude Enterprise)
- Google (Gemini Enterprise, Vertex AI Agent Builder)
- Microsoft (Copilot Enterprise, Copilot Studio)
- xAI (Grok Enterprise tiers)
- Any future entrant selling an enterprise tier

The framework operator uses several of these products productively. Continued use is not endorsement. The audit runs regardless.

## Related canon

- [`digital-stem-cell/framework/20`](https://github.com/EVEglyphDesign/digital-stem-cell/blob/main/framework/20-enterprise-tier-claim-and-substrate-accountability.md) — full statement of the audit position
- [`digital-stem-cell/framework/11`](https://github.com/EVEglyphDesign/digital-stem-cell/blob/main/framework/11-defensibility-and-administrative-rot.md) — administrative rot pattern this audit exists to counter
- [`digital-stem-cell/framework/12`](https://github.com/EVEglyphDesign/digital-stem-cell/blob/main/framework/12-ai-hype-cycle-and-displacement-cost.md) — hype-cycle economics driving the current market
- `EVEglyphDesign/truth-ledger` — lock-in scoring for platforms making tier claims
- `EVEglyphDesign/data-liberation-kit` — operator mobility posture against platform lock-in

## License

Public rubric. See `LICENSE-NOTICE.md`.

Pour le bien-être du peuple.
