---
marp: true
theme: default
paginate: true
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;500;700&display=swap');

:root {
  --color-background: #ffffff;
  --color-foreground: #1f2937;
  --color-heading: #111827;
  --color-accent: #10b981;
  --color-accent-gold: #f59e0b;
  --color-accent-purple: #8b5cf6;
  --color-accent-blue: #2563eb;
  --color-accent-red: #ef4444;
  --color-code-bg: #f9fafb;
  --color-border: #e5e7eb;
  --color-muted: #6b7280;
  --font-default: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --font-code: 'JetBrains Mono', 'Fira Code', Consolas, monospace;
}

section {
  background-color: var(--color-background);
  color: var(--color-foreground);
  font-family: var(--font-default);
  font-weight: 400;
  box-sizing: border-box;
  position: relative;
  line-height: 1.65;
  font-size: 20px;
  padding: 52px 56px 72px;
}

h1, h2, h3, h4, h5, h6 {
  font-weight: 800;
  color: var(--color-heading);
  margin: 0;
  padding: 0;
  letter-spacing: -0.03em;
}

h1 {
  font-size: clamp(40px, 8vw, 72px);
  line-height: 1.08;
  text-align: left;
}

h2 {
  font-size: clamp(30px, 4.8vw, 46px);
  margin-bottom: 24px;
  padding-bottom: 14px;
  border-bottom: 2px solid var(--color-border);
}

h3 {
  font-size: 24px;
  margin: 0 0 10px;
}

p {
  margin: 10px 0;
}

ul, ol {
  padding-left: 24px;
  margin: 10px 0;
}

li {
  margin-bottom: 8px;
}

li::marker {
  color: var(--color-accent);
  font-weight: 700;
}

strong {
  color: var(--color-accent);
  font-weight: 700;
}

code {
  background-color: var(--color-code-bg);
  color: var(--color-accent);
  padding: 2px 6px;
  border-radius: 4px;
  font-family: var(--font-code);
  font-size: 0.9em;
}

pre {
  background-color: var(--color-code-bg);
  border: 1px solid var(--color-border);
  border-radius: 10px;
  padding: 14px 16px;
  overflow-x: auto;
  font-family: var(--font-code);
  font-size: 15px;
  line-height: 1.45;
}

pre code {
  background: transparent;
  color: #1f2937;
  padding: 0;
}

table {
  border-collapse: collapse;
  width: 100%;
  margin: 16px 0;
  background-color: var(--color-code-bg);
}

th, td {
  border: 1px solid var(--color-border);
  padding: 10px 14px;
  text-align: left;
  font-size: 16px;
}

th {
  background-color: #eef2f7;
  color: var(--color-heading);
}

footer {
  font-size: 14px;
  color: #8b949e;
  font-family: var(--font-code);
  position: absolute;
  left: 56px;
  right: 56px;
  bottom: 32px;
  text-align: right;
}

footer::before {
  content: '// ';
  color: var(--color-accent);
}

section.lead {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

section.lead p {
  font-size: 22px;
  color: var(--color-muted);
}

section.lead blockquote {
  background: var(--color-code-bg);
  border-left: 4px solid var(--color-accent);
  border-radius: 0 12px 12px 0;
  padding: 18px 24px;
  margin-top: 28px;
  font-style: normal;
}

.date-label {
  font-family: var(--font-code);
  font-size: 14px;
  color: var(--color-muted);
  margin-bottom: 14px;
}

.feature-box {
  background: #ffffff;
  border: 1px solid var(--color-border);
  border-radius: 16px;
  padding: 20px 22px;
  margin: 12px 0;
  box-shadow: 0 1px 3px rgba(0,0,0,0.05);
}

.feature-box.green {
  background: linear-gradient(135deg, #10b981 0%, #059669 100%);
  color: white;
  border: none;
}

.feature-box.gold {
  background: linear-gradient(135deg, #f59e0b 0%, #d97706 100%);
  color: white;
  border: none;
}

.feature-box.purple {
  background: linear-gradient(135deg, #8b5cf6 0%, #7c3aed 100%);
  color: white;
  border: none;
}

.feature-box.blue {
  background: linear-gradient(135deg, #2563eb 0%, #1d4ed8 100%);
  color: white;
  border: none;
}

.feature-box.red {
  background: linear-gradient(135deg, #ef4444 0%, #dc2626 100%);
  color: white;
  border: none;
}

.feature-box h3,
.feature-box p,
.feature-box li,
.feature-box strong,
.feature-box .label {
  color: inherit;
}

.label {
  font-family: var(--font-code);
  font-size: 12px;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  color: var(--color-muted);
  margin-bottom: 8px;
}

.two-col {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 18px;
}

.three-col {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 16px;
}

.four-col {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  gap: 14px;
}

.compact-list li {
  margin-bottom: 4px;
}

.kpi-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 14px;
  margin-top: 20px;
}

.kpi-card {
  border: 1px solid var(--color-border);
  border-radius: 18px;
  padding: 18px;
  background: linear-gradient(180deg, #ffffff 0%, #f8fafc 100%);
}

.kpi-card .kpi-value {
  font-size: 34px;
  font-weight: 800;
  color: var(--color-heading);
  line-height: 1.1;
}

.kpi-card .kpi-label {
  font-size: 13px;
  color: var(--color-muted);
  margin-top: 8px;
}

.step-flow {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 14px;
  margin-top: 20px;
}

.step-card {
  border: 1px solid var(--color-border);
  border-radius: 18px;
  padding: 18px;
  background: #fff;
  position: relative;
}

.step-num {
  width: 34px;
  height: 34px;
  border-radius: 999px;
  background: var(--color-accent);
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 800;
  font-size: 16px;
  margin-bottom: 12px;
}

.compare-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 18px;
}

.compare-card {
  border: 1px solid var(--color-border);
  border-radius: 18px;
  padding: 20px;
  background: #fff;
}

.compare-card.good {
  border-top: 6px solid var(--color-accent);
}

.compare-card.warn {
  border-top: 6px solid var(--color-accent-gold);
}

.small {
  font-size: 15px;
  color: var(--color-muted);
}

.arch-box {
  border: 1px solid var(--color-border);
  border-radius: 18px;
  padding: 16px;
  background: #fff;
  text-align: center;
}

.arch-stack {
  display: grid;
  gap: 12px;
  margin-top: 18px;
}

.note-strip {
  margin-top: 16px;
  padding: 14px 16px;
  border-radius: 14px;
  background: #eff6ff;
  border: 1px solid #bfdbfe;
  color: #1e3a8a;
  font-size: 16px;
}
</style>

<!-- _class: lead -->

# 🦞 OpenClaw小龙虾

## 个人AI助手平台培训

> **面向 ZZCreation 团队**

*2026年第二季度版*

---

## 📋 今日议程

1. OpenClaw 是什么
2. 为什么值得关注
3. Windows 用户如何安装
4. 飞书如何完成接入
5. 风险边界与落地建议
6. 适合 ZZCreation 的试点场景

---

## 一、什么是小龙虾？

### 产品定义

**OpenClaw**，一个开源的个人 AI 助手平台。

它的核心不是“再做一个聊天框”，而是把下面几件事连起来：

- **消息入口**，如飞书、Telegram、网页控制台
- **模型能力**，如 OpenAI、Anthropic、Google
- **真实工具**，如浏览器、shell、文档、搜索
- **本地状态**，配置、记忆、日志都可留在自己环境里

---

## 它解决什么问题？

<div class="three-col">

<div class="feature-box">
<div class="label">沟通入口</div>
<h3>不只在网页里用</h3>
<p>可以直接从聊天软件里和 AI 协作，而不是切换一堆窗口。</p>
</div>

<div class="feature-box">
<div class="label">执行能力</div>
<h3>不只回答问题</h3>
<p>可以调用工具、读写文件、跑流程，向“助手”更进一步。</p>
</div>

<div class="feature-box">
<div class="label">部署方式</div>
<h3>更适合自己掌控</h3>
<p>适合本地、私有机或 VPS，方便保留配置和长期上下文。</p>
</div>

</div>

---

## 对 ZZCreation 的现实价值

<div class="two-col">

<div class="feature-box green">
<div class="label">短期</div>
<h3>先提升个人效率</h3>
<ul>
<li>飞书内直接问答和查资料</li>
<li>把常见重复操作交给 Agent</li>
<li>统一沉淀工具和技能</li>
</ul>
</div>

<div class="feature-box blue">
<div class="label">中期</div>
<h3>再接业务流程</h3>
<ul>
<li>文档协作与内容生成</li>
<li>项目跟进与汇报辅助</li>
<li>面向团队的自动化工作流</li>
</ul>
</div>

</div>

<div class="note-strip">
更准确地说，OpenClaw 的价值不是“替代人”，而是让团队先拥有一个能接消息、能调工具、能持续配置的 AI 工作底座。
</div>

---

## OpenClaw 如何工作

<div class="step-flow">

<div class="step-card">
<div class="step-num">1</div>
<h3>消息进入</h3>
<p>用户从飞书、网页或其它渠道发起请求。</p>
</div>

<div class="step-card">
<div class="step-num">2</div>
<h3>Gateway 路由</h3>
<p>OpenClaw Gateway 接收消息并分配给对应 Agent。</p>
</div>

<div class="step-card">
<div class="step-num">3</div>
<h3>模型 + 工具</h3>
<p>Agent 调用模型、技能、浏览器、文档等工具完成任务。</p>
</div>

<div class="step-card">
<div class="step-num">4</div>
<h3>结果返回</h3>
<p>处理结果再回到原渠道，形成完整闭环。</p>
</div>

</div>

---

## 核心架构图

<div class="arch-stack">
  <div class="arch-box"><strong>消息渠道层</strong><br>Feishu / Telegram / Dashboard / 更多平台</div>
  <div class="arch-box"><strong>Gateway</strong><br>消息接收、路由、权限控制、会话管理</div>
  <div class="two-col">
    <div class="arch-box"><strong>Agent Runtime</strong><br>上下文、推理、任务编排</div>
    <div class="arch-box"><strong>Skills / Tools</strong><br>Browser / Exec / Docs / Search / Memory</div>
  </div>
  <div class="arch-box"><strong>本地状态层</strong><br>配置文件 / 日志 / 记忆 / 工作区文件</div>
</div>

<div class="note-strip">
培训里最重要的理解是，OpenClaw 不是单点工具，而是一个把“聊天入口、模型能力、真实工具、长期状态”连接起来的平台。
</div>

---

## 可以做什么，不适合什么

<div class="compare-grid">

<div class="compare-card good">
<h3>✅ 更适合</h3>
<ul>
<li>个人 AI 助手</li>
<li>团队内部轻量自动化</li>
<li>文档、消息、搜索、浏览器协作</li>
<li>需要长期配置和持续迭代的场景</li>
</ul>
</div>

<div class="compare-card warn">
<h3>⚠️ 不适合直接上来就做</h3>
<ul>
<li>高风险审批流程自动放权</li>
<li>未梳理边界的对外自动发送</li>
<li>完全无人值守的关键业务链路</li>
<li>把它当成“万能全自动员工”</li>
</ul>
</div>

</div>

---

## 二、创始人与项目背景

<div class="feature-box">

### Peter Steinberger (steipete)

- GitHub: **@steipete**
- 前 PSPDFKit 创始人
- 退休后回归开源，专注 OpenClaw
- 项目最初是个人 AI 实验场，后来逐步演化成完整平台

</div>

<div class="kpi-grid">
  <div class="kpi-card"><div class="kpi-value">42.6k</div><div class="kpi-label">GitHub Followers</div></div>
  <div class="kpi-card"><div class="kpi-value">13k+</div><div class="kpi-label">OpenClaw 提交数</div></div>
  <div class="kpi-card"><div class="kpi-value">318k+</div><div class="kpi-label">项目星标</div></div>
  <div class="kpi-card"><div class="kpi-value">MIT</div><div class="kpi-label">开源协议</div></div>
</div>

---

## 背景故事与演进

<div class="feature-box">

### 项目演进

```text
Warelay → Clawdbot → Moltbot → OpenClaw
```

### 设计理念

- **本地优先**，数据和状态自己掌控
- **可扩展**，技能系统支持定制能力
- **多模态**，文字、语音、图像等逐步覆盖
- **跨平台**，支持 macOS / Linux / Windows / 移动端节点

</div>

---

## 🦐 国内龙虾系列对比

| 产品名 | 厂商 | 特点 | 首页 |
|:-------|:----:|:-----|:-----|
| **ArkClaw** | 字节跳动 | 零配置操作，降低门槛 | - |
| **QClaw** | 腾讯电脑管家 | 微信/QQ接入，桌面级Agent | qclaw.qq.com |
| **WorkBuddy** | 腾讯 | 企业微信接入，全场景覆盖 | - |
| **CoPaw** | 阿里云 | 开源本地部署、钉钉/飞书原生 | copaw.github.io |
| **LobsterAI** | 网易有道 | 7×24小时待命、16种内置技能 | lobsterai.com |
| **360安全龙虾** | 360 | 沙箱隔离、龙虾卫士安全防护 | - |

> 这一页保留作行业观察视角，用来帮助大家理解：个人 AI 助手正在从单点问答，进入“接渠道、接工具、接工作流”的平台阶段。

---

## 三、Windows 用户如何安装

### 为什么推荐 WSL2

<div class="compare-grid">

<div class="compare-card good">
<div class="label">推荐路径</div>
<h3>WSL2 + Ubuntu</h3>
<ul>
<li>更接近官方主流文档环境</li>
<li>CLI、Gateway、工具链兼容性更稳</li>
<li>更适合长期运行和后续扩展</li>
<li>对团队培训更容易统一口径</li>
</ul>
</div>

<div class="compare-card warn">
<div class="label">可用但次选</div>
<h3>原生 Windows</h3>
<ul>
<li>适合轻量 CLI 体验</li>
<li>部分服务管理仍有差异</li>
<li>文档与社区经验更多偏向 Linux / WSL2</li>
<li>培训时更容易出现环境差异问题</li>
</ul>
</div>

</div>

<div class="note-strip">
一句话理解，**WSL2 就是在 Windows 里准备一套更稳定的 Linux 工作环境，让 OpenClaw 按它最熟悉的方式运行。**
</div>

---

## 什么是 WSL2

<div class="two-col">

<div class="feature-box">
<div class="label">给非技术同事的解释</div>
<h3>Windows 里的 Linux 工作区</h3>
<p>你平时还是用 Windows，但真正跑 OpenClaw 的，是 WSL2 里的 Ubuntu 环境。</p>
</div>

<div class="feature-box">
<div class="label">为什么它重要</div>
<h3>更像官方标准环境</h3>
<p>很多命令、服务、依赖都更贴近 Linux，踩坑更少，团队也更容易统一安装步骤。</p>
</div>

</div>

---

## Windows + WSL2 + OpenClaw 架构图

<div class="three-col">

<div class="feature-box">
<div class="label">Windows 层</div>
<ul class="compact-list">
<li>PowerShell</li>
<li>浏览器 Dashboard</li>
<li>飞书客户端</li>
</ul>
</div>

<div class="feature-box green">
<div class="label">WSL2 Ubuntu 层</div>
<ul class="compact-list">
<li>OpenClaw CLI</li>
<li>Gateway 服务</li>
<li>配置与日志</li>
</ul>
</div>

<div class="feature-box blue">
<div class="label">外部服务层</div>
<ul class="compact-list">
<li>Feishu 平台</li>
<li>模型 API</li>
<li>其它插件 / 工具</li>
</ul>
</div>

</div>

<div class="note-strip">
消息路径可以简单理解为：<strong>人在飞书发消息 → Feishu 把事件交给 Gateway → Gateway 调用模型和工具 → 结果再回到飞书。</strong>
</div>

---

## WSL2 安装 4 步法

<div class="step-flow">

<div class="step-card">
<div class="step-num">1</div>
<h3>装 WSL2</h3>
<p>在 Windows 安装 WSL2 和 Ubuntu。</p>
<pre><code>wsl --install</code></pre>
</div>

<div class="step-card">
<div class="step-num">2</div>
<h3>开 systemd</h3>
<p>这是安装 Gateway 服务的关键前提。</p>
<pre><code>[boot]
systemd=true</code></pre>
</div>

<div class="step-card">
<div class="step-num">3</div>
<h3>装 OpenClaw</h3>
<p>在 Ubuntu 终端里执行官方安装流程。</p>
<pre><code>curl -fsSL https://openclaw.ai/install.sh | bash</code></pre>
</div>

<div class="step-card">
<div class="step-num">4</div>
<h3>跑引导</h3>
<p>用 onboarding 完成模型、密钥和 Gateway 初始化。</p>
<pre><code>openclaw onboard --install-daemon</code></pre>
</div>

</div>

---

## 安装成功怎么判断

<div class="three-col">

<div class="feature-box">
<div class="label">检查 1</div>
<h3>Gateway 正常</h3>
<p><code>openclaw gateway status</code> 能看到服务状态。</p>
</div>

<div class="feature-box">
<div class="label">检查 2</div>
<h3>Dashboard 可打开</h3>
<p><code>openclaw dashboard</code> 能在浏览器里正常打开控制台。</p>
</div>

<div class="feature-box">
<div class="label">检查 3</div>
<h3>首条消息可回复</h3>
<p>无论在控制台还是飞书，发出首条消息都能拿到结果。</p>
</div>

</div>

---

## 四、飞书集成怎么做

### 先理解整体流程

<div class="step-flow">

<div class="step-card">
<div class="step-num">1</div>
<h3>创建飞书应用</h3>
<p>先准备一个企业应用，拿到它的身份信息。</p>
</div>

<div class="step-card">
<div class="step-num">2</div>
<h3>开启 Bot 能力</h3>
<p>让应用具备接收和回复消息的能力。</p>
</div>

<div class="step-card">
<div class="step-num">3</div>
<h3>接入 OpenClaw</h3>
<p>把 App ID 和 App Secret 配进 OpenClaw。</p>
</div>

<div class="step-card">
<div class="step-num">4</div>
<h3>测试与配对</h3>
<p>首次发消息后完成 pairing，就能进入正式使用。</p>
</div>

</div>

---

## 飞书集成整体架构图

<div class="three-col">

<div class="feature-box">
<div class="label">飞书侧</div>
<ul class="compact-list">
<li>用户发消息</li>
<li>企业应用 / Bot</li>
<li>事件订阅</li>
</ul>
</div>

<div class="feature-box green">
<div class="label">OpenClaw 侧</div>
<ul class="compact-list">
<li>Feishu Channel</li>
<li>Gateway</li>
<li>Pairing / 权限控制</li>
</ul>
</div>

<div class="feature-box blue">
<div class="label">能力侧</div>
<ul class="compact-list">
<li>模型 API</li>
<li>工具 / Skills</li>
<li>工作区与记忆</li>
</ul>
</div>

</div>

---

## 飞书接入前，需要准备什么

<div class="two-col">

<div class="feature-box">
<h3>飞书侧</h3>
<ul>
<li>一个企业应用</li>
<li><strong>App ID</strong></li>
<li><strong>App Secret</strong></li>
<li>Bot 能力</li>
<li>消息事件订阅</li>
</ul>
</div>

<div class="feature-box">
<h3>OpenClaw 侧</h3>
<ul>
<li>OpenClaw 已安装完成</li>
<li>Gateway 可以正常运行</li>
<li>能执行 <code>openclaw channels add</code></li>
<li>准备好模型 API Key</li>
</ul>
</div>

</div>

---

## 飞书接入 5 步法

<div class="step-flow" style="grid-template-columns: repeat(5, 1fr);">

<div class="step-card"><div class="step-num">1</div><h3>创建应用</h3><p>在飞书开放平台创建企业应用。</p></div>
<div class="step-card"><div class="step-num">2</div><h3>复制凭证</h3><p>拿到 App ID 和 App Secret。</p></div>
<div class="step-card"><div class="step-num">3</div><h3>开权限</h3><p>按官方要求导入必要权限。</p></div>
<div class="step-card"><div class="step-num">4</div><h3>开 Bot + 事件</h3><p>启用 Bot，并订阅消息接收事件。</p></div>
<div class="step-card"><div class="step-num">5</div><h3>接入 OpenClaw</h3><p>在 OpenClaw 中录入凭证并启动测试。</p></div>

</div>

---

## OpenClaw 里的最小配置思路

<div class="feature-box">

### 对非技术人员，先记住这件事就够了

真正要填进 OpenClaw 的核心信息，通常只有：

- **App ID**
- **App Secret**

然后通过：

```bash
openclaw channels add
```

选择 **Feishu**，按提示填入即可。

</div>

<div class="note-strip">
培训时不建议一开始就深讲全部配置字段，先让大家完成“能接入、能发消息、能收到回复”这个最小闭环。
</div>

---

## 首次测试与 Pairing 机制

<div class="two-col">

<div class="feature-box gold">
<div class="label">为什么会看到配对码</div>
<h3>这是默认安全机制</h3>
<p>未知用户第一次私聊机器人时，默认不会直接放行，而是先返回一个 pairing code。</p>
</div>

<div class="feature-box green">
<div class="label">完成后会怎样</div>
<h3>通过批准后可正常聊天</h3>
<p>管理员批准配对后，这个用户就能正式和 OpenClaw 建立稳定会话。</p>
</div>

</div>

<pre><code>openclaw pairing approve feishu &lt;CODE&gt;</code></pre>

---

## 常见问题（安装 + 飞书）

<div class="two-col">

<div class="feature-box">
<h3>安装类</h3>
<ul>
<li>为什么推荐 WSL2，不直接装 Windows？</li>
<li>为什么要开 systemd？</li>
<li>为什么 PowerShell 和 Ubuntu 命令不同？</li>
</ul>
</div>

<div class="feature-box">
<h3>飞书类</h3>
<ul>
<li>机器人不回消息，通常先查 Gateway 是否运行</li>
<li>事件订阅未生效，通常与应用配置有关</li>
<li>应用未发布，机器人可能无法正常对外使用</li>
<li>未批准 pairing，首次私聊不会直接放行</li>
</ul>
</div>

</div>

---

## 五、风险提示与安全建议

<div class="feature-box red">
<div class="label">安全前提</div>
<h3>入站消息应默认视为不可信输入</h3>
<p>因为 OpenClaw 接入真实聊天平台，所以任何 DM、群消息、外部输入，都不应默认被视为可信操作指令。</p>
</div>

---

## 安全检查清单

- ✅ 使用 <code>pairing</code> 作为默认私聊策略
- ✅ 只给飞书应用最小必要权限
- ✅ 不把 API 密钥提交到代码仓库
- ✅ 定期更新 OpenClaw 版本
- ✅ 群聊先从 allowlist 或 requireMention 开始
- ✅ 重要外发动作保留人工确认

---

## 六、对 ZZCreation 的落地建议

<div class="three-col">

<div class="feature-box">
<div class="label">阶段 1</div>
<h3>个人试点</h3>
<p>先在少数成员电脑上完成 WSL2 安装与飞书接入。</p>
</div>

<div class="feature-box">
<div class="label">阶段 2</div>
<h3>团队协作</h3>
<p>沉淀可复用技能，统一常见操作与文档流程。</p>
</div>

<div class="feature-box">
<div class="label">阶段 3</div>
<h3>业务接入</h3>
<p>把稳定的能力逐步接入内容、运营、项目管理等实际场景。</p>
</div>

</div>

---

## 建议的下一步

1. 先完成 **Windows + WSL2 标准安装模板**
2. 再完成 **飞书应用的标准接入 SOP**
3. 最后沉淀 **ZZCreation 内部技能 / 工作流模板**

<div class="note-strip">
如果把这三步做好，OpenClaw 在团队里的角色就不只是“一个能聊天的 AI”，而会变成一个真正可持续迭代的工作平台。
</div>

---

<!-- _class: lead -->

# 🦞 谢谢

### Q & A

- 官网：openclaw.ai
- 文档：docs.openclaw.ai
- GitHub：github.com/openclaw/openclaw
- Discord：discord.gg/clawd

---

*最后更新：2026年4月9日 | 版本：v2.0-stage1*