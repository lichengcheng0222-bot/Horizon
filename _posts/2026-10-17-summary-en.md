---
layout: default
title: "Horizon Summary: 2026-10-17 (EN)"
date: 2026-10-17
lang: en
---

> From 40 items, 14 important content pieces were selected

---

**Technology News**
1. [Claude traces NIST ECDSA curve seeds to lrand48 timestamps](#item-tech-news-1) ⭐️ 9.0/10
2. [JPEG XL vs. AVIF comparison published for web use-cases](#item-tech-news-2) ⭐️ 8.0/10
3. [Research Exploits 37-Year-Old OpenBSD Kernel Bug](#item-tech-news-3) ⭐️ 8.0/10
4. [StepFun releases Step 5 Preview agentic flagship model](#item-tech-news-4) ⭐️ 8.0/10
5. [Llama.cpp port runs GGUF models natively on jailbroken PS5](#item-tech-news-5) ⭐️ 7.0/10
6. [Apple demos Muse Spark Open via MLX distributed inference on Mac Studios](#item-tech-news-6) ⭐️ 7.0/10
7. [Mercor analysis says AI benchmarks miss 90% of US work hours](#item-tech-news-7) ⭐️ 7.0/10
8. [StarSkirmish Bench v0.2 ranks flagship LLMs writing StarCraft bot code](#item-tech-news-8) ⭐️ 7.0/10
9. [Anthropic team: AI code review should run continuously, not as a final gate](#item-tech-news-9) ⭐️ 7.0/10
10. [ORL accelerates diffusion LLM decoding, open-sources models and dlmrt engine](#item-tech-news-10) ⭐️ 7.0/10
11. [Court Documents Reveal Telegram&\#x27;s U.S. User-Data Disclosures](#item-tech-news-11) ⭐️ 7.0/10

**Financial News**
1. [Market Selloff and Rising Rates Stall AI Data Center Listings](#item-finance-news-1) ⭐️ 7.0/10
2. [China Proposes Export Controls on 40 AI, Biopharma, and Solar Technologies](#item-finance-news-2) ⭐️ 7.0/10
3. [Investors trim Anthropic IPO valuation expectations to about $1.5 trillion](#item-finance-news-3) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Claude traces NIST ECDSA curve seeds to lrand48 timestamps](https://www.anthropic.com/research/ecdsa-curve-origins) ⭐️ 9.0/10

Anthropic reports that Claude has traced the origins of the NIST ECDSA curve seeds: the P-192, P-224, P-256, P-384, and P-521 seeds were not outputs of a hash algorithm but of the C library&\#x27;s lrand48 random-number generator seeded with a Unix timestamp. The discovery is said to have taken under half an hour and would resolve a long-standing cryptographic provenance mystery. One binary seed, B-163, remains unexplained. The supplied material is a Hacker News submission linking to the report, and the full report&\#x27;s details are not included.

hackernews · ahlCVA · Oct 16, 18:55 · [Discussion](https://news.ycombinator.com/item?id=50122800)

**「Background」** ECDSA curves are specified by seed values, and standard practice is to derive those seeds by hashing a fixed, public phrase so that anyone can verify the curve constants were not chosen to conceal a weakness; the published NIST P-curve seeds, however, matched no known hash input, leaving their origin unexplained for decades and sustaining speculation that they had been selected deliberately. The puzzle drew renewed attention through a bounty organized by Filippo Valsorda, and Anthropic said the $36,864 award associated with it will be donated.

**「Impact」** The practical consequence is for provenance and trust in NIST curves, not interoperability: the lrand48 explanation does not change the curve parameters, but it also does not prove that the seeds were not selected from many candidates, since discarded outputs and timestamp searches would be invisible in the published constants.

**「Community discussion」** Commenters treated the result as strong evidence about the generation method but debated what it proves about selection: fidotron argued that reproducing the lrand48 mechanism cannot rule out deliberate timestamp searching, while tptacek said it was devastating for NIST conspiracy theories. teddyh suggested the unexplained B-163 seed may simply be a typo in the published number.

<details><summary>References</summary>
<ul>
<li>Claude Traces NIST ECDSA Curve Seeds to Unix Timestamps | Trending Stories | HyperAI</li>

</ul>
</details>

**Tags**: `#cryptography`, `#ECDSA`, `#NIST`, `#AI-assisted research`, `#security`

---

<a id="item-tech-news-2"></a>
### [JPEG XL vs. AVIF comparison published for web use-cases](https://jakearchibald.com/2026/jpeg-xl-vs-avif/) ⭐️ 8.0/10

A technical comparison of JPEG XL and AVIF for web use-cases was published on October 16, 2026, covering encoding performance, settings, and codec maturity. The article targets web developers and systems engineers choosing between the two image formats, and the accompanying Hacker News discussion includes user-reported benchmarks and tooling recipes. Specific benchmark numbers and conclusions from the article itself are not available in the supplied material.

hackernews · farlight · Oct 16, 16:12 · [Discussion](https://news.ycombinator.com/item?id=50120224)

**「Background」** AVIF and JPEG XL are both modern image codecs promoted as smaller alternatives to JPEG and WebP for web delivery. By 2026, AVIF had broad browser support while JPEG XL remained behind a flag in Chrome 145, and multiple mid-2026 comparisons focused on their compression ratios, browser-support gaps, and adoption trade-offs for developers.

**「Community discussion」** Commenters debated codec maturity and quality trade-offs: yhjc2692 said libjxl&\#x27;s maximum effort takes 9–46 seconds \(50–180x its default\) for 2–7% smaller photos and about 25% smaller screenshots/illustrations, while jixel achieves similar results in a couple of seconds, attributing the slowness to Butteraugli; Metricon shared an ffmpeg AVIF recipe for 10x+ smaller files with PNG transparency; ezst cautioned against declaring a winner before codecs mature, citing MP3/LAME and WebP; and PaulHoule criticized AVIF for replacing fine highlights with plausible detail in the F1 example. These are individual opinions and reported experiences, not verified consensus.

<details><summary>References</summary>
<ul>
<li><a href="https://fastedit.net/blog/jpeg-xl-browser-support-2026">JPEG XL Browser Support 2026: JXL vs AVIF and WebP</a></li>
<li><a href="https://coretoolshub.com/blog/avif-vs-webp-vs-jpeg-xl-2026/">AVIF vs WebP vs JPEG XL — 2026 Format Comparison</a></li>
<li><a href="https://www.inverity.ai/posts/avif-vs-webp-vs-jpeg-xl-2026">AVIF vs WebP vs JPEG XL in 2026: Which Format Wins?</a></li>

</ul>
</details>

**Tags**: `#JPEG XL`, `#AVIF`, `#image compression`, `#web performance`, `#codecs`

---

<a id="item-tech-news-3"></a>
### [Research Exploits 37-Year-Old OpenBSD Kernel Bug](https://calif.io/research/big-fish) ⭐️ 8.0/10

A security research write-up published at calif.io describes the discovery and exploitation of a kernel bug that survived roughly 37 years in OpenBSD&\#x27;s codebase. The supplied item contains only a high-level description and no source text, so the affected subsystem, vulnerable versions, the specific exploit primitive, and any patch, advisory, or CVE are not established here.

hackernews · rs\_rs\_rs\_rs\_rs · Oct 16, 14:44 · [Discussion](https://news.ycombinator.com/item?id=50118977)

**「Background」** The vulnerability stems from shared-memory counter code inherited from the original BSD kernel, roughly 37 years old; Calif&\#x27;s proof-of-concept chains an overflow in that code with a separate kernel out-of-bounds write to escalate from local access to a root shell on OpenBSD. Coverage of the research reports that OpenBSD issued errata addressing the underlying issues before the exploit was published on October 16, 2026. One commenter also noted that a 1999 rewrite of the corresponding code path in NetBSD appears to have eliminated the bug there by accident, though the source write-up does not establish that history.

**「Community Discussion」** Commenter phendrenad2 said the related code path was rewritten in NetBSD in August 1999, which accidentally fixed the bug there. Another commenter, ozereray1, argued that the bug&\#x27;s survival in a heavily audited codebase shows how hard some kernel bugs are to catch by review alone, and asked whether fuzzing or static analysis could realistically have found this class of bug or whether it required a human reasoning about the exploit primitive.

<details><summary>References</summary>
<ul>
<li><a href="https://cybersecuritynews.com/37-year-old-kernel-openbsd-flaw/">37-Year-Old Kernel Flaw Exploited to Gain Root Access on ...</a></li>
<li><a href="https://aicrier.com/post/got9bqqjbi3quvvti9pq">Big Fish Exploits 37-Year OpenBSD Bug — AICrier</a></li>
<li><a href="https://thedailytechfeed.com/37-year-old-kernel-bug-in-openbsd-finally-patched-after-root-exploit-poc/">37-Year-Old Kernel Bug in OpenBSD Finally Patched After Root ...</a></li>

</ul>
</details>

**Tags**: `#security`, `#OpenBSD`, `#kernel`, `#exploit-development`, `#vulnerability-research`

---

<a id="item-tech-news-4"></a>
### [StepFun releases Step 5 Preview agentic flagship model](https://huggingface.co/stepfun-ai/Step-5-Preview) ⭐️ 8.0/10

StepFun published Step 5 Preview on Hugging Face, a sparse Mixture-of-Experts flagship model aimed at agentic work, with 600 billion total parameters and 27 billion activated parameters. It supports up to 1 million tokens of context and accepts text, image, and video inputs. The model can be deployed through an OpenAI-compatible API with vLLM or SGLang under the StepFun Model License 1.0. StepFun claims leading performance on software engineering, long-horizon agent execution, and professional knowledge tasks, with particular strength in financial scenarios, but these are vendor claims for a preview release that have not been independently verified.

telegram · zaihuapd · Oct 16, 06:36

**「Background」** Step 5 Preview is a sparse mixture-of-experts model: of its roughly 600 billion total parameters only about 27 billion are active per token, which keeps per-token compute far below what the full weight count implies. Third-party write-ups describe it as an early preview of the Step 5 line, and it is already surfaced as a preview deployment served in NVFP4 on NVIDIA&\#x27;s NIM platform.

**「Impact」** Developers can already serve Step 5 Preview through vLLM or SGLang behind an OpenAI-compatible API, so existing OpenAI-style client integrations do not need to be rewritten. Third-party write-ups report it scoring 44 on the Artificial Analysis Intelligence Index \(top three among open models\) and 67.7% on DeepSWE v1.1, slightly above Kimi K3 and GLM-5.3, with a per-task cost reported at one-eighth of Claude Opus 5; because the release is labeled a preview, these figures should be treated as preliminary rather than an independently verified production baseline.

<details><summary>References</summary>
<ul>
<li><a href="https://www.orcarouter.ai/blog/step-5-preview-vs-intern-s2-mobius">Step 5 Preview vs Intern-S2 Mobius: Flagship or 35B?</a></li>
<li><a href="https://www.eesel.ai/blog/stepfun-step-5">StepFun Step 5 Preview : specs, pricing, benchmarks, and... | eesel AI</a></li>
<li><a href="https://build.nvidia.com/stepfun-ai/step-5-preview">Step 5 Preview Model by Stepfun -ai | NVIDIA NIM</a></li>
<li><a href="https://ai-bot.cn/step-5-preview/">Step 5 Preview - 阶 跃 星 辰 推出的新一代旗舰基座 模 型 | AI工具集</a></li>
<li><a href="https://m.21jingji.com/article/20260921/herald/742325e7deb08d056e5801bcae9c9974.html">“单任务成本仅为Claude Opus 5的1/8”， 阶 跃 星 辰 Step 5 Preview ...</a></li>

</ul>
</details>

**Tags**: `#大语言模型`, `#稀疏MoE`, `#多模态`, `#AI智能体`, `#模型发布`

---

<a id="item-tech-news-5"></a>
### [Llama.cpp port runs GGUF models natively on jailbroken PS5](https://github.com/cobanov/PS5LM) ⭐️ 7.0/10

A GitHub project called PS5LM demonstrates running llama.cpp and GGUF models natively on a jailbroken PlayStation 5, extending local LLM inference to repurposed console hardware. The repository targets users with jailbroken PS5 consoles, but the supplied evidence does not include performance figures, memory limits, supported model sizes, or installation requirements. The item is a demonstration project rather than a shipped consumer feature, and no vendor or independent benchmark results are provided.

hackernews · Anon84 · Oct 16, 18:32 · [Discussion](https://news.ycombinator.com/item?id=50122431)

**「Background」** llama.cpp is a local inference runtime that loads models in the GGUF quantized format, with prebuilt binaries and an optional OpenAI-compatible server mode \[tool-2-3\]. According to a listing of the project, PS5LM ports that runtime to a jailbroken PlayStation 5, letting the console download GGUF models and chat with them through its browser \[tool-2-1\].

**「Practical impact」** Because the port depends on a jailbroken console, it gives no inference path for a stock PS5 — anyone evaluating it needs a unit on exploitable firmware and GGUF-format model weights. Developers without such a console have an existing alternative on closely related silicon: the AMD BC-250, a former cryptomining board built on the PS5&\#x27;s &quot;Cyan Skillfish&quot; APU, already has a hardware-tuned llama.cpp fork and a setup guide that wraps llama.cpp in an HTTP API and caps the GPU clock at 1500 MHz.

**「Community discussion」** Commenters debated whether hosting such a project on GitHub is risky, with one arguing it should be on a custom domain because Sony might seek a takedown. Others reported or speculated about practical use, including a claim that it runs a 27B Qwen model at 2-bit quantization for low-cost long-running tasks, plus suggestions that similar inference could work on BC250 ex-mining APU boards or enable LLM-driven game NPCs; these are community assertions, not verified results.

<details><summary>References</summary>
<ul>
<li><a href="https://reporank.net/en/repo/cobanov-ps5lm.html">PS 5 LM : llama . cpp Inference on a Jailbroken PS 5 - Open Source...</a></li>
<li><a href="https://huggingface.co/unsloth/Qwen3.8-27B-GGUF">unsloth/Qwen3.8-27B- GGUF · Hugging Face</a></li>
<li><a href="https://github.com/TechMakesArt/llama.cpp-bc250">GitHub - TechMakesArt/ llama . cpp - bc 250 : llama . cpp fork with Vulkan...</a></li>
<li><a href="https://github.com/akandr/bc250">GitHub - akandr/ bc 250 : AMD BC - 250 ( PS 5 APU ) setup guide...</a></li>

</ul>
</details>

**Tags**: `#llama.cpp`, `#GGUF`, `#local LLM inference`, `#PS5 jailbreak`, `#hardware repurposing`

---

<a id="item-tech-news-6"></a>
### [Apple demos Muse Spark Open via MLX distributed inference on Mac Studios](https://machinelearning.apple.com/research/mlx-distributed-inference) ⭐️ 7.0/10

Apple&\#x27;s machine-learning research team published an MLX distributed-inference demonstration that runs Muse Spark Open, a nearly trillion-parameter model, across a cluster of four Mac Studios at over 36 tokens per second, using a version of MLX it says was released the same day. Apple describes scaling from a single Mac Studio with up to 512GB of unified memory out to multiple machines, and frames the throughput as above average human reading speed. Those figures come from Apple&\#x27;s own post rather than independent measurement, and commenters point out that the headline tokens-per-second chart reflects an 8,192-token context, which they consider too short for many current uses.

hackernews · antipaul · Oct 16, 13:43 · [Discussion](https://news.ycombinator.com/item?id=50118320)

**「Background」** MLX is Apple&\#x27;s framework for running models locally on Apple silicon, and third-party tools such as LM Studio support it on macOS. The model being demonstrated, Muse Spark Open, is an 816-billion-parameter open-weight model described as an Apple–Meta collaboration; Apple&\#x27;s research page frames the work as local and distributed large-LLM inference with MLX and RDMA, so the prerequisite step is distributing an oversized model across multiple Macs rather than running it on a single host.

**「What it means for local deployments」** For developers who want to run frontier-scale models on their own hardware, the practical change is that MLX can now shard a model across multiple Mac Studios over a network instead of requiring one machine large enough to hold it — Apple&\#x27;s own write-up describes storing half of a model on each of two Mac Studios and pipelining inference between them. The throughput figures in the release were measured at an 8,192-token context, as one commenter noted, so teams planning long-context or high-concurrency workloads should validate speed at their own sequence lengths before sizing a cluster, and the 4-bit quantization used for the featured model means memory budgets for higher-precision runs will be larger than the headline numbers suggest.

**「Community discussion」** Commenters disputed the benchmark&\#x27;s fairness: peri-cl argued the demo quantized Meta&\#x27;s model to 4-bit while running Qwen only at native BF16, and mrboatshoepants noted the 15-36 tokens/second range was measured at an 8,192-token context. liuliu reported contrasting single-machine results — an M5 Ultra with 256GiB running DeepSeek 4.1 Flash 0910 at roughly 3,200 tokens/second prefill and about 45 tokens/second, and GLM 5.3 Flash on an M5 Max with 128GiB — and ks2048 cast the demo as Apple profiting from open-weight models built by others.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/LM_Studio">LM Studio - Wikipedia</a></li>
<li><a href="https://machinelearning.apple.com/research/mlx-distributed-inference">Local and Distributed Large LLM Inference with MLX and RDMA on...</a></li>
<li><a href="https://www.youtube.com/watch?v=XIxUnKQx92s">Apple and Meta Launch Muse Spark Open for Mac Studio - YouTube</a></li>
<li><a href="https://machinelearning.apple.com/research/mlx-distributed-inference">Local and Distributed Large LLM Inference with MLX and RDMA on...</a></li>

</ul>
</details>

**Tags**: `#MLX`, `#distributed inference`, `#Apple Silicon`, `#local LLM inference`, `#benchmarking`

---

<a id="item-tech-news-7"></a>
### [Mercor analysis says AI benchmarks miss 90% of US work hours](https://www.mercor.com/research/labor-index/benchmark-map/) ⭐️ 7.0/10

A Mercor research post argues that 90% of U.S. working hours are spent on tasks with little or no coverage from existing AI benchmarks, using an O\*NET-based mapping of benchmark prompts to real work tasks. Mercor says this makes it hard to know how good AI models are at the work Americans actually do. The post is an analysis rather than a new benchmark or an independently validated measurement, and commenters raised methodological caveats about how coverage is defined.

hackernews · speckx · Oct 16, 17:08 · [Discussion](https://news.ycombinator.com/item?id=50121179)

**「Background」** The post&\#x27;s mapping rests on O\*NET, the US Department of Labor occupational database that decomposes jobs into discrete tasks; comparing those task descriptions against benchmark prompts is how the analysis arrives at its coverage estimate. Mercor, the firm behind the labor index, also runs its own APEX benchmark suite, whose tasks are developed and validated with its network of domain experts rather than sourced from public benchmark collections. That makes the report an assessment of the benchmark landscape by an organization that is simultaneously building competing expert-written evaluations.

**「Impact」** For AI evaluation teams, the report&\#x27;s claim implies that current benchmark scores may not support broad claims about workplace readiness; teams using benchmarks to compare models on real jobs should audit what tasks those benchmarks actually cover. Because the 90% figure is an argument about coverage rather than an independently confirmed result, it should be treated as a prompt for better benchmark design, not as a settled measure of model capability.

**「Community Discussion」** Commenters questioned Mercor&\#x27;s coverage threshold, with OtherShrezzing arguing that categories such as &quot;counsel parents with child rearing problems&quot; count as &quot;well covered&quot; despite having only 13 prompts, while b800h compared the framing to the Doorman Fallacy. Others drew broader labor implications: 10111001 read the reported wage-bill skew as directing AI at &quot;good jobs,&quot; and legitster described becoming 20x more productive at coding while spending more time on presentations, Jira, and QA.

<details><summary>References</summary>
<ul>
<li><a href="https://opportunitiesforyouth.org/2026/09/02/mercor-research-fellowship-apex-2026-earn-up-to-80000-to-build-the-next-generation-of-ai-benchmarks-and-economic-research/">Mercor Research Fellowship APEX 2026... - Opportunities for Youth</a></li>

</ul>
</details>

**Tags**: `#AI benchmarks`, `#AI evaluation`, `#labor market`, `#O\*NET`, `#future of work`

---

<a id="item-tech-news-8"></a>
### [StarSkirmish Bench v0.2 ranks flagship LLMs writing StarCraft bot code](https://starskirmish.com/bench/v0-2/) ⭐️ 7.0/10

StarSkirmish Bench v0.2 is a refreshed benchmark in which LLMs play StarCraft: Brood War by writing bot code, with results for flagship models from OpenAI, Anthropic, Google, and Muse. In the thread, one commenter reports the ranking as GPT-6 Astra ahead of GPT-6.1 Sol, Gemini 4 Argon, Claude Opus 5.5, Claude Fable 5.1, and Claude Sonnet 5.5. Another commenter says each model runs in its lab&\#x27;s first-party CLI harness at the highest reasoning setting, with web search and fetch disabled and no other internet access; the source post itself provides the refreshed results and links to the benchmark.

hackernews · \_\_cayenne\_\_ · Oct 16, 14:18 · [Discussion](https://news.ycombinator.com/item?id=50118688)

**「Background」** StarSkirmish is a benchmark in which each LLM is given a fixed amount of wall-clock time to write a StarCraft: Brood War Protoss bot in C++, after which the resulting bots are evaluated in a tournament against other models&\#x27; bots and established human-written bots. The earlier v0.1 version of the bench used one-hour runs at &\#x27;high&\#x27; reasoning; the v0.2 refresh keeps that code-writing format and adds results from the flagship models of OpenAI, Anthropic, Google, and Muse.

**「Impact」** For teams using agentic code-generation benchmarks to compare models, v0.2 results depend on each lab&\#x27;s CLI harness, reasoning setting, and internet restrictions, so the ranking is not directly comparable to bare-model coding scores. The thread also questions whether a short time limit keeps agent-written bots below the best human-written StarCraft bots, which limits how much strategic code-generation ability the benchmark can show.

**「Community Discussion」** Commenters raised methodology questions: cgearhart asked whether agent-written bots are just inferior versions of the best human bots because of the short time limit, and whether they might be imitating human-written code. GodelNumbering reported that the v0.2 ranking matches the exact order from a separate 9x9 Go LLM benchmark, while djoldman highlighted that each model runs in its lab&\#x27;s first-party CLI with web tools disabled.

<details><summary>References</summary>
<ul>
<li><a href="https://starskirmish.com/bench/">StarSkirmish : where LLMs write code to play StarCraft .</a></li>
<li><a href="https://simpleprog.com/news/show-hn-a-starcraft-bw-arena-where-llms-play-by-writing-code-3b3d2564">Show HN: A StarCraft BW Arena where LLMs play by writing code</a></li>

</ul>
</details>

**Tags**: `#LLM benchmarks`, `#AI agents`, `#code generation`, `#StarCraft`, `#model evaluation`

---

<a id="item-tech-news-9"></a>
### [Anthropic team: AI code review should run continuously, not as a final gate](https://simonwillison.net/2026/Oct/16/code-review/) ⭐️ 7.0/10

In a post on claude.dev, Anthropic&\#x27;s Claude Code team — Addy Osmani, Morgan Westlee Lunt and Qing Wang — argue that asking &quot;did a human read the code?&quot; is an imprecise proxy for the question that matters: what could go wrong with a change, and which check, automated or human, is best placed to catch it. They describe review inside their team as now running continuously, &quot;more like spellcheck while you write,&quot; rather than as a gate at the end of a pull request, with most changes already reviewed and fixed by Claude at least once before a human is asked to look. The stated payoff is that routine mistakes are caught early and team attention is saved for higher-level questions and scrutiny. The passage is the team&\#x27;s own account of its workflow, not an independent measurement of defect rates or review quality.

rss · Simon Willison · Oct 16, 22:06

**「Background」** The shift described by Anthropic&\#x27;s Claude Code team comes amid a broader code-volume problem: The Register reported in October 2026 that writing code is no longer the bottleneck at Anthropic, and that the company&\#x27;s focus has moved to managing code after it is written through source control, builds, and continuous integration \(tool-2-2\). In the team&\#x27;s own account, once it had achieved high coverage and deep reviews, it began optimizing for the minimum amount of human review time that would not increase reverts or incidents \(tool-2-1\).

**「Impact」** For teams adopting this pattern, the concrete change is what humans are asked to do: rather than serving as the default catch-all for every diff, a reviewer becomes a second pass reserved for higher-level design and risk questions — which means the automated checks in front of them must be trusted or verified. Organizations that currently use &quot;a human read this code&quot; as an audit or compliance signal would need a substitute, since the authors&\#x27; framing makes the choice of check, not the identity of the reader, the thing to design around.

<details><summary>References</summary>
<ul>
<li><a href="https://claude.dev/blog/solving-code-review-at-anthropic/">How the Claude Code team does code review / claude.dev Blog</a></li>
<li><a href="https://www.theregister.com/devops/2026/10/13/anthropic-reinvents-source-control-as-claude-floods-the-world-with-code/5302943">Anthropic reinvents source control as Claude floods the world ...</a></li>

</ul>
</details>

**Tags**: `#AI-assisted code review`, `#Claude Code`, `#software engineering practices`, `#developer workflow`, `#Anthropic`

---

<a id="item-tech-news-10"></a>
### [ORL accelerates diffusion LLM decoding, open-sources models and dlmrt engine](https://www.reddit.com/r/MachineLearning/comments/1x7qgr0/research_2788_tokenss_on_a_single_rtx_5090_with_a/) ⭐️ 7.0/10

The Introspective Diffusion team announced ORL \(On-Policy Residual Learning\), a post-training method for diffusion language models that carries each denoising step&\#x27;s own predictions forward as residual context and trains on fresh on-policy trajectories, together with dlmrt, a custom inference engine that captures the whole denoising loop in a CUDA graph and supports NVFP4 on Blackwell GPUs. The Reddit post claims 2,788 tokens/s for LLaDA-2.1-mini + ORL in NVFP4 on a single RTX 5090, 7,708 tokens/s for DiffusionGemma 26B MoE + ORL on 8× B200, and up to 6.9× higher end-to-end throughput on QwenDLM-4B, with QwenDLM-4B HumanEval pass@1 rising from 82.9% to 89.6%. Reported training cost for LLaDA-2.1-mini is 4.2M self-generated training tokens and 36 H100 GPU-hours, while dlmrt is said to run 1.2–1.6× faster than SGLang/vLLM in the authors&\#x27; single-H100 comparisons. These are author-reported peak results for single-request decoding at batch size 1, not aggregate throughput or averages across arbitrary prompts, and no independent reproduction is presented; models, training code, evaluation pipeline, inference engine, and checkpoints are released openly.

reddit · r/MachineLearning · /u/arty\_photography · Oct 16, 20:03

**「Background」** Diffusion language models \(dLLMs\) generate text by denoising many token positions in parallel instead of emitting one token at a time as autoregressive models do, but their practical speed depends on how few denoising forward passes are needed for the sequence to converge. ORL targets that convergence bottleneck by training on residual-conditioned trajectories produced by the current model, an approach described in the arXiv paper linked from the announcement \(tool-2-1\). The released QwenDLM-4B-ORL checkpoint is a block diffusion language model post-trained with this method \(tool-2-3\).

**「What it means for adopters」** Developers who want the advertised RTX 5090 or B200 throughput must adopt the project&\#x27;s own dlmrt inference engine, because the figures depend on CUDA-graph-captured denoising plus NVFP4 on Blackwell-class GPUs; the post reports dlmrt running only 1.2–1.6× faster than SGLang/vLLM on identical models, so the headline speedups do not transfer to existing serving stacks. Since every published result is a single-request, batch-size-1 peak on selected benchmarks, teams evaluating this for production serving should treat it as latency evidence rather than aggregate throughput; the co-released LLaDA-2.1-mini ORL NVFP4 checkpoint is the intended target for independent reproduction on a consumer RTX 5090, a card on which a diffusion model of comparable scale \(DiffusionGemma&\#x27;s NVFP4 build via vLLM\) is already reported to fit in roughly 18 GB of VRAM.

<details><summary>References</summary>
<ul>
<li>On-Policy Residual Learning for Diffusion Language Models - arXiv</li>
<li>yifanyu/QwenDLM-4B-ORL - Hugging Face</li>
<li><a href="https://www.digitalapplied.com/blog/google-diffusiongemma-open-weight-text-diffusion-model-guide">Google DiffusionGemma: First Open-Weight Text Diffusion</a></li>
<li><a href="https://rohitraj.tech/en/notes/run-diffusiongemma-locally-vllm-rtx5090-2026">How to Run DiffusionGemma Locally: A vLLM Serving Guide for RTX ...</a></li>

</ul>
</details>

**Tags**: `#diffusion language models`, `#inference optimization`, `#open source`, `#GPU performance`, `#LLM systems`

---

<a id="item-tech-news-11"></a>
### [Court Documents Reveal Telegram&\#x27;s U.S. User-Data Disclosures](https://www.404media.co/heres-what-telegram-giving-data-to-the-u-s-government-looks-like/) ⭐️ 7.0/10

Newly released court documents, reported by 404 Media, show that Telegram provided U.S. law enforcement with one user&\#x27;s phone number, user ID, and IP address in response to a U.S. court order. In its letter, Telegram described the disclosure as voluntary and stated that it does not recognize U.S. jurisdiction. The user is identified in the case as Mahmoud Al-Muhtadi, who is accused of involvement in the October 7, 2023 attack on Israel. According to the report, Telegram had supplied data on 2,253 users to U.S. authorities as of January.

telegram · zaihuapd · Oct 16, 14:57

**「Background」** Telegram&\#x27;s transparency reporting from 2024 said the company disclosed data on 2,253 users in response to 900 U.S. legal requests, providing primarily phone numbers and IP addresses \(tool-2-2, tool-2-3\). That reporting also documented a sharp policy shift after its CEO was arrested in France: Telegram fulfilled nearly 1,000 U.S. law enforcement requests in the months after the arrest, up from just 14 between Jan. 1 and Sept. 30, 2024 \(tool-2-3\).

**「Impact」** Telegram users caught up in U.S. investigations should assume that a court order can surface their phone number, user ID, and IP address: the released records show exactly those identifiers for one user, and Telegram reported handing over data on 2,253 users by January. Telegram&\#x27;s description of the disclosure as &quot;voluntary&quot; and its refusal to recognize U.S. jurisdiction did not prevent the identifiers from reaching law enforcement, and external analysis of its disclosure practices notes that investigators now have a clearer legal path to IP addresses and phone numbers tied to Telegram accounts, with compliance rising.

<details><summary>References</summary>
<ul>
<li><a href="https://factually.co/fact-checks/technology/telegram-user-records-disclosed-to-us-authorities-2024-2025-legal-processes-e0b45a">How Many User Records Did Telegram Disclose to U.S. Au...</a></li>
<li><a href="https://www.pcmag.com/news/telegram-reports-huge-spike-in-data-sharing-with-law-enforcement">Telegram Reports Huge Spike in Data Sharing With Law Enforcement Does Telegram Report CSAM to Law Enforcement? What Changed Telegram evidence beyond the cloud | Andrea Fortuna The Wiretap: Telegram Handing Data On Thousands Of Users To ... US Prosecutors Gained Legal Approval to Hack Telegram Servers</a></li>
<li><a href="https://factually.co/fact-checks/technology/telegram-data-sharing-law-enforcement-what-is-shared-legal-conditions-199e73">What Exactly Does Telegram Share With Law Enforcement ...</a></li>

</ul>
</details>

**Tags**: `#Telegram`, `#privacy`, `#government surveillance`, `#data disclosure`, `#tech policy`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Market Selloff and Rising Rates Stall AI Data Center Listings](https://www.kitco.com/news/off-the-wire/2026-10-15/market-selloff-rising-rates-test-ai-data-centre-deal-boom) ⭐️ 7.0/10

Over the past week, planned listings tied to AI data centers — AirTrunk&\#x27;s REIT offering and the IPOs of Nvidia-backed Firmus and SoftBank-backed SB Energy — were withdrawn or paused, as investors demanded evidence that companies can absorb higher interest rates and computing costs. Dealogic data show Asian data center M&amp;A has reached $21.3 billion so far this year, roughly double 2025&\#x27;s full-year total of $10 billion, while equity financing fell 4.6% year over year.

telegram · zaihuapd · Oct 16, 05:10

**「Background」** The paused or withdrawn deals follow Nvidia-backed Firmus scrapping its planned IPO on October 8 — an offering that could have raised up to US$5 billion — and SoftBank&\#x27;s US data-centre developer SB Energy slowing its IPO timeline. Data-centre operators are watched as a gauge of investor appetite for AI infrastructure because the business is capital-intensive and typically relies on borrowed money, making it sensitive to interest rates.

**「Impact」** AI data center developers that depend on stock market listings or equity raises face a higher bar to secure funding, even as takeover activity in the sector accelerates.

<details><summary>References</summary>
<ul>
<li><a href="https://au.finance.yahoo.com/news/stock-sinks-23-australia-30bn-034730756.html">A stock sinks 23% as Australia’s $30bn Firmus AI data - centre IPO ...</a></li>
<li><a href="https://www.ft.com/content/8b7e2800-3e36-4d0c-9016-32deaae67b62">Why the IPO market is booming and busting</a></li>

</ul>
</details>

**Tags**: `#AI data centers`, `#capital markets`, `#M&amp;A`, `#IPOs`, `#interest rates`

---

<a id="item-finance-news-2"></a>
### [China Proposes Export Controls on 40 AI, Biopharma, and Solar Technologies](https://aqygzj.mofcom.gov.cn/flzc/gzjgfxwj/art/2026/art_c99f95ca0cd043829ac9991495fc283c.html) ⭐️ 7.0/10

China&\#x27;s Ministry of Commerce has imposed temporary registration on exports of certain artificial intelligence, biopharmaceutical, and solar technologies and opened a public comment period on a proposed revision to its export control list covering 40 such technologies. The proposal includes exemptions for technologies already in the public domain and streamlined licensing for certain biopharma out-licensing deals.

telegram · zaihuapd · Oct 16, 09:12

**「Background」** The Catalogue of Technologies Prohibited or Restricted from Export is China&\#x27;s official list of technologies whose transfer abroad requires government approval; the Ministry of Commerce revises it periodically and has publicly addressed why artificial-intelligence technologies were proposed for addition.

**「可能影响」** 该目录若按征求意见稿落地，中国人工智能、生物医药和光伏企业及其海外合作方的跨境技术转让（含相关关键核心设备）将需办理出口许可，可能放慢技术授权与联合研发；目前仍为征求意见阶段，最终范围待定。

<details><summary>References</summary>
<ul>
<li><a href="https://finance.sina.com.cn/roll/2026-10-16/doc-inivmazf7040150.shtml">finance.sina.com.cn/roll/ 2026 -10-16/doc-inivmazf7040150.shtml</a></li>

</ul>
</details>

**Tags**: `#出口管制`, `#人工智能`, `#生物医药`, `#光伏`, `#产业政策`

---

<a id="item-finance-news-3"></a>
### [Investors trim Anthropic IPO valuation expectations to about $1.5 trillion](https://www.reuters.com/business/finance/investors-temper-anthropic-ipo-valuation-expectations-over-revenue-growth-2026-10-15/) ⭐️ 7.0/10

Anthropic reported third-quarter revenue of $16.8 billion, up 45% from the prior quarter, with adjusted profitability and positive quarterly cash flow, but some investors cut their expected IPO valuation from $2 trillion to about $1.5 trillion, Reuters reported, citing slowing growth, intensifying price competition among AI models and pressure from compute spending. The figures are company-reported results, while the valuation change reflects investor expectations for a listing that has not yet occurred.

telegram · zaihuapd · Oct 16, 15:46

**「Background」** The $16.8 billion figure comes from people familiar with the matter rather than a company filing, and compares with about $11.6 billion in the second quarter, as Anthropic prepares for an IPO \(initial public offering, when a company first sells shares to public investors\).

**「What it means for other AI developers」** If investors apply the same more conservative valuation stance to peers, Chinese model developers such as Zhipu, MiniMax, Kimi and DeepSeek could face closer scrutiny of revenue durability, gross margin and capital efficiency as they pursue listings — Zhipu and MiniMax had previously been valued at a premium as scarce listed large-model targets \[tool-2-1\].

<details><summary>References</summary>
<ul>
<li><a href="https://www.reuters.com/business/finance/anthropics-q3-revenue-surges-45-nearly-17-billion-2026-10-14/">At Anthropic pre-IPO meet: ‘Thinking’ caps, surging revenue ...</a></li>
<li><a href="https://eu.36kr.com/en/p/3896477565191561">DeepSeek Sprinting Toward IPO: The &quot;Four AI Rising Stars ...</a></li>

</ul>
</details>

**Tags**: `#Anthropic`, `#IPO估值`, `#AI行业`, `#财务业绩`, `#估值压力`

---