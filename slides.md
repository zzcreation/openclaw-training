---
marp: true
theme: default
paginate: true
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;700&family=Fira+Code:wght@400;500;700&display=swap');

:root {
  --color-background: #0d1117;
  --color-foreground: #c9d1d9;
  --color-heading: #58a6ff;
  --color-accent: #7ee787;
  --color-code-bg: #161b22;
  --color-border: #30363d;
  --font-default: 'Noto Sans JP', 'Hiragino Kaku Gothic ProN', 'Meiryo', sans-serif;
  --font-code: 'Fira Code', 'Consolas', 'Monaco', monospace;
}

section {
  background-color: var(--color-background);
  color: var(--color-foreground);
  font-family: var(--font-default);
  font-weight: 400;
  box-sizing: border-box;
  border-left: 4px solid var(--color-accent);
  position: relative;
  line-height: 1.6;
  font-size: 20px;
  padding: 56px;
}

h1, h2, h3, h4, h5, h6 {
  font-weight: 700;
  color: var(--color-heading);
  margin: 0;
  padding: 0;
  font-family: var(--font-code);
}

h1 {
  font-size: 52px;
  line-height: 1.3;
  text-align: left;
}

h1::before {
  content: '# ';
  color: var(--color-accent);
}

h2 {
  font-size: 38px;
  margin-bottom: 40px;
  padding-bottom: 12px;
  border-bottom: 2px solid var(--color-border);
}

h2::before {
  content: '## ';
  color: var(--color-accent);
}

h3 {
  color: var(--color-foreground);
  font-size: 26px;
  margin-top: 32px;
  margin-bottom: 12px;
}

h3::before {
  content: '### ';
  color: var(--color-accent);
}

ul, ol {
  padding-left: 32px;
}

li {
  margin-bottom: 10px;
}

li::marker {
  color: var(--color-accent);
}

pre {
  background-color: var(--color-code-bg);
  border: 1px solid var(--color-border);
  border-radius: 6px;
  padding: 16px;
  overflow-x: auto;
  font-family: var(--font-code);
  font-size: 16px;
  line-height: 1.5;
}

code {
  background-color: var(--color-code-bg);
  color: var(--color-accent);
  padding: 2px 6px;
  border-radius: 3px;
  font-family: var(--font-code);
  font-size: 0.9em;
}

pre code {
  background-color: transparent;
  padding: 0;
  color: var(--color-foreground);
}

footer {
  font-size: 14px;
  color: #8b949e;
  font-family: var(--font-code);
  position: absolute;
  left: 56px;
  right: 56px;
  bottom: 40px;
  text-align: right;
}

footer::before {
  content: '// ';
  color: var(--color-accent);
}

section.lead {
  border-left: 4px solid var(--color-accent);
  display: flex;
  flex-direction: column;
  justify-content: center;
}

section.lead h1 {
  margin-bottom: 24px;
}

section.lead p {
  font-size: 22px;
  color: var(--color-foreground);
  font-family: var(--font-code);
}

strong {
  color: var(--color-accent);
  font-weight: 700;
}

table {
  border-collapse: collapse;
  width: 100%;
  margin: 20px 0;
  background-color: var(--color-code-bg);
}

th, td {
  border: 1px solid var(--color-border);
  padding: 12px 16px;
  text-align: left;
}

th {
  background-color: var(--color-border);
  color: var(--color-heading);
}

td {
  background-color: var(--color-code-bg);
}

blockquote {
  border-left: 3px solid var(--color-accent);
  margin: 16px 0;
  padding: 8px 16px;
  background-color: var(--color-code-bg);
  font-style: italic;
}

.feature-box {
  background: var(--color-code-bg);
  border: 1px solid var(--color-border);
  border-radius: 8px;
  padding: 16px;
  margin: 12px 0;
}

.two-col {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
}

.three-col {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 20px;
}

.four-col {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  gap: 16px;
}
</style>

<!-- _class: lead -->

# 🦞 OpenClaw小龙虾

## 个人AI助手平台培训

> **面向 ZZCreation 团队**

*2026年第一季度*

---

## 📋 目录

1. 什么是小龙虾？
2. 创始人故事
3. 背景故事与诞生
4. 当前现状与生态
5. 保姆级安装教程
6. 风险提示与安全建议
7. 未来展望
8. 参考资料

---

## 一、什么是小龙虾？

### 产品定义

**OpenClaw** — 开源的个人AI助手平台

> *"Your own personal AI assistant. Any OS. Any Platform. The lobster way."*

---

### 核心特性

<div class="two-col">

<div class="feature-box">

**本地优先** 🏠

数据存储本地，保护创意/客户数据

</div>

<div class="feature-box">

**多通道接入** 📡

支持20+即时通讯平台

</div>

<div class="feature-box">

**语音交互** 🎤

支持语音唤醒+对话

</div>

<div class="feature-box">

**Canvas画布** 🎨

实时可视化工作区

</div>

</div>

---

## 二、创始人故事

### Peter Steinberger (steipete)

<div class="feature-box">

**👤 个人简介**

- **GitHub**: @steipete
- **职位**: 全职开源开发者 (Full-Time Open-Sourcerer)
- **位置**: 维也纳 & 伦敦
- **推特**: @steipete
- **网站**: steipete.me

</div>

---

### 职业经历

<div class="two-col">

<div class="feature-box">

**🎯 当前**

全职开发 OpenClaw ("Clawdfather")

> *"Came back from retirement to mess with AI."*

</div>

<div class="feature-box">

**📜 之前**

**PSPDFKit** 创始人

- 知名 iOS/Android PDF SDK 公司
- 成功退出后退休
- 为"玩AI"重返开源社区

</div>

</div>

---

### 成就数据

<div class="four-col">

<div class="feature-box">

**⭐ 42.6k**

GitHub 粉丝

</div>

<div class="feature-box">

**📝 13k+**

OpenClaw 提交

</div>

<div class="feature-box">

**⭐ 318k+**

项目星标

</div>

<div class="feature-box">

**🏆**

Pair Extraordinaire x4
Pull Shark x4
Starstruck x4

</div>

</div>

---

## 三、背景故事与诞生

<div class="feature-box">

- **GitHub星标：** 318K+ ⭐
- **开源协议：** MIT License
- **技术栈：** Node.js ≥22、TypeScript
- **项目性质：** 开源社区项目

</div>

---

### 起源与发展

> OpenClaw 最初是一个**个人学习AI的游乐场**，旨在构建一个真正有用的助手——可以在真实计算机上运行真实任务的助手。

**项目演进：**

```
Warelay → Clawdbot → Moltbot → OpenClaw
```

---

### 设计理念

1. **本地化** — 你的数据你做主
2. **可扩展** — 技能系统支持自定义工具
3. **多模态** — 文字/语音/图像/视频全覆盖
4. **跨平台** — macOS/Linux/Windows/iOS/Android

---

## 四、当前现状与生态

### 产品版本

| 版本 | 标签 | 说明 |
|:----:|:----:|:-----|
| Stable | vYYYY.M.D | 正式版 |
| Beta | vYYYY.M.D-beta.N | 测试版 |
| Dev | main分支 | 开发版 |

---

### 核心架构

```
┌─────────────────────────────────────────┐
│           OpenClaw Gateway              │
├─────────────────────────────────────────┤
│  Channel Manager │ Agent Runtime │ Skills│
├─────────────────────────────────────────┤
│             本地数据存储                  │
└─────────────────────────────────────────┘
```

---

### 集成合作伙伴

- OpenAI — 底层模型支持
- Vercel — 部署托管
- Blacksmith — 工具链
- Convex — 后端服务
- Anthropic — Claude模型支持

---

### 社区活跃度

- GitHub ⭐ **318K+**
- GitHub Fork **61K+**
- Discord 社区: **discord.gg/clawd**
- 社区展示项目: **clawhub.ai**

---

### MCP 支持

> OpenClaw 通过 **mcporter** 支持 MCP (Model Context Protocol)

- 无需重启 Gateway 即可添加/更改 MCP 服务器
- 保持核心工具/上下文精简
- 减少 MCP 变动对核心稳定性的影响

---

### 特色功能 — 社区展示

<div class="two-col">

<div class="feature-box">

**🤖 PR 审核机器人**

GitHub PR 审核 → Telegram 反馈

</div>

<div class="feature-box">

**🍷 酒窖管理技能**

从 CSV 构建本地酒窖管理技能

</div>

<div class="feature-box">

**🛒 超市自动下单**

每周菜单 → 自动下单配送

</div>

<div class="feature-box">

**📸 截图转 Markdown**

热键截图 → AI 分析 → Markdown

</div>

</div>

---

## 五、保姆级安装教程

### 环境要求

| 操作系统 | 要求 |
|:--------:|:-----|
| macOS | Node ≥22 |
| Linux | Node ≥22 |
| Windows | WSL2（强烈推荐） |

---

### 安装步骤

```bash
# 1. 安装 OpenClaw
npm install -g openclaw@latest
# 或: pnpm add -g openclaw@latest

# 2. 启动安装向导（推荐）
openclaw onboard --install-daemon

# 3. 启动 Gateway
openclaw gateway --port 18789 --verbose

# 4. 发送测试消息
openclaw message send --to +1234567890 --message "Hello"
```

---

### 飞书配置

1. 在飞书开放平台创建应用
2. 获取 App ID 和 App Secret
3. 配置权限
4. 在 OpenClaw 配置中添加

```json
{
  "channels": {
    "feishu": {
      "enabled": true,
      "appId": "YOUR_APP_ID",
      "appSecret": "YOUR_APP_SECRET"
    }
  }
}
```

---

### 验证安装

```bash
# 运行诊断
openclaw doctor

# 检查状态
openclaw status
```

---

## 六、风险提示与安全建议

> ⚠️ **重要：** OpenClaw 连接真实通讯平台，入站 DM 应视为**不可信输入**

---

### DM 配对机制

| 策略 | 说明 |
|:----:|:-----|
| pairing（默认） | 陌生用户需配对码 |
| open | 允许所有 DM |

---

### 安全检查清单

- ✅ 运行 `openclaw doctor` 检查配置
- ✅ 避免将 API 密钥提交到代码仓库
- ✅ 定期更新 OpenClaw 版本
- ✅ 敏感数据使用本地存储
- ✅ 飞书应用权限最小化
- ✅ 启用 DM 配对机制（默认）

---

## 七、未来展望

### 2026 年路线图

| 方向 | 预期功能 |
|:----:|:---------|
| AI 模型升级 | 更强推理能力 |
| 多模态增强 | 视频理解与分析 |
| 企业版 | 团队协作增强 |
| 插件市场 | 第三方技能商店 (ClawHub) |

---

### 对 ZZCreation 的价值

<div class="two-col">

<div class="feature-box">

**🎯 短期（Q1-Q2）**

飞书集成、客户沟通效率提升

</div>

<div class="feature-box">

**🎯 中期（Q3-Q4）**

主题乐园智能客服、数据分析

</div>

</div>

---

## 📚 参考资料

### 官方文档

- 官网：https://openclaw.ai
- 文档：https://docs.openclaw.ai
- GitHub：https://github.com/openclaw/openclaw

### 社区资源

- Discord：https://discord.gg/clawd
- ClawHub（插件市场）：https://clawhub.ai
- 社区展示：https://docs.openclaw.ai/start/showcase

### 核心文档

- VISION.md：https://github.com/openclaw/openclaw/blob/main/VISION.md
- 安全指南：https://docs.openclaw.ai/gateway/security
- Getting Started：https://docs.openclaw.ai/start/getting-started

### 视频教程

- Full Setup Walkthrough：https://www.youtube.com/watch?v=SaWSPZoPX34

### 创始人信息

- GitHub：https://github.com/steipete
- 推特：https://x.com/@steipete
- 博客：https://steipete.me

---

<!-- _class: lead -->

# 🦞 谢谢！

### 加入社区

- 官网：openclaw.ai
- 文档：docs.openclaw.ai
- Discord：discord.gg/clawd
- GitHub：github.com/openclaw/openclaw

---

*最后更新：2026年3月17日 | 版本：v1.2*