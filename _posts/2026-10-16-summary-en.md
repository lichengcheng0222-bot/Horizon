---
layout: default
title: "Horizon Summary: 2026-10-16 (EN)"
date: 2026-10-16
lang: en
---

> From 47 items, 11 important content pieces were selected

---

**Technology News**
1. [Meta releases Muse Spark Open, an 816B-A42B open-weight model](#item-tech-news-1) ⭐️ 8.0/10
2. [BIPM resolves to stop adding leap seconds to UTC](#item-tech-news-2) ⭐️ 8.0/10
3. [Libreboot 26.10 &\#x27;Ominous Olive&\#x27; adds UEFI, Chromebook support](#item-tech-news-3) ⭐️ 8.0/10
4. [RPKI route-origin validation now covers about 70% of internet routes](#item-tech-news-4) ⭐️ 7.0/10
5. [Goodfire post argues neural networks are &\#x27;clean,&\#x27; drawing interpretability debate](#item-tech-news-5) ⭐️ 7.0/10
6. [Anthropic tells investors quarterly revenue up nearly 50% to $16.8bn ahead of IPO](#item-tech-news-6) ⭐️ 7.0/10
7. [StepFun Releases Step 5 Preview: 600B MoE Agent Model](#item-tech-news-7) ⭐️ 7.0/10

**Technology Blog**
1. [Scaling Kimi K3 on AMD MI355X with vLLM](#item-tech-blog-1) ⭐️ 8.0/10
2. [AI&\#x27;s Software Boom Shows Up in Modest Projects](#item-tech-blog-2) ⭐️ 7.0/10

**Financial News**
1. [AI data-centre listings pulled as market selloff and higher rates hit deal boom](#item-finance-news-1) ⭐️ 7.0/10
2. [China proposes temporary export registration for 40 AI, biopharma and solar technologies](#item-finance-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Meta releases Muse Spark Open, an 816B-A42B open-weight model](https://research.meta.ai/blog/muse-spark-open) ⭐️ 8.0/10

Meta released Muse Spark Open, an open-weight model listed as 816B-A42B and published on Hugging Face, with reporting that it is optimized to run on Mac Studio. The release is accompanied by a license that permits general use but restricts third parties from offering the model as a service via API or similar interface once the licensee and its affiliates exceed $20 million in aggregate gross revenue. Commenters cite Artificial Analysis comparisons showing it underperforming Qwen3.8 Flash Next and GLM 5.3 Flash, both of which they say run on a single B300, and note that Meta&\#x27;s own headline frames the model as the most capable US open-weight model rather than the most capable overall.

hackernews · bigwheels · Oct 15, 17:47 · [Discussion](https://news.ycombinator.com/item?id=50107379)

**「Background」** Muse Spark Open is a mixture-of-experts model from Meta Superintelligence Labs: 816B total parameters with 42B activated per token, a 1M-token context window, and native text, image, video and audio input, released under the new Muse Model License \(tool-2-1, tool-2-2\). Meta has also published deployment support for it through Amazon SageMaker JumpStart, which lists both a BF16 and an NVFP4 variant \(tool-2-3\).

**「Impact」** Organizations planning to build commercial API products on Muse Spark Open need to check the Model-as-a-Service clause, since providers above the $20 million aggregate revenue threshold are not licensed to serve the model&\#x27;s outputs to third parties; the Mac Studio optimization points instead at local or self-hosted deployment. For teams choosing among open-weight options, community-cited benchmarks place Muse Spark Open behind Qwen3.8 Flash Next and GLM 5.3 Flash on hardware that is reported to fit on a single B300.

**「Community discussion」** Commenters debated the framing and competitiveness of the release: one noted that open-weight vendors increasingly claim the &quot;best in the US/EU&quot; rather than best overall, while another pointed to Artificial Analysis numbers showing it behind Qwen3.8 Flash Next and GLM 5.3 Flash, and criticized those comparisons for only covering the highest reasoning level rather than the low and medium settings used in high-volume production. One commenter who read the license summarized it as free to use except for the Model-as-a-Service revenue clause, and another argued Meta&\#x27;s strategy is to build a moat around a sticky product rather than to rent out frontier intelligence.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/meta-models/Muse-Spark-Open-816B-A42B">meta-models/Muse-Spark-Open-816B-A42B · Hugging Face</a></li>
<li><a href="https://dev.meta.ai/resources/blog/build-with-muse-spark-open">Build with Muse Spark Open - dev.meta.ai</a></li>
<li><a href="https://aws.amazon.com/blogs/machine-learning/metas-muse-spark-open-now-available-in-amazon-sagemaker-jumpstart/">Meta’s Muse Spark Open now available in Amazon SageMaker ...</a></li>

</ul>
</details>

**Tags**: `#open-weight models`, `#Meta`, `#LLM release`, `#model licensing`, `#local inference`

---

<a id="item-tech-news-2"></a>
### [BIPM resolves to stop adding leap seconds to UTC](https://www.bipm.org/en/cgpm-2026/resolution-5) ⭐️ 8.0/10

BIPM has published a CGPM 2026 resolution to stop adding leap seconds to UTC, the international time scale it maintains. Readers of the resolution report that insertions and removals end on 20 May 2027 and are not planned afterwards, which would leave the 27 leap seconds added so far as the last, and they note that the resolution page lists several reasons for the change. No resolution text was available in the source item, so the 2027 date, the &quot;27&quot; count, and the precise scope of the change come from community descriptions of the document rather than from the document itself.

hackernews · gliffie · Oct 15, 16:11 · [Discussion](https://news.ycombinator.com/item?id=50105777)

**「Background」** UTC is a time standard maintained by the International Bureau of Weights and Measures \(BIPM\) that has historically been adjusted with leap seconds to keep it close to solar time, while International Atomic Time \(TAI\) is a continuous atomic timescale. The 28th General Conference on Weights and Measures \(CGPM\) adopted Resolution 5 on the technical actions needed to ensure the continuity of UTC, following earlier planning to eliminate the leap second and stabilize DUT1 by 2035.

**「Impact」** The immediate practical effect falls on operators of distributed systems and other time-sensitive software: the move to a &quot;leap hour&quot; approach from next year is intended to remove the recurring risk of systems tripping over minutes that last 61 or 59 seconds instead of 60. Researchers quoted in coverage note that such non-standard minutes have already broken software assumptions about time, so the deferral shifts the compatibility burden away from frequent one-second insertions without eliminating the need to plan for a future, much larger adjustment.

**「Community discussion」** Commenters broadly welcomed the move: myself248 called leap seconds &quot;always stupid&quot; and long overdue, while tialaramex said a decision to stop adding them had already been taken and that this resolution instead settles UTC&\#x27;s definitional tie to solar time by deferring the problem far into the future. xvilka argued the change adds urgency to interplanetary and relativistic time standards as more satellites and computers operate in deep space.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/General_Conference_on_Weights_and_Measures">General Conference on Weights and Measures - Wikipedia</a></li>
<li><a href="https://www.bipm.org/en/cgpm-2026/resolution-5">Resolution 5 ( 2026 ) - BIPM</a></li>
<li><a href="https://www.bipm.org/en/cgpm-2026">28th meeting of the CGPM ( 2026 ) - BIPM</a></li>
<li><a href="https://www.theguardian.com/science/2026/oct/15/times-up-for-the-leap-second-as-scientists-swap-it-for-the-leap-hour">How an accelerating Earth led experts to adopt the leap ... | The Guardian</a></li>
<li><a href="https://www.abc.net.au/news/science/2026-10-12/we-may-be-about-to-lose-the-leap-second-for-good/107207528">World&#x27;s timekeepers to vote on ditching leap second - ABC News</a></li>

</ul>
</details>

**Tags**: `#UTC`, `#leap seconds`, `#time standards`, `#BIPM`, `#distributed systems`

---

<a id="item-tech-news-3"></a>
### [Libreboot 26.10 &\#x27;Ominous Olive&\#x27; adds UEFI, Chromebook support](https://libreboot.org/news/libreboot2610.html) ⭐️ 8.0/10

Libreboot 26.10, codenamed &quot;Ominous Olive&quot;, has been released with UEFI/EDK2 integration and Chromebook support. According to a community comment quoting the release notes, it imports all 233 currently supported Chromebooks from the MrChromebox coreboot distribution, with only Baytrail \(Kip\) tested so far and the Chromebook support provided source-only, meaning users must build from source rather than use prebuilt binaries.

hackernews · iamnothere · Oct 15, 12:52 · [Discussion](https://news.ycombinator.com/item?id=50102923)

**「Background」** MrChromebox is an established project that distributes custom coreboot-based firmware and flashing utilities for Chromebooks and Chromeboxes, offering capabilities that stock Google firmware does not. Libreboot&\#x27;s 26.10 release builds on that project by importing its 233 currently supported Chromebook targets, which is why the expanded device list arrives as source-only code with just the Baytrail &quot;Kip&quot; board reported as tested.

**「Impact」** Owners of the 233 newly imported Chromebooks can now run Libreboot instead of stock firmware, but this release is source-only — no binaries are provided — and the project reports only Baytrail \(Kip\) as tested, so other models require building from source and independent verification before users rely on them. Because Libreboot replaces vendor BIOS/UEFI on specific x86 and ARM boards, those installing it on untested Chromebooks take on the risk of an unvalidated build.

**「Community Discussion」** Commenters debated whether the release&\#x27;s AI contribution policy or its UEFI/EDK2 and Chromebook support was the more important change, with one developer reporting that MrChromebox&\#x27;s code was merged as an upstream dependency for a first ChromeOS port in the Heads project and that two more ports are in progress. Another commenter called the strict policy on LLM-assisted contributions refreshing, while a third pointed to the project&\#x27;s AGENTS file as evidence of its stance on AI.

<details><summary>References</summary>
<ul>
<li><a href="https://mrchromebox.tech/">MrChromebox .tech</a></li>
<li><a href="https://docs.mrchromebox.tech/docs/firmware/">ChromeOS Device Firmware | MrChromebox .tech</a></li>
<li><a href="https://libreboot.org/">Libreboot – Free and Open Source BIOS/ UEFI boot firmware</a></li>

</ul>
</details>

**Tags**: `#Libreboot`, `#UEFI`, `#Chromebook`, `#open-source firmware`, `#coreboot`

---

<a id="item-tech-news-4"></a>
### [RPKI route-origin validation now covers about 70% of internet routes](https://ipinfo.io/blog/rpki-protects-70-internet-routes) ⭐️ 7.0/10

IPinfo reports that RPKI route-origin validation now covers roughly 70% of internet routes, a milestone for the system that lets network operators cryptographically attest which autonomous systems may originate their prefixes. Much of the recent increase came from China, where the share of IPv4 addresses in valid routes rose from 3.7% to 83.0% — close to 60% of the global gain when counted by addresses, according to the article. These are the publisher&\#x27;s adoption measurements rather than an independent audit of reduced BGP hijacking.

hackernews · emot · Oct 16, 00:52 · [Discussion](https://news.ycombinator.com/item?id=50112330)

**「Background」** RPKI \(Resource Public Key Infrastructure\) is a cryptographic framework that lets network operators verify that an autonomous system is authorized to originate a specific IP prefix, helping prevent BGP route hijacks. Adoption of RPKI validation has historically been uneven across regions, and the recent global jump in valid routes is driven in large part by a sharp increase in China.

**「Operators still need more than ROV」** Route Origin Validation only proves that a prefix&\#x27;s announced origin is authorized, so a forged-origin hijack that advertises a path through the real origin can still pass RPKI checks — a class of attack Cloudflare documents ASPA as being designed to stop. Operators treating the ~70% ROV coverage figure as sufficient protection should plan for AS\_PATH validation \(ASPA\) and route filtering alongside origin validation.

**「Community discussion」** Commenters raised the centralization trade-off: one argued that concentrating a country&\#x27;s permitted routes in a registry server abroad, with automatic enforcement, would make it easy for a foreign government to cut off that country&\#x27;s connectivity by tampering with the database. Another said their organization had pushed to make its own and downstream customer routes RPKI-valid, and noted that ASPA is now available for ASN path validation, while a third asked whether any public service can verify which country or certificate an IP block belongs to, describing whois as deprecated.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.cloudflare.com/aspa-secure-internet/">ASPA: making Internet routing more secure | Cloudflare Blog</a></li>
<li><a href="https://www.systemshardening.com/articles/network/bgp-security-rpki/">BGP Security and RPKI: Route Origin Validation for Production ...</a></li>

</ul>
</details>

**Tags**: `#RPKI`, `#BGP`, `#routing security`, `#internet infrastructure`, `#internet governance`

---

<a id="item-tech-news-5"></a>
### [Goodfire post argues neural networks are &\#x27;clean,&\#x27; drawing interpretability debate](https://already-clean.goodfire.com/) ⭐️ 7.0/10

Goodfire published a post titled &quot;Neural networks are clean&quot; by Nick Cammarata, arguing against the view that individual neurons are heavily polysemantic and that they instead carry small, clean roles. In a linked launch post quoted in the Hacker News thread, Cammarata says he co-authored early mechanistic interpretability work at OpenAI and &quot;came away pessimistic,&quot; framing the new argument as good news for alignment research. The supplied item contains little beyond the link itself, so the claim is presented as an argument rather than an independently verified or benchmarked result, and commenters disputed whether it proves its case.

hackernews · themgt · Oct 15, 16:04 · [Discussion](https://news.ycombinator.com/item?id=50105647)

**「Background」** Mechanistic interpretability has long held that individual neurons are “polysemantic” — responding to many unrelated concepts at once — and explained this with superposition, the idea that models encode far more features than they have neurons. The essay&\#x27;s author, Nick Cammarata, was an early contributor to OpenAI&\#x27;s mechanistic-interpretability work before founding Goodfire. The Goodfire post revisits those famously messy neurons and argues that polysemanticity arose not from superposition but from several ordinary, mostly fixable issues.

**「What it means for interpretability work」** For developers and researchers using current mechanistic interpretability tooling, the post&\#x27;s claim that individual neurons have a small, clean role conflicts with the superposition premise that networks pack more features into shared directions than they have neurons, which is the rationale for analyzing combinations of neurons and for sparse-autoencoder-based methods. Because commenters argue the evidence does not establish that parameter overloading is absent, the &quot;clean&quot; reading should be treated as a contested hypothesis rather than a reason to retire existing superposition-based pipelines.

**「Community Discussion」** Commenters disagreed about whether the post&\#x27;s evidence supports its framing: bluejay2387 called the claims &quot;an overreach of what is actually proven,&quot; noting that progressive feature complexity and training-structure effects such as the Lottery Ticket Hypothesis are not mutually exclusive with parameter overloading, while antics described the post as a &quot;massive evidentiary brief&quot; arguing it may be easier than thought to &quot;sequence the AI genome.&quot; sigbottle asked whether relabeling a &quot;Cat &amp; Car&quot; neuron as a &quot;V-shaped neuron&quot; is a substantive change or merely a shift in description.

<details><summary>References</summary>
<ul>
<li><a href="https://agihunt.info/en/story/1a14041e1e9ec53c60dad009282">The Debate Over Whether Neural Networks Are… · AGI Hunt</a></li>
<li><a href="https://www.explainx.ai/blog/goodfire-neural-networks-are-already-clean-cammarata-neurons-interpretable-90-percent-qwen3-32b-2026">&quot;Neural Networks Are Already Clean&quot;: Goodfire&#x27;s Cammarata ...</a></li>
<li><a href="https://www.goodfire.com/research/already-clean">Neural Networks Are Already Clean - Goodfire</a></li>
<li><a href="https://arxiv.org/html/2602.11180v1">Mechanistic Interpretability for Large Language Model ...</a></li>
<li><a href="https://arxiv.org/abs/2602.11180">[2602.11180] Mechanistic Interpretability for Large Language ... Mechanistic Interpretability: Reverse-Engineering Neural ... Mechanistic Interpretability Is Having Its Moment: What ... Superposition and Polysemanticity in AI Interpretability Superposition in LLMs and Feature Representation Mechanistic Interpretability for AI Safety — the field ...</a></li>

</ul>
</details>

**Tags**: `#mechanistic interpretability`, `#neural networks`, `#AI alignment`, `#AI research`, `#superposition`

---

<a id="item-tech-news-6"></a>
### [Anthropic tells investors quarterly revenue up nearly 50% to $16.8bn ahead of IPO](https://simonwillison.net/2026/Oct/15/anthropic-tells-investors/) ⭐️ 7.0/10

Ahead of an IPO, Anthropic told investors on Wednesday that its third-quarter revenue was $16.8bn, up nearly 50% from $11.5bn in Q2, according to an FT report summarized by Simon Willison. The report, citing people with knowledge of the matter, also said Q1 revenue was about $4.8bn, Q3 adjusted operating margins excluding stock-based compensation were 11%, and the company brought in $1.70 for every $1 spent on computing power. Anthropic told investors that distillation — rivals training on its model outputs — accounted for 5% to 7% of revenue and that it had cut it back materially in Q3; Willison&\#x27;s arithmetic suggests unnamed labs spent over $500m distilling Anthropic&\#x27;s models in Q2. The report says Anthropic no longer appears to be leaning on &quot;annualized run-rate revenue&quot; in these investor communications.

rss · Simon Willison · Oct 15, 13:04

**「Background」** Anthropic&\#x27;s path to a public listing has been building since it filed a confidential draft S-1 with the SEC in late May 2026, after a $65bn Series H round that reporting put at roughly a $965bn post-money valuation \(tool-2-2, tool-2-3\). The company has also changed how it describes growth: the source notes that Anthropic previously leaned on &quot;annualized run-rate revenue&quot; in such communications, whereas this investor-day disclosure gave actual quarterly figures instead.

**「Impact」** Anthropic&\#x27;s own disclosures indicate the revenue it reported is partly built on a stream it is deliberately shutting off: the company told investors distillation accounted for 5% to 7% of revenue before it was cut back &quot;materially&quot; in Q3, while its research posts describe industrial-scale extraction campaigns by DeepSeek, Moonshot and MiniMax \(with a September 2026 threat report adding Alibaba among seven China-based labs\) and claim defenses have since reduced the rate of distillation by more than 90%. For developers and API customers, that enforcement posture is the practical compatibility concern — accounts and access patterns resembling bulk model-output harvesting face restriction — and for anyone assessing the IPO, the growth figures should be read net of a stream Anthropic says it is actively suppressing.

<details><summary>References</summary>
<ul>
<li><a href="https://enersys.co.th/en/insights/anthropic-ipo-s1-965-billion-valuation-2026">Anthropic IPO S-1 + Series H $65B / $965B Valuation 2026 | Enersys</a></li>
<li><a href="https://www.thestatesman.com/technology/anthropic-ipo-openai-race-valuation-2026-explained-1503600868.html">Explained: Anthropic just filed for an IPO at a $965 billion valuation ...</a></li>
<li><a href="https://betterstack.com/community/guides/ai/anthropic-threat-report-2026/">Anthropic&#x27;s September 2026 Threat Report: Illicit ...</a></li>
<li><a href="https://www.anthropic.com/research/detecting-and-preventing-distillation-attacks">Detecting and preventing distillation attacks \ Anthropic</a></li>
<li><a href="https://www.anthropic.com/research/distillation-defenses">Strengthening our defenses against distillation attacks</a></li>

</ul>
</details>

**Tags**: `#Anthropic`, `#AI industry`, `#IPO`, `#revenue growth`, `#distillation`

---

<a id="item-tech-news-7"></a>
### [StepFun Releases Step 5 Preview: 600B MoE Agent Model](https://huggingface.co/stepfun-ai/Step-5-Preview) ⭐️ 7.0/10

StepFun published Step 5 Preview on Hugging Face, a sparse Mixture-of-Experts multimodal model aimed at agentic workloads. It has 600 billion total parameters with 27 billion active, supports up to a 1 million-token context window, and accepts text, image, and video input. The model can be deployed through an OpenAI-compatible API with vLLM or SGLang under the StepFun Model License 1.0. StepFun claims the model leads on software engineering, long-horizon agent execution, and professional-knowledge tasks, with particular strength in financial scenarios, but the release is a preview and no benchmarks or independent measurements accompany these claims.

telegram · zaihuapd · Oct 16, 06:36

**「Background」** StepFun first detailed Step 5 Preview in September as a long-context agent model, saying it uses a sparse-attention scheme called Sparse GQA to select task-relevant history and cut the number of tokens actually entering attention for a 1M-token window \(tool-2-2\). The company then open-sourced the model on October 15, releasing BF16 and FP8 weights, a technical report, supporting development tools, and deployment guides \(tool-2-3\), which the Hugging Face posting follows.

**「Impact」** The practical integration path for developers is an OpenAI-compatible API served through vLLM or SGLang, but the release ships under the custom StepFun Model License 1.0 rather than a standard open-source license, so organizations should review commercial-use and redistribution terms before building on it. Independent verification is still thin: a third-party benchmark tracker lists Step 5 Preview at \#20 of 224 with an estimated 69.44/100, while StepFun&\#x27;s own &quot;frontier-level&quot; performance description remains a vendor claim for a preview model.

<details><summary>References</summary>
<ul>
<li><a href="https://news.qq.com/rain/a/20260920A06EUP00">阶跃发布Step 5 Preview：600B MoE瞄准长程Agent，10月将开源</a></li>
<li><a href="https://news.qq.com/rain/a/20261015A097DD00">阶跃开源Step 5 Preview，模型权重与技术报告同日发布</a></li>
<li><a href="https://github.com/stepfun-ai/Step-5-Preview">GitHub - stepfun-ai/Step-5-Preview: StepFun&#x27;s flagship model ...</a></li>
<li><a href="https://benchlm.ai/models/step-5-preview">Step 5 Preview Benchmarks, Pricing &amp; Speed (October 2026)</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#Mixture-of-Experts`, `#long-context`, `#AI agents`, `#model release`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Scaling Kimi K3 on AMD MI355X with vLLM](https://vllm.ai/blog/2026-10-16-kimi-k3-mi355x) ⭐️ 8.0/10

rss · vLLM Blog · Oct 16, 00:00

**「Background」** Kimi K3&\#x27;s agent workload reuses long prefixes but still touches three costly state types: MLA compressed KV history, KDA recurrent state matrices, and MoE expert weights. Under tensor parallelism, each GPU replicated the full MLA history and repeated MoE output work.

**「Solution」** AMD and Embedded LLM&\#x27;s vLLM work attacks these costs layer by layer. Eight-way decode context parallelism \(DCP8\) partitions MLA history across GPUs—cutting an estimated 1.96 GB per GPU for a 142,000-token conversation to about 245 MB—while CPU offload preserves MLA and KDA state with aligned resume points. MoE output ownership makes each GPU compute only its assigned output coordinates and fold them into the existing shared-expert all-reduce; the authors report 3.05–4.91% higher output throughput at TP8, and a later separate test freed about 3.85 GiB per GPU across 92 MoE layers while lifting high-concurrency throughput 28.9%. Other changes fuse the single-token KDA path and AttnRes/RMSNorm \(14.2% higher output throughput\), pad MLA&\#x27;s query heads to 16 to enable AMD AITER assembly \(43.8 to 23.6 ms/token at 32K input\), and narrow speculative-verification tiles, cutting a kernel test from 16.20 to 5.61 microseconds per layer \(2.89×\). The authors treat draft depth as a cost budget: four drafts yield 3.36 versus 3.00 expected committed tokens per cycle—12% more—so they pay only if the full cycle grows less than 12%. The headline AgentX result—7,567 versus 6,083 total tokens/s/GPU at 50 tokens/s/user P90, and 87.4% more tokens per dollar under modeled TCO—is vendor-authored and partly modeled, from separate tests.

**「Takeaway」** The larger point is that serving wins here come from eliminating duplicated or unused work across GPUs, kernels, and the whole draft–verify–commit cycle—not from peak FLOPS alone—though the NVIDIA comparison still needs independent validation.

**Tags**: `#LLM inference optimization`, `#AMD MI355X`, `#vLLM`, `#MoE/attention kernels`, `#speculative decoding`

---

<a id="item-tech-blog-2"></a>
### [AI&\#x27;s Software Boom Shows Up in Modest Projects](https://seangoedecke.com/ai-is-driving-a-boom-in-modestly-successful-software/) ⭐️ 7.0/10

rss · Sean Goedecke · Oct 16, 00:00

**「Background」** If coding agents let anyone turn an idea into working software, why is there no visible explosion of impressive new products? Sean Goedecke argues the missing software exists, but is spread across many modestly successful projects rather than concentrated in blockbusters.

**「Solution」** To test this, the author compared installation counts across roughly twenty marketplaces, plugin registries, and modding platforms before agentic coding went mainstream \(2022-24\) and after \(2025-26\). Overall, somewhere between 2x and 20x more new software is being created depending on where you look, with no real growth in massively successful projects and about 2x growth in modestly successful ones. Concretely, the NVDA screen-reader directory had over twice as many new addons with more than a thousand downloads but no change above ten thousand; HACS home-automation plugins doubled above a hundred installs with no change above a thousand; Steam games with over a hundred reviews are roughly 60% more common; and Obsidian plugins, Firefox and Chrome extensions, Nexus game mods, and Blender extensions followed the same pattern, while Google Play and WordPress plugins did not. The author chose plugins and mods partly to exclude AI tooling itself and focus on ordinary problems, and partly because install data reveals actual use rather than merely created repositories. He concedes that AI attribution is hard, since hobbyist communities punish disclosure, and that some counts needed scaling for platform changes, such as Obsidian relaxing admin review of new plugins. Speculating on the shape of the boom, he suggests large companies already have the visible features they want and are slowed by technical paralysis, while it remains unclear why no wildly successful hobbyist projects have emerged — perhaps good ideas are simply hard, or successful projects need years to grow.

**「Takeaway」** Goedecke&\#x27;s thesis is that AI&\#x27;s measurable effect so far is a broad boom in small software serving hundreds or thousands of users, not an explosion of blockbuster products — a causal link he argues is strongly implied but not directly proven.

**Tags**: `#AI coding agents`, `#software ecosystem measurement`, `#open source plugins`, `#empirical analysis`, `#developer productivity`

---

## Financial News

<a id="item-finance-news-1"></a>
### [AI data-centre listings pulled as market selloff and higher rates hit deal boom](https://www.kitco.com/news/off-the-wire/2026-10-15/market-selloff-rising-rates-test-ai-data-centre-deal-boom) ⭐️ 7.0/10

Over the past week, AI data-centre listing plans from AirTrunk \(a REIT float\), Nvidia-backed Firmus and SoftBank-backed SB Energy were withdrawn or paused, as a market selloff and higher interest rates led investors to demand proof that companies can absorb rising rates and computing costs. Dealogic data show Asia data-centre merger and acquisition deals have reached $21.3 billion so far this year — roughly double full-year 2025&\#x27;s $10 billion — while equity financing for the sector fell 4.6% year on year.

telegram · zaihuapd · Oct 16, 05:10

**「Background」** AI data centres are capital-heavy projects usually financed through debt and equity sales, so higher interest rates directly raise the cost of building them. Blackstone-backed AirTrunk had already planned a Singapore real-estate investment trust \(REIT\) listing — a property fund whose shares trade publicly — before delaying it.

**「Impact」** Data-centre developers in Asia that had lined up share listings now face delayed or reduced fundraising and may instead sell assets, as the doubling of data-centre M&amp;A to $21.3bn this year alongside a 4.6% fall in equity financing shows buyers and backers shifting toward deals where they can verify projects can cover higher borrowing and computing costs.

<details><summary>References</summary>
<ul>
<li><a href="https://www.businesstimes.com.sg/companies-markets/why-tech-data-centre-ipos-are-facing-delays-and-what-investors-can-expect-market-now">Why tech and data centre IPOs are facing delays now - The ...</a></li>
<li><a href="https://therealdeal.com/international/2026/10/14/data-center-ipos-suddenly-on-shaky-ground-worldwide/">Data Center IPOs Suddenly on Shaky Ground Worldwide</a></li>

</ul>
</details>

**Tags**: `#AI data centers`, `#IPO withdrawals`, `#interest rates`, `#Asia M&amp;A`, `#market selloff`

---

<a id="item-finance-news-2"></a>
### [China proposes temporary export registration for 40 AI, biopharma and solar technologies](https://aqygzj.mofcom.gov.cn/flzc/gzjgfxwj/art/2026/art_c99f95ca0cd043829ac9991495fc283c.html) ⭐️ 7.0/10

China&\#x27;s Ministry of Commerce has proposed adding 40 artificial intelligence, biopharmaceutical and photovoltaic technologies to its export-control technology catalog, subjecting them to temporary export registration; the measure is a draft now open for public comment. The draft covers 23 AI items \(including large models, agents and compute clusters\), 5 biopharma items \(including cell and gene therapy and small nucleic acid drugs\) and 12 solar items \(including polysilicon, wafer and cell manufacturing and key equipment\), and excludes AI technology already in the public domain through open-source release or academic publication, according to the ministry.

telegram · zaihuapd · Oct 16, 09:12

**「Background」** China&\#x27;s Catalogue of Technologies Prohibited or Restricted from Export sets out which technologies need government clearance before being transferred abroad, and the Ministry of Commerce revises it from time to time. This revision is still a draft open for public comment, so the 40 listed technologies are proposals rather than final rules, and the source gives no implementation dates.

**「Who is affected」** Chinese companies that license or transfer these AI, biopharma and solar technologies abroad — along with the foreign partners and buyers relying on them, including polysilicon, wafer and cell manufacturers — would face a pre-export registration step while the draft is under consultation, adding a compliance requirement before any deal proceeds.

<details><summary>References</summary>
<ul>
<li><a href="https://finance.sina.com.cn/tech/digi/2026-10-16/doc-inivmiic6932807.shtml">商务部回应《中国禁止出口限制出口技术目录》拟增列人工智能等技术：...</a></li>
<li><a href="https://news.cctv.com/2026/10/16/ARTIvDJFbJhCwbMmCTdWztKG261016.shtml">商务部新闻发言人就修订《中国禁止出口限制出口技术目录》答记者问_新...</a></li>

</ul>
</details>

**Tags**: `#export controls`, `#China regulation`, `#artificial intelligence`, `#biopharmaceuticals`, `#solar/photovoltaics`

---