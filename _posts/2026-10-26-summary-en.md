---
layout: default
title: "Horizon Summary: 2026-10-26 (EN)"
date: 2026-10-26
lang: en
---

> From 28 items, 3 important content pieces were selected

---

**Technology News**
1. [Brotli CVE-2026-111497 spreads to Python and Node.js HTTP components](#item-tech-news-1) ⭐️ 8.0/10
2. [Apple Reportedly to Unveil First Touchscreen MacBook Pro on Wednesday](#item-tech-news-2) ⭐️ 7.0/10

**Financial News**
1. [China’s 2025 Population Falls 3.39 Million to 1.40489 Billion](#item-finance-news-1) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Brotli CVE-2026-111497 spreads to Python and Node.js HTTP components](https://www.aikido.dev/blog/python-packages-vulnerable-node2shell-brotli-cve-2026-111497) ⭐️ 8.0/10

A high-severity flaw in Google&\#x27;s Brotli decoder, tracked as CVE-2026-111497, affects Brotli versions 1.0.3 through 1.2.0 and extends to Python and Node.js HTTP components, according to Aikido Security. The vulnerability carries a CVSS 4.0 score of 9.2 and allows an unauthenticated remote attacker to send a crafted compressed stream that causes memory corruption, leaks sensitive data, crashes the process, or potentially executes arbitrary code. Fixed releases are Brotli 1.2.1 and brotlicffi 1.2.1.0 for Python, and Node.js 22.23.4, 24.22.1, or 26.12.1. The flaw was first disclosed as Node2Shell and later called HTTP2Shell; OpenAI says it discovered the issue in February.

telegram · zaihuapd · Oct 25, 02:42

**「Brotli 解码器缺陷的背景」** Brotli 是许多 HTTP 栈用于压缩响应体的压缩算法，因此客户端和服务器会自动把传入的 \`Content-Encoding: br\` 流交给解码器处理——这意味着攻击者可控的输入无需任何身份验证即可到达存在缺陷的代码。该 CVE 记录把一个未检查的返回值（CWE-252）与一个越界写入（CWE-787）配对，这正是内存破坏类问题出现的原因；Aikido 的博客指出，这个缺陷最初因位于 Node.js 的解码路径中而被称为 Node2Shell，之后又因为相同的解码器代码出现在 Python 包和其他绑定中而获得了 HTTP2Shell 这一名称。

**「Impact」** Teams running affected Python packages should move to Brotli 1.2.1 or brotlicffi 1.2.1.0, while Node.js deployments need version 22.23.4, 24.22.1, or 26.12.1. Because the attack requires no authentication, the vulnerable decoder can be reached through ordinary HTTP traffic, making the listed fixed releases the concrete mitigation the report points to.

<details><summary>References</summary>
<ul>
<li><a href="https://www.aikido.dev/blog/python-packages-vulnerable-node2shell-brotli-cve-2026-111497">Node 2Shell Brotli vuln ( CVE - 2026 - 111497 ) evolves to HTTP2Shell, as...</a></li>
<li><a href="https://defend.network/briefings/brotli-rce-microsoft-patches-shinyhunters-arrest-2026-10-25.html">Brotli RCE spans Node . js , Python , Bun</a></li>

</ul>
</details>

**Tags**: `#security vulnerability`, `#Brotli`, `#Python`, `#Node.js`, `#CVE`

---

<a id="item-tech-news-2"></a>
### [Apple Reportedly to Unveil First Touchscreen MacBook Pro on Wednesday](https://www.bloomberg.com/news/newsletters/2026-10-25/apple-to-unveil-touch-screen-macbook-pro-executive-promotions-in-box-checker) ⭐️ 7.0/10

A Telegram post summarizing a Bloomberg report says Apple will unveil its first touchscreen MacBook Pro on Wednesday, adding touch input and OLED displays to the Mac for the first time along with Dynamic Island. The report describes 14- and 16-inch models priced above the current $2,499 starting point. It says touch will complement the keyboard and trackpad, and it characterizes Apple&\#x27;s reversal as driven more by revenue and marketing than by ergonomics. The claims are reported plans and have not been independently verified.

telegram · zaihuapd · Oct 25, 14:25

**「Apple&\#x27;s long-standing resistance to touch」** For years, Apple executives publicly rejected touchscreens on Mac laptops, citing ergonomics — the argument that reaching up to touch a vertical display is uncomfortable compared with a keyboard and trackpad. The reported reversal therefore overturns a position the company had defended for much of the Mac&\#x27;s modern history, and the source frames it as a shift toward revisiting past decisions rather than insisting the industry follow Apple&\#x27;s lead.

**「Impact」** If accurate, the report leaves a key compatibility question unanswered: it does not say whether existing macOS apps will support touch or whether developers will need to adapt them, so buyers would be paying a higher price for a capability with unspecified software support.

**Tags**: `#Apple`, `#MacBook Pro`, `#touchscreen`, `#OLED`, `#hardware`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China’s 2025 Population Falls 3.39 Million to 1.40489 Billion](https://weibo.com/1796087453/5357878513767954) ⭐️ 7.0/10

China’s year-end 2025 population fell by 3.39 million from a year earlier to 1.40489 billion, according to a report citing the China Statistical Yearbook 2026, leaving the total close to falling below 1.4 billion. The same report said there were 7.92 million births, a birth rate of 5.63 per 1,000, and a natural growth rate of -2.41 per 1,000.

telegram · zaihuapd · Oct 25, 12:02

**「Background」** A 2026 China population report cited by Tencent News says the country’s population has fallen for four consecutive years; negative natural growth means deaths outnumbered births.

<details><summary>References</summary>
<ul>
<li><a href="https://news.qq.com/rain/a/20260223A00L5H00">中 国 人 口 形势报告2026：鼓励 生 育_腾讯新闻</a></li>

</ul>
</details>

**Tags**: `#China demographics`, `#population decline`, `#birth rate`, `#macroeconomic trends`, `#official statistics`

---