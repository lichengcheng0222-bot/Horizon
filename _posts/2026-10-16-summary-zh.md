---
layout: default
title: "Horizon Summary: 2026-10-16 (ZH)"
date: 2026-10-16
lang: zh
---

> 从 47 条内容中筛选出 15 条重要资讯。

---

**科技新闻**
1. [Meta 发布开放权重模型 Muse Spark Open](#item-tech-news-1) ⭐️ 8.0/10
2. [RPKI 覆盖 70% 互联网路由，中国采用率跃升](#item-tech-news-2) ⭐️ 8.0/10
3. [BIPM 通过决议：2027 年起 UTC 停止插入闰秒](#item-tech-news-3) ⭐️ 8.0/10
4. [Libreboot 26.10「Ominous Olive」发布，加入 UEFI/EDK 与 Chromebook 支持](#item-tech-news-4) ⭐️ 8.0/10
5. [Meta 新商业条款被指允许抓取新闻网站](#item-tech-news-5) ⭐️ 7.0/10
6. [GNOME 博客谈用 AI 逆向工程硬件](#item-tech-news-6) ⭐️ 7.0/10
7. [上海 AI 实验室开源 744B MoE 智能体模型 Atria Dawn](#item-tech-news-7) ⭐️ 7.0/10
8. [SemiAnalysis AgentX 实测：MI355X 局部反超 Blackwell 推理成本](#item-tech-news-8) ⭐️ 7.0/10
9. [阶跃星辰发布 Step 5 Preview 智能体旗舰模型](#item-tech-news-9) ⭐️ 7.0/10

**科技博客**
1. [AMD MI355X 上 Kimi K3 的 vLLM 推理优化](#item-tech-blog-1) ⭐️ 8.0/10
2. [AI 编码推动中等成功软件项目繁荣](#item-tech-blog-2) ⭐️ 7.0/10

**财经新闻**
1. [IMF：中国农村家庭医疗支出占可支配收入 8.7%，仅次于美国](#item-finance-news-1) ⭐️ 7.0/10
2. [哈佛捐赠基金 2026 财年回报 27.1%，SpaceX 成最大持仓](#item-finance-news-2) ⭐️ 7.0/10
3. [AI 数据中心投资受市场回调与利率上升，多项投资被撤回和暂停](#item-finance-news-3) ⭐️ 7.0/10
4. [商务部拟对 AI、生物医药、光伏 40 项技术出口征求意见](#item-finance-news-4) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Meta 发布开放权重模型 Muse Spark Open](https://research.meta.ai/blog/muse-spark-open) ⭐️ 8.0/10

Meta 发布开放权重模型 Muse Spark Open，Hugging Face 仓库标识为 816B-A42B，随附开发博客链接以及一则关于该模型针对 Mac Studio 运行优化的报道。该模型使用带限制的许可：评论者引用的条款文本显示，若被许可方及其关联方通过 API 或类似接口向第三方提供“模型即服务”（Model as a Service），且合计总收入超过 2000 万美元，则将受到额外约束（源文本在此处被截断）。目前可获得的一手材料基本是链接合集，模型的技术细节、权重与基准成绩多来自社区转述，因此相关定位表述仍需以官方说明或独立评测为准。

hackernews · bigwheels · 10月15日 17:47 · [社区讨论](https://news.ycombinator.com/item?id=50107379)

**「背景」** 开放权重模型指的是权重可下载并自行部署的模型，此前的检索结果显示，Muse Spark Open 定位为面向智能体编程的模型，可通过 SGLang、vLLM 或 Apple MLX 自行服务，也可经由托管 API 调用。Meta 此次采用的 Muse Model License 被外部报道描述为“对多数商业用途免费、限制与 Llama 类似”，属于其以往开源许可的延续；该许可同时要求在产品或服务界面显著标注“Built with Muse Spark Open”。正因开放权重模型可被第三方包装成服务转售，社区对其中“模型即服务”条款的适用范围格外关注。

**「对部署与商业使用的影响」** 许可证中的「模型即服务」条款值得提前核对：据社区评论引述，当被许可方及其关联方合计毛收入超过 2000 万美元、并通过 API 或类似接口向第三方提供模型输出时即受该条款约束，因此计划基于 Muse Spark Open 构建对外 API 产品的开发者需要先评估合规边界，相关许可要点也被第三方解读列为该发布需要留意的部分（tool-3-1）。在部署路径上，Meta 将该模型定位为可在 Apple M5 Ultra Mac Studio 上本地运行（tool-3-3），PyTorch 则提供了 Helion 推理内核以及 TorchTitan 的监督微调与强化学习支持（tool-3-2），使自托管推理与微调成为可操作的替代方案。

**「社区讨论」** 讨论主要围绕“开放性”与竞争力：有评论者查阅许可后认为除模型即服务条款外基本可自由使用，也有人据此质疑它是否算真正的开放权重。另有评论者引用 Artificial Analysis 的对比称该模型表现不及 Qwen3.8 Flash Next 与 GLM 5.3 Flash（后两者可在单张 B300 上运行），并抱怨该评测只提供最高推理档位的比较；还有评论者注意到宣传口径从“最强”转为“美国/欧盟最强”，认为 Meta 意在围绕黏性较高的 Muse 构建生态护城河。

<details><summary>参考链接</summary>
<ul>
<li>LICENSE.md · meta-models/Muse-Spark-Open ...</li>
<li>Meta Drops Muse Spark Open, an 816B Open-Weight Model Rivaling ...</li>
<li>Build with Muse Spark Open - Meta AI</li>
<li><a href="https://penchan.co/en/ai/meta-muse/muse-spark-open/">What Is Muse Spark Open? Meta&#x27;s Open-Weight Model: Benchmarks ...</a></li>
<li><a href="https://pytorch.org/blog/muse-spark-open/">Muse Spark Is Now an Open-Weights Model - PyTorch</a></li>
<li><a href="https://research.meta.ai/blog/muse-spark-open">Introducing Muse Spark Open, The Most Capable US Open‑Weight ...</a></li>

</ul>
</details>

**标签**: `#open-weight models`, `#Meta`, `#model licensing`, `#LLM release`, `#community debate`

---

<a id="item-tech-news-2"></a>
### [RPKI 覆盖 70% 互联网路由，中国采用率跃升](https://ipinfo.io/blog/rpki-protects-70-internet-routes) ⭐️ 8.0/10

据 ipinfo 的报告，RPKI 路由起源验证现已覆盖约 70% 的互联网路由，其中中国的采用率大幅上升：其 IPv4 地址处于有效路由中的比例从 3.7% 升至 83.0%，按地址计算贡献了全球增量的近 60%。报告称这使 RPKI 有效路由范围达到新水平，但这是采用率里程碑，并非新的协议能力或独立复核的技术突破。对路由安全从业者来说，这意味着更多路由可被起源验证机制检查，不过覆盖范围本身并不等于完整的 ASN 路径验证。

hackernews · emot · 10月16日 00:52 · [社区讨论](https://news.ycombinator.com/item?id=50112330)

**「背景」** RPKI（资源公钥基础设施）用于对 BGP 路由来源做密码学验证，让网络运营商能判断某条路由公告是否得到地址持有者授权，从而减少路由劫持和误宣告。IPinfo 的对比数据显示，一年前 RPKI 有效路由比例约为 54%；同期 ASPA 部署也在加速，用于补充 AS 路径验证。

**「对运营商的直接影响」** 对网络运营商而言，覆盖率提高并不等于同等比例的劫持被挡住：RPKI 的源验证（ROV）只校验前缀与 ASN 的绑定，不校验 AS 路径，伪造源劫持、路由泄露和 BGP 属性攻击仍可绕过验证。工具结果在相近的覆盖水平下也记录了这些盲点，因此仅部署 ROV 并把高覆盖率当作完整防护，会留下安全预期落差，运营商需要另行部署 ASPA 等 AS 路径验证机制来补齐。

**「社区讨论」** 评论中，cowlevel 担忧 RPKI 将路由授权集中到注册机构数据库后，可能因法律或政治压力而被篡改，例如把所有俄罗斯允许路由集中到荷兰服务器并自动执行会带来断网风险。1473-bytes 则分享其组织推动自身及下游客户路由达到 RPKI 有效的经验，提到 ASPA 似已可用于 ASN 路径验证，并建议未来考虑采用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ipinfo.io/blog/rpki-protects-70-internet-routes">RPKI Now Protects 70% of Internet Routes, Up From 54% a Year Ago</a></li>
<li><a href="https://news.lavx.hu/article/rpki-now-protects-70-of-internet-routes-up-from-54-a-year-ago">RPKI Now Protects 70% of Internet Routes, Up From 54% a Year ...</a></li>
<li><a href="https://ipregistry.co/blog/rpki-blind-spots">RPKI Covers 67% of Routes, But Four Attack Classes Slip Right Past It</a></li>

</ul>
</details>

**标签**: `#RPKI`, `#BGP security`, `#internet routing`, `#network security`, `#internet infrastructure`

---

<a id="item-tech-news-3"></a>
### [BIPM 通过决议：2027 年起 UTC 停止插入闰秒](https://www.bipm.org/en/cgpm-2026/resolution-5) ⭐️ 8.0/10

国际计量大会（CGPM）通过决议，决定自 2027 年起不再向 UTC 插入闰秒，此前累计插入的 27 次闰秒预计将成为历史上的全部。该决议把 UTC 与太阳时之间偏差的后续修正责任推迟到极远的未来，届时才需要考虑更简单的处理方式。对操作系统、NTP/PTP 时间同步、数据库和分布式系统而言，这意味着沿用数十年的闰秒应对逻辑不再有新的触发场景。BIPM 公布的页面本身是一份简短的决议文本，未给出实施细节。

hackernews · gliffie · 10月15日 16:11 · [社区讨论](https://news.ycombinator.com/item?id=50105777)

**「背景」** UTC 自 1972 年起通过不定期插入闰秒，将与基于地球自转的 UT1 之间的偏差控制在 1 秒以内（tool-2-2）。BIPM 同时要求国际地球自转与参考系统服务（IERS）相应调整闰秒的运作与公布方式，并确定连续 UTC 自 2027 年 5 月 20 日起生效（tool-2-1）。该决议由 10 月 13 日至 15 日在凡尔赛举行的第 28 届国际计量大会通过（tool-2-2）。

**「对时间敏感系统的影响」** 对运行时间敏感系统的开发者而言，2027 年起不再插入闰秒意味着 23:59:60 这类“61 秒分钟”不再出现，旧式 NTP 实现在插入闰秒时可能损坏数据库、日志与分布式账本的那一类故障随之消失。但同一资料指出，UTC 与 UT1 的允许偏差将从目前的 0.9 秒扩大，因此依赖太阳时或地球自转对准的应用——天文观测、卫星跟踪、天球导航等——需要在自己的逻辑中累计并补偿这一持续扩大的偏移，而不能等待标准时间自动校正。

**「社区讨论」** 评论者 tialaramex 认为，不再新增闰秒的决定此前已经作出，这份决议实际解决的是遗留矛盾：定义 UTC 的协议称其跟踪太阳时，而 TAI 并不如此；新做法是把该问题推迟到文明尺度之外，未来若真需要修正，可用相当简单的办法处理。另一位评论者 BoppreH 补充说，停止增删闰秒的生效日期为 2027 年 5 月 20 日，并将长期维持，因此已插入的 27 次闰秒很可能就是全部；另有评论者提出应着手制定行星际时间标准并更好处理相对论时间效应。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bipm.org/en/cgpm-2026/resolution-5">Resolution 5 (2026) - BIPM</a></li>
<li><a href="https://trustlist.uk/news/leap-seconds-end-continuous-utc-from-20-may-2027-cgpm-resolution-5">Leap seconds end as UTC becomes continuous on 20 May 2027</a></li>
<li><a href="https://dev.to/leojulieta/future-proof-your-systems-ditch-leap-seconds-by-2027-1ef3">Future‑Proof Your Systems: Ditch Leap Seconds by 2027</a></li>
<li><a href="https://www.bigiron.cc/guides/leap-seconds-and-the-smearing-debate-what-breaks">Leap seconds and the smearing debate: what actually breaks ...</a></li>

</ul>
</details>

**标签**: `#timekeeping`, `#standards`, `#UTC`, `#distributed-systems`, `#infrastructure`

---

<a id="item-tech-news-4"></a>
### [Libreboot 26.10「Ominous Olive」发布，加入 UEFI/EDK 与 Chromebook 支持](https://libreboot.org/news/libreboot2610.html) ⭐️ 8.0/10

Libreboot 26.10（代号「Ominous Olive」）发布，主要变化是引入 UEFI/EDK 集成，并从 MrChromebox 的 coreboot 发行版导入全部 233 款当前受支持的 Chromebook。据社区评论引述的发布说明，本版本中这部分 Chromebook 支持为「仅源码」（source-only，不提供二进制，需自行编译），其中 Baytrail（Kip）已测试，其余机型仍待测试。该版本同时因 LLM 辅助贡献政策引发讨论。

hackernews · iamnothere · 10月15日 12:52 · [社区讨论](https://news.ycombinator.com/item?id=50102923)

**「背景」** Libreboot 是一个基于 coreboot 的自由开源 BIOS/UEFI 引导固件发行版。此次纳入的 Chromebook 支持来自 MrChromebox.tech —— 一个长期为 Chromebook、Chromebox 提供定制 coreboot 固件与配套工具的独立项目。据外部报道，26.10 版把引导层切换到 EDK2 以提供完整的 UEFI 支持，从而可以引导 Windows 10 和 11。

**「影响」** 对 Chromebook 用户而言，本版本暂不提供可直接刷写的二进制镜像，需自行从源码构建，且除 Baytrail（Kip）外的机型尚未验证，实际可用性取决于后续测试。评论者指出，接入 EDK 后新增设备的门槛将明显降低，未来机型更容易被纳入支持范围。

**「社区讨论」** 评论者 iamnothere 认为外界过度关注 AI 政策，UEFI/EDK 集成与 Chromebook 支持才是「巨大进步」，因为它成倍扩大了可用设备数量；AdmiralAsshat 也确认了 233 款机型与「仅源码、Baytrail 已测试」的细节。lf88 则称严格限制 LLM 辅助贡献「令人耳目一新」，只接受 AI 辅助的缺陷报告；cwiggs 分享了自己在 Heads 项目中基于 MrChromebox 代码合并首个 ChromeOS 移植 PR 的经验。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mrchromebox.tech/">MrChromebox .tech</a></li>
<li><a href="https://libreboot.org/">Libreboot – Free and Open Source BIOS/ UEFI boot firmware</a></li>
<li><a href="https://dzen.ru/a/atDluHbGGgLj999U">Libreboot 26 . 10 сделал EDK 2 основой загрузки Windows... | Дзен</a></li>

</ul>
</details>

**标签**: `#Libreboot`, `#open-source firmware`, `#UEFI`, `#Chromebook support`, `#LLM contribution policy`

---

<a id="item-tech-news-5"></a>
### [Meta 新商业条款被指允许抓取新闻网站](https://www.niemanlab.org/2026/10/metas-new-commercial-terms-will-allow-the-scraping-of-news-sites-legal-experts-say/) ⭐️ 7.0/10

据 Nieman Lab 报道，法律专家称 Meta 的新商业条款将允许 Meta 抓取新闻网站内容，并引发对 AI 训练数据用途和内容许可的争论。该报道未提供条款全文，现有材料也无法确认其适用范围、是否已经生效或实际执行。相关讨论的关键在于，这类条款能否让 Meta 有效获得新闻内容的使用许可，以及它对新闻出版商意味着什么。

hackernews · 0in · 10月15日 23:37 · [社区讨论](https://news.ycombinator.com/item?id=50111852)

**「背景」** 此次争论的一个前提是：AI 训练依赖大量网络内容，而新闻出版商常常只从第三方获得有限的内容授权，未必有权允许 Meta 抓取其网站内容。据一则俄语报道，Meta 的新商业条款将于 2026 年 10 月 30 日生效，把商业账户与“收集网站内容”的许可绑定在一起（tool-2-3）。因此，平台与商业用户之间的合同条款，可能成为决定新闻网站内容能否被用于 AI 训练的法律依据。

**「影响」** 对与 Meta 有商业账户关系的新闻出版商来说，这一条款变更意味着 Meta 可据以主张抓取其内容并用于 AI 训练（来源报道称此为法律专家的解读），因此出版商需要先核对自己是否有权作出这种再许可。由于 2019 年 hiQ 诉 LinkedIn 先例认定抓取公开可访问数据通常不违反联邦法（tool-3-2），而 2024 年 Meta 诉 Bright Data 裁定确认违反合同限制的抓取仍可能构成违约（tool-3-3），出版方可用的主要救济手段落在合同条款而非抓取法本身。

**「社区讨论」** HN 评论者中，amluto 质疑该法律逻辑：如果发布者本身是从第三方获得授权，未必有权再向 Meta 授予抓取和内容许可，因此条款可能无法成立。nananana9 则认为，Meta 要求合作伙伴授予训练许可，可能反而削弱 AI 公司“无需版权所有者许可即可训练”的普遍主张，并可能推动“需要许可”的先例；另有评论者推测 Meta 可能已在抓取，新条款只是提供法律掩护。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://dzen.ru/b/atGnB_5wA2igkbBt">Meta свяжет бизнес-аккаунты с разрешением собирать... | Дзен</a></li>
<li>Meta&#x27;s new commercial terms will allow the scraping of news sites ...</li>
<li>Third-Party Web Scrapers Poised to Benefit from Growing AI Training ...</li>
<li>Web Scraping Legal Issues: 2025 Enterprise Compliance Guide</li>

</ul>
</details>

**标签**: `#AI training data`, `#copyright and licensing`, `#web scraping`, `#Meta`, `#tech policy`

---

<a id="item-tech-news-6"></a>
### [GNOME 博客谈用 AI 逆向工程硬件](https://blogs.gnome.org/uraeus/2026/10/15/aiandreverseengineerhardware/) ⭐️ 7.0/10

GNOME 博客平台发表了一篇关于用 AI 辅助硬件逆向工程的文章，但提供给编辑的材料只有标题和 Hacker News 评论区，没有正文、方法细节或可验证结果，因此无法确认文中提出了哪些具体做法，也无法判断是否包含突破性发现。相关讨论集中在三类话题：实际逆向工作流、专利与知识产权风险，以及消费设备安全。评论者对 AI 降低逆向门槛的利弊看法并不一致。

hackernews · ErenayDev · 10月15日 14:35 · [社区讨论](https://news.ycombinator.com/item?id=50104299)

**「背景」** 这篇文章出自 Christian Fredrik Kalager Schaller 的 GNOME 博客；据该博客存档显示，他早在 2026 年 3 月 23 日就发表过一篇文章，讲述如何用 AI 为自己手头的 Elgato 灯具和 Dell Ultrasharp 摄像头编写控制程序（tool-1-1）。因此本文延续的是同一类实践：面对厂商不再维护或从未公开协议的消费级硬件，借助 AI 推断设备行为并补上缺失的工具或驱动，而不是从头研究芯片层面的逆向方法。

**「法律风险：逆向合法不等于产品合法」** 对打算把 AI 逆向结果做成产品的人来说，风险并不止于逆向工程这一步：有法律分析指出，逆向工程通常合法，但制造、使用或销售受专利保护的方案仍构成侵权，同一行为还可能同时触发专利、商业秘密与合同三重责任（tool-3-1、tool-3-2）。因此，基于逆向出的接口或算法推出兼容设备或驱动的开发者，需要在量产或发布前单独核查目标市场的专利与许可条款，而不能仅以“逆向过程本身被允许”作为依据。

**「社区讨论」** 多位评论者报告了具体经验：revolvingthrow 称自己几乎逆向过所有自有电子设备（处理 USB 外设、读取 Rodecaster 状态、为 macOS 27 重写旧打印机驱动），Doohickey-d 则说用 LLM 为一台 2006 年后就没有可用驱动的 FireWire 转 USB 设备写出了用户态驱动，xnx 呼吁把同样手段用于智能电视以移除广告和僵尸网络。另一方面，amelius 设想让 AI 自动比对专利并通知权利人，valdiorn 则作为小型吉他效果器厂商表达了对算法被快速复制、竞争加剧的焦虑——以上均为评论者的个人经验或担忧，未经独立证实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blogs.gnome.org/uraeus/">Christian F.K. Schaller | Blog talking about Fedora, GNOME ...</a></li>
<li><a href="https://www.lawgratis.com/blog-detail/ai-hardware-reverse-engineering-ip-disputes">Ai Hardware Reverse Engineering Ip Disputes. - Law Gratis</a></li>
<li><a href="https://lumenci.com/blogs/reverse-engineering-patent-law/">Reverse Engineering &amp; Patent Law: Doctrines, Cases &amp; Limits</a></li>

</ul>
</details>

**标签**: `#AI-assisted reverse engineering`, `#hardware reverse engineering`, `#embedded systems`, `#consumer device security`, `#patent/IP concerns`

---

<a id="item-tech-news-7"></a>
### [上海 AI 实验室开源 744B MoE 智能体模型 Atria Dawn](https://atria-asi.ai/) ⭐️ 7.0/10

上海人工智能实验室 10 月 12 日发布智能体模型 Atria Dawn，称其基于 744B 参数的 MoE 架构 GLM-5.2 构建，面向科研与工程场景，支持工具调用和多步任务执行。该模型上下文窗口为 256K，支持本地部署与托管访问，代码和权重以 MIT 许可证开源。官方演示展示其可完成蛋白质结构预测、CAD 建模、知识可视化、PPT 制作和数据分析等任务。由于该消息来自简短 Telegram 通告，尚无独立验证或基准数据，上述能力仍属官方声明。

telegram · zaihuapd · 10月16日 01:32

**「背景」** 今年 9 月中旬已有外部报道称，上海人工智能实验室悄然在 Hugging Face 上放出了「Atria Dawn Preview」：7440 亿参数的 MoE 智能体模型、MIT 许可的开放权重，且没有配套博客、论文或定价说明，其底座取自智谱（Z.ai）的 GLM-5.2，而非实验室自研的前沿基座（tool-1-2、tool-1-3）。与那次静默发布相比，本次是官方正式发布，并明确给出工具调用、多步任务执行与 256K 上下文窗口等规格；不过早期报道曾把上下文写成 1M，与当前口径不一致，具体规格仍以官方说明为准（tool-1-1）。

**「影响」** 对开发者而言，MIT 许可证与代码、权重开源意味着可以自托管并进行修改和二次开发；但 744B MoE 的规模也意味着实际部署门槛将取决于尚未披露的硬件要求、显存占用与推理吞吐。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.orcarouter.ai/blog/atria-dawn-preview-quiet-release">Atria Dawn Preview: InternLM&#x27;s 744 B Agentic MoE Ships Quietly</a></li>
<li><a href="https://reupload.io/en/articles/2026-09-16-shanghai-ai-lab-releases-744b-open-weight-agentic-model">Shanghai AI Lab Releases 744 B Open-Weight Agentic Model</a></li>
<li><a href="https://sonasi.app/en/blog/atria-dawn-preview-glm-5-2-post-training">Shanghai AI Lab Did Not Train Its Frontier Model . It Post-Trained Z. ai &#x27;s</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#open-source AI`, `#large language models`, `#MoE`, `#Shanghai AI Lab`

---

<a id="item-tech-news-8"></a>
### [SemiAnalysis AgentX 实测：MI355X 局部反超 Blackwell 推理成本](https://github.com/SemiAnalysisAI/InferenceX) ⭐️ 7.0/10

SemiAnalysis 开源了真实 Agent 轨迹数据集 AgentX（称耗资 300 万美元，覆盖 1M+ 极长上下文、多轮分支以及 95%+ KV 缓存命中的代码生成负载），并据此给出推理成本对比：在 Kimi K3、GLM-5.3 等超大 MoE 架构与中等延迟场景下，AMD MI355X 依靠 288 GB 显存拉高批处理密度，每百万 Token 综合成本比英伟达 Blackwell 低 9%–40%。消息称 AMD 仅用约 26 天，通过 70 余个开源社区 PR、TileLang 融合内核编译（打通 Fused MLA 与 FP8 KV Cache）以及自研 ATOM 运行时，让 MI355X 在 DeepSeek-V4-Pro 等模型上的吞吐翻倍。同一份对比也指出，在 &gt;150 tok/s 的极端低延迟交互和超大密集模型上，Blackwell 凭借 NVLink 与 FP4 仍保持 2–5 倍的能效与成本优势。需注意，以上内容来自 Telegram 的二手转述，属于机构基准声明而非独立复现，方法学细节有限，模型与性能数据均未获第三方验证。

telegram · zaihuapd · 10月16日 02:30

**「背景」** InferenceX 是 SemiAnalysis 维护的开源推理基准，其公开页面会在配置变化时更新 NVIDIA 与 AMD 的固定序列推理结果，供跨芯片、跨框架对比（tool-2-2）。此次引发讨论的 AgentX 是该基准中面向极长上下文、多轮代码生成的负载场景，专门用于替代脱离实际的固定序列测试，对比页面覆盖 Kimi K3、DeepSeek V4 Pro、MiniMax M3、Qwen 3.5、GLM 5.3 等模型（tool-2-1）。SemiAnalysis 在介绍 AgentX 时称双方都有较强结果，MI355X 在若干固定序列配置中也能领先，并认为 AgentX 更贴近当下的 agentic 推理负载（tool-2-3）。

**「对推理硬件选型的影响」** 对正在做推理硬件选型或成本核算的团队来说，具体含义是：若负载属于超大 MoE、中等延迟、高并发多轮场景，MI355X 的 288 GB HBM 能提升批处理密度，值得纳入逐 Token 成本对比测试——SemiAnalysis 早前也预期 288 GB HBM3e（对比 B200 的 192 GB）在多轮高并发下更占优。但这一“局部倒挂”不可外推：外部测试显示 NVIDIA B300 把显存容量补到 288 GB 后，在已公布的 K3 测试点上普遍领先 MI355X 约 1.25–1.75 倍，AMD 仅保住约 11% 的总体拥有成本优势，因此低延迟与密集模型负载仍应按 Blackwell 基准评估。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://inferencex.semianalysis.com/compare">AgentX Inference Comparisons | InferenceX by SemiAnalysis</a></li>
<li><a href="https://inferencex.semianalysis.com/">AI Accelerator System Benchmark | AcceleratorX by SemiAnalysis</a></li>
<li><a href="https://newsletter.semianalysis.com/p/agentx-inferencexv3-does-cuda-moat">AgentX - InferenceXv3: Does CUDA Moat Hold up in Agentic Inferencing?</a></li>
<li>InferenceX v2: NVIDIA Blackwell Vs AMD vs Hopper - SemiAnalysis</li>
<li>hopper, blackwell, and instinct: the exhaustive guide to llm inference ...</li>

</ul>
</details>

**标签**: `#AI inference`, `#AMD MI355X`, `#NVIDIA Blackwell`, `#CUDA ecosystem`, `#agent workloads`

---

<a id="item-tech-news-9"></a>
### [阶跃星辰发布 Step 5 Preview 智能体旗舰模型](https://huggingface.co/stepfun-ai/Step-5-Preview) ⭐️ 7.0/10

阶跃星辰在 Hugging Face 发布旗舰模型 Step 5 Preview，采用稀疏 MoE 架构，总参数 6000 亿、激活参数 270 亿，支持最高 100 万 token 上下文，并可接收文本、图像和视频输入。该模型明确面向智能体（agentic）与软件工程任务，官方称其在软件工程、长周期智能体执行和金融等专业知识任务上表现领先。模型可通过 OpenAI 兼容 API 配合 vLLM 或 SGLang 部署，并采用 StepFun Model License 1.0 许可。由于这是 Preview 版本，上述性能领先结论均来自厂商，尚无独立验证。

telegram · zaihuapd · 10月16日 06:36

**「背景」** 稀疏 MoE（混合专家）架构将模型拆分为多组专家网络，每个 token 只激活其中一小部分，因此 Step 5 Preview 虽然总参数为 6000 亿，实际每 token 只激活 270 亿——推理所需的算力与显存更接近一个 270 亿参数的稠密模型，同时保留更大的参数容量。赫吉脸（Hugging Face）与 ModelScope 上已同步放出该预览版的 BF16 与 FP8 权重，并附带技术博客，说明这是一次带开放权重的发布而非仅限内部测试。

**「对开发者与采购方的影响」** 对计划自部署智能体的团队，Step 5 Preview 提供了通过 vLLM 或 SGLang 暴露 OpenAI 兼容 API 的部署路径，已有 OpenAI 接口客户端的迁移成本相对较低；但模型采用 StepFun Model License 1.0 而非标准开源许可，商用或再分发前需先核对该许可的具体条款。外部测评称其在同等智能水平下成本低约 65%，该数字来自第三方测评而非独立复现，选型时宜自行验证。

<details><summary>参考链接</summary>
<ul>
<li>stepfun-ai/Step-5-Preview - Hugging Face</li>
<li>StepFun on X: &quot;Step 5 Preview is now open weights. BF16 and FP8 ...</li>
<li><a href="https://www.stepfun.com/step-5-preview">Step 5 Preview: Advancing the Pareto Frontier</a></li>
<li><a href="https://www.explainx.ai/blog/stepfun-step-5-preview-pareto-frontier-launch-2026">StepFun Step 5 Preview: A New Pareto Frontier for Agentic AI</a></li>

</ul>
</details>

**标签**: `#LLM`, `#MoE`, `#agentic AI`, `#long context`, `#model release`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [AMD MI355X 上 Kimi K3 的 vLLM 推理优化](https://vllm.ai/blog/2026-10-16-kimi-k3-mi355x) ⭐️ 8.0/10

rss · vLLM Blog · 10月16日 00:00

**「背景」** AgentX 这类编码代理负载回放真实会话的长度、时序与前缀共享模式，理论上可复用超过 96% 的前缀，但 Kimi K3 的 24 层 MLA（随对话增长的压缩 KV 历史）与 69 层 KDA（固定维度递归状态）意味着每一轮仍要触碰大量缓存与状态数据。硬件上，AMD Instinct MI355X 的稠密低精度峰值 10.1 PFLOP/s 低于 NVIDIA B300 的 13.5 PFLOP/s，两者 HBM 容量与带宽相同（288 GB、8 TB/s），因此性能必须从软件栈里找。

**「方案」** 作者把工作分成六类。缓存方面，DCP8 把 MLA 历史按位置切分到 8 张卡，142K 上下文的每卡占用从约 1.96 GB 降到约 245 MB；CPU offload 用主机 DRAM 保留 MLA 历史与 KDA 检查点，并通过对齐二者的恢复位置（\#54736）避免前缀重算。MoE 方面，原先每个 rank 都重复执行 routed-expert 输出投影，改为各卡只计算自己拥有的输出坐标、复用已有的 all-reduce（\#51253），PR 测试吞吐提升 3.05–4.91%；后续按 rank 加载权重行（\#59591）每卡省下约 3.85 GiB，在并发 70 时带来 28.9% 提升，前缀命中率从 74.8% 升到 80.1%。内存搬运方面，融合单 token 的 KDA 路径与 AttnRes+RMSNorm 减少 kernel 启动和拷贝（吞吐 +14.2%），并把矩阵乘法输入打包移入专用分支，消除每步 69 次无用拷贝。MLA 方面，把每卡 12 个 query head 补齐到 16 以启用 AMD AITER 汇编路径，长上下文下每输出 token 从 43.8 ms 降到 23.6 ms，短输入几乎不变。KDA 方面，预填充用分组并行打破 token 间依赖，投机验证改用四列窄 tile，把 workgroup 从 48 提高到 384，单 GPU 图重放测试中每层从 16.20 降到 5.61 微秒。投机解码则要在提交 token 数与整个 draft-verify-commit 周期成本之间权衡：按 AgentX 的固定接受参考，4 个 draft 只多 12% 已提交输出，周期涨幅超过 12% 就不划算。按作者报告的公开结果，50 tokens/s/user P90 下 MI355X 约 7,567 tokens/s/GPU，对比 B300 的 6,083，高出 24.4%；按 SemiAnalysis 建模的每 GPU 小时成本 1.50 与 2.26 美元，每美元 token 多 87.4%。

**「启示」** 作者的结论是：这类性能来自消除重复计算、跨卡协作以及让 kernel 始终保持足够的并行工作量，而非单看某一 kernel 的峰值；同时他提醒头条数字是厂商提交、基于合成 token 与建模 TCO 的基准，部分优化（如 \#59591）是在头条所用镜像之后才落地的。

**标签**: `#LLM inference optimization`, `#vLLM`, `#AMD ROCm`, `#Mixture-of-Experts`, `#speculative decoding`

---

<a id="item-tech-blog-2"></a>
### [AI 编码推动中等成功软件项目繁荣](https://seangoedecke.com/ai-is-driving-a-boom-in-modestly-successful-software/) ⭐️ 7.0/10

rss · Sean Goedecke · 10月16日 00:00

**「背景」** 如果 AI 写代码这么厉害，为什么没有出现大量惊艳的新软件产品？Sean Goedecke 把这个问题落到可观测数据上：他选取约二十个暴露安装量的软件市场、插件注册表和 Mod 平台，对比智能体编码于 2025 年中期主流化前后的成功项目数量。

**「方案」** 他发现新软件总量按来源不同增长约 2 至 20 倍，但增长几乎都落在“中等成功”区间：成功项目总体约翻倍，而极成功的软件项目（不计 AI 工具）没有真实增长。具体地，NVDA 屏幕阅读器插件中下载超 1000 的约增两倍而超 1 万的不变，HACS 中超 100 安装的翻倍而超 1000 的不变，Steam 上超 100 条评测的新游戏比 2024 年前多约 60%，Obsidian、Firefox/Chrome 扩展、Nexus Mod、Blender 扩展也呈类似模式；Google Play、WordPress 等例外。作者提醒，平台自然增长、Obsidian 放宽插件审核等会干扰数据，而社区对 AI 的敌意也使自愿披露不可靠，因此不能断定每个项目都用了 AI。他把原因解释明确标为推测：成熟大公司功能已饱和、技术惯性大且新增功能常很细微；至于为何没有更多超级成功的业余项目，可能是好点子本就稀少，或长尾项目需要时间成长。研究本身也借助 AI 完成。

**「启示」** 作者的结论是，AI 更可能把软件生态的长尾变厚，让大量插件、Mod、扩展和小游戏获得几百到几千用户，而不是立刻抬高最头部的超级产品。

**标签**: `#AI coding agents`, `#software ecosystem metrics`, `#open-source plugins`, `#empirical analysis`, `#hobbyist software`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [IMF：中国农村家庭医疗支出占可支配收入 8.7%，仅次于美国](https://www.cnbc.com/2026/10/15/chinese-spending-nearly-as-much-of-income-as-americans-on-healthcare.html) ⭐️ 7.0/10

国际货币基金组织（IMF）在新书《迈向中国经济增长新模式》中指出，中国农村家庭将 8.7%的可支配收入用于医疗，在 20 个主要经济体中仅次于美国的 9.9%；中国城镇家庭为 5.4%，排名第三。

rss · CNBC Finance · 10月15日 23:00

**「背景」** 这项分析出自国际货币基金组织 2026 年 9 月出版的《迈向中国经济增长新模式》一书。在中国，户籍（即决定居民能享受哪些社会福利的登记制度）为农村的人口进城务工后，往往难以获得与城市户籍居民同等的医疗和养老保障，因而更需要为看病和养老自行存钱。

**「影响」** IMF 称，针对农村地区增加政府医疗和社会保障支出，可显著降低农村家庭的储蓄率并提振消费，同时指出中国社会支出低于国际同行。

<details><summary>参考链接</summary>
<ul>
<li>Toward a New Economic Growth Model for China</li>

</ul>
</details>

**标签**: `#China economy`, `#healthcare spending`, `#IMF report`, `#household savings`, `#rural-urban inequality`

---

<a id="item-finance-news-2"></a>
### [哈佛捐赠基金 2026 财年回报 27.1%，SpaceX 成最大持仓](https://www.cnbc.com/2026/10/15/harvards-endowment-jumps-27percent-with-spacex-as-top-holding.html) ⭐️ 7.0/10

哈佛大学 10 月 15 日发布的年度财报显示，其捐赠基金 2026 财年（截至 6 月 30 日）回报率为 27.1%，为五年来最强，规模增至近 680 亿美元，跑赢标普 500 同期 22.3%的总回报；该基金最大持仓为价值 22 亿美元的 SpaceX 股份，同期联邦资助研究收入下降 19.5%至 5.09 亿美元。

rss · CNBC Finance · 10月15日 19:53

**「背景」** 哈佛捐赠基金面临的政策压力来自 2025 年签署生效的联邦法律：该法把对哈佛捐赠基金投资收益征收的消费税税率从 1.4%上调至 8%（tool-1-1）；此前特朗普政府还宣布冻结对哈佛的联邦拨款（tool-1-2）。这解释了为什么投资回报创下佳绩的同时，联邦资助的研究收入却在减少。

**「影响」** 哈佛校方称，自本财年起联邦对其净投资收益的消费税将从 1.4%升至 8%，估计每年增加约 3 亿美元成本，这将进一步限制捐赠基金对学校运营的支持；校方表示其分配机制刻意平滑，以免支出随市场大起大落。

<details><summary>参考链接</summary>
<ul>
<li>Trump Signs Spending Package Into Law, Imposing 8% Tax on Harvard&#x27;s ...</li>
<li>Money Up, Admissions Down: Harvard&#x27;s Endowment Management ...</li>

</ul>
</details>

**标签**: `#Harvard endowment`, `#SpaceX`, `#higher education funding`, `#endowment tax`, `#institutional investing`

---

<a id="item-finance-news-3"></a>
### [AI 数据中心投资受市场回调与利率上升，多项投资被撤回和暂停](https://www.kitco.com/news/off-the-wire/2026-10-15/market-selloff-rising-rates-test-ai-data-centre-deal-boom) ⭐️ 7.0/10

AI data-centre investment is being tested by market selloff and rising rates, with several listings withdrawn or paused and Asia data-centre M&amp;A reportedly doubling prior-year levels.

telegram · zaihuapd · 10月16日 05:10

**标签**: `#AI data centers`, `#financing`, `#IPOs`, `#interest rates`, `#data-center M&amp;A`

---

<a id="item-finance-news-4"></a>
### [商务部拟对 AI、生物医药、光伏 40 项技术出口征求意见](https://aqygzj.mofcom.gov.cn/flzc/gzjgfxwj/art/2026/art_c99f95ca0cd043829ac9991495fc283c.html) ⭐️ 7.0/10

商务部就修订《中国禁止出口限制出口技术目录》公开征求意见，拟将人工智能、生物医药、光伏三个领域的 40 项技术纳入出口管理。其中人工智能 23 项（已通过开源、发表论文等方式进入公共领域的技术不纳入管理），生物医药 5 项（不涉及所有权转让的对外授权适用自动许可等便利措施），光伏 12 项（涵盖多晶硅、硅片、电池制造技术及承载相关技术的关键和核心设备）。该目录目前仍处征求意见阶段，尚未成为正式实施的规则。

telegram · zaihuapd · 10月16日 09:12

**「背景」** 《中国禁止出口限制出口技术目录》是中国管理技术出口的基础清单，被列入的技术出口需经许可。此次修订仍处于公开征求意见阶段，尚未成为最终生效规则。

**标签**: `#China export controls`, `#artificial intelligence`, `#biotechnology`, `#photovoltaics`, `#trade policy`

---