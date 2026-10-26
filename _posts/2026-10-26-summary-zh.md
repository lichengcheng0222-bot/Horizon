---
layout: default
title: "Horizon Summary: 2026-10-26 (ZH)"
date: 2026-10-26
lang: zh
---

> 从 28 条内容中筛选出 3 条重要资讯。

---

**科技新闻**
1. [Brotli 解码器高危漏洞波及 Python 与 Node.js](#item-tech-news-1) ⭐️ 8.0/10
2. [苹果据报周三发布首款触屏 MacBook Pro](#item-tech-news-2) ⭐️ 7.0/10

**财经新闻**
1. [2025 年全国总人口减少 339 万](#item-finance-news-1) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Brotli 解码器高危漏洞波及 Python 与 Node.js](https://www.aikido.dev/blog/python-packages-vulnerable-node2shell-brotli-cve-2026-111497) ⭐️ 8.0/10

谷歌 Brotli 解码器的漏洞 CVE-2026-111497 影响 1.0.3 至 1.2.0 版本，CVSS 4.0 评分为 9.2，Python 和 Node.js 的相关 HTTP 组件均在受影响范围内。远程未认证攻击者可发送特制压缩流，造成内存损坏、敏感数据泄露或进程崩溃，并可能执行任意代码。Python 的 Brotli 应升级至 1.2.1，brotlicffi 应升级至 1.2.1.0；Node.js 的修复版本为 22.23.4、24.22.1 和 26.12.1。该漏洞最初以 Node2Shell 披露、后称 HTTP2Shell，据来源文章，OpenAI 表示该问题于 2 月被发现。

telegram · zaihuapd · 10月25日 02:42

**「背景」** Brotli 是 HTTP 常用的压缩内容编码；当程序解码来自网络的压缩流时，如果没有检查解码函数的返回值，畸形的输入就可能进入越界写路径。该 CVE 记录同时列出“未检查返回值”（CWE-252）和“越界写”（CWE-787）。这个漏洞早期因为首先影响 Node.js 而被称为 Node2Shell，后来随着 Python、Bun 和 Envoy 等组件也被确认受影响，又被改称为 HTTP2Shell。

**「影响」** 运行受影响 Python 包或 Node.js 版本、并处理来自不可信来源的 Brotli 数据的服务应立即升级到上述修复版本。在完成升级前，这类服务仍可能因恶意压缩流而面临内存破坏、数据泄露或代码执行风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.aikido.dev/blog/python-packages-vulnerable-node2shell-brotli-cve-2026-111497">Node 2Shell Brotli vuln ( CVE - 2026 - 111497 ) evolves to HTTP2Shell, as...</a></li>
<li><a href="https://defend.network/briefings/brotli-rce-microsoft-patches-shinyhunters-arrest-2026-10-25.html">Brotli RCE spans Node . js , Python , Bun</a></li>

</ul>
</details>

**标签**: `#security vulnerability`, `#Brotli`, `#Python`, `#Node.js`, `#CVE`

---

<a id="item-tech-news-2"></a>
### [苹果据报周三发布首款触屏 MacBook Pro](https://www.bloomberg.com/news/newsletters/2026-10-25/apple-to-unveil-touch-screen-macbook-pro-executive-promotions-in-box-checker) ⭐️ 7.0/10

据一则 Telegram 帖子援引 Bloomberg 报道，苹果计划于本周三推出首款触屏 MacBook Pro，这将是 Mac 首次支持触控并采用 OLED 屏幕，同时加入灵动岛，提供 14 英寸和 16 英寸两种版本。帖子称其售价比现款 2499 美元的起售价更高，但相关发布计划尚未获独立证实。帖子还提到，苹果高管此前多年以人体工学为由反对触屏笔记本，此次转变被描述为更侧重营收与营销，触控则定位为键盘和触控板的补充。

telegram · zaihuapd · 10月25日 14:25

**「背景」** 多年来苹果高管一直以人体工学为由公开否定触屏笔记本，Mac 产品线此前也从未提供触摸屏，因此这次传闻中的发布被视为苹果立场的一次反转。该报道本身也把这一转变描述为更偏向营收与营销的考量，并称触控将作为键盘和触控板的补充而非替代。

**「影响」** 若报道准确，考虑升级的 Mac 用户将面对高于现款 2499 美元起售价的门槛，而触控只是键盘和触控板的补充，原有输入方式仍会保留。

**标签**: `#Apple`, `#MacBook Pro`, `#touchscreen`, `#OLED`, `#hardware`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [2025 年全国总人口减少 339 万](https://weibo.com/1796087453/5357878513767954) ⭐️ 7.0/10

据《中国统计年鉴 2026》数据，2025 年末全国总人口为 140489 万人，比 2024 年末减少 339 万人；全年出生 792 万人，自然增长率为-2.41‰。

telegram · zaihuapd · 10月25日 12:02

**「背景」** 据腾讯新闻 2026 年报道，中国总人口已连续四年负增长，因此此次减少是延续性趋势，而非首次下降。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.qq.com/rain/a/20260223A00L5H00">中 国 人 口 形势报告2026：鼓励 生 育_腾讯新闻</a></li>

</ul>
</details>

**标签**: `#China demographics`, `#population decline`, `#birth rate`, `#macroeconomic trends`, `#official statistics`

---