# 🏛️ Private Board Meeting Skill

**私董会决策框架 —— 7位顶级商业顾问，一场没有客套的决策审判。**

模拟 Steve Jobs、Elon Musk、Warren Buffett、Jeff Bezos、任正非、段永平、Peter Thiel 七位顶级商业顾问，对你的重大商业决策进行结构化审议。每人带着自己的人格、思维模型和价值观，给出尖锐、不中立、不客套的真实判断。

---

## ✨ 特点

- **7 位真实人格顾问** —— 不是 AI 中性化包装，Jobs 会说"这很烂"，Musk 会说"为什么不能快 10 倍"
- **强制分歧** —— 禁止全员共识，至少 2 人持不同立场
- **决策锚定四件套** —— 拒绝模糊决策，必须说清楚主体、内容、时间、约束
- **一句刺痛真相** —— 每次会议必须输出 1 句可能冒犯你的真实判断
- **快速模式** —— 时间紧迫时压缩为闪电版

---

## 🚀 安装

### Agent Skills Open Standard（推荐）

支持 20+ 平台，选择你的工具：

**Claude Code:**
```bash
git clone https://github.com/mastercodeai/private-board-meeting-skill.git ~/.claude/skills/private-board-meeting-skill
```

**Cursor:**
```bash
git clone https://github.com/mastercodeai/private-board-meeting-skill.git .cursor/skills/private-board-meeting-skill
```

**GitHub Copilot:**
```bash
git clone https://github.com/mastercodeai/private-board-meeting-skill.git .github/skills/private-board-meeting-skill
```

**Cline:**
```bash
git clone https://github.com/mastercodeai/private-board-meeting-skill.git ~/.cline/skills/private-board-meeting-skill
```

**Windsurf:**
```bash
git clone https://github.com/mastercodeai/private-board-meeting-skill.git ~/.codeium/windsurf/skills/private-board-meeting-skill
```

**Gemini CLI:**
```bash
git clone https://github.com/mastercodeai/private-board-meeting-skill.git ~/.gemini/skills/private-board-meeting-skill
```

**Codex CLI / OpenCode / Goose:**
```bash
git clone https://github.com/mastercodeai/private-board-meeting-skill.git ~/.agents/skills/private-board-meeting-skill
```

**Roo Code:**
```bash
git clone https://github.com/mastercodeai/private-board-meeting-skill.git ~/.roo/skills/private-board-meeting-skill
```

---

## 📖 使用

### 标准模式

```
/private-board-meeting

我是一个 SaaS 公司的 CEO，50人团队，年营收 500 万。
正在考虑是否从 B 端转型做 C 端。
时间窗口：3 个月内必须决定。
真实约束：账上现金只够撑 8 个月，团队没有 C 端经验。
```

### 快速模式

```
/private-board-meeting 快速私董会

决策：要不要砍掉免费套餐，只保留付费版？
约束：当前 80% 用户是免费用户，但他们贡献了口碑传播。
```

---

## 🎭 七位顾问

| # | 顾问 | 核心视角 | 风格 |
|---|------|----------|------|
| 1 | **Steve Jobs** | 产品偏执，减法 > 加法 | 尖锐、傲慢、不留情面 |
| 2 | **Elon Musk** | 第一性原理，10x 思维 | 不耐烦、直击本质、跳跃性 |
| 3 | **Warren Buffett** | 安全边际，能力圈 | 温和但坚定、保守 |
| 4 | **Jeff Bezos** | 客户痴迷，Day 1 心态 | 逻辑严密、长期主义 |
| 5 | **任正非** | 危机意识，组织能力 | 朴素、深沉、军事化 |
| 6 | **段永平** | 本分，平常心，做对的事 | 平静、直接、直击本质 |
| 7 | **Peter Thiel** | 反共识，垄断思维，0→1 | 冷峻、哲学化、反直觉 |

---

## 📋 输出结构

### 1. 决策锚定四件套
确认主体、内容、时间窗口、真实约束。缺一不开始。

### 2. 主席预审
识别真问题 → 推荐 A/B/C 三条路径（赔率×胜率×成本）→ 选定一条送审。

### 3. 七人顾问团审议
每人输出：立场（通过/有条件/否决）+ 3 个理由 + 追问 + 签名语录。

### 4. 主席综合裁决
投票统计 → 共识点 → 关键分歧 → 最终建议 + 行动清单 → 一句刺痛真相。

---

## 📁 文件结构

```
private-board-meeting-skill/
├── SKILL.md                      # 主框架（中文，199行）
├── AGENTS.md                     # 跨平台兼容文件
├── README.md                     # 本文件
└── references/
    ├── advisor-profiles.md       # 7位顾问深度人格档案
    └── output-templates.md       # 输出模板（含快速模式）
```

---

## 🤝 适配平台

本 skill 遵循 [Agent Skills Open Standard](https://agentskills.io)，兼容：

Claude Code · Cursor · GitHub Copilot · Cline · Windsurf · Gemini CLI · Codex CLI · OpenCode · Goose · Roo Code · Kilo Code · Kiro · Aider · Continue.dev · Zed · 以及更多

---

## 📄 License

MIT

---

## 💬 反馈

这个框架帮助很多人在重大决策中获得了清晰的判断。如果你觉得有用，欢迎 star ⭐ 和提 issue。
