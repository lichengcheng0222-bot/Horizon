---
layout: default
title: "Horizon Summary: 2026-10-17 (ZH)"
date: 2026-10-17
lang: zh
---

> 从 40 条内容中筛选出 14 条重要资讯。

---

**科技新闻**
1. [Claude 将 NIST ECDSA 曲线种子追溯至 lrand48](#item-tech-news-1) ⭐️ 9.0/10
2. [JPEG XL 与 AVIF 网页用例对比：编码性能与生态成熟度](#item-tech-news-2) ⭐️ 8.0/10
3. [Big Fish：利用 OpenBSD 存活 37 年的内核漏洞](#item-tech-news-3) ⭐️ 8.0/10
4. [阶跃星辰发布 Step 5 Preview 智能体旗舰模型](#item-tech-news-4) ⭐️ 8.0/10
5. [Llama.cpp 借 PS5LM 在越狱 PS5 上原生运行 GGUF 模型](#item-tech-news-5) ⭐️ 7.0/10
6. [苹果 MLX 分布式推理：四台 Mac Studio 跑近万亿参数模型](#item-tech-news-6) ⭐️ 7.0/10
7. [Mercor 研究：90% 美国工作时间缺乏 AI 基准覆盖](#item-tech-news-7) ⭐️ 7.0/10
8. [StarSkirmish Bench v0.2 刷新，LLM 写代码玩《星际争霸》](#item-tech-news-8) ⭐️ 7.0/10
9. [Anthropic Claude Code 团队主张把代码审查改为持续 AI 检查](#item-tech-news-9) ⭐️ 7.0/10
10. [ORL 加速扩散语言模型推理：单张 RTX 5090 达 2,788 tokens/s 并开源](#item-tech-news-10) ⭐️ 7.0/10
11. [法院文件披露 Telegram 向美执法部门提供用户数据细节](#item-tech-news-11) ⭐️ 7.0/10

**财经新闻**
1. [AI 数据中心投资受市场回调与利率上升，多项上市计划被撤回或暂停](#item-finance-news-1) ⭐️ 7.0/10
2. [商务部拟修订技术出口目录，涉人工智能、生物医药、光伏 40 项技术](#item-finance-news-2) ⭐️ 7.0/10
3. [投资者下调 Anthropic IPO 估值预期至约 1.5 万亿美元](#item-finance-news-3) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Claude 将 NIST ECDSA 曲线种子追溯至 lrand48](https://www.anthropic.com/research/ecdsa-curve-origins) ⭐️ 9.0/10

Anthropic 发布的一份报告称，Claude 在不到半小时内追溯出 NIST P-192、P-224、P-256、P-384 和 P-521 曲线种子的来源：它们并非哈希算法输出，而是 C 标准库 lrand48 随机数生成器以 Unix 时间戳为种子生成的。报告还称，第五个二进制种子 B-163 不符合 Claude 尝试的任何方法，仍未得到解释。由于当前条目只提供报告链接、未附全文，这一说法应视为报告及其 HN 讨论中的主张，而非独立复现的定论。

hackernews · ahlCVA · 10月16日 18:55 · [社区讨论](https://news.ycombinator.com/item?id=50122800)

**「背景」** NIST 的 P-192、P-224、P-256、P-384、P-521 等 ECDSA 曲线参数附带的种子值，按设计应可证明参数不是为隐藏后门而特意挑选，但其生成方法从未公开，因而长期引发 NSA 干预的猜测。Filippo Valsorda 曾为此发起种子来源调查并设立悬赏；Anthropic 现在称 Claude 将 NIST 曲线种子追溯到 1997 年时钟时间起始的 lrand48 运行，且五个 NIST 素数曲线种子与五个 ANSI X9.62 种子都呈现 lrand48\(\) &gt;&gt; 23 的模式。

**「影响」** 对密码学与安全研究者而言，该溯源若成立，会把 NIST 曲线种子的来源解释为普通伪随机输出，从而削弱关于种子被刻意挑选或植入后门的长期猜测；但评论者和报告本身留下的限制意味着它不能证明曲线未经过候选筛选，也不能解释 B-163 异常。

**「社区讨论」** HN 评论者 fidotron 指出，确认 lrand48 生产方式并不能说明曲线如何被选中，因为生成过程中被丢弃的候选不可见，理论上仍可能通过搜索时间戳来挑选具特定属性的曲线。评论者 teddyh 则提出，未解释的 B-163 最简单的解释可能是发布过程中某位数字被误写，因此按数字正确的前提无法求解。

<details><summary>参考链接</summary>
<ul>
<li>Claude reveals ECDSA curve origins - Anthropic</li>
<li>Claude Solves the NIST Curve Seed Mystery: It Was Timestamps - CellCog</li>
<li>Claude Traces NIST ECDSA Curve Seeds to Unix Timestamps | Trending Stories | HyperAI</li>

</ul>
</details>

**标签**: `#cryptography`, `#ECDSA`, `#NIST`, `#AI-assisted research`, `#security`

---

<a id="item-tech-news-2"></a>
### [JPEG XL 与 AVIF 网页用例对比：编码性能与生态成熟度](https://jakearchibald.com/2026/jpeg-xl-vs-avif/) ⭐️ 8.0/10

一篇面向网页用例的技术对比文章比较 JPEG XL 与 AVIF，重点涉及编码性能、参数设置和编解码器生态成熟度。评论区中，yhjc2692 引用文章数据称 libjxl 的最高 effort 对照片仅比默认小 2–7%，对截图和插画约小 25%，但耗时 9–46 秒，是默认的 50–180 倍；jixel 可在数秒内得到相同结果。Metricon 则表示 AVIF 已用于生产环境，并分享了以 ffmpeg 生成更小文件且保留透明度的参数。

hackernews · farlight · 10月16日 16:12 · [社区讨论](https://news.ycombinator.com/item?id=50120224)

**「背景」** JPEG XL 与 AVIF 是当前 Web 端最主要的两种下一代图像格式：AVIF 基于 AV1 的帧内编码，JPEG XL 则强调对既有 JPEG 的无损重压缩与渐进式解码。据搜索结果，AVIF 已获得约 93% 的浏览器支持，而 JPEG XL 在 Chrome 中仍以实验标志的形式提供（Chrome 145，搜索结果说法）。这也意味着两者在真实业务中的取舍，主要取决于编码耗时、文件体积与画质的权衡，而不只是格式能否被浏览器解码。

**「影响」** 对需要批量转码的团队，追求 JPEG XL 最高 effort 可能用 50–180 倍编码时间换取照片 2–7% 的体积下降，因此应把吞吐量、实现选择（如 jixel 与 libjxl）和 AVIF 的透明度/工具链支持一起纳入测试。

**「社区讨论」** 评论区的核心分歧是编解码器成熟度：一方认为 AVIF 已可用于生产环境并给出具体 ffmpeg 参数，另一方以 MP3/LAME 和 WebP 的历史为鉴，主张等待更长时间再接受“赢家”结论；也有评论认为 AVIF 会抹掉照片高光并生成看似合理但失真的细节。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.inverity.ai/posts/avif-vs-webp-vs-jpeg-xl-2026">AVIF vs WebP vs JPEG XL in 2026: Which Format Wins?</a></li>

</ul>
</details>

**标签**: `#JPEG XL`, `#AVIF`, `#image compression`, `#web performance`, `#codecs`

---

<a id="item-tech-news-3"></a>
### [Big Fish：利用 OpenBSD 存活 37 年的内核漏洞](https://calif.io/research/big-fish) ⭐️ 8.0/10

安全研究人员在 calif.io 发布了一份题为《Big Fish》的技术报告，详述其如何发现并利用一个在 OpenBSD 内核代码库中存续约 37 年的缺陷；报告结合了内核内部机制分析与利用原语（exploit primitive）的推理，并附带历史溯源。该研究于 2026 年 10 月 16 日经 Hacker News 讨论传播，属于单点漏洞研究，而非厂商安全公告。当前可供参考的材料没有给出受影响的 OpenBSD 版本、补丁状态或 CVE 编号，因此漏洞的具体触发条件与修复情况仍不明确。

hackernews · rs\_rs\_rs\_rs\_rs · 10月16日 14:44 · [社区讨论](https://news.ycombinator.com/item?id=50118977)

**「背景」** 据 Calif 的研究，这个漏洞可追溯到约 37 年前原始 BSD 内核代码中的共享内存计数器溢出，研究者将其与一处内核越界写串联成提权链，从而在 OpenBSD 上取得 root shell（tool-2-1、tool-2-2）。在 PoC 于 2026 年 10 月 16 日公开之前，OpenBSD 已通过 errata 修复了相关问题（tool-2-2、tool-2-3）。

**「社区讨论」** 评论者 phendrenad2 指出，相关代码路径似乎是在 1999 年 8 月 NetBSD 重写该部分代码时被顺带修掉的（此说法来自评论者，未在材料中得到独立验证）。另一位评论者 ozereray1 认为，一个缺陷能在被高度审计的代码库中存活 37 年，说明部分内核缺陷难以仅靠人工审查发现，并提出疑问：这类缺陷能否由模糊测试或静态分析现实地找出，还是必须由人从利用原语的角度思考才能发现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cybersecuritynews.com/37-year-old-kernel-openbsd-flaw/">37-Year-Old Kernel Flaw Exploited to Gain Root Access on ...</a></li>
<li><a href="https://aicrier.com/post/got9bqqjbi3quvvti9pq">Big Fish Exploits 37-Year OpenBSD Bug — AICrier</a></li>
<li><a href="https://thedailytechfeed.com/37-year-old-kernel-bug-in-openbsd-finally-patched-after-root-exploit-poc/">37-Year-Old Kernel Bug in OpenBSD Finally Patched After Root ...</a></li>

</ul>
</details>

**标签**: `#security`, `#OpenBSD`, `#kernel`, `#exploit-development`, `#vulnerability-research`

---

<a id="item-tech-news-4"></a>
### [阶跃星辰发布 Step 5 Preview 智能体旗舰模型](https://huggingface.co/stepfun-ai/Step-5-Preview) ⭐️ 8.0/10

阶跃星辰在 Hugging Face 发布旗舰模型 Step 5 Preview，主打智能体工作负载。该模型采用稀疏 MoE 架构，总参数 6000 亿、激活参数 270 亿，支持最高 100 万 token 上下文，可接收文本、图像和视频输入。发布信息称其在软件工程、长周期智能体执行和专业知识任务上表现领先，尤其擅长金融场景，但这些性能说法尚未经独立验证，且模型仍为 Preview 版本。模型可通过 OpenAI 兼容 API 配合 vLLM 或 SGLang 部署，采用 StepFun Model License 1.0 许可。

telegram · zaihuapd · 10月16日 06:36

**「背景」** 该模型采用的是稀疏 MoE（混合专家）架构，其关键特征是总参数与单次推理实际激活的参数相互分离：外部资料称 Step 5 Preview 总参数约 6000 亿、激活参数约 270 亿，因此推理开销更接近一个 270 亿参数级模型，而模型容量来自更大的参数池（tool-2-2）。另有第三方平台资料提到，该模型支持推理与工具调用，并以 NVFP4 精度在 NVIDIA NIM 上提供（tool-2-3）。

**「部署与选型影响」** 对准备接入的团队来说，Step 5 Preview 可用 OpenAI 兼容 API 搭配 vLLM 或 SGLang 部署，接口迁移成本较低，但需注意其采用 StepFun Model License 1.0 许可，且当前只是 Preview 版本，不适合直接作为长期生产基线。据第三方测评，该模型在 Artificial Analysis 智能指数得 44 分、单任务成本约为 Claude Opus 5 的 1/8，DeepSWE v1.1 得分 67.7%、略高于 Kimi K3 与 GLM-5.3，实测在前端开发、塔防与 3D 互动游戏等场景可用；这些均为外部测评数据而非独立复现的官方基准，实际选型前应自行验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.eesel.ai/blog/stepfun-step-5">StepFun Step 5 Preview : specs, pricing, benchmarks, and... | eesel AI</a></li>
<li><a href="https://build.nvidia.com/stepfun-ai/step-5-preview">Step 5 Preview Model by Stepfun -ai | NVIDIA NIM</a></li>
<li><a href="https://ai-bot.cn/step-5-preview/">Step 5 Preview - 阶 跃 星 辰 推出的新一代旗舰基座 模 型 | AI工具集</a></li>
<li><a href="https://m.21jingji.com/article/20260921/herald/742325e7deb08d056e5801bcae9c9974.html">“单任务成本仅为Claude Opus 5的1/8”， 阶 跃 星 辰 Step 5 Preview ...</a></li>
<li><a href="https://www.woshipm.com/ai/6467696.html">实 测 Step 5 Preview ，又一个 能 打的国产 模 型 来了 | 人人都是产品经理</a></li>

</ul>
</details>

**标签**: `#大语言模型`, `#稀疏MoE`, `#多模态`, `#AI智能体`, `#模型发布`

---

<a id="item-tech-news-5"></a>
### [Llama.cpp 借 PS5LM 在越狱 PS5 上原生运行 GGUF 模型](https://github.com/cobanov/PS5LM) ⭐️ 7.0/10

GitHub 项目 cobanov/PS5LM 展示了在越狱 PlayStation 5 上原生运行 llama.cpp 与 GGUF 模型，目标用户是已越狱主机的本地推理爱好者。当前材料没有提供具体模型兼容性、推理速度、内存占用或安装条件，因此还不能确认其实际可用程度；这也不是索尼支持的能力。

hackernews · Anon84 · 10月16日 18:32 · [社区讨论](https://news.ycombinator.com/item?id=50122431)

**「背景」** llama.cpp 是一个用 C/C++ 编写的开源推理引擎，可直接加载 GGUF 量化模型并在本地硬件上运行，因而成为在非标准设备上部署本地大模型的常用选择。要在 PS5 上运行它，前提是主机已被越狱，从而能够执行非官方签名的自制程序。据工具结果中的仓库介绍页面，PS5LM 正是把 llama.cpp 移植到越狱后的 PS5，使用户能在主机浏览器中下载 GGUF 模型并进行对话。

**「对本地推理用户的实际影响」** 对无法或不愿新购硬件的本地推理用户，更直接的复用路径在于同一芯片血统：社区已为采用 PS5「Cyan Skillfish」精简版 APU 的二手 AMD BC-250 维护 llama.cpp 专用分支与部署指南，后者还提供将该硬件 GPU 核心频率限制在 1500 MHz 的时钟控制（工具结果 tool-3-1、tool-3-2）。需要留意的是，该项目以已越狱的 PS5 为前提，且来源与社区讨论均未给出可验证的性能或模型兼容性数据，实际可用性仍取决于主机固件与越狱环境。

**「社区讨论」** 评论中，Rabbit504030201 认为项目主站不应设在 GitHub，因为索尼可能随时下架并建议使用自有域名；xnx 和 pwython 则对把锁定游戏机变成通用计算机、以及 LLM 驱动的 NPC 表示兴趣。jjcm 称即便在 2 bit 量化下运行 Qwen 模型也能用于监控服务器错误率、分析监控画面等长时任务，并估算约每天 70 美分电费、约 200 万输出 token；shiftpgdn 推测类似硬件 BC250 也可运行，这些性能、成本与兼容性说法均来自评论者，未经独立验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://reporank.net/en/repo/cobanov-ps5lm.html">PS 5 LM : llama . cpp Inference on a Jailbroken PS 5 - Open Source...</a></li>
<li><a href="https://github.com/TechMakesArt/llama.cpp-bc250">GitHub - TechMakesArt/ llama . cpp - bc 250 : llama . cpp fork with Vulkan...</a></li>
<li><a href="https://github.com/akandr/bc250">GitHub - akandr/ bc 250 : AMD BC - 250 ( PS 5 APU ) setup guide...</a></li>

</ul>
</details>

**标签**: `#llama.cpp`, `#GGUF`, `#local LLM inference`, `#PS5 jailbreak`, `#hardware repurposing`

---

<a id="item-tech-news-6"></a>
### [苹果 MLX 分布式推理：四台 Mac Studio 跑近万亿参数模型](https://machinelearning.apple.com/research/mlx-distributed-inference) ⭐️ 7.0/10

苹果机器学习研究团队随研究博客发布了新版 MLX，并演示了跨机分布式推理：在四台 Mac Studio 组成的集群上运行近万亿参数的 Muse Spark Open，生成速度超过 36 token/秒。博文称可以从单台 Mac Studio（最高 512GB 统一内存）起步，再横向扩展到多台机器。上述数字均为苹果自测结果，尚未经独立验证；围绕该项工作的讨论主要集中在对比基准是否公平以及可用上下文长度上。

hackernews · antipaul · 10月16日 13:43 · [社区讨论](https://news.ycombinator.com/item?id=50118320)

**「背景」** MLX 是 Apple 面向 Apple Silicon 的机器学习框架，LM Studio 等本地推理工具已经把它作为在 Mac 上运行模型的引擎之一。此前的这类本地推理主要依赖单台 Mac 的统一内存，Apple 研究页面把本次发布定位为在 Apple Silicon 上做分布式大模型推理，并给出在 M5 Ultra Mac Studio、8,192 token 上下文下测得的解码速度。

**「本地部署的实际门槛」** 对想在本地运行前沿规模模型的开发者来说，这次演示把关键约束从“单机显存够不够”变成“能否搭起多机集群”：既然超大模型装不进一台机器，苹果的做法是把模型分片存放到两台或多台 Mac Studio 上做跨机流水线推理，单机 512GB 统一内存装不下时必须依赖 MLX 的分布式能力与机器间互联，选型和成本评估也因此从单台设备转向集群（tool-3-2、tool-3-1）。此外，有评论者指出演示中 15–36 tokens/s 的吞吐对应的是 8192 token 上下文，因此长上下文或多轮超长对话场景并不能直接照搬这一配置。

**「社区讨论」** 评论者 peri-cl 质疑基准不公平：Muse Spark Open 以 4-bit 量化测试，而 Qwen 只给出原生 BF16 结果，并称 Muse Spark 并不在其会优先考虑的前十模型之列；mrboatshoepants 指出那张 15–36 token/秒的图表对应 8,192 token 上下文，认为这一长度对当下实际使用远远不够。ks2048 评论说 Meta 花大钱做开放权重模型、用户却要花约 2 万美元买苹果硬件；liuliu 则报告单台 M5 Ultra（256GiB）跑 DeepSeek 4.1 Flash 0910 约 45 token/秒、M5 Max（128GiB）跑 GLM 5.3 Flash 也正常，并用 MathArena Apex、GPQA Diamond 等核对了质量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/LM_Studio">LM Studio - Wikipedia</a></li>
<li><a href="https://machinelearning.apple.com/research/mlx-distributed-inference">Local and Distributed Large LLM Inference with MLX and RDMA on...</a></li>
<li><a href="https://contracollective.com/blog/mlx-distributed-inference-multi-mac-cluster-2026">MLX Distributed Inference : Multi- Mac Cluster Setup for Local LLMs...</a></li>
<li><a href="https://machinelearning.apple.com/research/mlx-distributed-inference">Local and Distributed Large LLM Inference with MLX and RDMA on...</a></li>

</ul>
</details>

**标签**: `#MLX`, `#distributed inference`, `#Apple Silicon`, `#local LLM inference`, `#benchmarking`

---

<a id="item-tech-news-7"></a>
### [Mercor 研究：90% 美国工作时间缺乏 AI 基准覆盖](https://www.mercor.com/research/labor-index/benchmark-map/) ⭐️ 7.0/10

Mercor 发布研究称，按 O\*NET 任务映射后，90% 的美国工作时间投入在现有 AI 基准覆盖不足或未覆盖的任务上，因此很难用这些基准判断模型在美国人实际工作中的表现。这是 Mercor 自己的研究结论与度量主张，属于该机构的分析，而非独立复现的评测结果。研究还称，即便控制 AI 暴露度，工资总额更大的职业在基准提示词中仍被显著过度代表。

hackernews · speckx · 10月16日 17:08 · [社区讨论](https://news.ycombinator.com/item?id=50121179)

**「背景」** 这篇研究把现有 AI 基准的提示词映射到 O\*NET 职业任务分类，再按各类任务对应的全国工时计权，估算基准覆盖了多少美国人实际从事的工作。发布方 Mercor 本身也开发 AI 基准：其 APEX 系列基准由领域专家参与开发与验证（tool-2-3），第三方站点 BenchLM 于 2026 年 10 月 2 日记录的 APEX-1 榜单收录了 68 个已公布配置及其分数，BenchLM 说明这些是 Mercor 评测体系给出的结果、未自行复跑（tool-2-2）。

**「影响」** 对依赖现有基准判断模型能否胜任实际工作的企业和评测者来说，直接后果是基准分数可能无法外推到大量美国工作时间对应的任务；在招聘、部署或采购模型时，需要按自身任务补充评测，而不是直接采用通用榜单结论。

**「社区讨论」** Hacker News 讨论主要争论“覆盖良好”的定义与方法：OtherShrezzing 指出，某些类别只要有 13 条提示词就被算作“覆盖良好”，不足以代表社工等复杂工作。10111001 则引述研究称高工资总额职业在基准提示词中过度代表，并据此认为评测更容易关注“好工作”，而不是所有劳动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://benchlm.ai/benchmarks/mercorapex1">APEX-1 ( Mercor ) Leaderboard &amp; Scores — October 2026 | BenchLM. ai</a></li>
<li><a href="https://opportunitiesforyouth.org/2026/09/02/mercor-research-fellowship-apex-2026-earn-up-to-80000-to-build-the-next-generation-of-ai-benchmarks-and-economic-research/">Mercor Research Fellowship APEX 2026... - Opportunities for Youth</a></li>

</ul>
</details>

**标签**: `#AI benchmarks`, `#AI evaluation`, `#labor market`, `#O\*NET`, `#future of work`

---

<a id="item-tech-news-8"></a>
### [StarSkirmish Bench v0.2 刷新，LLM 写代码玩《星际争霸》](https://starskirmish.com/bench/v0-2/) ⭐️ 7.0/10

StarSkirmish Bench v0.2 已刷新，这是一个让 LLM 通过编写代码来玩《星际争霸：母巢之战》的基准测试，作者公布了 OpenAI、Anthropic、Google 和 Muse 旗舰模型的对比结果。评论中列出的排序为 GPT-6 Astra &gt; GPT-6.1 Sol &gt; Gemini 4 Argon &gt; Claude Opus 5.5 &gt; Claude Fable 5.1 &gt; Claude Sonnet 5.5，但该排序来自评论而非原始正文。评测按模型所在实验室的第一方 CLI 运行——Anthropic 用 Claude Code、OpenAI 用 Codex、Google 用 Antigravity CLI、Meta 用 Muse Code——并在其提供的最高推理设置下运行，同时关闭 CLI 的网页搜索与抓取工具且不提供其他联网访问。

hackernews · \_\_cayenne\_\_ · 10月16日 14:18 · [社区讨论](https://news.ycombinator.com/item?id=50118688)

**「背景」** StarSkirmish 是一个让大语言模型通过写代码来打《星际争霸：母巢之战》的基准测试：每个模型获得一小时，用 C++ 编写一个星灵（Protoss）机器人，再让它与其他模型生成的机器人以及既有人类编写的机器人对战 \[tool-2-1\]\[tool-2-2\]。该基准此前的 v0.1 版本采用一小时的运行时长和 “high” 推理档位 \[tool-2-1\]；本次 v0.2 是刷新后的版本，参评者换成了 OpenAI、Anthropic、Google 和 Muse 的旗舰模型，按评论中的描述，各模型在自家一方 CLI 工具中以最高推理档位运行，且关闭了联网工具。

**「影响」** 对使用该基准比较编程代理的开发者而言，结果只能解释为特定约束下的表现：各模型必须用自家第一方 CLI、最高推理设置运行，且没有联网检索能力，因此不能直接等同于模型在开放环境中的编码或规划能力。

**「社区讨论」** GodelNumbering 表示，该基准的模型排序与其朋友用 KataGo Elo 作锚点的 9x9 围棋基准完全一致，不过这只是他报告的关联，并非因果证据。cgearhart 则质疑时间限制是否让代理编写的机器人只能成为最佳人类机器人的劣化版，以及它们是否真的能通过实验反馈或领域经验发现新策略。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://starskirmish.com/bench/">StarSkirmish : where LLMs write code to play StarCraft .</a></li>
<li><a href="https://simpleprog.com/news/show-hn-a-starcraft-bw-arena-where-llms-play-by-writing-code-3b3d2564">Show HN: A StarCraft BW Arena where LLMs play by writing code</a></li>

</ul>
</details>

**标签**: `#LLM benchmarks`, `#AI agents`, `#code generation`, `#StarCraft`, `#model evaluation`

---

<a id="item-tech-news-9"></a>
### [Anthropic Claude Code 团队主张把代码审查改为持续 AI 检查](https://simonwillison.net/2026/Oct/16/code-review/) ⭐️ 7.0/10

Simon Willison 博客引述了 Anthropic 博文《How the Claude Code team does code review》中的一段话：Claude Code 团队的 Addy Osmani、Morgan Westlee Lunt 和 Qing Wang 表示，他们认为“有没有人读过这段代码”只是“这次改动可能出什么问题、该由哪种检查（自动还是人工）来发现”的不精确替代指标。按照这一思路，审查的时机也变了——过去审查是流程终点的关卡（写代码、开 PR、等同事），现在审查持续进行，更像写作时的拼写检查：多数改动在请人工查看之前，已经由 Claude 至少审查并修复过一次，从而把团队注意力留给了更高层次的问题。这是该团队对自己工作方式的描述，来源仅为一段引文，未提供实现细节或可量化的效果数据。

rss · Simon Willison · 10月16日 22:06

**「背景」** 编码智能体让写代码不再是瓶颈之后,问题转移到代码写完之后的管理环节——代码评审、版本控制、构建与持续集成。Anthropic 的 Claude Code 团队在同一篇博客中说明,他们是在评审覆盖率和评审深度都达到较高水平之后,才开始以“在不增加回滚或事故的前提下把人工评审时间压到最低”为目标进行优化。

**「影响」** 对采用类似流程的团队而言，人工审查不再是变更的第一道检查，Claude 的首轮审查成为常规改动的默认过滤层，人的注意力转向设计取舍等更高层问题；这也意味着“合并前有人读过代码”不再是统一的审计假设，哪些改动仍必须由人确认需要另行判断。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://claude.dev/blog/solving-code-review-at-anthropic/">How the Claude Code team does code review / claude.dev Blog</a></li>
<li><a href="https://www.theregister.com/devops/2026/10/13/anthropic-reinvents-source-control-as-claude-floods-the-world-with-code/5302943">Anthropic reinvents source control as Claude floods the world ...</a></li>

</ul>
</details>

**标签**: `#AI-assisted code review`, `#Claude Code`, `#software engineering practices`, `#developer workflow`, `#Anthropic`

---

<a id="item-tech-news-10"></a>
### [ORL 加速扩散语言模型推理：单张 RTX 5090 达 2,788 tokens/s 并开源](https://www.reddit.com/r/MachineLearning/comments/1x7qgr0/research_2788_tokenss_on_a_single_rtx_5090_with_a/) ⭐️ 7.0/10

Reddit 研究帖宣布开源 ORL（On-Policy Residual Learning）扩散语言模型（dLLM）加速方法及配套推理引擎 dlmrt，并同时开放模型权重、训练代码、评测流程，帖中称可在不牺牲生成质量的前提下显著提速。作者给出的峰值数据包括：单张 RTX 5090 上 LLaDA-2.1-mini + ORL（NVFP4）达 2,788 tokens/s，8× B200 上 DiffusionGemma 26B MoE 达 7,708 tokens/s，QwenDLM-4B 端到端吞吐最高提升约 6.9×，其 HumanEval pass@1 从 82.9% 升至 89.6%。在单张 H100 的对比中，作者称 QwenDLM-4B + ORL 为 1,298 tokens/s，是 DFlash（746 tokens/s）的 1.74 倍，但 ORL 使用 dlmrt、对比方案使用 vLLM，且作者称 dlmrt 在同模型同解码设置下比 SGLang/vLLM 快 1.2–1.6×。作者明确指出这些数字均为 batch size 1 的单请求峰值结果，而非并发聚合吞吐或任意提示词上的平均值，因此属于发布者自述的基准声明，暂无独立复现或第三方验证。

reddit · r/MachineLearning · /u/arty\_photography · 10月16日 20:03

**「背景」** 扩散语言模型（dLLM）不像自回归模型那样一次只生成一个 token，而是可以并行细化并确定多个 token，但其长期瓶颈在于需要较多去噪前向次数才能收敛，难以把并行性转化为实际吞吐。作为对照，自回归解码一侧常用 DFlash、EAGLE3 等投机解码来降低单请求延迟，本次发布也正是在这一维度上给出比较。该工作的论文与模型检查点已随发布同步公开（tool-2-1、tool-2-3）。

**「对本地推理开发者的影响」** 对想在本地跑扩散 LLM 的开发者而言，可操作的变化是 ORL 的模型权重、训练代码、评测流程与 dlmrt 推理引擎均已开源，拥有 RTX 5090 的用户可直接尝试 LLaDA-2.1-mini + ORL 的 NVFP4 checkpoint；但 2,788 tokens/s 是单请求峰值且为作者自报，作者称 dlmrt 在单张 H100 上比 SGLang/vLLM 快 1.2–1.6×，意味着要复现其峰值数字需改用 dlmrt 而非现有 vLLM 服务路径。作为规模参照，有资料称 DiffusionGemma 26B 的 NVFP4 版本在单张 RTX 5090 上约为 700+ tokens/s、占用约 18GB 显存，但两者模型规模、量化方式与测试基准不同，不能据此直接横向比较。

<details><summary>参考链接</summary>
<ul>
<li>On-Policy Residual Learning for Diffusion Language Models - arXiv</li>
<li>yifanyu/QwenDLM-4B-ORL - Hugging Face</li>
<li><a href="https://www.digitalapplied.com/blog/google-diffusiongemma-open-weight-text-diffusion-model-guide">Google DiffusionGemma: First Open-Weight Text Diffusion</a></li>
<li><a href="https://rohitraj.tech/en/notes/run-diffusiongemma-locally-vllm-rtx5090-2026">How to Run DiffusionGemma Locally: A vLLM Serving Guide for RTX ...</a></li>

</ul>
</details>

**标签**: `#diffusion language models`, `#inference optimization`, `#open source`, `#GPU performance`, `#LLM systems`

---

<a id="item-tech-news-11"></a>
### [法院文件披露 Telegram 向美执法部门提供用户数据细节](https://www.404media.co/heres-what-telegram-giving-data-to-the-u-s-government-looks-like/) ⭐️ 7.0/10

据 404 Media 报道，新公开的法院文件显示，Telegram 在回应美国法院命令时向执法部门提供了一名用户的手机号、用户 ID 和 IP 地址。文件称，Telegram 在信函中将此举描述为“自愿”，且不承认受美国司法管辖；该案涉及被控参与 2023 年 10 月 7 日袭击以色列事件的 Mahmoud Al-Muhtadi。文件还显示，截至今年 1 月，Telegram 已向美方提供 2253 名用户的数据。

telegram · zaihuapd · 10月16日 14:57

**「背景」** Telegram 过去极少配合美国执法部门的数据请求：PCMag 的报道称，2024 年 1 月 1 日至 9 月 30 日期间该公司仅处理了 14 起美国请求，而在其 CEO 于法国被捕后的几个月内完成了近 1000 起。Factually 的事实核查则指出，Telegram 在 2024 年回应了 900 起法律请求、涉及 2253 名美国用户，披露内容以手机号和 IP 地址为主，并将其归因于 2024 年 9 月扩大数据共享适用情形的政策转变。此次曝光的法院文件正是这一转变下一个具体请求的处理细节。

**「对用户的实际影响」** 对 Telegram 用户而言，此次披露的数据虽只包括手机号、用户 ID 和 IP 地址，却足以把匿名用户名对应到真实号码和网络位置，因此仅靠用户名隐藏真实身份的做法在收到法院命令时并不成立。截至今年 1 月已有 2253 名用户的数据被提供给美方，说明这并非孤例；不过 Telegram 在信函中称系「自愿」提供且不承认美国司法管辖，该披露在法律上的强制性与适用范围仍存在争议。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://factually.co/fact-checks/technology/telegram-user-records-disclosed-to-us-authorities-2024-2025-legal-processes-e0b45a">How Many User Records Did Telegram Disclose to U.S. Au...</a></li>
<li><a href="https://www.pcmag.com/news/telegram-reports-huge-spike-in-data-sharing-with-law-enforcement">Telegram Reports Huge Spike in Data Sharing With Law Enforcement Does Telegram Report CSAM to Law Enforcement? What Changed Telegram evidence beyond the cloud | Andrea Fortuna The Wiretap: Telegram Handing Data On Thousands Of Users To ... US Prosecutors Gained Legal Approval to Hack Telegram Servers</a></li>
<li><a href="https://www.404media.co/heres-what-telegram-giving-data-to-the-u-s-government-looks-like/">Here’s What Telegram Giving Data to the U.S. Government Looks ...</a></li>
<li><a href="https://factually.co/fact-checks/technology/telegram-data-sharing-law-enforcement-what-is-shared-legal-conditions-199e73">What Exactly Does Telegram Share With Law Enforcement ...</a></li>

</ul>
</details>

**标签**: `#Telegram`, `#privacy`, `#government surveillance`, `#data disclosure`, `#tech policy`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [AI 数据中心投资受市场回调与利率上升，多项上市计划被撤回或暂停](https://www.kitco.com/news/off-the-wire/2026-10-15/market-selloff-rising-rates-test-ai-data-centre-deal-boom) ⭐️ 7.0/10

过去一周，AirTrunk 的 REIT 上市计划、英伟达支持的 Firmus 及软银支持的 SB Energy 的上市安排被撤回或暂停，因市场抛售与利率上升，投资者要求企业证明能消化升高的利率与算力成本。Dealogic 数据显示，亚洲数据中心并购交易今年迄今已达 213 亿美元，约为 2025 年全年 100 亿美元的两倍；股权融资同比下降 4.6%。

telegram · zaihuapd · 10月16日 05:10

**「背景」** 这次被撤回或暂停的上市计划此前都在推进中：AirTrunk 计划在新加坡发行房地产投资信托（REIT）、目标募资约 15 亿美元（tool-1-2），英伟达支持的 Firmus 拟募资最高 50 亿美元（tool-2-1），SB Energy 则是软银旗下的美国数据中心开发商（tool-3-2）。当市场利率上升、股价回调时，投资者对新股定价会更挑剔，要求企业证明自己能够承受更高的利息支出和算力成本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.mingtiandi.com/real-estate/data-centres/blackstones-airtrunk-taps-banks-for-singapore-reit-ipo-targeting-1-5b-raise/">AirTrunk Taps Banks for Singapore REIT IPO Seeking... - Mingtiandi</a></li>
<li><a href="https://au.finance.yahoo.com/news/stock-sinks-23-australia-30bn-034730756.html">A stock sinks 23% as Australia’s $30bn Firmus AI data - centre IPO ...</a></li>
<li><a href="https://www.ft.com/content/8b7e2800-3e36-4d0c-9016-32deaae67b62">Why the IPO market is booming and busting</a></li>

</ul>
</details>

**标签**: `#AI data centers`, `#capital markets`, `#M&amp;A`, `#IPOs`, `#interest rates`

---

<a id="item-finance-news-2"></a>
### [商务部拟修订技术出口目录，涉人工智能、生物医药、光伏 40 项技术](https://aqygzj.mofcom.gov.cn/flzc/gzjgfxwj/art/2026/art_c99f95ca0cd043829ac9991495fc283c.html) ⭐️ 7.0/10

商务部就修订《中国禁止出口限制出口技术目录》公开征求意见，拟对人工智能、生物医药、光伏三个领域共 40 项技术加强出口管理，其中人工智能 23 项、生物医药 5 项、光伏 12 项。该目录修订目前仍处征求意见阶段，最终管理范围和执行细节尚未确定，已通过开源或发表论文进入公共领域的技术拟不纳入管理范围。

telegram · zaihuapd · 10月16日 09:12

**「背景」** 中国商务部通过《中国禁止出口限制出口技术目录》管理技术出口，列入限制类的技术对外转让须获得许可。商务部已就此次拟增列人工智能技术的考虑公开回应说明，而本轮修订目前仍处于公开征求意见阶段，最终纳入范围尚未确定。

**「影响」** 若该修订最终落地，向境外转让或许可相关技术的中国人工智能、生物医药和光伏企业需办理出口登记或许可手续；不涉及所有权转让的对外授权仍适用自动许可等便利措施。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://finance.sina.com.cn/roll/2026-10-16/doc-inivmazf7040150.shtml">finance.sina.com.cn/roll/ 2026 -10-16/doc-inivmazf7040150.shtml</a></li>

</ul>
</details>

**标签**: `#出口管制`, `#人工智能`, `#生物医药`, `#光伏`, `#产业政策`

---

<a id="item-finance-news-3"></a>
### [投资者下调 Anthropic IPO 估值预期至约 1.5 万亿美元](https://www.reuters.com/business/finance/investors-temper-anthropic-ipo-valuation-expectations-over-revenue-growth-2026-10-15/) ⭐️ 7.0/10

据路透社报道，部分投资者将人工智能公司 Anthropic 的 IPO 估值预期从此前的 2 万亿美元下调至约 1.5 万亿美元。此前该公司公布第三季度营收 168 亿美元，环比增长 45%，并称经调整后实现盈利、季度现金流转正。报道称估值预期下调的原因包括营收增速放缓、模型价格竞争加剧以及算力投入带来的资金压力。

telegram · zaihuapd · 10月16日 15:46

**「背景」** 据路透社和 CNBC 援引知情人士，Anthropic 2026 年第三季度营收为 168 亿美元，高于第二季度的约 116 亿美元，这也是“环比增长 45%”的比较基线。该公司目前尚未上市，报道中的 1.5 万亿美元是投资者在其 IPO 前的估值预期，而非已完成的交易价格。

**「影响」** 来源分析认为，这一估值预期下调可能成为智谱、MiniMax、Kimi 和 DeepSeek 等 AI 公司的估值压力测试，市场将更关注其收入持续性、毛利率和资本效率；此前智谱和 MiniMax 曾因稀缺性享有上市溢价（tool-2-1）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.reuters.com/business/finance/anthropics-q3-revenue-surges-45-nearly-17-billion-2026-10-14/">At Anthropic pre-IPO meet: ‘Thinking’ caps, surging revenue ...</a></li>
<li><a href="https://www.cnbc.com/2026/10/15/anthropics-third-quarter-revenue-hits-16point8-billion-ipo.html">Anthropic&#x27;s Q3 revenue is said to hit $16.8 billion ahead of IPO</a></li>
<li><a href="https://eu.36kr.com/en/p/3896477565191561">DeepSeek Sprinting Toward IPO: The &quot;Four AI Rising Stars ...</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#IPO估值`, `#AI行业`, `#财务业绩`, `#估值压力`

---