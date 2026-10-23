---
layout: default
title: "Horizon Summary: 2026-10-23 (ZH)"
date: 2026-10-23
lang: zh
---

> 从 43 条内容中筛选出 18 条重要资讯。

---

**科技新闻**
1. [Quad9 因 DNS 封锁纠纷将退出法国](#item-tech-news-1) ⭐️ 8.0/10
2. [Switch 2 越狱博文称实现解密文件系统读写](#item-tech-news-2) ⭐️ 8.0/10
3. [澳洲法院裁定苹果须开放 iPhone 第三方应用商店](#item-tech-news-3) ⭐️ 8.0/10
4. [NVIDIA OpenShell：面向自主 AI 智能体的沙箱运行时](#item-tech-news-4) ⭐️ 7.0/10
5. [GNU Taler 筹备在德国开展实际运营](#item-tech-news-5) ⭐️ 7.0/10
6. [研究项目借 QEMU 与部分小米机型启动 iOS 16.5 固件](#item-tech-news-6) ⭐️ 7.0/10
7. [eMudhra 宣布退出全球 SSL/TLS 证书业务](#item-tech-news-7) ⭐️ 7.0/10
8. [号称快于 Earcut：489 毫秒处理 370 万地图多边形](#item-tech-news-8) ⭐️ 7.0/10
9. [Anthropic 将 Agent Skills 标准捐赠给 Agentic AI 基金会](#item-tech-news-9) ⭐️ 7.0/10
10. [Carbon-X 开源 14.8B DNA-文本联合模型](#item-tech-news-10) ⭐️ 7.0/10
11. [WhissleAI 发布 11.84 MB 边缘版 SteerTTS，WER 不变](#item-tech-news-11) ⭐️ 7.0/10
12. [研究：部分智能电视关闭 ACR 后仍上报观看数据](#item-tech-news-12) ⭐️ 7.0/10
13. [米哈游与清华开源 GameScaling 键鼠操作模型](#item-tech-news-13) ⭐️ 7.0/10
14. [甲骨文就 JSSE 漏洞 CVE-2026-91403 发布高危警报](#item-tech-news-14) ⭐️ 7.0/10
15. [333 个 Tor 出口中继因 Ebury 后门下线](#item-tech-news-15) ⭐️ 7.0/10
16. [据报禁运 Nvidia B300 服务器进入中国移动数据中心](#item-tech-news-16) ⭐️ 7.0/10

**科技博客**
1. [软件性能取决于设计，而非语言](#item-tech-blog-1) ⭐️ 7.0/10

**财经新闻**
1. [沪深 300 较 6 月高点回落 20%，A 股逼近熊市](#item-finance-news-1) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Quad9 因 DNS 封锁纠纷将退出法国](https://quad9.net/news/blog/au-revoir-france/) ⭐️ 8.0/10

Quad9 计划退出法国。其 CTO 在讨论中表示，公司很可能在 11 月 24 日之后用 geoIP 过滤阻止法国用户访问服务。此事发生在一场围绕 DNS 封锁的诉讼之后：评论中引述的案情称，原告 Sony Music Entertainment GmbH 用 VPN 从德国访问被封锁内容，法院据此认定 Quad9 未遵守命令并判其藐视法庭罚款。CTO 同时承认，geoIP 封锁无法对特定域名做选择性拒绝解析，且上述时间与执行方式仍是“很可能”的计划，而非已完成的退出。

hackernews · farrokhi · 10月22日 14:32 · [社区讨论](https://news.ycombinator.com/item?id=50195959)

**「背景」** Quad9 是一家总部位于瑞士的非营利公共 DNS 解析器，主打隐私保护。法国法院此前命令其封锁 58 个域名，否则面临 58 万欧元罚款；在 Quad9 采用 geoIP 方式限制后，原告索尼音乐从德国通过 VPN 绕过限制，法院据此认定其未遵守命令并处以藐视法庭罚款。

**「对法国用户与解析器运营者的影响」** Quad9 首席技术官在讨论中表示，公司很可能在 11 月 24 日之后启用 geoIP 过滤，阻止法国用户使用其服务，这意味着法国境内的个人和企业用户需在此之前改用其他解析器，否则相关域名解析可能中断。该表态同时说明，geoIP 封锁无法精确到个别域名，运营者被迫在“按法院要求屏蔽特定名称”与“继续为整个国家提供服务”之间做取舍，其他公共解析器面临类似的合规边界问题。

**「社区讨论」** 讨论的核心争议是责任归属：有评论者认为，原告用 VPN 绕过 geoIP 封锁后，法院却因 Quad9 未阻止访问而判其藐视法庭，等于惩罚无法控制用户行为的解析器；也有人用“电话簿是否应为罪犯号码负责”作类比。Quad9 的 CTO 回应称，geoIP 过滤无法实现对特定域名的选择性拒绝解析，因此把讨论集中在“如何封锁法国用户”上并非重点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=50195959">Quad 9 ( DNS Resolver) to Exit France | Hacker News</a></li>
<li><a href="https://reclaimthenet.org/quad9-considers-leaving-france-over-website-blocking-order">French court asks Quad 9 to block 58 domains or face a €580,000 fine .</a></li>

</ul>
</details>

**标签**: `#DNS`, `#internet governance`, `#privacy`, `#geo-blocking`, `#legal liability`

---

<a id="item-tech-news-2"></a>
### [Switch 2 越狱博文称实现解密文件系统读写](https://pepsipu.com/blog/2026-10-switch2-jailbreak-ns2jb/) ⭐️ 8.0/10

一篇技术博文描述了针对 Nintendo Switch 2 的越狱，核心内容包括解密后的文件系统读写、游戏转储，以及用 LLM 驱动的 KVM 自动化操作主机。相关说法来自该博文和讨论，尚未在提供的材料中获得独立验证。若属实，影响将集中在主机改装、游戏转储与逆向工程社区。

hackernews · ledoge · 10月22日 08:01 · [社区讨论](https://news.ycombinator.com/item?id=50192536)

**「背景：什么是 ns2jb」** ns2jb 被作者描述为一种“纯软件、需重新注入”（tethered）的越狱：它不依赖硬件 modchip，但主机重启后必须重新触发漏洞，并非一次性永久破解。其能力落点是以普通 sysmodule 乃至内置 fs 文件系统模块的身份运行任意原生代码——GBAtemp 与 Notebookcheck 均据此称，若属实，这将是 Switch 2 上首个纯软件越狱，并声称适用于最新的 23.0.1 固件（上述说法来自作者与转述媒体，尚待独立验证）。正因触及文件系统层，社区讨论才立刻转向游戏转储与在非原厂硬件上运行独占作品的可能性。

**「实际影响」** 若博客所称的解密文件系统读写权限属实，最直接的影响是游戏转储与逆向工程的门槛被大幅降低：评论者 hturan 预计转储文件可能很快出现，并经由 recomp/decomp 让主机独占作品在非 Switch 2 硬件上运行，这被视为对任天堂最不利的情形——但该权限本身尚未获独立验证。另一可复用的结果是，JetKVM 通过 USB 注入手柄输入、HDMI 采集画面，再配合 SwitchBot Bot 按压电源键重启崩溃主机，形成了一套可自动循环的硬件测试流程，可供其他安全研究者借鉴。

**「社区讨论」** 评论者将“解密文件系统读写”视为尚未证实但影响最大的部分：hturan 认为若属实则可能出现 Switch 2 游戏转储，并让独占作品运行在任意硬件上；valgaze 则补充了用 JetKVM 经 USB 发送手柄输入、经 HDMI 获取画面，并用蓝牙开关按压电源键的自动化细节。rootsudo 质疑 Codex 在安全研究中的可用性限制，KeplerBoy 更看重 KVM、USB 手柄支持和蓝牙机械装置等现代工具带来的自动化能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pepsipu.com/blog/2026-10-switch2-jailbreak-ns2jb/">pepsipu .com/blog/2026-10- switch 2 - jailbreak - ns 2 jb</a></li>
<li><a href="https://gbatemp.net/news/switch-2-jailbreak-ns2jb-released-software-only-exploit-tethered.685698/">Switch 2 jailbreak &quot; ns 2 jb &quot; released. Software-only... | GBAtemp.net</a></li>
<li><a href="https://www.notebookcheck.net/The-Nintendo-Switch-2-has-reportedly-been-jailbroken-through-a-software-only-exploit.1431060.0.html">The Nintendo Switch 2 has reportedly been... - Notebookcheck News</a></li>

</ul>
</details>

**标签**: `#Nintendo Switch 2`, `#console jailbreak`, `#hardware security`, `#reverse engineering`, `#LLM automation`

---

<a id="item-tech-news-3"></a>
### [澳洲法院裁定苹果须开放 iPhone 第三方应用商店](https://9to5mac.com/2026/10/21/apple-must-open-iphone-to-alternative-app-stores-in-australia-after-epic-games-ruling/) ⭐️ 8.0/10

澳大利亚联邦法院在 Epic 反垄断诉讼中裁定，苹果须自 2027 年 3 月 1 日起允许澳区 iPhone 用户通过第三方应用商店和网站安装应用，并开放替代支付方式及外部支付链接。Fortnite 将立即重返澳区 App Store。法院认定苹果在 iOS 应用分发和支付市场具有实质性市场力量，相关限制违反澳大利亚竞争法。苹果表示将上诉并申请暂缓执行。

telegram · zaihuapd · 10月22日 06:54

**「背景」** 这起诉讼源自 Epic Games 对苹果提起的反垄断诉讼，核心争议是苹果是否利用对 iOS 应用分发和应用内支付的控制权限制竞争。澳大利亚联邦法院采纳了 Epic 的主张，认定苹果在相关市场具有实质性市场力量，其限制措施违反澳大利亚竞争法；苹果已表示将上诉并申请暂缓执行，因此该裁决尚未最终生效。

**「影响」** 对澳区开发者和用户而言，裁决生效后应用分发和支付渠道将不再局限于 App Store 与苹果内购；但苹果已表示上诉并申请暂缓执行，因此 2027 年 3 月 1 日的生效时间表仍可能变化。

**标签**: `#Apple`, `#反垄断`, `#应用商店`, `#Epic Games`, `#监管`

---

<a id="item-tech-news-4"></a>
### [NVIDIA OpenShell：面向自主 AI 智能体的沙箱运行时](https://github.com/NVIDIA/OpenShell) ⭐️ 7.0/10

NVIDIA 在 GitHub 上提供了 OpenShell，一个面向成批自主 AI 智能体的沙箱运行时。它旨在让智能体在读文件、安装软件包、调用 API 和使用凭据时，仍受文件、密钥和网络访问限制。所给材料未给出支持平台、版本号或独立安全测试结果，因此这些隔离效果仍属项目方描述。

hackernews · niemandhier · 10月22日 17:44 · [社区讨论](https://news.ycombinator.com/item?id=50198675)

**「背景」** 自主智能体通常需要读写文件、安装依赖、调用 API 并使用凭据；如果直接以用户权限运行，一次误操作或越权行为就可能触及宿主机上的数据与网络。沙箱与容器隔离因此成为前提：通过文件系统挂载、进程隔离和网络策略，把代理的能力限制在可控边界内；OpenShell 正是把这类隔离与访问控制封装成运行时。

**「影响」** 对要让智能体处理私有代码或生产凭据的团队，OpenShell 把文件、密钥和网络权限作为运行时配置来管理；采用前仍应针对出站流量和凭据使用做实际测试。

**「社区讨论」** 评论者报告了两种实践：有人已在 OpenShell 上叠加团队策略、安全 Git 使用和 SCA/SAST，也有人用其他代理按域名限制网络。争论焦点是安全承诺的边界：有评论认为，将网络限制到可信域名仍无法阻止代码库等数据外泄，而“更多能力不等于更多访问”的说法被质疑为过度承诺。

**标签**: `#AI agents`, `#security`, `#sandboxing`, `#runtime`, `#open source`

---

<a id="item-tech-news-5"></a>
### [GNU Taler 筹备在德国开展实际运营](https://www.taler.net/en/news/2026-13.html) ⭐️ 7.0/10

GNU Taler 项目发布公告，表示正在为在德国开展实际运营做准备，但所提供的材料中没有给出上线时间、合作机构或牌照进展等具体细节，因此目前可确认的是筹备状态，而非已经投入运行的支付服务。讨论中引用 Taler 官方 FAQ 指出，其电子现金带有有效期：钱包应在到期前一个月自动把即将失效的数字现金兑换为延长有效期的现金，若钱包离线过久未联网，相关代币会失效。评论者还提到 GLS 银行与 Taler 存在关联，并把该项目的意义放在欧洲减少对美国支付体系依赖的背景下讨论。

hackernews · dewey · 10月22日 16:14 · [社区讨论](https://news.ycombinator.com/item?id=50197404)

**「背景」** GNU Taler 是一个基于自由软件的电子支付系统；公开资料介绍，它与多数加密支付项目不同，不采用区块链。其官网此前还列出了 2026 年 5 月与 be-BOP 的新集成，以及 2026 年 6 月关于数字欧元保密性的文章，显示该项目在筹备德国运营期间也在推进商户集成并参与欧洲数字欧元讨论。

**「社区讨论」** 部分评论者认为，必须联网且离线过久会失效的机制使其在体验上不如比特币，另有人质疑：只要资金最终来自银行转账等留有痕迹的渠道，所谓买方隐私就难以成立，并预计 KYC 要求会在关键环节削弱隐私保护。也有支持者对此表示欢迎，一位自称 GLS 银行客户的评论者提到该行的参与，希望欧洲借此降低对美国支付公司的依赖与对外制裁风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.taler.net/">GNU Taler : Home</a></li>
<li><a href="https://www.wikiwand.com/en/GNU_Taler">GNU Taler - Wikiwand</a></li>

</ul>
</details>

**标签**: `#GNU Taler`, `#digital payments`, `#privacy`, `#open source`, `#EU regulation`

---

<a id="item-tech-news-6"></a>
### [研究项目借 QEMU 与部分小米机型启动 iOS 16.5 固件](https://github.com/oosexgang/hackios-xnu-kernel) ⭐️ 7.0/10

一个名为 hackios-xnu-kernel 的研究项目演示了通过 QEMU 以及部分 Android 真机启动 iOS 16.5 / XNU 固件，真机范围包括 POCO X5 Pro 5G 和部分小米设备。据评论中引述的项目说明，它是研究用的实验台而非可用 ROM：一次会话只持续设定的秒数，随后内核返回 loader 并交出日志。因此「在 Android 上跑完整 iOS」的说法更像是标题层面的概括，而非可供日常使用的系统移植。

hackernews · aghuang · 10月22日 15:26 · [社区讨论](https://news.ycombinator.com/item?id=50196718)

**「背景」** XNU 是苹果开源的底层内核，iOS 16.5 对应的版本为 xnu-8796.121.2；但 iOS 的用户空间组件和许多硬件驱动并不开源。据项目仓库说明，HackiOS 通过自制的 EFI 加载器、闭源驱动的替代实现、UEFI 移植以及兼容层上的 Linux Wi-Fi 驱动，让这一内核与未修改的 iOS 16.5 用户空间（launchd、backboardd、SpringBoard 及应用）一同启动，目前已可在 QEMU 和部分骁龙 Android 手机上运行。

**「实际影响」** 想复现的人需要走 QEMU 路径或持有 POCO X5 Pro 5G、部分受支持的小米机型，其他 Android 设备目前没有对应支持；而会话到时即返回 loader 并输出日志的设计，说明它面向的是内核调试与验证，而不是装机日常使用。

**「社区讨论」** 有评论者引用项目说明强调它是限时的研究实验台、不是 ROM，并猜测这一限制可能与部署时的安全考虑有关。另一位评论者则担心这类项目会让二手市场上「伪装成 iPhone 的安卓机」更难辨别，提醒购买旧款 iPhone 时要多加核实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/oosexgang/hackios-xnu-kernel">GitHub - oosexgang/ hackios -xnu-kernel</a></li>
<li><a href="https://hackiosx.dev/">hackiosx: iOS on Android phones</a></li>

</ul>
</details>

**标签**: `#iOS`, `#Android`, `#XNU kernel`, `#QEMU`, `#systems hacking`

---

<a id="item-tech-news-7"></a>
### [eMudhra 宣布退出全球 SSL/TLS 证书业务](https://emudhra.com/en/press-release/emudhra-to-exit-global-ssl-tls-certificate-business) ⭐️ 7.0/10

eMudhra 公开宣布退出全球 SSL/TLS 证书业务。此举发生在其证书颁发机构（CA）运营受到浏览器根证书计划审查之际；公告将外界关注称为“不成比例”，但现有材料未说明事故根因。对使用其全球 TLS 证书的站点而言，这意味着需要评估迁移到其他 CA 并更新证书与信任配置。

hackernews · bo0tzz · 10月22日 13:33 · [社区讨论](https://news.ycombinator.com/item?id=50195110)

**「背景」** eMudhra 是一家 2008 年成立、总部位于班加罗尔并受印度认证主管机构（Controller of Certifying Authorities）许可的 PKI 公司，长期在印度签发数字签名证书。此次退出的是其全球 SSL/TLS 证书业务；在浏览器根证书计划就疑似 CA 运营失败展开审查的背景下，这一业务与该公司在印度本土的数字签名证书主业并不相同。

**「客户需要迁移证书」** 对使用 eMudhra 全球 SSL/TLS 证书的网站运营方来说，最直接的后果是必须把这些证书更换为由其他 CA 签发的证书，并同步更新服务器证书链和客户端信任配置；否则一旦该 CA 的中间证书被浏览器根计划取消信任，现有部署就可能无法通过验证。这一风险已有具体依据：有研究者称恢复了 eMudhra 8 张中间 CA 证书的私钥，公司董事会则于 10 月 22 日决定退出该业务。

**「社区讨论」** 评论者集中批评 eMudhra 未解释事故如何发生，并以私钥强度极弱等说法质疑其“审视不成比例”的表述；还有人指出，“受影响 CA 未签发终端实体证书”的说法站不住脚，因为该 CA 本身具备签发能力。上述均为评论者观点，公告未提供可独立核实的根因说明。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/EMudhra">eMudhra - Wikipedia</a></li>
<li><a href="https://thehackernews.com/2026/10/emudhra-to-exit-global-ssltls-business.html">eMudhra to Exit Global SSL / TLS Business After 8 Intermediate CA...</a></li>
<li><a href="https://emudhra.com/en/press-release/emudhra-to-exit-global-ssl-tls-certificate-business">eMudhra to Exit global SSL / TLS Certificate Business</a></li>
<li><a href="https://www.moneycontrol.com/technology/emudhra-to-exit-global-website-security-certificate-business-after-key-generation-flaw-article-14057821.html">eMudhra to exit global website security certificate business after...</a></li>

</ul>
</details>

**标签**: `#PKI`, `#TLS certificates`, `#certificate authorities`, `#web security`, `#browser trust stores`

---

<a id="item-tech-news-8"></a>
### [号称快于 Earcut：489 毫秒处理 370 万地图多边形](https://globus.software/blog/2026/10/16/cutting-map-polygons/) ⭐️ 7.0/10

一篇面向地图渲染开发者的博客声称，其三角剖分方法在 489 毫秒内处理了 370 万个地图多边形，速度超过 Earcut。Earcut 作者在 Hacker News 讨论中回应称，Earcut 为控制包体积刻意放弃了部分优化，最小化并 gzip 后为 4.1 KB，并询问该方法的 WASM 构建有多大。

hackernews · molind · 10月22日 09:31 · [社区讨论](https://news.ycombinator.com/item?id=50193170)

**「背景：三角化与耳切法」** 地图渲染要把多边形拆成三角形才能交给 GPU，Earcut 是 Mapbox GL JS 等库长期采用的 JavaScript 三角化实现，其名字来自基于 Meisters 双耳定理的“耳切法”（ear clipping）。耳切法要求输入为简单多边形，而该文指出地图数据会被取整到瓦片网格，取整可能破坏简单性，使“找不到耳朵”成为需要专门处理的情形。作者以此为基础给出了自己的三角化方案，并称在同一批多边形上耗时 489 ms，比 Delaunay 基线少 6.0 倍。

**「影响」** 对考虑用该方法替换 Earcut 的地图开发者，Earcut 作者指出其 4.1 KB 的压缩体积来自为控制包体积而做的取舍；选型时因此还需确认该方案的 WASM 构建大小，而不能只比较 489 毫秒的剖分耗时。

**「社区讨论」** 评论中的主要分歧在算法选择：有人质疑为何耳切法加优化长期胜过 Seidel 梯形法，并称后者复杂度接近线性；也有人担心结果中的细长三角形会不利于 GPU 光栅化。Delaunay32 作者称其分治式约束 Delaunay 实现尚未在该数据集上做基准测试，且当前 API 要求简单环和不接触的孔洞。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://globus.software/blog/2026/10/16/cutting-map-polygons/">Faster than earcut : triangulating 3 . 7 M map polygons in 489 ms</a></li>

</ul>
</details>

**标签**: `#computational geometry`, `#triangulation`, `#performance optimization`, `#WebAssembly`, `#geospatial`

---

<a id="item-tech-news-9"></a>
### [Anthropic 将 Agent Skills 标准捐赠给 Agentic AI 基金会](https://simonwillison.net/2026/Oct/22/donating-agent-skills/) ⭐️ 7.0/10

Anthropic 宣布把 Agent Skills 标准捐赠给 Linux 基金会下属的 Agentic AI Foundation（AAIF），并表示目的是让该标准保持开放、社区驱动和厂商中立。AAIF 由 Anthropic 与 Block、OpenAI 于去年共同创立，Anthropic 此前已向该基金会捐赠 Model Context Protocol（MCP）规范。这是一项公告，源报道未披露移交时间表、治理章程，也没有第三方独立验证。

rss · Simon Willison · 10月22日 18:09

**「背景」** Agent Skills 在被捐赠前已由 Anthropic 作为“开放标准”提出；此次捐赠把该规范的管理权移交给中立的基金会。AAIF 由 Anthropic 与 Block、OpenAI 共同创立，且此前已接收 Anthropic 捐赠的 Model Context Protocol（MCP），因此这次安排延续了同一套开放治理路径。

**「影响」** 对采用 Agent Skills 的开发者而言，Anthropic 声称的目标是让标准保持厂商中立，也就是未来规范变更可能由基金会而非单一厂商主导。但源报道没有给出移交时间表、提案与表决流程，也没有说明新旧版本兼容规则，所以实际影响仍取决于后续章程细则。

**标签**: `#agentic AI`, `#Agent Skills`, `#open standards`, `#AI governance`, `#Anthropic`

---

<a id="item-tech-news-10"></a>
### [Carbon-X 开源 14.8B DNA-文本联合模型](https://www.reddit.com/r/MachineLearning/comments/1xchayq/carbonx_is_an_open_148b_model_trained_jointly_on/) ⭐️ 7.0/10

Carbon-X 是一个采用 Apache 2.0 许可证的 14.8B 参数解码器模型，可直接在普通对话中接收原始 DNA 并用英文回答；文本与 DNA 共用一条 token 流，DNA 使用 6-mer token，并在 302B token 上进行了中期训练。据其 Hugging Face 模型卡，在关闭 thinking 时，该模型在五项 DNA 基准上的平均得分为 66.7%，低于 GPT-6.1 Sol 的 67.5%；这些基准结果尚未得到独立验证。模型权重以 bfloat16 可装入单张 80 GB GPU，但模型卡明确说明它未经临床验证，精确序列操作仍应交由代码处理。

reddit · r/MachineLearning · /u/jatingargiitk · 10月22日 12:32

**「背景」** Carbon-X 延续了 Hugging Face Bio 的 Carbon 系列：该系列此前已有 3B 和 8B 版本；根据 Carbon-X 模型卡，它从 Qwen3-14B 继续训练，并在五项 DNA 基准上比该基座模型平均高 27 个百分点。

**「影响」** 对处理敏感基因组数据的团队，Apache 2.0 权重和单张 80 GB GPU 的部署需求使本地运行更可行；但临床用途仍受未经验证的限制，且精确序列操作需交给代码，不能把对话输出当作序列编辑工具。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/HuggingFaceBio/Carbon-X">HuggingFaceBio / Carbon - X · Hugging Face</a></li>
<li><a href="https://github.com/huggingface/carbon">GitHub - huggingface/ carbon : The home of Carbon Genomic...</a></li>

</ul>
</details>

**标签**: `#DNA language models`, `#open weights`, `#multimodal models`, `#bioinformatics`, `#model evaluation`

---

<a id="item-tech-news-11"></a>
### [WhissleAI 发布 11.84 MB 边缘版 SteerTTS，WER 不变](https://www.reddit.com/r/MachineLearning/comments/1xcum4s/we_shrank_our_steerable_small_tts_to_1184_mb_wer/) ⭐️ 7.0/10

WhissleAI 发布 SteerTTS 的边缘变体 steer-tts-edge，应用需随包发布的全部内容（权重、音色、文本前端和 Python 运行时）合计 11.84 MB，仍支持用数字参数控制语音风格。做法上，9.25M 参数、attention 加双向 Mamba-3 的声学模型与 6.2M 参数的 Vocos 类声码器（从 charactr/vocos-mel-24khz 蒸馏而来）均做了 int4 量化感知训练，文本前端改为纯 numpy 实现，运行时不再依赖 NLTK、g2p\_en、torchaudio 或 num2words。作者按 Open TTS Leaderboard 协议本地评测（并非官方提交），fp32 版与 edge 版 Seed-TTS WER 均为 0.96%，UTMOS 由 4.20 降至 4.11；作者称降幅几乎全部来自小型 int4 声码器，12 项控制参数各自保留至少 95% 的 fp32 效果。限制包括仅支持英文、内置 200 个音色（完整模型为 2825 个）、设备端不含语音克隆、自由文本提示和 flow refiner，且权重在加载时反量化为 fp32，因此收益体现在体积而非速度。

reddit · r/MachineLearning · /u/Working\_Hat5120 · 10月22日 20:57

**「背景」** SteerTTS v1 是作者此前发布的小型英文 TTS，可用数字参数控制语速、音高、停顿等风格；本次边缘版是在该模型基础上的端侧压缩版本。其关键前提是 int4 量化感知训练：在训练时模拟低精度舍入，以减少把声学模型和声码器压到 4 位后带来的质量损失；文本前端则改为纯 numpy，以避免运行时依赖 NLTK、g2p\_en、torchaudio 或 num2words。

**「影响」** 对希望在设备端本地合成语音的开发者，作者在仅有 CPU 的 2018 款 Threadripper（带负载）上测得 4 线程 RTF 0.053（约 19 倍实时）、首段音频约 120 ms，并支持句级流式输出；但由于加载时反量化为 fp32，内存和算力占用不会随之下降，要获得速度收益需为边缘设备另写算子。作者公开征求对声码器质量差距以及 ONNX、移动端、WASM 等边缘目标的反馈。

**标签**: `#text-to-speech`, `#quantization-aware training`, `#int4`, `#edge ML`, `#speech synthesis`

---

<a id="item-tech-news-12"></a>
### [研究：部分智能电视关闭 ACR 后仍上报观看数据](https://watchingthewatchers.github.io/watchingthewatchers/index.html) ⭐️ 7.0/10

一项针对美国智能电视自动内容识别（ACR）的研究测试了 10 家厂商的共 12 台电视，完成 5943 次受控实验，发现部分机型即便在设置中关闭 ACR，仍会继续发送与所看内容相关的流量。研究还指出，两家平台以未加密形式外传观看内容：VIDAA OS 通过 MQTT 明文发送数据，其中包含无法重置的设备 ID 和音频指纹；Vizio 的 WatchFree+ 则把节目名称写入未加密的域名查询，且用户无法关闭。该研究由 Watching the Watchers 发布，结论来自受控实验测量，而非厂商声明。

telegram · zaihuapd · 10月22日 09:50

**「背景」** ACR（自动内容识别）通过音频或画面指纹判断电视正在播放什么，厂商将其作为内容识别和观看统计的数据来源；用户在设置中关闭 ACR，通常预期相关采集与上报也会停止。MQTT 是物联网设备常用的轻量消息协议，DNS 查询则用于把域名解析为 IP 地址；这两类流量若未加密，网络观察者可能看出设备正在传输或访问什么。

**「对用户的实际影响」** 对用户来说，设置里的 ACR 开关目前不能当作有效的退出机制：据 Ars Technica 报道，Samsung、Vizio 和 Roku 的电视在用户选择退出后仍向 ACR 端点发送数据，而研究本身显示，VIDAA OS 通过明文 MQTT 发送不可重置的设备 ID 与音频指纹，Vizio 的 WatchFree+ 则把节目名写入用户无法关闭的未加密 DNS/SNI 查询。用户和负责管理物联网设备的人因此需要把控制点移到网络层，例如在路由器或 DNS 层面屏蔽相关 ACR 域名、对电视单独隔离网段，但这些措施只能减少特定上报通道，无法改变设备端明文传输和不可重置标识符带来的暴露风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arstechnica.com/gadgets/2026/10/does-opting-out-of-smart-tv-tracking-work-research-finds-suspicious-traffic/">Does opting out of smart TV tracking work? Research... - Ars Technica</a></li>
<li><a href="https://watchingthewatchers.github.io/watchingthewatchers/index.html">Watching the Watchers : Privacy Analysis of U.S. Smart TV Automatic...</a></li>

</ul>
</details>

**标签**: `#smart TVs`, `#privacy`, `#ACR`, `#IoT security`, `#data exposure`

---

<a id="item-tech-news-13"></a>
### [米哈游与清华开源 GameScaling 键鼠操作模型](https://arxiv.org/abs/2610.28698v1) ⭐️ 7.0/10

米哈游崩坏 AI 团队联合清华大学等发布 GameScaling，这是一个基于 Qwen3.5 视觉语言模型、面向键盘鼠标操作继续预训练的模型系列，参数规模覆盖 0.8B 至 27B。模型每次输出未来 200 毫秒的键鼠动作，论文用 120 组训练配置考察数据量、数据多样性与模型规模的影响。八个检查点与推理客户端已按 Apache-2.0 开源，但训练代码未一并发布。论文报告称，数据越多，同源表现越好；多样性有助于迁移到相近游戏，但对差异较大的游戏提升有限。

telegram · zaihuapd · 10月22日 11:32

**「背景」** GameScaling 属于游戏智能体方向：把视觉语言模型直接当作策略网络，根据屏幕画面预测键盘和鼠标动作。它没有从零训练，而是在 Qwen3.5 视觉语言模型骨干上做面向键鼠操作的继续预训练。项目页显示，评估时以未训练的 Qwen3.5 骨干为对照基线，用 150 次 rollout 的累计成功率随最大允许步数变化的关系，来考察测试时扩展效果。

**「影响」** 开发者现在可以直接获取八个检查点和推理客户端，在自有游戏中做推理评测或集成；但训练代码缺失，意味着无法复现论文的 120 组训练配置。论文所称的跨游戏迁移收益主要限于相近游戏，面向差异较大的游戏仍需自行验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://gamescaling.github.io/">Scaling in Games : Continued Pre-Training for Embodied Agents in...</a></li>

</ul>
</details>

**标签**: `#game AI`, `#vision-language models`, `#open-source models`, `#model scaling`, `#keyboard/mouse control`

---

<a id="item-tech-news-14"></a>
### [甲骨文就 JSSE 漏洞 CVE-2026-91403 发布高危警报](https://www.oracle.com/security-alerts/alert-cve-2026-91403.html) ⭐️ 7.0/10

甲骨文发布安全警报称，Java SE 的 JSSE 组件存在编号 CVE-2026-91403 的高危漏洞，CVSS 评分为 9.1，攻击者无需身份验证即可通过网络远程利用，可能严重破坏数据的机密性与完整性。受影响版本包括 Java SE 8u511、11.0.33、17.0.21、21.0.13、25.0.5、27.0.1 以及 GraalVM 的多个版本。甲骨文表示已提供修复补丁，并呼吁用户尽快升级至受支持版本。该警报未披露漏洞利用细节或是否已有在野攻击。

telegram · zaihuapd · 10月22日 12:30

**「背景」** JSSE（Java Secure Socket Extension）是 Java 平台中负责实现 SSL/TLS 加密通信的标准组件，Java 应用进行 HTTPS 等加密网络连接时通常依赖它。由于该组件被广泛内置于 Java SE 及 GraalVM 运行时中，其缺陷往往会影响大量未经改动的现有应用，而非仅限于显式调用该库的代码。

**「影响与处置」** 运行受影响 Java SE 8u511、11.0.33、17.0.21、21.0.13、25.0.5、27.0.1 或相关 GraalVM 版本的用户，面临 JSSE 漏洞被未认证远程利用、进而危及数据机密性与完整性的风险；甲骨文已提供补丁，应尽快升级到受支持版本，尤其是对外提供网络服务的 Java 应用。

**标签**: `#Java SE`, `#security vulnerability`, `#Oracle`, `#JSSE`, `#patching`

---

<a id="item-tech-news-15"></a>
### [333 个 Tor 出口中继因 Ebury 后门下线](https://kaba.cx/posts/20261020_Tor/) ⭐️ 7.0/10

一名 Tor 运营者用脚本扫描约 3000 个出口中继后发现，其中 333 个（约 10%）被植入 Ebury 后门；这些节点可将 22 端口的 SSH 连接劫持到 12 台拦截服务器并窃取凭据。10 月 4 日，这些节点被标记为 BadExit，次日全部下线。攻击者据称今年 8 月已入侵这些服务器，并屏蔽部分端口以收集未加密邮件流量，但入侵途径尚无定论。

telegram · zaihuapd · 10月22日 14:52

**「背景」** Tor 出口中继是用户流量离开 Tor 网络的最后一跳，因此运营者能够观察并篡改未加密流量；被标记为 BadExit 的中继会被客户端排除在出口路径之外。根据 KABA 的记录，这批节点在 10 月 2 日开始协同拦截 SSH 连接，Tor Project 随后于 10 月 4 日对其施加 BadExit 与 MiddleOnly 标记，到 10 月 5 日恶意配置节点已从 Tor Consensus 中消失。

**「影响」** 经由这些节点建立 SSH 连接或传输未加密邮件的用户，应把相关凭据视为可能已泄露，更换密码和密钥并检查异常登录记录；仅凭 Tor 出口节点是否在线，无法判断历史连接是否曾经过被控节点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://kaba.cx/posts/20261020_Tor/">How I got over 300 Tor exit nodes removed - KABA</a></li>
<li><a href="https://xakep.ru/2026/10/22/tor-exit-attack/">Хакеры захватили более 300 выходных узлов Tor ради перехвата...</a></li>

</ul>
</details>

**标签**: `#Tor`, `#cybersecurity`, `#backdoor`, `#Ebury`, `#SSH`

---

<a id="item-tech-news-16"></a>
### [据报禁运 Nvidia B300 服务器进入中国移动数据中心](https://theinference.org/article/china-s-state-money-bought-banned-nvidia-b300-servers-then-redacted-the-receipts) ⭐️ 7.0/10

据 The Inference 报道，一家中国国资控股的半导体租赁集团为荣耀视图科技融资，购入 32 台搭载禁运 Nvidia B300 芯片的华硕服务器，作为总额逾 30 亿元、700 余台服务器交易的一部分，计划部署在中国移动宁夏枢纽。B300 处于美国最严格出口管制层级，基本禁止对华出口。相关备案引发关注后，该租赁集团重新提交文件并抹去硬件描述；Nvidia 表示正与代工伙伴调查，华硕称遵守出口管制。

telegram · zaihuapd · 10月22日 15:22

**「背景」** 美国对先进 AI 芯片实施分层出口管制，B300 属于其中最严格的管控层级，对华基本处于禁运状态。因此，这类芯片一旦出现在中国国有网络中，就会直接引发出口合规审查。

**标签**: `#Nvidia B300`, `#export controls`, `#China`, `#AI hardware`, `#semiconductor supply chain`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [软件性能取决于设计，而非语言](https://seangoedecke.com/software-is-slow-because-of-bad-design-not-slow-languages/) ⭐️ 7.0/10

rss · Sean Goedecke · 10月23日 00:00

**「背景」** 面对“用 AI 把程序改写成 C、Rust 或汇编就能大幅提速”的说法，作者认为大多数程序并不会因换语言而显著变快，语言本身的执行速度通常不是性能瓶颈的主因。

**「方案」** 作者指出，真实程序大多受 I/O 限制。以一个带数据库的 CRUD 网站为例，若一次请求约 50% 的时间花在查询数据库上，改用 C 重写也只能优化剩下的一半，理论上最多快 2 倍，实践中往往只有约 1.5 倍，这正是 Amdahl 定律的含义。即使是明显的 CPU 密集型任务，慢语言也常通过库把工作交给快语言：Markdown 渲染可调用 cmark-gfm，Python 的机器学习依赖底层 C 或汇编实现矩阵运算，因此重写未必有用。真正有效的提速通常来自重新设计以减少工作量，例如缓存慢操作、把任务移到后台异步执行、并行化、合并 SQL 查询以消除 N+1、优化慢查询，以及跳过不必要的操作；这些都与语言速度无关。作者还引用 Bryan Cantrill 的经历：把精心优化的 C 程序按朴素方式改写成 Rust，结果反而快 30%，原因之一是 Rust 默认使用更缓存友好的 B 树，说明即便在 CPU 密集型场景，设计仍可能压过语言差异。高层语言反而让 N+1 查询或可移出请求链路的调用更易被发现，因此作者建议用 AI 做性能剖析、定位热点并重新设计程序；只有遇到确实无法重构、真正受 CPU 限制的少数热点，才值得把那一部分改写成更快的语言。

**「启示」** 作者的核心结论是：原始速度主要来自减少工作量和改善 I/O 与数据访问的设计，而不是把整个程序换成更快的语言；语言重写应服务于可移植性、可维护性等目标，或只用于极其狭窄的性能热点。

**标签**: `#software performance`, `#optimization`, `#I/O-bound systems`, `#language choice`, `#profiling`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [沪深 300 较 6 月高点回落 20%，A 股逼近熊市](https://www.bloomberg.com/news/articles/2026-10-22/china-stocks-set-for-bear-market-as-ai-trade-policy-hopes-fade) ⭐️ 7.0/10

沪深 300 指数周四一度下跌 1.7%，较 6 月高点累计回落 20%，A 股逼近熊市，背景是实质性财政刺激缺位和宁德时代季度利润增速低于预期。策略师称，若无新政策或科技催化，震荡行情可能延续至 2027 年初。

telegram · zaihuapd · 10月22日 05:05

**「背景」** 熊市通常指股指较近期高点下跌 20% 以上，沪深 300 这次正是以 6 月高点为基准累计回落 20%。此前市场期待实质性财政刺激和 AI 相关利好落地，但刺激措施缺位，加上宁德时代等公司季度业绩不及预期，构成这轮抛售的背景。

**标签**: `#China A-shares`, `#CSI 300`, `#bear market`, `#CATL earnings`, `#fiscal stimulus`

---