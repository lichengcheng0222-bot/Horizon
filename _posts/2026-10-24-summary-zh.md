---
layout: default
title: "Horizon Summary: 2026-10-24 (ZH)"
date: 2026-10-24
lang: zh
---

> 从 33 条内容中筛选出 8 条重要资讯。

---

**科技新闻**
1. [Calif 博客声称攻破 iPhone，社区讨论 Lockdown Mode 实效](#item-tech-news-1) ⭐️ 8.0/10
2. [Kimi K3.1-Pro 上线 API：3T 参数与 1M 上下文](#item-tech-news-2) ⭐️ 8.0/10
3. [Block 发布 Dessa：可本地运行的全双工语音模型](#item-tech-news-3) ⭐️ 7.0/10
4. [蜂群即单个强化学习智能体：作者主张精确等价](#item-tech-news-4) ⭐️ 7.0/10
5. [PHP 基金会建议暂禁上传进度功能](#item-tech-news-5) ⭐️ 7.0/10

**财经新闻**
1. [国办发文：稳慎推进 AI 应用，减缓就业替代影响](#item-finance-news-1) ⭐️ 8.0/10
2. [电动自行车等三类产品 CCC 认证新规将于 2026 年 11 月起实施](#item-finance-news-2) ⭐️ 7.0/10
3. [证监会核准设立花旗证券（中国）有限公司](#item-finance-news-3) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Calif 博客声称攻破 iPhone，社区讨论 Lockdown Mode 实效](https://blog.calif.io/p/iphone) ⭐️ 8.0/10

一篇发布在 blog.calif.io 的文章声称“今天，我们攻破了原本要攻破的目标：iPhone”，但现有摘录未给出漏洞类型、受影响的 iOS 版本、利用条件或复现步骤，因此这仍只是一项待验证的声明。Hacker News 的讨论集中在实际防护与可操作性：有评论者追问开启 Lockdown Mode 能否挡住这类利用，也有人提醒越狱可能导致 iCloud、iMessage 等服务无法使用。另有评论者感叹，前沿模型的 Red Team 访问只向少数内部成员或公司开放，使圈外研究者难以参与同类漏洞挖掘。

hackernews · pavel\_lishin · 10月23日 16:21 · [社区讨论](https://news.ycombinator.com/item?id=50211474)

**「背景」** Calif 团队并非首次公开此类研究：其 9 月 11 日的通讯称，团队此前演示了首个公开绕过 Apple MIE 的案例（针对 macOS 26.4.1），本次 iPhone 演示延续同一路线。据 heise 报道，上周公布的针对 iOS 27.0.1 的 untethered 越狱工具预计要等 Apple 通过更新修复相关漏洞后才会披露细节，因此当前公开材料仍以演示为主。

**「对用户的实际影响」** 目前公开信息没有说明这些演示针对哪些 iOS 版本，也没有说明在开启 Lockdown Mode 时是否仍然有效，因此用户无法据此判断 Lockdown Mode 是否已被绕过。可核实的参照是：据 2026 年 3 月报道，名为 Coruna 的 iOS 漏洞套件针对 iOS 13.0 至 17.2.1，对最新版 iOS 无效；同月 Apple 表示尚未见到开启 Lockdown Mode 的设备被间谍软件成功入侵。因此，在演示细节公布前，保持系统更新仍是现有证据支持的主要缓解措施。

**「社区讨论」** 评论中最实质的争论是 Lockdown Mode 的真实防护效果：有读者承认它在理论上能削减常见攻击面，但明确询问它能否挡住此次展示的利用。另一条评论则从越狱后的服务可用性出发，认为苹果可通过检测越狱把用户挡在 iCloud、iMessage 等生态服务之外，使改装后的设备实用性大降。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.calif.io/p/iphone">iPhone - Calif Newsletter</a></li>
<li><a href="https://blog.calif.io/">Calif Newsletter | Substack</a></li>
<li><a href="https://www.heise.de/en/news/Calif-io-jailbreak-How-the-untethered-tool-cracks-iOS-27-0-1-11492321.html">Calif.io jailbreak: How the untethered tool cracks iOS 27.0.1</a></li>
<li><a href="https://techcrunch.com/2026/03/27/apple-says-no-one-using-lockdown-mode-has-been-hacked-with-spyware/">Apple says no one using Lockdown Mode has been hacked with ...</a></li>
<li><a href="https://thehackernews.com/2026/03/coruna-ios-exploit-kit-uses-23-exploits.html">Coruna iOS Exploit Kit Uses 23 Exploits Across Five Chains ...</a></li>

</ul>
</details>

**标签**: `#iPhone security`, `#exploit research`, `#jailbreaking`, `#Lockdown Mode`, `#AI security access`

---

<a id="item-tech-news-2"></a>
### [Kimi K3.1-Pro 上线 API：3T 参数与 1M 上下文](https://www.kimi.ai/blog/kimi-k3-1-pro) ⭐️ 8.0/10

Kimi 发布 K3.1 系列首款模型 K3.1-Pro，已接入 Kimi、Work、Code 和 API，支持 100 万 token 上下文；官方称其规模为 3 万亿参数级，并计划在 2026 年 11 月 4 日前发布完整权重，因此当前还不是可下载的开放权重模型。同步推出的 Highspeed 版本速度为标准版的 2—3 倍，价格为两倍，但输入缓存命中同价；标准版 API 定价为每百万输入 token 2 美元、每百万输出 token 10 美元。官方基准称其 Terminal-Bench 4.0 得分为 65.7%，高于 GPT-6 Astra 的 58.2%、接近 Claude Opus 5.5 的 66.4%；第三方 Artificial Analysis 评分为 55，低于 Opus 5.5 的 58，高于 GPT-6 Astra、Claude Fable 5.1 和 Gemini 4 Argon 的 53。Kimi 称编程、3D 建模与金融工作流是升级重点，内部高难度测试的陈述级幻觉率从 23.4% 降至 8.3%，但明确表示这不等于日常使用错误率。

telegram · zaihuapd · 10月23日 17:14

**「背景」** 开放权重指模型参数可供下载并在自有环境中部署，区别于只能通过 API 调用。Kimi 此次先让 K3.1-Pro 接入 Kimi、Work、Code 和 API，完整权重则承诺在 2026 年 11 月 4 日前发布；该模型也是 K3.1 系列首款模型，官方称其在 K3 基础上扩大了后训练规模。

**「影响」** 对开发者而言，现在可通过 Moonshot API 调用 K3.1-Pro 评估长上下文和智能体编程任务，但若团队需要本地部署、微调或审计权重，仍要等到计划中的 11 月 4 日前发布，当前只能依赖托管服务；延迟敏感型应用还需注意 Highspeed 版本计费翻倍。

**标签**: `#AI models`, `#open-weight models`, `#coding benchmarks`, `#long context`, `#Kimi`

---

<a id="item-tech-news-3"></a>
### [Block 发布 Dessa：可本地运行的全双工语音模型](https://block.xyz/dessa) ⭐️ 7.0/10

Block 公布了名为 Dessa 的全双工语音模型，称其可在 MacBook Pro M4 Max 或更高配置的 Mac 上本地运行，并且只用一台 NVIDIA GB200 NVL72 完成训练。公告以“史上最真实的全双工语音模型”为卖点，但这是公司方的宣传表述，目前没有独立的技术验证或第三方延迟、自然度评测。现有材料未说明模型是否开放、采用何种许可，以及完整的硬件要求。

hackernews · dsr12 · 10月23日 19:09 · [社区讨论](https://news.ycombinator.com/item?id=50213925)

**「背景」** 全双工语音模型的核心是边听边说：它在输出语音的同时继续接收并处理用户的插话和反馈，而不是等一方说完后再依次转写、生成和合成。传统语音助手多采用回合制流水线，因此在响应延迟和对话自然度上受到限制；这也使低延迟的本地推理成为衡量此类模型的关键指标。

**「影响」** 如果本地低延迟的说法成立，开发者可在高端 Apple 芯片上构建不依赖云端的实时语音交互；但在获得模型访问权限和独立基准前，应按公告的 M4 Max 门槛评估兼容性，而不能把宣传中的自然度当作已测结果。

**「社区讨论」** 有评论者对演示中的低延迟、表现力以及单台 GB200 NVL72 训练表示惊讶，认为若能在本地设备复现，是独立 AI 的显著成果；也有人质疑“史上最真实”属于营销措辞，并称演示音轨听起来像由大量播客数据训练而成。另有评论者不喜欢演示中机器假装关心的对话方式，认为这削弱了交流价值。

**标签**: `#speech models`, `#full-duplex interaction`, `#on-device AI`, `#model training`, `#Hacker News`

---

<a id="item-tech-news-4"></a>
### [蜂群即单个强化学习智能体：作者主张精确等价](https://www.reddit.com/r/MachineLearning/comments/1xdhf7r/r_the_hive_mind_is_a_single_reinforcement/) ⭐️ 7.0/10

一篇发布在 r/MachineLearning 的帖子（作者 /u/mistlab）声称，基于局部模仿的群体集体决策——以蜜蜂通过摇摆舞选择巢址的加权投票模型为例——在数学上精确等价于多臂老虎机设定下的单智能体强化学习。作者将这一宏观算法命名为 Maynard-Cross Learning，并给出有效步长 α = 1/N：N 个不具学习能力的个体相当于 N 条并行环境采样。帖子链接了 arXiv 论文、项目页和复现代码，但内容为作者自述，未经同行评审，摘要也未提供实证验证或独立复现结果。

reddit · r/MachineLearning · /u/mistlab · 10月23日 15:37

**「背景」** 要理解这项推导，需要两个既有概念：多臂老虎机中的 Cross Learning 按观测奖励直接更新各选项被选中的概率，演化博弈论的复制子动力学则描述策略占比在群体中的传播；蜜蜂摇摆舞的“加权投票者”模型——侦察蜂按巢址质量决定宣传时长，同伴不比较收益而直接跟随——是本文推导 MCL 的生物学原型。作者随后把各选项的群体占比视为一个宏观智能体的策略，这一视角与将蜂群描述为与多个并行环境交互的单一在线强化学习智能体相通。

**「对群体系统设计者的影响」** 按论文推导，群体规模 N 直接决定有效学习率 α = 1/N，因此设计群体机器人或分布式决策系统时，扩大群体等同于调小步长，需要相应增加采样轮次或重新调整模仿与奖励参数，而不能假定个体越多收敛越快。作者在 GitHub 仓库 MISTLab/HiveMindRL 中提供了连接集体动力学的仿真代码，但该结论目前以理论推导和仿真呈现，尚未见到物理机器人或真实部署的验证，采用前应先行复现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2410.17517">The Hive Mind is a Single Reinforcement Learning Agent</a></li>
<li><a href="https://www.alphaxiv.org/abs/2410.17517">The Hive Mind is a Single Reinforcement Learning Agent | alphaXiv</a></li>
<li><a href="https://arxiv.org/html/2410.17517">The Hive Mind is a Single Reinforcement Learning Agent</a></li>
<li><a href="https://github.com/MISTLab/HiveMindRL">GitHub - MISTLab/ HiveMindRL : simulations connecting collective...</a></li>

</ul>
</details>

**标签**: `#reinforcement learning`, `#swarm intelligence`, `#multi-armed bandits`, `#collective decision-making`, `#theoretical ML`

---

<a id="item-tech-news-5"></a>
### [PHP 基金会建议暂禁上传进度功能](https://x.com/ThePHPF/status/2113580383875019242) ⭐️ 7.0/10

据这份简要的二次报道，PHP 基金会建议在下一个 PHP 版本发布前，将 session.upload\_progress.enabled 设为 0，以防范编号 CVE-2026-115560 的远程代码执行（RCE）漏洞。报道称，只有运行时把非默认的 serialize\_handler 切换为“php”的应用可能受影响，因此该建议的适用范围较窄。基金会此前还曾因 CVE-2026-109619 建议保持该功能禁用。

telegram · zaihuapd · 10月23日 13:46

**「背景」** PHP 的 session.upload\_progress 功能利用会话存储文件上传进度，应用可读取该状态向客户端报告进度；会话数据的序列化方式由 session.serialize\_handler 决定。来源提到，PHP 基金会此前已因 CVE-2026-109619 建议保持该功能禁用。

**「处置建议」** 目前没有紧急补丁；运维者应按建议在下一版 PHP 发布前将 session.upload\_progress.enabled 设为 0。由于只有运行时把 session.serialize\_handler 切换为 php 且开启上传进度的应用才会暴露，禁用前应核查代码和运行时配置，以免影响未使用该组合的服务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.getastra.com/blog/security-advisory/cve-2026-115560/">CVE-2026-115560: Another PHP Session-Handler RCE</a></li>
<li><a href="https://safeguard.sh/resources/blog/php-cve-2026-115560-session-upload-progress-mitigation">PHP CVE-2026-115560: unpatched session upload progress RCE ...</a></li>

</ul>
</details>

**标签**: `#PHP`, `#security vulnerability`, `#RCE`, `#CVE`, `#upload progress`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [国办发文：稳慎推进 AI 应用，减缓就业替代影响](https://mp.weixin.qq.com/s/St8URoMYcV-voM7kLAK3Bw) ⭐️ 8.0/10

国务院办公厅印发《关于适应人工智能技术发展助力构建就业友好型发展方式的意见》，要求稳慎把握人工智能在劳动密集型行业应用的范围、力度和节奏，并鼓励企业探索失业缓冲期制度，提前告知受影响劳动者并提供转型转岗支持，以减缓 AI 应用对就业的替代影响。

telegram · zaihuapd · 10月23日 12:54

**「背景」** 随着人工智能加快进入生产流程，劳动密集型岗位可能被替代的担忧上升；这份文件从国家层面提出构建“就业友好型发展方式”，要求优先在劳动力紧缺、环境高危等岗位推广 AI。

**「影响」** 劳动密集型企业和相关劳动者将直接受影响：企业部署 AI 时需评估应用范围和节奏，员工在岗位受到冲击前可获得提前告知及转岗支持。

**标签**: `#人工智能就业影响`, `#国务院政策`, `#劳动力市场`, `#就业友好型发展`, `#失业缓冲期`

---

<a id="item-finance-news-2"></a>
### [电动自行车等三类产品 CCC 认证新规将于 2026 年 11 月起实施](https://www.gelonghui.com/live/2726360) ⭐️ 7.0/10

中国市场监管总局升级电动自行车、玩具、童车三类产品的 CCC（中国强制性产品认证）实施规则，新规自 2026 年 11 月 1 日起实施。其中电动自行车须严格实行“一车一池一充一码”，出厂时配齐全部必需部件，并随车附带一致性证书；新规还要求型式试验后保留整车样品至证书有效期结束后至少 12 个月，并加严证后跟踪检查与抽样检测。

telegram · zaihuapd · 10月23日 10:12

**「背景」** CCC 认证是中国强制性产品认证，未获认证的产品不得出厂、销售或进口；据 IT 之家报道，此前市场监管总局已撤销超过 5 万张 CCC 证书。

**「影响」** 新规直接约束电动自行车、玩具和童车生产企业：电动自行车厂商须在出厂时配齐全部必需部件、随车附一致性证书，并将整车样品保留至证书有效期结束后至少 12 个月，合规管理与样品仓储负担随之增加。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ithome.com/1/017/160.htm">超 5 万张 证 书被撤销， 市 场 监 管 总 局 对 CCC ...</a></li>
<li><a href="https://www.ithome.com/1/017/160.htm">超 5 万张 证 书被撤销，市场监管总局对 CCC ...</a></li>

</ul>
</details>

**标签**: `#China regulation`, `#CCC certification`, `#electric bicycles`, `#product safety`, `#manufacturing compliance`

---

<a id="item-finance-news-3"></a>
### [证监会核准设立花旗证券（中国）有限公司](https://mp.weixin.qq.com/s/f_fCJUEObewqgAe5Ie7wHA) ⭐️ 7.0/10

10 月 23 日，中国证监会核准设立花旗证券（中国）有限公司，注册地为上海，注册资本人民币 12 亿元，由花旗环球金融控股有限公司 100%出资。获批业务范围包括证券经纪、证券投资咨询、证券承销与保荐及证券自营。

telegram · zaihuapd · 10月23日 12:29

**「背景」** 花旗集团是一家总部位于纽约的美国跨国银行。据彭博报道，花旗从申请到获得这张在华独资证券牌照，等待了将近五年。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Citigroup">Citigroup - Wikipedia</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2026-10-23/citigroup-secures-approval-for-solo-securities-venture-in-china">Citi Wins China Securities Approval After Five-Year Wait - Bloomberg</a></li>

</ul>
</details>

**标签**: `#China securities regulation`, `#Citigroup`, `#foreign financial institutions`, `#market entry`, `#CSRC approval`

---