# 🔬 科研论文写作 — AI 写作助手

> **你的专属 STEMM 论文 AI 写作教练。不是知识库——而是能帮你起草、修改、审阅和指导的主动型写作伙伴。**

本技能基于 Hilary Glasman-Deal 所著 *《Science Research Writing: For Native and Non-Native Speakers of English》*（第二版，帝国理工学院出版社），将书中的框架转化为适用于 Claude Code 和 CodeX 的**可操作写作助手**。

---

## ✨ 能做什么

| 模式 | 触发方式 | 你将获得 |
|------|---------|---------|
| 🔧 **修改润色** | 粘贴你的草稿 | 改进后的文本 + 带注释的修改说明 |
| ✍️ **根据笔记起草** | 提供原始数据 / 要点 / 声明 | 遵循通用模型的结构化章节草稿 |
| 🔍 **诊断审查** | 要求审阅 | 带严重程度评级的审计报告 + 具体修复方案 |
| 🧪 **逆向工程** | 提供已发表文章的文本 | 可复用的写作模型 + 词汇库 |
| 🗺️ **互动指导** | "帮我写我的[某章节]" | 逐步引导，完成每个组成部分 |

### 🎯 涵盖所有论文章节

摘要 · 引言 · 方法 · 结果 · 讨论 · 结论 · 标题

### 🧠 应用的核心框架

- **通用写作模型** — 每个章节经过验证的句子功能模板
- **确定性连续谱** — 将动词强度与证据水平匹配（绝不夸大或低估）
- **动词时态策略** — 使用时态作为信息状态和信心的信号
- **叙事包裹** — 用意义支撑你的数据，让读者无法误解
- **成果 vs 贡献** — 可追踪的内部成功 + 对外的学科影响
- **句子衔接** — this/these + 名词、复现衔接、信号词
- **评价性评论** — 拒绝裸数据；每个数据点都配有评论
- **投稿前检查清单** — 投稿前的 10 项审计

---

## 📦 安装

### Claude Code

**方式一：一键安装**

在 Claude Code 中输入：

```
/install-skill <项目文件夹路径>
```

**方式二：手动安装**

将整个项目文件夹复制到 Claude Code 的 skills 目录：

```bash
# Windows (PowerShell) — 将 <path> 替换为你的项目位置
$path = "<path>\Science-Research-Writing-Skills"
Copy-Item -Recurse $path "$env:USERPROFILE\.claude\skills\Science-Research-Writing-Skills"

# macOS / Linux
cp -r /path/to/Science-Research-Writing-Skills ~/.claude/skills/Science-Research-Writing-Skills
```

**方式三：符号链接（保持同步更新）**

```bash
# macOS / Linux
ln -s /path/to/Science-Research-Writing-Skills ~/.claude/skills/Science-Research-Writing-Skills

# Windows (PowerShell, 管理员权限) — 将 <path> 替换为你的项目位置
$target = "<path>\Science-Research-Writing-Skills"
New-Item -ItemType SymbolicLink -Path "$env:USERPROFILE\.claude\skills\Science-Research-Writing-Skills" -Target $target
```

安装后重启 Claude Code。

### CodeX

**方式一：通过 CodeX 扩展市场**

```
/extensions install Science-Research-Writing-Skills
```

**方式二：手动安装**

将项目文件夹复制到 CodeX 的 skills 目录：

```bash
# Windows (PowerShell) — 将 <path> 替换为你的项目位置
$path = "<path>\Science-Research-Writing-Skills"
Copy-Item -Recurse $path "$env:APPDATA\CodeX\skills\Science-Research-Writing-Skills"

# macOS / Linux
cp -r /path/to/Science-Research-Writing-Skills ~/.codex/skills/Science-Research-Writing-Skills
```

---

## 🚀 使用方法

使用 `/Science-Research-Writing-Skills` 调用技能，后面跟上你的需求。助手会自动判断你需要什么：

### 🔧 修改润色

```
/Science-Research-Writing-Skills
这是我的引言部分，帮我润色：

[你的草稿文本]
```

### ✍️ 根据笔记起草

```
/Science-Research-Writing-Skills
帮我写结果部分。我们的发现如下：
- XRD 显示在 600°C 出现晶相
- 添加 5wt% 填料后拉伸强度提高 40%
- SEM 图像显示均匀分散
```

### 🔍 诊断审查

```
/Science-Research-Writing-Skills
审阅我的讨论部分：

[你的草稿文本]
```

### 🧪 逆向工程目标期刊文章

```
/Science-Research-Writing-Skills
分析这篇 Nature Materials 论文的引言：

[粘贴已发表文章的引言]
```

### 🗺️ 互动指导

```
/Science-Research-Writing-Skills
帮我写摘要。我的论文是关于……
```

> 💡 **提示**：你也可以用简写——只需描述你的需求并粘贴文本，助手会自动匹配正确的模式。

---

## 📂 项目结构

```
Science-Research-Writing-Skills/
├── SKILL.md                    # 主技能定义 + 操作指令
├── cheatsheet.md               # 快速审计清单 + 修复指南
├── patterns.md                 # 8 种写作模式及操作步骤
├── glossary.md                 # 关键术语定义
├── references/                 # 详细参考文件（按需读取）
│   ├── 00-introduction-writing-for-a-reader.md
│   ├── 01-writing-the-introduction.md
│   ├── 02-writing-about-methods.md
│   ├── 03-writing-about-results.md
│   ├── 04-writing-the-discussion.md
│   ├── 05-writing-the-conclusion.md
│   ├── 06-writing-the-abstract.md
│   ├── 07-writing-the-title.md
│   ├── 08-checklist-and-tips.md
│   ├── appendix-a-prefixes-in-science-writing.md
│   └── appendix-b-research-verbs.md
├── README.md                   # 英文说明
└── README_zh.md                # 本文件
```

---

## 📖 基于原著

**Glasman-Deal, H.** (2021). *Science Research Writing: For Native and Non-Native Speakers of English* (2nd ed.). Imperial College Press.

本书的框架、模型和技巧已被提取、整理并转化为交互式 AI 助手。所有写作原则均基于对数千篇成功发表的 STEMM 研究文章的分析。

---

## 🎓 适用人群

- 📝 正在写第一篇论文的**研究生**
- 🔬 想写得更快更好的**博士后和科研人员**
- 🌍 正在应对英文学术发表的**非英语母语者**
- 📊 希望提高论文接收率的**所有 STEMM 领域研究者**（科学、技术、工程、数学、医学）

---

## ⚙️ 平台支持

| 平台 | 状态 |
|----------|--------|
| 🖥️ Claude Code (命令行) | ✅ 完全支持 |
| 🖥️ Claude Code (桌面应用) | ✅ 完全支持 |
| 💻 Claude Code (IDE 扩展) | ✅ 完全支持 |
| 🔧 CodeX | ✅ 完全支持 |

---

<p align="center">
  <sub>🤖 为 AI 辅助科研写作时代而生。基于证据，而非猜测。</sub>
</p>
