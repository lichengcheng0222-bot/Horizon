---
layout: default
title: "Horizon Summary: 2026-10-23 (EN)"
date: 2026-10-23
lang: en
---

> From 43 items, 18 important content pieces were selected

---

**Technology News**
1. [Quad9 plans to exit France after DNS-blocking contempt fine](#item-tech-news-1) ⭐️ 8.0/10
2. [Blog describes claimed Switch 2 jailbreak using Codex and KVM](#item-tech-news-2) ⭐️ 8.0/10
3. [Australia court orders Apple to open iPhone to third-party app stores](#item-tech-news-3) ⭐️ 8.0/10
4. [NVIDIA OpenShell sandboxes autonomous AI agents with access controls](#item-tech-news-4) ⭐️ 7.0/10
5. [GNU Taler outlines preparations to operate in Germany](#item-tech-news-5) ⭐️ 7.0/10
6. [HackiOS boots iOS 16.5/XNU firmware via QEMU on select Android devices](#item-tech-news-6) ⭐️ 7.0/10
7. [eMudhra to exit global SSL/TLS certificate business amid root-program scrutiny](#item-tech-news-7) ⭐️ 7.0/10
8. [Blog claims 3.7M map polygons triangulated in 489 ms, faster than Earcut](#item-tech-news-8) ⭐️ 7.0/10
9. [Anthropic Donates Agent Skills Standard to Linux Foundation&\#x27;s AAIF](#item-tech-news-9) ⭐️ 7.0/10
10. [Carbon-X: open 14.8B DNA-text model runs on one 80GB GPU](#item-tech-news-10) ⭐️ 7.0/10
11. [WhissleAI shrinks steerable TTS to 11.84 MB with int4 QAT](#item-tech-news-11) ⭐️ 7.0/10
12. [Study finds some smart TVs still report ACR data after opt-out](#item-tech-news-12) ⭐️ 7.0/10
13. [miHoYo and Tsinghua open-source GameScaling game-control VLMs](#item-tech-news-13) ⭐️ 7.0/10
14. [Oracle issues high-severity Java SE JSSE alert for CVE-2026-91403](#item-tech-news-14) ⭐️ 7.0/10
15. [333 Tor exit relays found with Ebury backdoor and taken offline](#item-tech-news-15) ⭐️ 7.0/10
16. [Report alleges banned Nvidia B300 servers in China state-linked deal](#item-tech-news-16) ⭐️ 7.0/10

**Technology Blog**
1. [Software Speed Comes From Design, Not Language Choice](#item-tech-blog-1) ⭐️ 7.0/10

**Financial News**
1. [CSI 300 falls 20% from June high, nearing bear market](#item-finance-news-1) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Quad9 plans to exit France after DNS-blocking contempt fine](https://quad9.net/news/blog/au-revoir-france/) ⭐️ 8.0/10

Quad9 plans to exit France after a court dispute over DNS blocking and a contempt fine, its CTO said in the discussion thread. The CTO said Quad9 will probably apply geoIP filters to block French users after November 24, while acknowledging that geoIP blocking is insufficient for selectively denying resolution of individual domain names. The dispute involved a Sony Music Entertainment blocking order; the CTO said Sony accessed blocked content via a VPN from Germany and the court found Quad9 noncompliant.

hackernews · farrokhi · Oct 22, 14:32 · [Discussion](https://news.ycombinator.com/item?id=50195959)

**「Background」** Quad9 is a Swiss nonprofit public DNS resolver, a service that translates domain names into IP addresses for users who choose it instead of their ISP&\#x27;s resolver. According to Reclaim The Net, a French court had ordered Quad9 to block 58 domains or face a €580,000 fine, the dispute that preceded the planned exit. In the Hacker News thread, a commenter identifying himself as Quad9&\#x27;s CTO said Sony Music used a VPN from Germany to reach blocked content, after which the court found noncompliance and imposed a contempt fine.

**「Consequences for French users」** Quad9&\#x27;s CTO said the organization will probably apply geoIP filters that block French users from its service after November 24, so French users of 9.9.9.9 will need to reconfigure their devices to another resolver. That may not sidestep the underlying regime: a commenter noted that Google, Cloudflare and Cisco have also been subject to French web-blocking orders, with Cisco having exited the market.

**「Community Discussion」** Commenters criticized the outcome as unfair, arguing that Sony allegedly circumvented Quad9&\#x27;s geoIP blocking with a VPN and then won a contempt ruling, and one compared holding a resolver liable to punishing a phone-book publisher for a criminal&\#x27;s listed number. Another urged resolvers to stop resolving domains of companies that sue them, while one commenter said Quad9 appeared to be following Cisco&\#x27;s earlier exit from France over similar blocking orders.

<details><summary>References</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=50195959">Quad 9 ( DNS Resolver) to Exit France | Hacker News</a></li>
<li><a href="https://reclaimthenet.org/quad9-considers-leaving-france-over-website-blocking-order">French court asks Quad 9 to block 58 domains or face a €580,000 fine .</a></li>

</ul>
</details>

**Tags**: `#DNS`, `#internet governance`, `#privacy`, `#geo-blocking`, `#legal liability`

---

<a id="item-tech-news-2"></a>
### [Blog describes claimed Switch 2 jailbreak using Codex and KVM](https://pepsipu.com/blog/2026-10-switch2-jailbreak-ns2jb/) ⭐️ 8.0/10

A technical blog post describes a claimed jailbreak of the Nintendo Switch 2, and the supplied discussion focuses on decrypted filesystem access, game dumping, and using Codex with JetKVM hardware to automate controller input. Commenters speculate that read/write filesystem access could lead to Switch 2 game dumps and make exclusives playable on arbitrary hardware, but the jailbreak&\#x27;s claims are not independently verified in the supplied material. The discussion also notes a Bluetooth light-switch flicker, identified as a SwitchBot Bot, used to press the console&\#x27;s power button after crashes.

hackernews · ledoge · Oct 22, 08:01 · [Discussion](https://news.ycombinator.com/item?id=50192536)

**「Context: software-only, tethered exploit」** Coverage of the release describes ns2jb as a software-only, tethered userland exploit for the Switch 2 that reportedly works on firmware 23.0.1 without a hardware modchip — an unusual combination for a current console, where jailbreaks have generally depended on physical modification or a boot-time flaw. The linked blog post is developer pepsipu&\#x27;s own technical account of that exploit chain.

**「What filesystem access enables」** If the reported decrypted read/write filesystem access holds, users on the affected firmware could extract game data directly from the console, and commenters argue that dumped Switch 2 exclusives could then run on non-Nintendo hardware through existing recompilation projects — a scenario one commenter calls a worst case for Nintendo. Neither the jailbreak&\#x27;s capability nor that downstream outcome has been independently verified in the supplied material, so the game-dumping risk remains a claim rather than a demonstrated result.

**「Community discussion」** Commenters disagreed mainly on what the result demonstrates: hturan called it &quot;incredible all around&quot; and said they would not be surprised to see game dumps within hours if decrypted read/write filesystem access is real, while KeplerBoy argued the AI&\#x27;s role matters less than the security expertise and praised the KVM, USB controller, and Bluetooth-switch automation. rootsudo questioned how Codex could be used for this kind of research when it has refused similar Android CVE work.

<details><summary>References</summary>
<ul>
<li><a href="https://gbatemp.net/news/switch-2-jailbreak-ns2jb-released-software-only-exploit-tethered.685698/">Switch 2 jailbreak &quot; ns 2 jb &quot; released. Software-only... | GBAtemp.net</a></li>
<li><a href="https://www.notebookcheck.net/The-Nintendo-Switch-2-has-reportedly-been-jailbroken-through-a-software-only-exploit.1431060.0.html">The Nintendo Switch 2 has reportedly been... - Notebookcheck News</a></li>

</ul>
</details>

**Tags**: `#Nintendo Switch 2`, `#console jailbreak`, `#hardware security`, `#reverse engineering`, `#LLM automation`

---

<a id="item-tech-news-3"></a>
### [Australia court orders Apple to open iPhone to third-party app stores](https://9to5mac.com/2026/10/21/apple-must-open-iphone-to-alternative-app-stores-in-australia-after-epic-games-ruling/) ⭐️ 8.0/10

Australia&\#x27;s Federal Court has ruled that Apple must, from March 1, 2027, let Australian iPhone users install apps through third-party app stores and websites, and must allow alternative payment methods and external payment links. The decision in Epic Games&\#x27; antitrust case also means Fortnite will return to the Australian App Store immediately. The judge found Apple holds substantial market power in iOS app distribution and payments and that its restrictions violate Australian competition law. Apple said it will appeal and seek a stay of the ruling, so the changes are not yet in effect.

telegram · zaihuapd · Oct 22, 06:54

**「Why iOS app distribution is at issue」** Apple has historically restricted iPhone app installation to its own App Store and required in-app purchases to run through its payment system, the arrangement the Federal Court found gave Apple substantial market power in iOS distribution and payments and violated Australian competition law. The case arises from Epic Games&\#x27; antitrust litigation against Apple. The ruling&\#x27;s obligations do not take effect immediately: third-party stores, website installation and alternative payment links are required from March 1, 2027, and Apple says it will appeal and seek a stay.

**「Impact」** If the ruling takes effect, Australian iOS developers will be able to distribute apps outside Apple&\#x27;s App Store and direct users to external payment pages, rather than relying solely on Apple&\#x27;s in-app purchase system. Apple&\#x27;s appeal and stay request create timing risk, so developers and users should treat the March 2027 opening as conditional until the stay is resolved.

**Tags**: `#Apple`, `#反垄断`, `#应用商店`, `#Epic Games`, `#监管`

---

<a id="item-tech-news-4"></a>
### [NVIDIA OpenShell sandboxes autonomous AI agents with access controls](https://github.com/NVIDIA/OpenShell) ⭐️ 7.0/10

NVIDIA has published OpenShell, an open-source sandboxed runtime for running fleets of autonomous AI agents with restricted access to files, secrets, and networks. The project is positioned for agents that need to read files, install packages, call APIs, and use credentials without receiving unrestricted access to the host environment. Its isolation properties are described by the project and its users; the available material contains no independent security audit or benchmark.

hackernews · niemandhier · Oct 22, 17:44 · [Discussion](https://news.ycombinator.com/item?id=50198675)

**「Why sandboxed agent runtimes exist」** Autonomous agents typically need to read files, install packages, call APIs, and use credentials, so running them with a user&\#x27;s full permissions creates a large blast radius if the agent is manipulated or goes off course. Sandboxed runtimes reduce that exposure by isolating the agent process and enforcing limits on filesystem, secret, and network access; container-based isolation is a common precursor to this kind of control layer.

**「Impact」** For teams already running agents in containers, OpenShell offers a policy layer for filesystem, secret, and network access instead of ad hoc sandbox scripts. Operators should still examine exfiltration paths, because restricting agents to trusted domains does not by itself prevent data from leaving through those domains.

**「Community discussion」** Commenters welcomed a dedicated management layer for agent containers but disputed the promise of broad access without added risk: one argued that capability and exposure trade off directly, while another said domain allowlisting leaves exfiltration through trusted domains unresolved. A user reported running OpenShell and building additional team-policy, safe-git, and SCA/SAST controls above it.

**Tags**: `#AI agents`, `#security`, `#sandboxing`, `#runtime`, `#open source`

---

<a id="item-tech-news-5"></a>
### [GNU Taler outlines preparations to operate in Germany](https://www.taler.net/en/news/2026-13.html) ⭐️ 7.0/10

GNU Taler, an open-source privacy-preserving digital payments project, has announced that it is getting ready to operate in Germany. The supplied announcement gives no launch date, participating banks or merchants, supported services, or technical details, so the scope of the German rollout is not established. It is therefore a preparation announcement rather than evidence that Taler is already available to German users or merchants.

hackernews · dewey · Oct 22, 16:14 · [Discussion](https://news.ycombinator.com/item?id=50197404)

**「Background」** GNU Taler is a free-software electronic payment system that, unlike most decentralized payment systems, does not use a blockchain, according to a project overview. The project&\#x27;s news page lists recent work on Taler as an sCBDC technology, confidentiality and the digital euro, and a new be-BOP integration, providing context for its move toward operational deployment.

**「Wallet connectivity requirement」** Users will need to bring their Taler wallet online periodically: a Taler FAQ passage quoted in the discussion says e-money has a validity period and that tokens nearing expiry should be exchanged for new ones about a month beforehand, so a wallet left offline may miss that refresh window.

**「Community Discussion」** Commenters challenged the design, with one calling a system that requires periodic internet access and expires offline tokens &quot;infinitely worse than Bitcoin,&quot; while another argued that EU KYC requirements will choke off meaningful payment privacy. A commenter who identified as a GLS Bank customer welcomed what they described as the bank&\#x27;s involvement and framed Taler as a way to reduce Europe&\#x27;s dependence on US payment providers.

<details><summary>References</summary>
<ul>
<li><a href="https://www.taler.net/">GNU Taler : Home</a></li>
<li><a href="https://www.wikiwand.com/en/GNU_Taler">GNU Taler - Wikiwand</a></li>

</ul>
</details>

**Tags**: `#GNU Taler`, `#digital payments`, `#privacy`, `#open source`, `#EU regulation`

---

<a id="item-tech-news-6"></a>
### [HackiOS boots iOS 16.5/XNU firmware via QEMU on select Android devices](https://github.com/oosexgang/hackios-xnu-kernel) ⭐️ 7.0/10

The HackiOS GitHub project demonstrates booting iOS 16.5/XNU firmware under QEMU and on a limited set of Android hardware, including the POCO X5 Pro 5G and some Xiaomi devices. It is a research bench rather than a usable iOS port or ROM: according to a commenter quoting the project&\#x27;s description, a session lasts for a fixed number of seconds, then the kernel returns to the loader and hands over its log. That makes the repository&\#x27;s “full iOS on Android” framing misleading for anyone expecting a daily-driver install.

hackernews · aghuang · Oct 22, 15:26 · [Discussion](https://news.ycombinator.com/item?id=50196718)

**「Background」** XNU is Apple&\#x27;s open-source kernel, but iOS&\#x27;s user space and hardware drivers are not, so booting iOS on Android requires a custom boot path and replacements for Apple&\#x27;s closed drivers. The project&\#x27;s GitHub description says HackiOS boots XNU 8796.121.2—the kernel shipped with iOS 16.5—and then runs the unmodified iOS 16.5 user space, using its own EFI loader, replacement drivers, a UEFI port, and a Linux Wi-Fi driver on a compatibility layer.

**「Impact」** Developers should treat HackiOS as a short-lived boot and logging target for XNU experiments, not an installable phone OS; the described fixed session length and return to the loader rule out normal daily use.

**「Community Discussion」** Commenters drew a line between a demo and a product: one quoted the project&\#x27;s own description that it is “a research bench, not a ROM,” with sessions ending after a set time and returning to the loader. Another speculated that such demos could make it harder to verify used iPhones, citing existing Android replica phones, but that concern was not tied to evidence about this project.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/oosexgang/hackios-xnu-kernel">GitHub - oosexgang/ hackios -xnu-kernel</a></li>

</ul>
</details>

**Tags**: `#iOS`, `#Android`, `#XNU kernel`, `#QEMU`, `#systems hacking`

---

<a id="item-tech-news-7"></a>
### [eMudhra to exit global SSL/TLS certificate business amid root-program scrutiny](https://emudhra.com/en/press-release/emudhra-to-exit-global-ssl-tls-certificate-business) ⭐️ 7.0/10

eMudhra announced it will exit its global SSL/TLS certificate business after browser-root-program scrutiny of an apparent certificate-authority operations failure. In the announcement, the company said social-media amplification had brought scrutiny &quot;out of proportion&quot; to SSL/TLS&\#x27;s place in its business, and it did not provide a clear root-cause account. The move affects customers relying on eMudhra-issued publicly trusted TLS certificates, who will need to migrate to another certificate authority.

hackernews · bo0tzz · Oct 22, 13:33 · [Discussion](https://news.ycombinator.com/item?id=50195110)

**「Background」** eMudhra is an Indian PKI company licensed by the Controller of Certifying Authorities to issue digital signature certificates in India; it has been publicly listed since 2022. Its global SSL/TLS business depends on browser root programs, which determine whether a certificate authority&\#x27;s certificates are trusted by mainstream browsers and operating systems.

**「Migration burden for eMudhra TLS customers」** Any organization whose certificates chain to eMudhra&\#x27;s global TLS hierarchy now has to replace those certificates and line up another CA, because eMudhra&\#x27;s board decided on October 22 to withdraw from the global SSL/TLS business entirely rather than reissue under the affected intermediates. The trigger was a researcher recovering the private keys of eight of the company&\#x27;s intermediate CA certificates, so operators should treat certificates issued under those intermediates as compromised and check replacement against their existing chain and renewal timelines.

**「Community discussion」** Commenters focused on the apparent CA-operations failure rather than the business decision. One said the absence of an apology or an explanation of whether the error was human or procedural made eMudhra look bad, another pointed to browser engineers&\#x27; detailed questions in a Mozilla root-program bug, and a joke about an RSA private key consisting of &quot;4&quot; reflected the view that the reported weak keys were implausibly basic.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/EMudhra">eMudhra - Wikipedia</a></li>
<li><a href="https://thehackernews.com/2026/10/emudhra-to-exit-global-ssltls-business.html">eMudhra to Exit Global SSL / TLS Business After 8 Intermediate CA...</a></li>
<li><a href="https://emudhra.com/en/press-release/emudhra-to-exit-global-ssl-tls-certificate-business">eMudhra to Exit global SSL / TLS Certificate Business</a></li>
<li><a href="https://www.moneycontrol.com/technology/emudhra-to-exit-global-website-security-certificate-business-after-key-generation-flaw-article-14057821.html">eMudhra to exit global website security certificate business after...</a></li>

</ul>
</details>

**Tags**: `#PKI`, `#TLS certificates`, `#certificate authorities`, `#web security`, `#browser trust stores`

---

<a id="item-tech-news-8"></a>
### [Blog claims 3.7M map polygons triangulated in 489 ms, faster than Earcut](https://globus.software/blog/2026/10/16/cutting-map-polygons/) ⭐️ 7.0/10

A blog post claims a polygon-triangulation approach processes 3.7 million map polygons in 489 ms, faster than Earcut. The post reports the result for map and geospatial workloads and publishes the datasets used for benchmarking; the figure is the author&\#x27;s claim, not an independent measurement.

hackernews · molind · Oct 22, 09:31 · [Discussion](https://news.ycombinator.com/item?id=50193170)

**「Background」** Earcut is the widely used JavaScript triangulator that converts map polygons into triangles for GPU rendering, and its ear-clipping approach rests on Meisters&\#x27; theorem, which applies to simple polygons. The blog notes that map data rounded to a tile grid can break that simplicity, which is where the harder cases arise; it also benchmarks against a Delaunay baseline, reporting 6.0 times less time on the same polygons.

**「Impact」** Developers evaluating triangulation libraries for large map datasets can use the published benchmark to reproduce or challenge the result. Adoption decisions also need to weigh WASM bundle size and output triangle quality, both raised in the discussion.

**「Community discussion」** Earcut&\#x27;s author said he intentionally rejected optimizations that would increase bundle size, noting Earcut is 4.1 kB min/gzip and asking how large the WASM build is; the Delaunay32 author asked how divide-and-conquer would compare and noted that his current polygon API accepts only simple rings with non-touching holes. Other commenters questioned whether the approach&\#x27;s long, thin triangles suit GPU rasterization and why ear clipping has beaten Seidel&\#x27;s method despite its asymptotic advantage.

<details><summary>References</summary>
<ul>
<li><a href="https://globus.software/blog/2026/10/16/cutting-map-polygons/">Faster than earcut : triangulating 3 . 7 M map polygons in 489 ms</a></li>

</ul>
</details>

**Tags**: `#computational geometry`, `#triangulation`, `#performance optimization`, `#WebAssembly`, `#geospatial`

---

<a id="item-tech-news-9"></a>
### [Anthropic Donates Agent Skills Standard to Linux Foundation&\#x27;s AAIF](https://simonwillison.net/2026/Oct/22/donating-agent-skills/) ⭐️ 7.0/10

Anthropic announced it is donating its Agent Skills standard to the Agentic AI Foundation \(AAIF\), the Linux Foundation body it co-founded with Block and OpenAI, saying it wants the standard to remain open, community-driven, and vendor-neutral. AAIF already hosts the Model Context Protocol, which Anthropic previously donated. Simon Willison notes that he predicted the move last December, when Anthropic first declared skills an &quot;open standard.&quot; The post is a governance announcement and describes no changes to the skills format itself.

rss · Simon Willison · Oct 22, 18:09

**「Background」** Agent Skills is Anthropic&\#x27;s format for packaging instructions, scripts, and resources that an agent loads on demand for a specific task. Anthropic first described skills as an &quot;open standard&quot; in December 2025, and the Agentic AI Foundation — co-founded by Anthropic, Block, and OpenAI — already hosts the Model Context Protocol specification that Anthropic previously donated.

**「Impact」** For developers building Agent Skills, the practical change is where the standard is steered: the announcement places its stewardship with AAIF alongside MCP, rather than solely with Anthropic. The post does not detail AAIF&\#x27;s approval process or timeline, so teams should treat the governance mechanics as pending until the foundation publishes them.

**Tags**: `#agentic AI`, `#Agent Skills`, `#open standards`, `#AI governance`, `#Anthropic`

---

<a id="item-tech-news-10"></a>
### [Carbon-X: open 14.8B DNA-text model runs on one 80GB GPU](https://www.reddit.com/r/MachineLearning/comments/1xchayq/carbonx_is_an_open_148b_model_trained_jointly_on/) ⭐️ 7.0/10

Hugging Face has published Carbon-X, an Apache 2.0 decoder-only model with 14.8B parameters that accepts raw DNA inside a normal chat and answers in English, using a single token stream with 6-mer DNA tokens and mid-training on 302B tokens. The model card reports a 66.7% average across five DNA benchmarks with thinking disabled, against 67.5% for GPT-6.1 Sol — figures that are vendor-reported and not independently validated in the release. The bf16 weights fit on one 80 GB GPU. The post states the model has not been clinically validated and that the model card directs exact sequence operations to code rather than to the model itself.

reddit · r/MachineLearning · /u/jatingargiitk · Oct 22, 12:32

**「Background」** Carbon-X belongs to Hugging Face&\#x27;s existing Carbon family of genomic models, which had previously shipped at smaller sizes such as Carbon-8B; the project is a joint effort between Hugging Face, Zhongguancun Academy, and TIGEM/University of Naples &quot;Federico II&quot; and is released under Apache 2.0. Carbon-X is mid-trained from Qwen3-14B, a general-purpose text model, and the model card reports its 66.7% five-benchmark DNA average as 27 points above that starting checkpoint and ahead of every other open model the team evaluated.

**「Impact」** Because the full weights run in bf16 on a single 80 GB GPU under a permissive Apache 2.0 license, genomics teams can keep sensitive sequence data on their own hardware instead of sending it to a hosted model API; the stated clinical caveat and the model card&\#x27;s guidance to handle exact sequence operations in code mean such local use still needs its own validation before anything downstream depends on the output.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/HuggingFaceBio/Carbon-X">HuggingFaceBio / Carbon - X · Hugging Face</a></li>
<li><a href="https://github.com/huggingface/carbon">GitHub - huggingface/ carbon : The home of Carbon Genomic...</a></li>

</ul>
</details>

**Tags**: `#DNA language models`, `#open weights`, `#multimodal models`, `#bioinformatics`, `#model evaluation`

---

<a id="item-tech-news-11"></a>
### [WhissleAI shrinks steerable TTS to 11.84 MB with int4 QAT](https://www.reddit.com/r/MachineLearning/comments/1xcum4s/we_shrank_our_steerable_small_tts_to_1184_mb_wer/) ⭐️ 7.0/10

WhissleAI has released steer-tts-edge, an 11.84 MB English text-to-speech package whose total size includes weights, 200 voices, a NumPy-only text front end, and the Python runtime. The 9.25M-parameter acoustic model and a 6.2M-parameter Vocos-style vocoder distilled from charactr/vocos-mel-24khz are int4 quantization-aware trained; the release reports that all 12 steering controls retain at least 95% of their fp32 effect. Under the Open TTS Leaderboard protocol run locally, not as an official submission, WER stayed at 0.96% while UTMOS fell from 4.20 to 4.11, mostly because of the small int4 vocoder. The model runs on CPU at RTF 0.053 with four threads and about 120 ms to first audio, but it is English-only and lacks voice cloning, free-text prompts, and the full model’s flow refiner.

reddit · r/MachineLearning · /u/Working\_Hat5120 · Oct 22, 20:57

**「Background」** SteerTTS is a small English text-to-speech model whose output is adjusted through numeric controls rather than text prompts; the edge release follows the author&\#x27;s earlier v1 model. Quantization-aware training simulates int4 arithmetic during training so weights adapt to low precision, and a vocoder converts the acoustic model&\#x27;s features into the final audio waveform.

**「Impact」** For edge developers, the practical change is a TTS stack small enough to bundle into an app, with 200 voices and numeric steering controls preserved after quantization. The size reduction does not by itself improve runtime speed: the int4 weights are dequantized to fp32 at load, so faster execution would require new edge kernels. Applications that need voice cloning, free-text style prompts, or the full model’s flow refiner must still use the larger model.

**Tags**: `#text-to-speech`, `#quantization-aware training`, `#int4`, `#edge ML`, `#speech synthesis`

---

<a id="item-tech-news-12"></a>
### [Study finds some smart TVs still report ACR data after opt-out](https://watchingthewatchers.github.io/watchingthewatchers/index.html) ⭐️ 7.0/10

A study of 12 smart TVs from 10 vendors, run as 5,943 controlled experiments, found that some models continued sending content-related traffic after automatic content recognition \(ACR\) was disabled in settings. Two platforms exposed viewing information in plaintext: VIDAA OS sent data over unencrypted MQTT, including a device ID that cannot be reset and audio fingerprints, while Vizio&\#x27;s WatchFree+ placed program names in unencrypted domain queries that users cannot turn off. The findings apply to the smart TV owners whose sets were tested and point to gaps between ACR opt-out controls and actual network behavior.

telegram · zaihuapd · Oct 22, 09:50

**「Background」** Automatic content recognition \(ACR\) works by capturing short audio or video fingerprints and matching them against a reference database to identify what is playing. On smart TVs, the feature is generally presented as optional and tied to privacy settings that are supposed to control whether viewing data is collected and shared.

**「Opting out is not enough」** The practical consequence for owners of the tested sets is that the in-menu ACR toggle cannot be relied on as a privacy control: Ars Technica reports that TVs running Samsung, Vizio and Roku software kept contacting ACR endpoints after users opted out, and the study found Vizio&\#x27;s WatchFree+ service writes program names into unencrypted DNS and SNI lookups to Amagi, which users have no setting to disable. Because VIDAA OS traffic arrives in plaintext MQTT with a non-resettable device ID and audio fingerprints, blocking those endpoints at the router or withholding network access is the only measure the evidence supports for concerned users.

<details><summary>References</summary>
<ul>
<li><a href="https://arstechnica.com/gadgets/2026/10/does-opting-out-of-smart-tv-tracking-work-research-finds-suspicious-traffic/">Does opting out of smart TV tracking work? Research... - Ars Technica</a></li>
<li><a href="https://watchingthewatchers.github.io/watchingthewatchers/index.html">Watching the Watchers : Privacy Analysis of U.S. Smart TV Automatic...</a></li>

</ul>
</details>

**Tags**: `#smart TVs`, `#privacy`, `#ACR`, `#IoT security`, `#data exposure`

---

<a id="item-tech-news-13"></a>
### [miHoYo and Tsinghua open-source GameScaling game-control VLMs](https://arxiv.org/abs/2610.28698v1) ⭐️ 7.0/10

miHoYo&\#x27;s Honkai AI team, working with Tsinghua University and other collaborators, released GameScaling, a family of Qwen3.5-based vision-language models continually pretrained to produce keyboard and mouse actions, ranging from 0.8B to 27B parameters. Each inference step outputs the next 200 milliseconds of keyboard/mouse input. The accompanying paper reports experiments across 120 training configurations spanning data volume, data diversity, and model size: more data improved performance on same-distribution games, while greater diversity aided transfer to similar games but gave limited gains on very different worlds. Eight checkpoints and an inference client are released under Apache-2.0; training code is not included. The release is currently reported through a Telegram channel alongside the arXiv preprint and GitHub link, and the code and checkpoint availability has not been independently verified here.

telegram · zaihuapd · Oct 22, 11:32

**「How GameScaling is trained and evaluated」** GameScaling adapts general Qwen3.5 vision-language backbones to keyboard-and-mouse gameplay through continued pre-training. Its project page reports test-time scaling on MCU, comparing GameScaling-0.8B-S1 and GameScaling-9B-S1 checkpoints with their untrained Qwen3.5 backbones over 150 rollouts as the allowed step budget increases.

**「Impact」** Game-AI and VLM-agent researchers can evaluate or fine-tune Apache-2.0 checkpoints from 0.8B to 27B without training a model from scratch, but the withheld training code means the 120-configuration scaling study cannot be reproduced directly, and extending the approach to substantially different games is exactly where the paper reports the smallest benefit from added data diversity.

<details><summary>References</summary>
<ul>
<li><a href="https://gamescaling.github.io/">Scaling in Games : Continued Pre-Training for Embodied Agents in...</a></li>

</ul>
</details>

**Tags**: `#game AI`, `#vision-language models`, `#open-source models`, `#model scaling`, `#keyboard/mouse control`

---

<a id="item-tech-news-14"></a>
### [Oracle issues high-severity Java SE JSSE alert for CVE-2026-91403](https://www.oracle.com/security-alerts/alert-cve-2026-91403.html) ⭐️ 7.0/10

Oracle issued a high-severity security alert for CVE-2026-91403, a flaw in the JSSE component of Java SE and GraalVM that is remotely exploitable without authentication and rated CVSS 9.1. The affected versions listed are Java SE 8u511, 11.0.33, 17.0.21, 21.0.13, 25.0.5, 27.0.1 and multiple GraalVM versions. Oracle says fixes are available and urges users to upgrade to supported versions; the alert warns of potential severe impact on data confidentiality and integrity.

telegram · zaihuapd · Oct 22, 12:30

**「Context on JSSE」** JSSE \(Java Secure Socket Extension\) is the Java SE component that provides SSL/TLS and secure socket support, so flaws in it can affect applications using Java&\#x27;s built-in encrypted networking rather than an external TLS library. Oracle assigned CVE-2026-91403 to the JSSE issue covered by this security alert.

**「Upgrade exposure window」** Because CVE-2026-91403 is remotely reachable without authentication through JSSE, organizations running the listed builds \(Java SE 8u511, 11.0.33, 17.0.21, 21.0.13, 25.0.5, 27.0.1, plus the affected GraalVM releases\) should treat internet-facing Java services as exposed and move to Oracle&\#x27;s patched builds; the alert does not name the fixed version numbers, so the exact upgrade target has to be confirmed against Oracle&\#x27;s advisory before rolling out.

**Tags**: `#Java SE`, `#security vulnerability`, `#Oracle`, `#JSSE`, `#patching`

---

<a id="item-tech-news-15"></a>
### [333 Tor exit relays found with Ebury backdoor and taken offline](https://kaba.cx/posts/20261020_Tor/) ⭐️ 7.0/10

A Tor operator scanned roughly 3,000 exit relays and found 333 infected with the Ebury backdoor — about 10% of exits — which redirected SSH connections on port 22 to 12 intercept servers to harvest credentials, according to a short news summary. The relays were flagged BadExit on October 4 and had all gone offline the following day. The attackers had compromised the servers in August and blocked some ports to focus on collecting unencrypted email traffic; how they gained initial access is still undetermined. The finding comes from a single operator&\#x27;s scripted scan and has not been independently confirmed.

telegram · zaihuapd · Oct 22, 14:52

**「Background」** Tor clients route traffic through a three-relay circuit, and the exit relay is the final hop that connects the circuit to the public internet; that position lets a compromised exit observe or redirect traffic bound for ordinary services. Tor&\#x27;s BadExit flag is used to tell clients not to select a relay for exit traffic.

**「Impact」** Anyone who made SSH connections through Tor exits during the exposure window should treat the credentials used as potentially compromised, since the BadExit flag only removes the relays from exit selection and does not undo credentials already captured.

<details><summary>References</summary>
<ul>
<li><a href="https://xakep.ru/2026/10/22/tor-exit-attack/">Хакеры захватили более 300 выходных узлов Tor ради перехвата...</a></li>

</ul>
</details>

**Tags**: `#Tor`, `#cybersecurity`, `#backdoor`, `#Ebury`, `#SSH`

---

<a id="item-tech-news-16"></a>
### [Report alleges banned Nvidia B300 servers in China state-linked deal](https://theinference.org/article/china-s-state-money-bought-banned-nvidia-b300-servers-then-redacted-the-receipts) ⭐️ 7.0/10

A report alleges that a Chinese state-controlled semiconductor leasing group financed the purchase of 32 ASUS servers carrying Nvidia&\#x27;s export-restricted B300 chips for the AI company 荣耀视图科技. The servers were part of a transaction covering more than 700 servers and worth over RMB 3 billion, and were intended for China Mobile&\#x27;s Ningxia hub, according to the report. The B300 sits in the strictest U.S. export-control tier and is effectively barred from China; after the filing drew scrutiny, the leasing group reportedly refiled with the hardware description redacted. Nvidia said it is investigating with its manufacturing partners, while ASUS said it complies with export controls.

telegram · zaihuapd · Oct 22, 15:22

**「Export-control context」** Nvidia&\#x27;s B300 is a data-center accelerator from its Blackwell generation, the class of chips Washington has placed under its strictest export-control tier for China—effectively an embargo, since licenses for such sales are largely not granted. Because the restrictions attach to the hardware itself, the appearance of B300 servers inside a Chinese state-linked deployment raises the question of how and when the units left Nvidia&\#x27;s supply chain, which is what the reported Nvidia and ASUS reviews are examining.

**Tags**: `#Nvidia B300`, `#export controls`, `#China`, `#AI hardware`, `#semiconductor supply chain`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Software Speed Comes From Design, Not Language Choice](https://seangoedecke.com/software-is-slow-because-of-bad-design-not-slow-languages/) ⭐️ 7.0/10

rss · Sean Goedecke · Oct 23, 00:00

**「Background」** Sean Goedecke challenges the claim that AI-driven rewrites into C, Rust, or assembly will generally make software faster, even though raw language speed can differ by orders of magnitude. The question is why that gap rarely translates into meaningful application speedups.

**「Solution」** His central explanation is that most real programs are I/O-bound: in a database-backed CRUD app, for example, he estimates half a request might be spent querying the database, so rewriting the rest in C could at best double performance and probably yield closer to 1.5x, a ceiling consistent with Amdahl’s law. Where work is CPU-bound, slow languages often already delegate it to optimized libraries, as Python does for machine learning and GPU matrix multiplication, and as markdown renderers do through libraries such as cmark-gfm. He concedes that neglected CPU-heavy programs may contain easy wins, but argues important programs tend to be optimized already; he cites an assembly rewrite of tiktoken that was roughly 5x faster on his laptop, while noting tokenization is marginal beside inference and that the gain may come from avoiding regex rather than language speed. His stronger evidence is design: Bryan Cantrill’s naive Rust rewrite of a carefully optimized C program ran 30% faster because Rust preferred a cache-efficient B-tree, and Goedecke’s own large wins came from caching, asynchronous or parallel execution, replacing N+1 SQL queries with one query, and skipping unnecessary work. These changes are independent of language speed, and higher-level code can make such redesigns easier to spot.

**「Takeaway」** Goedecke concludes that raw speed is primarily a property of design—doing less work and improving I/O—not language choice. He recommends using AI agents to profile, find hotspots, and propose redesigns, reserving language rewrites for rare, genuinely CPU-bound sections.

**Tags**: `#software performance`, `#optimization`, `#I/O-bound systems`, `#language choice`, `#profiling`

---

## Financial News

<a id="item-finance-news-1"></a>
### [CSI 300 falls 20% from June high, nearing bear market](https://www.bloomberg.com/news/articles/2026-10-22/china-stocks-set-for-bear-market-as-ai-trade-policy-hopes-fade) ⭐️ 7.0/10

The CSI 300 fell as much as 1.7% on Thursday and was 20% below its June high, leaving Chinese onshore stocks on the verge of a bear market amid a lack of substantive fiscal stimulus and weaker-than-expected earnings. CATL shares fell 12% on Wednesday after its quarterly profit growth missed expectations.

telegram · zaihuapd · Oct 22, 05:05

**「Background」** The CSI 300 tracks large, relatively liquid stocks listed in Shanghai and Shenzhen; a bear market is commonly defined as a decline of at least 20% from a recent peak.

**Tags**: `#China A-shares`, `#CSI 300`, `#bear market`, `#CATL earnings`, `#fiscal stimulus`

---