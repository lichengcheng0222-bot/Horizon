---
layout: default
title: "Horizon Summary: 2026-10-24 (EN)"
date: 2026-10-24
lang: en
---

> From 33 items, 8 important content pieces were selected

---

**Technology News**
1. [Blog post claims an iPhone hack, sparking jailbreak and Lockdown Mode debate](#item-tech-news-1) ⭐️ 8.0/10
2. [Kimi K3.1-Pro ships via API with 1M-token context, weights promised by Nov 4](#item-tech-news-2) ⭐️ 8.0/10
3. [Block announces Dessa full-duplex speech model with claimed local MacBook inference](#item-tech-news-3) ⭐️ 7.0/10
4. [Swarm Imitation Argued Equivalent to a Single Bandit-Learning Agent](#item-tech-news-4) ⭐️ 7.0/10
5. [PHP Foundation recommends disabling upload progress over RCE risk](#item-tech-news-5) ⭐️ 7.0/10

**Financial News**
1. [China issues guidelines to soften AI&\#x27;s job-replacement impact](#item-finance-news-1) ⭐️ 8.0/10
2. [China to implement upgraded CCC certification rules for e-bikes, toys and strollers from November 2026](#item-finance-news-2) ⭐️ 7.0/10
3. [China Approves Citigroup Securities \(China\) With RMB 1.2 Billion Registered Capital](#item-finance-news-3) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Blog post claims an iPhone hack, sparking jailbreak and Lockdown Mode debate](https://blog.calif.io/p/iphone) ⭐️ 8.0/10

A blog post titled &quot;Today, we hacked what we&\#x27;d set out to hack: the iPhone&quot; claims its authors achieved an iPhone compromise, and the post drew a large Hacker News thread \(741 points, 499 comments\). The supplied excerpt contains no exploit specifics — no affected iOS versions, vulnerability class, exploited component, or indication of whether Apple was notified — so the claim of a working hack is unverified beyond the authors&\#x27; own statement. The discussion frames the work around jailbreaking, Apple&\#x27;s Lockdown Mode, and who gets access to frontier-model security tooling.

hackernews · pavel\_lishin · Oct 23, 16:21 · [Discussion](https://news.ycombinator.com/item?id=50211474)

**「Background」** Calif&\#x27;s newsletter had earlier reported that the group demonstrated the first public bypass of Apple&\#x27;s Memory Integrity Enforcement on macOS 26.4.1, which frames the iPhone claim as a continuation of that memory-safety work rather than an isolated stunt. Coverage of the demonstration describes it as a jailbreak for iOS 27.0.1, with technical details expected to be published only after Apple closes the vulnerabilities in an update. Lockdown Mode, which commenters ask about, is Apple&\#x27;s opt-in hardening setting meant to shut down many of the common attack paths such exploit chains rely on.

**「Patch level and Lockdown Mode remain the practical controls」** For iPhone users, the actionable takeaway is that software version and Lockdown Mode still carry the defensive weight: Google&\#x27;s Threat Intelligence Group reported in March 2026 that the Coruna exploit kit&\#x27;s five iOS chains and 23 exploits targeted iOS 13.0 through 17.2.1 and were not effective against the latest iOS, and Apple said the same month that it had not seen a successful spyware attack against a device running Lockdown Mode. The supplied material does not establish whether the demo described in the post defeats Lockdown Mode, so any claim that the setting is bypassed remains unverified here.

**「Community discussion」** Commenters asked whether enabling Lockdown Mode actually blunts the demonstrated exploits, with one noting it should block many common attack vectors but that real-world effectiveness is unclear. Others focused on access: one researcher said frontier labs restrict red-team-capable models to an inner circle of companies, making &quot;trusted cyber access&quot; a moat rather than a safeguard, and another argued that Apple can detect a jailbreak and cut off iCloud and iMessage, reducing the device to an iPod touch.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.calif.io/">Calif Newsletter | Substack</a></li>
<li><a href="https://www.heise.de/en/news/Calif-io-jailbreak-How-the-untethered-tool-cracks-iOS-27-0-1-11492321.html">Calif.io jailbreak: How the untethered tool cracks iOS 27.0.1</a></li>
<li><a href="https://techcrunch.com/2026/03/27/apple-says-no-one-using-lockdown-mode-has-been-hacked-with-spyware/">Apple says no one using Lockdown Mode has been hacked with ...</a></li>
<li><a href="https://thehackernews.com/2026/03/coruna-ios-exploit-kit-uses-23-exploits.html">Coruna iOS Exploit Kit Uses 23 Exploits Across Five Chains ...</a></li>

</ul>
</details>

**Tags**: `#iPhone security`, `#exploit research`, `#jailbreaking`, `#Lockdown Mode`, `#AI security access`

---

<a id="item-tech-news-2"></a>
### [Kimi K3.1-Pro ships via API with 1M-token context, weights promised by Nov 4](https://www.kimi.ai/blog/kimi-k3-1-pro) ⭐️ 8.0/10

Kimi released K3.1-Pro, which it describes as its strongest three-trillion-parameter open-weight model, available now in Kimi, Kimi Work, Kimi Code and the API, with full model weights promised for release by November 4, 2026 — so the model is currently API-only. It carries a 1M-token context window and targets coding, 3D creation, financial research and complex agent tasks: Kimi&\#x27;s own figures put Terminal-Bench 4.0 at 65.7% \(versus 58.2% for GPT-6 Astra and 66.4% for Claude Opus 5.5\), internal long-task coding at 61.2% \(up from 55.95% for K3\), BenchCAD-assisted scoring at 92.7%, and statement-level hallucination on internal hard tests falling from 23.4% to 8.3%, though Kimi cautions that this does not represent everyday error rates. A Highspeed variant runs 2-3x faster at twice the price, except for cached input tokens, which are priced the same; standard US pricing is $2 per million input tokens and $10 per million output tokens, matching GPT-6.1 Sol and half of Claude Opus 5.5. Independent evaluator Artificial Analysis scored the model 55, behind Claude Opus 5.5 at 58 and ahead of Claude Fable 5.1, GPT-6 Astra and Gemini 4 Argon, all at 53.

telegram · zaihuapd · Oct 23, 17:14

**「Background」** Kimi K3.1-Pro is the first model in the K3.1 series and is described as building on K3 with expanded post-training. The “open-weight” label is prospective rather than current API availability: Kimi says the model is already available through Kimi, Work, Code and the API, while the full weights are due by Nov. 4, 2026.

**「Impact」** Developers can call the model today through an OpenAI-compatible endpoint at api.moonshot.ai/v1 using the model id kimi-k3.1-pro, with low, medium and max reasoning settings, at the same per-token price as GPT-6.1 Sol. Because only the API is live, anyone whose work depends on downloading, fine-tuning or self-hosting the weights has to wait until the promised November 4 release.

**Tags**: `#AI models`, `#open-weight models`, `#coding benchmarks`, `#long context`, `#Kimi`

---

<a id="item-tech-news-3"></a>
### [Block announces Dessa full-duplex speech model with claimed local MacBook inference](https://block.xyz/dessa) ⭐️ 7.0/10

Block has announced Dessa, a full-duplex speech model it says runs locally on a MacBook Pro M4 Max or better and was trained on a single NVIDIA GB200 NVL72. The company page bills it as &quot;the most authentic full-duplex speech model ever built,&quot; but the supplied material includes no independent latency measurements, benchmarks, licensing terms, model access details, or release date. Hacker News reaction mixed enthusiasm for the demo conversations and the local-inference claim with skepticism about the marketing framing.

hackernews · dsr12 · Oct 23, 19:09 · [Discussion](https://news.ycombinator.com/item?id=50213925)

**「Why full-duplex matters」** Conventional voice assistants are turn-based: they wait for the user to stop speaking, then transcribe and respond, which adds latency and makes interruptions or overlapping speech awkward. Full-duplex speech models keep listening while they talk, so the claimed advance concerns latency and natural turn-taking rather than transcription accuracy — and in this case the evidence rests on the company&\#x27;s own page and demos, with no independent benchmark supplied.

**「Impact」** If the local-inference claim holds, developers could run a low-latency full-duplex speech model on a high-end laptop instead of streaming audio to a server, which matters for offline use and audio privacy. Until Block publishes access details or third-party latency measurements, that remains a vendor claim rather than a capability developers can evaluate.

**「Community Discussion」** Commenters called the conversation demos impressive and singled out the claim of running on an M4 Max MacBook Pro and training on one GB200 NVL72 as a striking achievement for &quot;indie&quot; AI. Others objected that &quot;most authentic ever&quot; is marketing language rather than a technical claim, with one noting the title had been moderated after reaching the front page; another guessed from brief listens that the model was trained heavily on podcasts, and one found the simulated-companion framing off-putting.

**Tags**: `#speech models`, `#full-duplex interaction`, `#on-device AI`, `#model training`, `#Hacker News`

---

<a id="item-tech-news-4"></a>
### [Swarm Imitation Argued Equivalent to a Single Bandit-Learning Agent](https://www.reddit.com/r/MachineLearning/comments/1xdhf7r/r_the_hive_mind_is_a_single_reinforcement/) ⭐️ 7.0/10

A Reddit r/MachineLearning post by /u/mistlab argues that a population of individuals with no learning capability, who merely copy neighbors&\#x27; choices, behaves exactly like a single reinforcement-learning agent solving a multi-armed bandit. The authors say they bridge local imitation and global policy updates with evolutionary replicator dynamics: populations following &quot;imitation of success&quot; evolve like the expected update of the Cross Learning bandit algorithm, while the honey bee &quot;weighted voter&quot; waggle-dance model yields a macro-level algorithm they name Maynard-Cross Learning, in which each of N individuals acts as a parallel environment sample and the effective per-sample step size is alpha = 1/N. The claim is presented as a mathematical proof and links an arXiv preprint \(2410.17517\), a project page and a GitHub code repository, but the post itself supplies no peer review or empirical validation, so the equivalence and its practical usefulness remain unverified.

reddit · r/MachineLearning · /u/mistlab · Oct 23, 15:37

**「Background: bandits, replicator dynamics, and the superorganism claim」** A multi-armed bandit is the stripped-down reinforcement-learning setting in which an agent repeatedly chooses among options and updates its action probabilities from the rewards it observes; Cross Learning is one classic algorithm for that update. Evolutionary game theory supplies the other half of the picture through replicator dynamics, which describe how the share of a population using each strategy shifts when individuals imitate higher-payoff neighbors. The linked arXiv paper \(2410.17517\) frames the bee-colony &quot;hive mind&quot; as a single online RL agent interacting with many parallel environments, which is the framing the Reddit post restates and formalizes as Maynard-Cross Learning.

**「Implications for swarm design」** For developers building decentralized swarm-robotics or imitation-based decision systems, the derivation implies that the collective&\#x27;s effective per-sample step size scales as alpha = 1/N, so enlarging a population changes convergence behavior rather than simply speeding it up — population size and step size have to be considered together. The authors have also published simulation code alongside the paper, which is what would let others test the equivalence outside the analytical argument.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/html/2410.17517">The Hive Mind is a Single Reinforcement Learning Agent</a></li>
<li><a href="https://www.alphaxiv.org/abs/2410.17517">The Hive Mind is a Single Reinforcement Learning Agent | alphaXiv</a></li>
<li><a href="https://arxiv.org/html/2410.17517">The Hive Mind is a Single Reinforcement Learning Agent</a></li>
<li><a href="https://github.com/MISTLab/HiveMindRL">GitHub - MISTLab/ HiveMindRL : simulations connecting collective...</a></li>

</ul>
</details>

**Tags**: `#reinforcement learning`, `#swarm intelligence`, `#multi-armed bandits`, `#collective decision-making`, `#theoretical ML`

---

<a id="item-tech-news-5"></a>
### [PHP Foundation recommends disabling upload progress over RCE risk](https://x.com/ThePHPF/status/2113580383875019242) ⭐️ 7.0/10

The PHP Foundation is recommending that users set session.upload\_progress.enabled to 0 until the next PHP release to mitigate CVE-2026-115560, a remote code execution vulnerability tied to the upload progress feature. The advisory says only applications that switch the non-default serialize\_handler to &quot;php&quot; at runtime may be affected. The Foundation had previously recommended keeping the feature disabled because of CVE-2026-109619.

telegram · zaihuapd · Oct 23, 13:46

**「Background」** PHP&\#x27;s upload-progress feature reports the status of in-flight file uploads through session variables and is controlled by the \`session.upload\_progress.enabled\` setting. The source notes that the PHP Foundation had previously advised keeping this feature disabled because of CVE-2026-109619, so the new recommendation follows an earlier security concern involving the same optional capability.

**「Impact」** Administrators should apply session.upload\_progress.enabled=0 as an interim mitigation and check whether any application switches session.serialize\_handler to “php” at runtime, since that condition is what creates exposure. Deployments that keep the setting off will lose upload-progress reporting until a fix ships; no emergency patch was available at the time of the advisory.

<details><summary>References</summary>
<ul>
<li><a href="https://www.getastra.com/blog/security-advisory/cve-2026-115560/">CVE-2026-115560: Another PHP Session-Handler RCE</a></li>
<li><a href="https://safeguard.sh/resources/blog/php-cve-2026-115560-session-upload-progress-mitigation">PHP CVE-2026-115560: unpatched session upload progress RCE ...</a></li>

</ul>
</details>

**Tags**: `#PHP`, `#security vulnerability`, `#RCE`, `#CVE`, `#upload progress`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China issues guidelines to soften AI&\#x27;s job-replacement impact](https://mp.weixin.qq.com/s/St8URoMYcV-voM7kLAK3Bw) ⭐️ 8.0/10

China’s State Council General Office issued a policy document aimed at reducing AI’s job-replacement effects, saying AI should be promoted first in labor-shortage and high-risk roles. It asks that AI’s use in labor-intensive industries be advanced cautiously in scope, intensity and pace, and encourages firms to explore an “unemployment buffer period” system, with advance notice and support for affected workers to change or transfer jobs.

telegram · zaihuapd · Oct 23, 12:54

**「Background」** The State Council General Office is an administrative office under China’s cabinet, and the document sets a policy direction without quantitative targets, a detailed timeline or implementation scope, according to the report.

**「Impact」** The guidance directly concerns labor-intensive employers and their workers, since it ties the pace of AI adoption in those sectors to notice and transition support for displaced employees.

**Tags**: `#人工智能就业影响`, `#国务院政策`, `#劳动力市场`, `#就业友好型发展`, `#失业缓冲期`

---

<a id="item-finance-news-2"></a>
### [China to implement upgraded CCC certification rules for e-bikes, toys and strollers from November 2026](https://www.gelonghui.com/live/2726360) ⭐️ 7.0/10

China’s market regulator will implement upgraded CCC certification rules for electric bicycles, toys and strollers on November 1, 2026. Under the rules, e-bikes must follow a “one vehicle, one battery, one charger, one code” system, ship with all required parts and a conformity certificate, and retain a whole-vehicle sample for at least 12 months after the certificate expires, with stricter post-certification checks.

telegram · zaihuapd · Oct 23, 10:12

**「Background」** CCC certification is China’s compulsory product-safety mark that regulated goods must obtain before sale. The November 2026 changes upgrade the existing CCC implementation rules for e-bikes, toys, and strollers rather than create a new certification regime.

**「Who is affected」** Electric-bike manufacturers and certificate holders will bear the direct burden: factory-completeness checks, retained samples and post-certification market sampling put their certificates at risk, and the market regulator has already revoked more than 50,000 certificates under tightened CCC enforcement.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ithome.com/1/017/160.htm">超 5 万张 证 书被撤销，市场监管总局对 CCC ...</a></li>

</ul>
</details>

**Tags**: `#China regulation`, `#CCC certification`, `#electric bicycles`, `#product safety`, `#manufacturing compliance`

---

<a id="item-finance-news-3"></a>
### [China Approves Citigroup Securities \(China\) With RMB 1.2 Billion Registered Capital](https://mp.weixin.qq.com/s/f_fCJUEObewqgAe5Ie7wHA) ⭐️ 7.0/10

China&\#x27;s securities regulator on Oct. 23 approved the establishment of Citigroup Securities \(China\) Co., Ltd. in Shanghai with RMB 1.2 billion in registered capital, wholly funded by Citigroup Global Financial Holdings and licensed for securities brokerage, investment advisory, underwriting and sponsorship, and proprietary trading.

telegram · zaihuapd · Oct 23, 12:29

**「Background」** Citigroup, a U.S.-based global bank, had waited nearly five years for this securities approval, Bloomberg reported.

**「Impact」** The license gives Citigroup a wholly owned onshore platform to compete for Chinese brokerage and underwriting business, expanding foreign participation in the sector.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Citigroup">Citigroup - Wikipedia</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2026-10-23/citigroup-secures-approval-for-solo-securities-venture-in-china">Citi Wins China Securities Approval After Five-Year Wait - Bloomberg</a></li>

</ul>
</details>

**Tags**: `#China securities regulation`, `#Citigroup`, `#foreign financial institutions`, `#market entry`, `#CSRC approval`

---