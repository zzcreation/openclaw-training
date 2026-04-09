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
  transition: transform 0.22s ease, box-shadow 0.22s ease, border-color 0.22s ease;
}

.feature-box:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 28px rgba(15, 23, 42, 0.12);
  border-color: #cbd5e1;
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
  transition: transform 0.22s ease, box-shadow 0.22s ease, border-color 0.22s ease;
}

.step-card:hover, .compare-card:hover, .kpi-card:hover, .mini-kpi:hover, .flow-node:hover, .arch-box:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 28px rgba(15, 23, 42, 0.10);
  border-color: #cbd5e1;
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
  .flow-band {
    display: flex;
    align-items: stretch;
    justify-content: space-between;
    gap: 12px;
    margin-top: 18px;
  }

  .flow-node {
    flex: 1;
    border-radius: 18px;
    padding: 18px 16px;
    border: 1px solid var(--color-border);
    background: linear-gradient(180deg, #ffffff 0%, #f8fafc 100%);
    text-align: center;
  }

  .flow-node .emoji {
    font-size: 28px;
    display: block;
    margin-bottom: 8px;
  }

  .flow-arrow {
    display: flex;
    align-items: center;
    color: var(--color-muted);
    font-size: 26px;
    font-weight: 800;
  }

  .mini-kpis {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 14px;
    margin-top: 18px;
  }

  .mini-kpi {
    border-radius: 16px;
    padding: 16px;
    background: #fff;
    border: 1px solid var(--color-border);
  }

  .mini-kpi strong {
    display: block;
    font-size: 30px;
    line-height: 1.1;
    margin-bottom: 6px;
  }

  .check-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 14px;
    margin-top: 18px;
  }

  .check-card {
    border: 1px solid var(--color-border);
    border-radius: 18px;
    padding: 18px;
    background: linear-gradient(180deg, #ffffff 0%, #f8fafc 100%);
    transition: transform 0.22s ease, box-shadow 0.22s ease, border-color 0.22s ease;
  }

  .check-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 12px 28px rgba(15, 23, 42, 0.10);
    border-color: #cbd5e1;
  }

  .check-card .icon {
    font-size: 26px;
    display: block;
    margin-bottom: 8px;
  }

  .phase-roadmap {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 16px;
    margin-top: 18px;
  }

  .phase-card {
    border-radius: 20px;
    padding: 20px;
    color: white;
    min-height: 180px;
    transition: transform 0.22s ease, box-shadow 0.22s ease;
  }

  .phase-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 14px 32px rgba(15, 23, 42, 0.14);
  }

  .phase-card.p1 { background: linear-gradient(135deg, #10b981 0%, #059669 100%); }
  .phase-card.p2 { background: linear-gradient(135deg, #2563eb 0%, #1d4ed8 100%); }
  .phase-card.p3 { background: linear-gradient(135deg, #8b5cf6 0%, #7c3aed 100%); }

  .phase-card h3, .phase-card p, .phase-card li, .phase-card .label {
    color: white;
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

<div class="flow-band">
  <div class="flow-node"><span class="emoji">💬</span><strong>消息进入</strong><br><span class="small">飞书 / 网页 / 其它渠道</span></div>
  <div class="flow-arrow">→</div>
  <div class="flow-node"><span class="emoji">🧭</span><strong>Gateway 路由</strong><br><span class="small">接收消息、分配 Agent</span></div>
  <div class="flow-arrow">→</div>
  <div class="flow-node"><span class="emoji">🛠️</span><strong>模型 + 工具</strong><br><span class="small">推理、搜索、文档、浏览器</span></div>
  <div class="flow-arrow">→</div>
  <div class="flow-node"><span class="emoji">✅</span><strong>结果返回</strong><br><span class="small">回到原来的消息渠道</span></div>
</div>

---

## 核心架构图

<div class="arch-stack">
  <div class="arch-box"><strong>消息渠道层</strong><br>Feishu / Telegram / Dashboard / 更多平台</div>
  <div class="arch-box" style="background:linear-gradient(135deg,#ecfeff 0%,#f0fdf4 100%);"><strong>Gateway</strong><br>消息接收、路由、权限控制、会话管理</div>
  <div class="two-col">
    <div class="arch-box"><strong>Agent Runtime</strong><br>上下文、推理、任务编排</div>
    <div class="arch-box"><strong>Skills / Tools</strong><br>Browser / Exec / Docs / Search / Memory</div>
  </div>
  <div class="arch-box"><strong>本地状态层</strong><br>配置文件 / 日志 / 记忆 / 工作区文件</div>
</div>

<div class="mini-kpis">
  <div class="mini-kpi"><strong>20+</strong>接入渠道</div>
  <div class="mini-kpi"><strong>本地优先</strong>数据和状态自己掌控</div>
  <div class="mini-kpi"><strong>可扩展</strong>技能和工具可持续增加</div>
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

> 2026年"龙虾元年"：国内大厂纷纷推出OpenClaw衍生版本，形成"龙虾共斗"局面。

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

## WSL2 是什么

<div class="two-col">

<div class="feature-box">
<div class="label">一句话解释</div>
<h3>Windows 里的 Linux 工作区</h3>
<p>你平时还是用 Windows，但真正跑 OpenClaw 的，是 WSL2 里的 Ubuntu 环境，所以兼容性更稳。</p>
</div>

<div class="feature-box blue">
<div class="label">三层架构</div>
<p><strong>Windows 层</strong>：PowerShell、浏览器、飞书客户端</p>
<p><strong>WSL2 层</strong>：OpenClaw CLI、Gateway、配置文件</p>
<p><strong>外部服务层</strong>：Feishu 平台、模型 API、插件工具</p>
<p class="small">消息路径：飞书消息 → Gateway → 模型/工具 → 返回飞书。</p>
</div>

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
<p>在 <code>/etc/wsl.conf</code> 里开启。</p>
<pre><code>[boot]
systemd=true</code></pre>
</div>

<div class="step-card">
<div class="step-num">3</div>
<h3>装 OpenClaw</h3>
<p>在 Ubuntu 终端里执行官方安装流程。</p>
<pre><code>curl -fsSL openclaw.ai/install.sh | bash</code></pre>
</div>

<div class="step-card">
<div class="step-num">4</div>
<h3>跑引导</h3>
<p>完成模型、密钥和 Gateway 初始化。</p>
<pre><code>openclaw onboard</code></pre>
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
<p><code>openclaw dashboard</code> 能正常打开控制台。</p>
</div>

<div class="feature-box green">
<div class="label">检查 3</div>
<h3>首条消息可回复</h3>
<p>无论在控制台还是飞书，发出首条测试消息都能拿到结果。</p>
</div>

</div>

<div class="note-strip">
先完成“装好 OpenClaw + 能正常回消息”这个最小闭环，再讲更细的配置，会更适合培训节奏。
</div>

---

## 飞书接入总览

<div class="flow-band">
  <div class="flow-node"><span class="emoji">🏢</span><strong>创建应用</strong><br><span class="small">准备企业应用</span></div>
  <div class="flow-arrow">→</div>
  <div class="flow-node"><span class="emoji">🔑</span><strong>拿到凭证</strong><br><span class="small">App ID / App Secret</span></div>
  <div class="flow-arrow">→</div>
  <div class="flow-node"><span class="emoji">🤖</span><strong>开启能力</strong><br><span class="small">Bot + 事件订阅</span></div>
  <div class="flow-arrow">→</div>
  <div class="flow-node"><span class="emoji">🚀</span><strong>接入测试</strong><br><span class="small">录入 OpenClaw 并发首条消息</span></div>
</div>

<div class="note-strip">
对培训对象来说，飞书集成先抓住主线就够了，不需要一开始就展开所有配置字段。
</div>

---

## 四、飞书集成怎么做

<div class="two-col">

<div class="feature-box blue">
<div class="label">整体路径</div>
<ul>
<li>飞书侧准备企业应用、Bot 和事件订阅</li>
<li>OpenClaw 侧录入 App ID / Secret</li>
<li>启动 Gateway，发起首条测试消息</li>
<li>首次私聊通过 pairing 完成授权</li>
</ul>
</div>

<div class="feature-box">
<div class="label">三层架构</div>
<ul class="compact-list">
<li><strong>飞书侧</strong>：用户、企业应用、事件订阅</li>
<li><strong>OpenClaw 侧</strong>：Feishu Channel、Gateway、Pairing</li>
<li><strong>能力侧</strong>：模型 API、Tools、Workspace</li>
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

## 最小配置 + 首次 Pairing

<div class="two-col">

<div class="feature-box">
<div class="label">最小配置</div>
<p>对非技术人员，先记住真正要填进 OpenClaw 的核心信息通常只有两个：</p>
<ul>
<li><strong>App ID</strong></li>
<li><strong>App Secret</strong></li>
</ul>
<pre><code>openclaw channels add</code></pre>
<p class="small">选择 Feishu，按提示填入即可。</p>
</div>

<div class="feature-box gold">
<div class="label">首次 Pairing</div>
<p>未知用户第一次私聊机器人时，默认不会直接放行，而是先返回一个 pairing code。</p>
<pre><code>openclaw pairing approve feishu &lt;CODE&gt;</code></pre>
<p class="small">批准之后，这个用户就可以正常聊天。</p>
</div>

</div>

---

## 常见问题（安装 + 飞书）

<div class="two-col">

<div class="feature-box gold">
<div class="label">为什么会看到配对码</div>
<h3>这是默认安全机制</h3>
<p>未知用户第一次私聊机器人时，默认不会直接放行，而是先返回一个 pairing code。</p>
<pre><code>openclaw pairing approve feishu &lt;CODE&gt;</code></pre>
</div>

<div class="feature-box green">
<div class="label">完成后会怎样</div>
<h3>通过批准后可正常聊天</h3>
<p>管理员批准配对后，这个用户就能正式和 OpenClaw 建立稳定会话。</p>
</div>

</div>

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

<div class="check-grid">
  <div class="check-card"><span class="icon">🔐</span><strong>默认启用 pairing</strong><p class="small">私聊先配对，再建立稳定会话。</p></div>
  <div class="check-card"><span class="icon">🪪</span><strong>最小权限原则</strong><p class="small">飞书应用只给必要权限，不多开。</p></div>
  <div class="check-card"><span class="icon">🧯</span><strong>密钥不入库</strong><p class="small">API Key 不提交到 Git 仓库。</p></div>
  <div class="check-card"><span class="icon">🔄</span><strong>保持更新</strong><p class="small">OpenClaw 版本和依赖定期升级。</p></div>
  <div class="check-card"><span class="icon">👀</span><strong>群聊先收口</strong><p class="small">先从 allowlist 或 requireMention 开始。</p></div>
  <div class="check-card"><span class="icon">✋</span><strong>高风险动作人工确认</strong><p class="small">涉及外发、审批、关键操作时保留人工把关。</p></div>
</div>

---

## 六、对 ZZCreation 的落地建议

<div class="phase-roadmap">
  <div class="phase-card p1">
    <div class="label">阶段 1</div>
    <h3>个人试点</h3>
    <p>先在少数成员电脑上完成 WSL2 安装与飞书接入。</p>
    <ul>
      <li>统一安装口径</li>
      <li>验证消息闭环</li>
    </ul>
  </div>
  <div class="phase-card p2">
    <div class="label">阶段 2</div>
    <h3>团队协作</h3>
    <p>沉淀可复用技能，统一常见操作与文档流程。</p>
    <ul>
      <li>形成标准 SOP</li>
      <li>沉淀内部技能</li>
    </ul>
  </div>
  <div class="phase-card p3">
    <div class="label">阶段 3</div>
    <h3>业务接入</h3>
    <p>把稳定的能力逐步接入内容、运营、项目管理等实际场景。</p>
    <ul>
      <li>接业务流程</li>
      <li>保留人工审核</li>
    </ul>
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