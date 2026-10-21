---
layout: default
title: "Horizon Summary: 2026-10-21 (EN)"
date: 2026-10-21
lang: en
---

> From 42 items, 12 important content pieces were selected

---

**Technology News**
1. [Eight eMudhra intermediate CA keys compromised, forcing trust-store updates](#item-tech-news-1) ⭐️ 9.0/10
2. [Google open-sources TorchTPU, a native PyTorch backend for TPUs](#item-tech-news-2) ⭐️ 8.0/10
3. [tsrs: a Rust port of TypeScript for WASM sandboxes](#item-tech-news-3) ⭐️ 8.0/10
4. [Over 300 Tor exit nodes removed after SSH MITM campaign](#item-tech-news-4) ⭐️ 8.0/10
5. [Mistral&\#x27;s Voxtral 3 targets real-time speech and voice agents](#item-tech-news-5) ⭐️ 7.0/10
6. [Google Cloud europe-west2 outage disrupts European banks and services](#item-tech-news-6) ⭐️ 7.0/10
7. [Rust Compiler Contributor Outlines 2026 Trait Solver and Polonius Work](#item-tech-news-7) ⭐️ 7.0/10
8. [Battle Drones: browser RTS with audio-based local multiplayer](#item-tech-news-8) ⭐️ 7.0/10
9. [DeepSeek reportedly open-sources DeepInfer, claiming 155T tokens/day](#item-tech-news-9) ⭐️ 7.0/10
10. [OpenAI claims major low-resource coding gains, 97.9% COBOL migration accuracy](#item-tech-news-10) ⭐️ 7.0/10
11. [OpenAI API adds 12-hour prompt caching, report says](#item-tech-news-11) ⭐️ 7.0/10

**Financial News**
1. [Super Micro raises outlook; SpaceX reports revenue jump and Tesla merger talks](#item-finance-news-1) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Eight eMudhra intermediate CA keys compromised, forcing trust-store updates](https://simonwillison.net/2026/Oct/20/emudhra-certificates/) ⭐️ 9.0/10

Private keys for eight eMudhra intermediate CA certificates have been compromised, and they chain to roots trusted by the Mozilla, Microsoft, Apple and Chrome root programs as well as many downstream trust stores. Any software that bundles a trusted-certificate list must be updated; Linux distributions need new ca-certificates packages. Python users can get upgraded lists in uv 0.13.4, pip 26.2.2 and certifi 2026.10.19.

rss · Simon Willison · Oct 20, 23:50

**「Why intermediate CA keys matter」** Intermediate CA certificates sit between a trusted root and the leaf certificates used by websites, and they can issue those leaf certificates. Because the eight compromised eMudhra intermediates chain to roots trusted by the Mozilla, Microsoft, Apple, and Chrome root programs and by downstream trust stores, any software that bundles its own trusted-certificate list must replace that list to remove the affected intermediates.

**「Remediation burden falls on bundled trust stores」** Operators of systems that ship their own CA bundles must patch them: Python users need uv 0.13.4, pip 26.2.2, and certifi 2026.10.19, and Linux distributions need updated \`ca-certificates\` packages. Firefox users are protected automatically because Mozilla blocked the certificates through OneCRL without requiring an update or restart, according to Mozilla&\#x27;s security blog.

**「Community discussion」** Commenters highlighted both the trivial-looking key material and the uneven cleanup: one said all eight keys reportedly used a single byte, with one literally “4,” while another noted Mozilla’s OneCRL protected Firefox automatically within hours but vendored CA stores elsewhere may stay vulnerable. A commenter quoting eMudhra’s Mozilla bug report said the company traced the problem to a flaw in the KGC script used that day to create the ECC issuers.

<details><summary>References</summary>
<ul>
<li><a href="https://emudhra.we-have-a-problem.com/">eMudhra Intermediate CA Compromise</a></li>
<li><a href="https://blog.mozilla.org/security/2026/10/20/protecting-firefox-users-following-the-compromise-of-emudhra-intermediate-certificates/">Protecting Firefox users following the compromise of eMudhra ...</a></li>
<li><a href="https://discuss.python.org/t/information-for-python-users-regarding-emudhra-emsign-ca-certificate-security-incident/109576">Information for Python users regarding eMudhra / emSign CA ...</a></li>

</ul>
</details>

**Tags**: `#TLS certificates`, `#CA compromise`, `#trust stores`, `#security incident`, `#software supply chain`

---

<a id="item-tech-news-2"></a>
### [Google open-sources TorchTPU, a native PyTorch backend for TPUs](https://github.com/google-pytorch/torch_tpu) ⭐️ 8.0/10

Google has open-sourced TorchTPU, a native PyTorch backend for TPUs, with the code published on GitHub. The project is aimed at PyTorch users who want to target TPU hardware directly; the supplied item does not specify supported PyTorch or TPU generations, performance results, or a compatibility matrix. A Telegram-sourced summary included with the item further claims TorchTPU was co-developed with Meta’s PyTorch team and is already integrated with vLLM, SGLang, llm-d, TorchTitan, and Hugging Face Transformers v5, but those claims are not independently confirmed in the supplied discussion.

hackernews · ilreb · Oct 20, 16:40 · [Discussion](https://news.ycombinator.com/item?id=50169053)

**「Prior path: PyTorch/XLA」** Until now, running PyTorch on TPUs meant going through PyTorch/XLA, the \`torch\_xla\` Python package that implements XLA as a PyTorch backend and generally pushes workloads through XLA graph compilation. Google&\#x27;s own documentation states that once TorchTPU is public it will replace PyTorch/XLA, while third-party write-ups describe the two as complementary routes to PyTorch on TPUs. Google has framed TorchTPU as an &quot;Eager First&quot; stack built around XLA integration, aimed at simplifying model migration rather than requiring a JAX-style mental model.

**「Concrete migration path for PyTorch users」** For teams experimenting with TPUs, the supported path is now framework-level rather than a custom port: in Hugging Face Transformers v5, deploying a model to a TPU is done by passing \`device\_map=&quot;tpu&quot;\`, and the Diffusers library runs natively on TPUs in eager mode and under \`torch.compile\`. Scaling large generative models past a single accelerator still requires Diffusers&\#x27; tensor parallelism, so multi-chip setups remain a configuration step rather than a default.

**「Community discussion」** Commenters welcomed the release as first-party PyTorch-on-TPU support and compared it with adjacent efforts: one reported that an open-source libtpu implementation for Tenstorrent accelerators can already run most of TorchTPU, and another pointed to AWS’s torch-neuronx backend. Others argued XLA may be stronger compiler infrastructure than Inductor across hardware and read the release as further weakening TensorFlow’s position—opinions rather than measured results.

<details><summary>References</summary>
<ul>
<li><a href="https://developers.googleblog.com/torchtpu-running-pytorch-natively-on-tpus-at-google-scale/">TorchTPU : Running PyTorch Natively on TPUs at Google Scale</a></li>
<li><a href="https://docs.pytorch.org/xla/release/r2.8/index.html">PyTorch / XLA documentation — PyTorch / XLA master documentation</a></li>
<li><a href="https://www.sourcetrail.com/python/pytorch-on-tpus-deep-dive-into-torchtpu-xla-and-cloud-tpu/">PyTorch on TPUs : TorchTPU , XLA and Cloud TPU Explained</a></li>
<li><a href="https://cloud.google.com/blog/topics/ai-infrastructure/torchtpu-is-now-open-source-run-native-pytorch-on-tpus">TorchTPU is now open source: Run native PyTorch on TPUs</a></li>

</ul>
</details>

**Tags**: `#PyTorch`, `#TPU`, `#XLA`, `#open-source`, `#ML infrastructure`

---

<a id="item-tech-news-3"></a>
### [tsrs: a Rust port of TypeScript for WASM sandboxes](https://blog.cloudflare.com/typescript-rust-port/) ⭐️ 8.0/10

A Cloudflare blog post describes tsrs, a Rust port of the TypeScript compiler. Commenters say the driving motivation was a TypeScript compiler that could run inside a WASM-only sandbox without pulling in the full Go runtime that the existing Go-based tsc port requires, and that the Rust build turned out faster than that Go implementation. TypeScript team member Dan Rosenwasser said the team has been working with the tsrs maintainers to understand which optimizations are safe, and that its own Rust port suggests much of the speed comes from specific optimizations rather than the language choice, with some of those gains expected to land in TypeScript 7.1. The port uses a documented memory model that avoids a garbage collector by allocating long-lived objects in never-freed arenas.

hackernews · hnisjafx40 · Oct 20, 13:18 · [Discussion](https://news.ycombinator.com/item?id=50165953)

**「Background」** tsrs is a Rust implementation of the TypeScript 7 type checker, hosted in the oxc-project and published as an npm package. Cloudflare says it is collaborating on the port with VoidZero and Max Schwenk of Owner.com.

**「Impact」** For anyone who needs to type-check code inside a WASM sandbox — Cloudflare Workers among them — tsrs offers a route that avoids shipping the Go runtime that the existing Go-based compiler port carries. The arena scheme that makes a GC-based compiler tractable in Rust is also the main open question: commenters note it must still be shown sound, and the blog&\#x27;s description of the port as largely AI-generated draws objections from developers who rely on TypeScript daily.

**「Community discussion」** Rosenwasser&\#x27;s TypeScript-team comment pushes back on the framing that Rust alone explains the speedup, attributing much of it to optimizations that could also benefit the reference compiler. Other commenters focus on the design tradeoffs: afdbcreid describes the never-freed arenas as a way to fake a GC, while egonschiele welcomes the performance gains but objects to moving from a carefully handwritten port to an almost entirely AI-generated one.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.cloudflare.com/typescript-rust-port/">Introducing tsrs : a Port of TypeScript to Rust | Cloudflare Blog</a></li>
<li><a href="https://github.com/oxc-project/tsrs">GitHub - oxc - project / tsrs : Rust port of the TypeScript 7 type checker</a></li>

</ul>
</details>

**Tags**: `#TypeScript`, `#Rust`, `#compiler engineering`, `#WebAssembly`, `#memory management`

---

<a id="item-tech-news-4"></a>
### [Over 300 Tor exit nodes removed after SSH MITM campaign](https://kaba.cx/posts/20261020_Tor/) ⭐️ 8.0/10

The author reports that on October 2, 333 Tor exit nodes—roughly 10% of exits—began redirecting port 22 traffic to 12 interception servers running a paramiko-based man-in-the-middle that stole passwords and tried to deploy Ebury on targets. The first-person write-up says the operation led to more than 300 exit nodes being removed. The figures and attribution come from the author&\#x27;s account and were not independently confirmed in the supplied material.

hackernews · kabakabakaba · Oct 20, 13:39 · [Discussion](https://news.ycombinator.com/item?id=50166257)

**「Background」** Tor exit nodes are the relays that pass traffic between the anonymity network and the open internet, so whoever operates one can observe and rewrite any connection that is not encrypted above the transport layer — the reason a forged SSH host-key banner is a tell for a man-in-the-middle. Scanning exit relays for exactly this kind of tampering has a long history: commenter phw, who says they built exitmap more than ten years ago, notes the tool was still the one used to find the redirecting nodes in this case.

**「Impact」** For users authenticating to SSH through an affected Tor exit during the campaign, password-based logins were the exposed path; a commenter notes that key-based authentication should not be affected, so switching to keys avoids that specific credential-theft route.

**「Community Discussion」** phw, who says they built exitmap over ten years ago, welcomed its continued use in the response. jandrese argued the SSH targeting was poorly conceived because the MITM banner made detection and tracing easy, while another commenter noted key-based SSH authentication should be unaffected and highlighted a quoted warning that compromised hosting providers can be an Ebury vector.

**Tags**: `#Tor`, `#SSH`, `#MITM`, `#malware`, `#network security`

---

<a id="item-tech-news-5"></a>
### [Mistral&\#x27;s Voxtral 3 targets real-time speech and voice agents](https://mistral.ai/news/voxtral-3/) ⭐️ 7.0/10

Mistral has announced Voxtral 3, a speech model release presented with a voice-agent SDK that announcement text quoted in the discussion says combines listening, reasoning, tool calling, and speaking in real time over phone or web. The supplied announcement page had no accessible content, so model size, language coverage, latency, licensing, pricing, and availability remain unverified. Discussion immediately disputed the licensing, with one commenter calling the model closed, while another reported commercial offline deployment of the earlier open-weight Voxtral Mini 4B Realtime on commodity hardware.

hackernews · ilreb · Oct 20, 16:02 · [Discussion](https://news.ycombinator.com/item?id=50168396)

**「Background」** Voxtral is Mistral&\#x27;s speech model family, and earlier voice systems generally chained separate speech-to-text, reasoning, and text-to-speech components, which Mistral says remain hard to run together reliably in real time. The Voxtral 3 family splits models for recorded versus live audio and extends transcription coverage to 50+ languages, with the new SDK wrapping those pieces into one streaming pipeline.

**「Impact」** Teams building multilingual meeting transcription or voice agents get a new hosted option in Voxtral Small Transcribe 3, which adds speaker diarization and keyphrase-based context biasing—useful for identifying speakers and correcting domain terms—though Mistral&\#x27;s state-of-the-art accuracy claim still needs validation on their own audio. Budget planning should also account for the separate Voxtral TTS 3, listed on OpenRouter at $13 per million characters.

**「Community discussion」** Commenters split on licensing and practicality: one called Voxtral 3 closed and said local TTS/STT options remain weak, while another reported shipping commercial Windows software that runs the earlier Voxtral Mini 4B Realtime offline in 4 GB of VRAM, faster than realtime on a Ryzen 5 5600U iGPU, with a Linux port underway. Others described Microsoft Teams and 8x8 transcripts as too poor to feed LLMs reliably, and one raised a security concern about wiring a voice agent directly to a company intranet, imagining a caller asking it to fetch an internal accounting URL.

<details><summary>References</summary>
<ul>
<li><a href="https://mistral.ai/news/voxtral-3/">Voxtral 3: Voice Agent SDK &amp; Speech Models in 50+ Languages</a></li>
<li><a href="https://www.goodiebase.com/news/mistral-voxtral-3-voice-agent-sdk-2026-10-20">Mistral launches Voxtral 3 speech models and a toolkit for ...</a></li>
<li><a href="https://www.technobezz.com/news/mistral-ai-voxtral-3-voice-agent-sdk">Mistral AI Launches Voxtral 3 With Voice Agent SDK and 50 ...</a></li>
<li><a href="https://mistral.ai/news/voxtral-3/">Voxtral 3 : Voice Agent SDK &amp; Speech Models in 50+ Languages</a></li>
<li><a href="https://openrouter.ai/mistralai/voxtral-mini-tts-3-0">Voxtral TTS 3 - API Pricing &amp; Providers | OpenRouter</a></li>

</ul>
</details>

**Tags**: `#speech-to-text`, `#Mistral`, `#voice-agents`, `#open-weight-models`, `#real-time-inference`

---

<a id="item-tech-news-6"></a>
### [Google Cloud europe-west2 outage disrupts European banks and services](https://www.neowin.net/news/google-cloud-outage-takes-down-hsbc-revolut-bank-of-scotland-llyods-equifax-more/) ⭐️ 7.0/10

A Google Cloud outage in the europe-west2 region disrupted banking and other services across Europe, affecting HSBC, Revolut, Bank of Scotland, Lloyds, Equifax and others, according to Neowin. Google&\#x27;s status page said multiple services were affected beginning Monday, 2026-10-19 23:08 PDT, after a power event in the europe-west2-b zone; it said the power event was mitigated, with partial mitigation to infrastructure services expected within 30 minutes and remaining services to follow. The report does not establish a full restoration time or independently verify every affected service.

hackernews · paweladamczuk · Oct 20, 10:26 · [Discussion](https://news.ycombinator.com/item?id=50163961)

**「Incident origin」** The status-page excerpt quoted in the discussion said the europe-west2 incident began with a power event in the europe-west2-b zone at 23:08 PDT on 2026-10-19. It added that the power event had been mitigated, with partial mitigation for infrastructure services expected within 30 minutes.

**「Customer access and failover」** Customers of affected banks faced a loss of routine payment access: HSBC, Lloyds and Revolut services were disrupted, and one Revolut user reported that the app, withdrawals and card payments were unavailable, with no phone support to fall back on. For the banks and other affected organizations, the immediate continuity problem was dependence on a single cloud region: The Register reported &quot;no workarounds for now,&quot; leaving them waiting on Google&\#x27;s recovery rather than failing over to an alternate path.

**「Community Discussion」** Commenters reported uneven impact: one said Revolut left them unable to access their main account, make withdrawals or card payments, while another said HSBC was working normally and warned that Downdetector reports reflect user reports rather than confirmed outages. A separate comment argued that the EU should build alternatives to AWS and Google Cloud.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theregister.com/paas-and-iaas/2026/10/20/google-clouds-london-zones-takes-a-nap-multiple-services-disrupted/5304084">Google Cloud &#x27;s London zones takes a nap, multiple services disrupted</a></li>
<li><a href="https://www.bbc.co.uk/news/live/c58jd2kjp93xt">Google Cloud says services are recovering after outage hit banks ...</a></li>

</ul>
</details>

**Tags**: `#Google Cloud`, `#cloud outage`, `#europe-west2`, `#banking infrastructure`, `#service reliability`

---

<a id="item-tech-news-7"></a>
### [Rust Compiler Contributor Outlines 2026 Trait Solver and Polonius Work](https://yoyo-code.com/2026-is-exciting-year-for-rust-compiler-and-me/) ⭐️ 7.0/10

A Rust compiler contributor&\#x27;s personal post outlines planned 2026 compiler work covering the new trait solver, Polonius, compile-time improvements, and implications for async Rust. It is a forward-looking roadmap rather than an announcement of shipped features, and the available excerpt provides no version numbers, delivery dates, or measured results.

hackernews · panstromek · Oct 20, 13:53 · [Discussion](https://news.ycombinator.com/item?id=50166502)

**「Background」** Rust&\#x27;s compiler is replacing its trait solver, the component that proves trait bounds and normalizes associated types, with a next-generation solver intended to take over those type-system tasks \[tool-2-3\]. That effort has been underway for almost a decade and is meant to fix soundness bugs and unblock long-standing language features and fixes \[tool-2-1\]. Separately, Polonius is a new borrow checker intended to allow more code to compile than the current one \[tool-2-1\].

**「Stability and compile-time effects」** The next trait solver and Polonius remain in alpha, pre-stabilization testing, so stable-channel users should not expect behavior changes; developers exercising unstable features — including inside the standard library and the compiler itself — may instead hit new errors under that dedicated CI configuration. Async Rust users also still face gaps the solver work does not immediately close: async iterators \(streams\) and some uses of async in traits remain rough or not yet well-supported on stable. Independently, a benchmark of 629 measurements between 29 July and 28 September 2026 recorded a 4.57% mean wall-time reduction, suggesting compile-time work is producing modest measured gains rather than a step change.

**「Community Discussion」** Commenters welcomed the long-awaited trait solver work and hoped it, together with Polonius, would unblock specialization; others raised concerns about Rust compile times and target-directory size, and asked how the solver would affect async Rust and whether polymorphism settings could be controlled.

<details><summary>References</summary>
<ul>
<li><a href="https://daily.dev/posts/2026-is-an-exciting-year-for-the-rust-compiler-and-me--52dhmmibn">2026 is an exciting year for the Rust compiler (and me)</a></li>
<li><a href="https://goals.rust-lang.org/2026/next-solver.html">Stabilize the next-generation trait solver - Rust Project Goals</a></li>
<li><a href="https://rustc-dev-guide.rust-lang.org/tests/x86_64-gnu-next-trait-solver-polonius-ci-job.html">Pre-stabilization CI job for the next solver and polonius alpha - Rust ...</a></li>
<li><a href="https://rust-lang.github.io/async-book/">Introduction - Asynchronous Programming in Rust</a></li>
<li><a href="https://sitech.ge/en/blog/how-to-speed-up-the-rust-compiler-in-september-2026/">How rustc got faster in September 2026: mean compile time down...</a></li>

</ul>
</details>

**Tags**: `#Rust`, `#compiler development`, `#trait solver`, `#Polonius`, `#async Rust`

---

<a id="item-tech-news-8"></a>
### [Battle Drones: browser RTS with audio-based local multiplayer](https://simonwillison.net/2026/Oct/20/battledrones/) ⭐️ 7.0/10

Simon Willison published Battle Drones, a browser-based Command &amp; Conquer-style RTS built largely through Claude Code across 12 major iterations and 321 agent commits. It runs on mobile and desktop with six maps, a random map generator, skirmish and Last Stand modes, AI-vs-AI and LLM agent-vs-agent play, and a local multiplayer mode that synchronizes two nearby devices via audio. An update adds online multiplayer; Willison says the audio approach caused headaches and notes he reviewed almost none of the TypeScript code, relying on playtesting instead.

rss · Simon Willison · Oct 20, 19:34

**「Background」** Battle Drones is the latest in Simon Willison&\#x27;s series of LLM-assisted browser game experiments; he describes its audio multiplayer as an extension of &quot;Chirp Pong,&quot; an earlier experiment in device-to-device audio messaging linked in the post to October 15, 2026. The project began in July with Claude Fable 5 and grew through 12 major iterations and 321 commits by coding agents, mostly Claude Code. Early versions used the Phaser 2D framework and OpenAI-generated sprites before later revisions moved the game to 3D.

**「Impact」** Players can open the game in a desktop or mobile browser and inspect the TypeScript source on GitHub; developers considering sound-based networking should treat the audio mode as a working but troublesome local-only approach, since Willison added online multiplayer as a follow-up.

**Tags**: `#AI-assisted coding`, `#game development`, `#audio-based networking`, `#WebAudio`, `#real-time strategy`

---

<a id="item-tech-news-9"></a>
### [DeepSeek reportedly open-sources DeepInfer, claiming 155T tokens/day](https://github.com/deepseek-ai/DeepInfer) ⭐️ 7.0/10

DeepSeek reportedly open-sourced its internal large-scale inference framework, DeepInfer, on October 20, alongside a token codec component called deepseek-recipe. The framework is said to support distributed inference, speculative decoding, and structured output, and to run on Nvidia and Huawei Ascend hardware; its KVCache is claimed to retain data for more than 72 hours. The same single-source Telegram post claims that DeepInfer lets DeepSeek&\#x27;s V4.1 Flash reach 155 trillion tokens per day on a single cluster, but no independent verification or benchmark details accompany the claim.

telegram · zaihuapd · Oct 20, 09:11

**「Background」** DeepInfer is described on its GitHub repository as the high-performance inference framework powering DeepSeek&\#x27;s large-scale production services; the open-source release is characterized there as providing offline inference with the core features needed for serving at scale, with DeepSeek-V4.1-Flash listed as the supported model. DeepSeek-V4.1-Flash was already available as a model, with SGLang serving instructions on Hugging Face and a hosted version offered through OpenRouter.

**「Impact」** For teams evaluating model-serving stacks, the reported Huawei Ascend support would offer an alternative to Nvidia-only deployments, while the claimed 72-hour KVCache retention would require capacity planning for long-lived sessions; the claims should be checked against the repository before production use.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/deepseek-ai/DeepInfer">GitHub - deepseek -ai/ DeepInfer : DeepInfer : High-performance...</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash">deepseek -ai/ DeepSeek - V 4 . 1 - Flash · Hugging Face</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4.1-flash-1017">DeepSeek V 4 . 1 Flash 1017 - API Pricing &amp; Benchmarks | OpenRouter</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#inference framework`, `#open source`, `#distributed inference`, `#model serving`

---

<a id="item-tech-news-10"></a>
### [OpenAI claims major low-resource coding gains, 97.9% COBOL migration accuracy](https://openai.com/index/low-resource-programming-languages/) ⭐️ 7.0/10

OpenAI’s newest models reportedly deliver large gains in low-resource programming languages such as COBOL, Fortran, and Visual Basic, and the company has open-sourced the evaluation set on GitHub. In an OpenAI-attributed test that builds a SQLite engine across 20 languages, GPT-6 Astra’s average pass rate rose from GPT-5.6 Sol’s 26.8% to 87.4%; the cheaper GPT-6 Luna reached 40.3%, with API cost down 78%. For COBOL-to-modern-language migration, GPT-6.1 Sol rose from 5.4% accuracy at low reasoning to 86.6%, at 39% lower cost, and reached 97.9% at high reasoning. The figures are vendor-reported, and the supplied item is a brief aggregator post that provides no methodology or independent verification.

telegram · zaihuapd · Oct 20, 14:24

**「How the benchmarks were run」** OpenAI presents the gains as results on newly introduced evaluations: a multi-language software-engineering and SQLite benchmark, plus a separate COBOL migration test. A DEV Community analysis notes that the build benchmark is public while the COBOL migration tests are not, so the migration accuracy figures are vendor-reported rather than independently reproducible from the released test set.

**「Impact」** The GitHub evaluation set gives teams a way to compare models for legacy COBOL modernization, but the headline accuracy should be reproduced on their own code before adoption.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/low-resource-programming-languages/">Advancing coding in low ‑ resource programming languages | OpenAI</a></li>
<li><a href="https://qelvato.com/openai-boosts-coding-in-low-resource-programming-languages/">OpenAI boosts coding in low - resource programming languages</a></li>
<li><a href="https://dev.to/gabrielanhaia/openais-cobol-migration-score-jumped-from-54-to-866-the-tests-are-hidden-29go">OpenAI &#x27;s COBOL Migration Score Jumped From... - DEV Community</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#COBOL migration`, `#low-resource programming languages`, `#AI coding benchmarks`, `#legacy modernization`

---

<a id="item-tech-news-11"></a>
### [OpenAI API adds 12-hour prompt caching, report says](https://x.com/OpenAIDevs/status/2112603916076781778) ⭐️ 7.0/10

OpenAI&\#x27;s developer account has announced that the API now supports 12-hour prompt caching, according to a Telegram relay of the post. Persistent agents can reuse shared instructions, tools, and context throughout the day and still be billed at the lower cached-input rate even when requests are hours apart. Codex and Work signed-in users are also said to get permanent caching, with no penalty for returning to old conversations or resuming after a pause and a guarantee of cache hits. The relay does not provide official pricing details or the full eligibility scope.

telegram · zaihuapd · Oct 21, 01:21

**「Background」** Prompt caching lets an API reuse a previously processed input prefix, billing those tokens at a discounted cached-input rate rather than the full input price. The 12-hour extension announced on October 20, 2026 applies to the Responses API, where cache writes are billed at 2.5x, so whether a long-lived agent actually saves money depends on how often its cached instructions and tools are reused.

<details><summary>References</summary>
<ul>
<li><a href="https://articlesaboutai.com/openai-12-hour-prompt-caching-api/">OpenAI Adds 12-Hour Prompt Caching to Its API: Costs ...</a></li>

</ul>
</details>

**Tags**: `#OpenAI API`, `#prompt caching`, `#LLM infrastructure`, `#AI agents`, `#API pricing`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Super Micro raises outlook; SpaceX reports revenue jump and Tesla merger talks](https://www.cnbc.com/2026/10/20/stocks-making-the-biggest-moves-after-hours-isrg-nflx-spcx.html) ⭐️ 7.0/10

Super Micro Computer shares jumped 14% after hours after the data-center server company raised its fiscal first-quarter revenue outlook to $18.5 billion–$19.5 billion from $14.5 billion–$15.5 billion. SpaceX shares gained 8% after the company reported a 161% jump in third-quarter revenue to $14.58 billion, and Elon Musk said SpaceX and Tesla had formed special committees to discuss a merger.

rss · CNBC Finance · Oct 20, 22:55

**「Background」** Super Micro’s raised range is for fiscal first-quarter 2027, which ended Sept. 30, 2026, and came in a preliminary update ahead of full results scheduled for Nov. 3; Tesla and SpaceX each formed committees of independent directors to evaluate a possible merger, with no deal confirmed.

<details><summary>References</summary>
<ul>
<li><a href="https://techcrunch.com/2026/10/20/spacex-and-tesla-boards-form-special-committees-to-review-merger/">SpaceX and Tesla boards form special committees to review merger</a></li>
<li><a href="https://www.tesstudio.com/blogs/tesla-news/tesla-spacex-merger-special-committees-verified-brief">Tesla, SpaceX Form Merger Committees: What Is Confirmed</a></li>
<li><a href="https://ir.supermicro.com/news/news-details/2026/Supermicro-Provides-First-Quarter-of-Fiscal-Year-2027-Preliminary-Business-Update/default.aspx">Super Micro Computer, Inc. - Supermicro Provides First ...</a></li>
<li><a href="https://www.supermicro.com/en/pressreleases/supermicro-provides-first-quarter-fiscal-year-2027-preliminary-business-update">Supermicro Provides First Quarter of Fiscal Year 2027 ...</a></li>

</ul>
</details>

**Tags**: `#after-hours earnings`, `#corporate guidance`, `#SpaceX-Tesla merger talks`, `#market movers`, `#quarterly results`

---