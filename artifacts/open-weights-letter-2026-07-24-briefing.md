# Briefing note — Open Weights letter, 24 July 2026

**To:** EVEglyphDesign development team (Tobias, Andy, Luke, Vida)
**From:** Dany Thériault (Apex, EVEglyphDesign)
**Date:** 27 July 2026
**Status:** Decision requested — silent assent by 03 August 2026

---

## The one-line

Twenty-five US technology companies, including Perplexity, signed an open letter on 24 July 2026 asking Washington not to restrict open-weight AI models. **OpenAI, Anthropic, Google and xAI did not sign.** The question in front of us is whether EVEglyphDesign should co-sign, endorse, ignore, or publicly qualify the letter — and the decision needs to be a group one, not a unilateral one.

## What the letter is

- **Title:** *Open Weights and American AI Leadership*
- **Date:** 24 July 2026
- **Length:** three pages, roughly 1,200 words, six sections
- **Primary source:** hosted as a PDF on NVIDIA's own image server — `images.nvidia.com/pdf/Open-Weights-and-American-AI-Leadership.pdf`
- **Launched by:** Jensen Huang's first-ever post on X, echoed by Satya Nadella nine minutes later, reposted by Y Combinator
- **Character:** an industry lobbying position paper aimed at US policymakers. No legal force. No specific bill named. It is written in response to a US administration push, four days earlier, to ban or sanction Chinese open-weight labs (DeepSeek, Moonshot, Alibaba's Qwen line)

## What the letter asks Washington to do

1. Expand compute access for startups and researchers
2. Fund shared training assets — datasets, tools, evaluation frameworks
3. **Avoid "premature restrictions" on open models** that stifle competition or drive innovation overseas
4. Treat distillation as a legitimate model-development technique — attack unlawful extraction through targeted legal frameworks, not blanket bans on the technique itself
5. Build stronger application layers so sovereign use of AI diffuses across the economy

## Who signed at launch (25)

Chip and hardware: **NVIDIA**, **Dell Technologies**
Cloud and platform: **Microsoft**, **IBM**, **Box**
Social and infrastructure: **Meta**, **Mozilla**
AI labs and models: **Mistral**, **Arcee AI**, **Black Forest Labs**, **Reflection**, **Perplexity**
Enterprise software: **CrowdStrike**, **Palantir**, **ServiceNow**, **Replit**
Investment: **Andreessen Horowitz**, **Emergence Capital**, **Y Combinator**, **Telnyx**
AI community: **Hugging Face**, **The Linux Foundation**, **Arena**, **Mariana Minerals**
Coalition: **American Innovators Network**

Ten added within 24 hours, taking the count to 35: **OpenAI** (joined late), **Cisco**, **Palo Alto Networks**, **DoorDash**, **GitHub** (Microsoft-owned), **Cohere**, **Fireworks AI**, **Nous Research**, **OpenClaw**, **Prime Intellect**.

## Who has not signed, and how to read that

- **Anthropic** — has declined to comment and has not signed at any version of the letter
- **Amazon** — absent from every version
- **Google** — did not sign at launch; Sundar Pichai posted personal support but Google itself has not added its name
- **xAI** — did not sign at launch

Two credible reads on the non-signers, in ascending order of cynicism:

1. **The competition-position read** (PacketNebula, Forbes, Bankwatch). The non-signers ship the strongest closed frontier models. A world where every enterprise fine-tunes its own open-weight model is a world where the frontier API business gets cannibalised. Endorsing that world publicly is off-strategy for closed-frontier labs even if some individual leaders privately agree.
2. **The "don't turn us into web browsers" read** (your framing). Closed-frontier labs are protecting a proprietary product surface. Open-weight models plus commodity inference is what the browser wars did to Netscape — a business collapsed into a free feature of the OS. Anthropic in particular sits closest to that risk: no cloud parent, no chip business, no consumer moat. Signing a letter that publicly celebrates open weights as the future of American AI leadership would be Anthropic underwriting the argument for its own commoditisation.

The letter's own arguments quietly support this read. Section 4 warns that "relying solely on closed models is not inherently safe: they can be breached, misused, or fail in ways that outsiders cannot detect, and concentrating advanced AI capabilities behind a small number of closed models compounds that risk." That is a competitive strike at closed-frontier labs dressed as a safety argument, and closed-frontier labs correctly read it as such.

## What the letter does not say

- It does not name China, DeepSeek, Moonshot, Alibaba or Qwen — though it was published three days after the US Treasury Secretary threatened sanctions over K3-line distillation
- It does not name any US organisation that currently intends to ship a frontier open-weight model. Meta paused Llama frontier releases; Mistral is European; Black Forest Labs and Reflection are pre-frontier. "American open-weight leadership" is, as things stand, a policy ask without an American frontier product behind it
- It does not carry safety commitments from the open-weight signers themselves — no red-team disclosure, no failure-mode publication, no substrate roster. It asks Washington to avoid restrictions without offering a counter-discipline

## Where this touches EVEglyphDesign

Three specific surfaces:

1. **[`enterprise-grade-criteria`](https://github.com/EVEglyphDesign/enterprise-grade-criteria)** — our seven-point audit rubric for enterprise-tier AI platforms. The letter's non-signers (OpenAI, Anthropic, Google, xAI) are all vendors we audit. So is a signer (Perplexity — used to write this briefing). The audit runs regardless of signature status. Nothing in the letter changes the rubric. But the rubric now has a live signal to report on: **which vendors are publicly staking a position on open weights, and which are staying silent**.
2. **[`digital-stem-cell`](https://github.com/EVEglyphDesign/digital-stem-cell)** — our substrate-accountability framework. The letter argues open weights strengthen safety through transparency. Our framework agrees on the transparency point and adds a discipline the letter omits: open weights without a published failure-mode disclosure are not automatically safer, they are just more auditable in principle. Endorsement should be conditional on that discipline.
3. **[`sap-sovereign-ai-monitor`](https://github.com/EVEglyphDesign/eve-hyperloop)** — our SAP vendor-lock-in escalation watch. The letter's lock-in language ("As organizations invest in AI, they want to know that they will not become locked into a single provider or lose the knowledge and capabilities they build over time") is close to verbatim from our own SAP lock-in critique. That parallel is worth naming publicly.

## Options in front of the team

**Option A — Co-sign as an open-source institution.** Add EVEglyphDesign to the coalition. Aligns with our public position on data sovereignty, open records, and lock-in. Cost: we become a party to an industry lobbying document whose primary beneficiaries are companies far larger than us, and whose framing (American leadership) may not match our Canadian-Charter and parish-governed lanes.

**Option B — Publish a conditional endorsement.** Support the four operative asks, add a fifth requirement of our own: any open-weight signer should also publish a failure-mode disclosure and a foundation-model roster at the cadence we require of enterprise-tier vendors. This lands as a public artifact in `enterprise-grade-criteria`. Cost: takes a week of drafting time. Upside: turns the letter into a public durable asset that carries our discipline forward.

**Option C — Ignore and note.** Do not co-sign, do not comment publicly. Continue the audit rubric as written. Cost: minimal. Upside: minimal. This is the default if no one objects.

**Option D — Publish the read on the non-signers.** Do not join the coalition. Instead, publish a short public brief explaining the "browser wars" read on Anthropic and OpenAI's absence, and file it in `enterprise-grade-criteria` as context for the audit. Cost: two days of drafting. Upside: this is the analytical contribution the coalition letter itself does not make, and it strengthens the audit rubric.

**Apex-proposed default:** **Option B + D.** Publish a conditional endorsement that names the discipline we require of open-weight vendors, and publish the read on the non-signers as audit context. Both land in `enterprise-grade-criteria`, both are durable, neither commits us to the coalition itself.

## The decision request

If you disagree with Option B + D, reply on this issue thread by **Sunday 02 August 2026, 20:00 CDT**. Silent assent after that time means we proceed with Option B + D.

If you agree but want to sharpen the discipline language, propose exact wording in the same thread.

If you think we should just co-sign (Option A) or stay quiet (Option C), say so plainly. The point of the note is that this is a group decision, not a unilateral one.

## Sources

1. *Open Weights and American AI Leadership* — primary PDF, NVIDIA, 24 July 2026: https://images.nvidia.com/pdf/Open-Weights-and-American-AI-Leadership.pdf
2. Tom's Hardware — *Nvidia and 24 other companies sign open-weights letter as Washington weighs Chinese AI model ban*, 24 July 2026: https://www.tomshardware.com/tech-industry/artificial-intelligence/nvidia-and-24-other-companies-sign-open-weights-letter-as-washington-weighs-chinese-ai-model-ban
3. NDTV Profit — *Microsoft, Nvidia, Other US Tech Giants Champion Open Weight AI Models In Joint Letter To US Govt*, 24 July 2026: https://www.ndtvprofit.com/technology/microsoft-nvidia-other-us-tech-giants-champion-open-weight-ai-models-in-joint-letter-to-us-govt-11817359
4. Open-TechStack — *25 Companies Sign Open-Weight Letter: 'American AI Leadership'*, 25 July 2026: https://open-techstack.com/blog/nvidia-microsoft-meta-and-22-more-companies-sign-open-weight-letter-american-ai-leadership/
5. PacketNebula — *Open Weights letter: 25 signers, and what it changes*, 25 July 2026: https://packetnebula.com/articles/open-weights-letter-25-signers/
6. Forbes / Sandy Carter — *Nvidia Open Weights Letter Doubled To 50 Without Amazon And Anthropic*, 26 July 2026: https://www.forbes.com/sites/sandycarter/2026/07/25/huangs-open-weights-letter-doubled-to-50-without-amazon-and-anthropic/
7. AIStockWire — *NVDA open-weights letter: OpenAI signed, Anthropic hasn't*, 25 July 2026: https://aistockwire.com/blog/openai-signs-open-weights-letter-anthropic-holdout-july-2026
8. Bankwatch — *"Open Weights and American AI Leadership" — A Reading*, 24 July 2026: https://bankwatch.ca/2026/07/24/open-weights-and-american-ai-leadership-a-reading/
9. Reuters — *Nvidia forms industry alliance for open AI security after Hugging Face hack*, 27 July 2026: https://www.reuters.com/business/nvidia-forms-industry-alliance-open-ai-security-after-hugging-face-hack-2026-07-27/
10. Open Source For You — *Nvidia, Microsoft And Others To Defend Open-Weight AI Against Premature Regulation*, 27 July 2026: https://www.opensourceforu.com/2026/07/nvidia-microsoft-and-others-to-defend-open-weight-ai-against-premature-regulation/

---

*Pour le bien-être du peuple.*
