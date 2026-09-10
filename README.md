# 🔬 Science Research Writing — AI Writing Assistant

[中文版](./README_zh.md)

> **Your personal AI coach for STEMM research papers. Not a knowledge base — an active writing partner that drafts, revises, reviews, and guides.**

Built on Hilary Glasman-Deal's *"Science Research Writing: For Native and Non-Native Speakers of English"* (2nd Ed., Imperial College London), this skill transforms the book's frameworks into an **actionable writing assistant** for Claude Code and CodeX.

---

## ✨ What This Skill Does

| Mode | Trigger | You Get |
|------|---------|---------|
| 🔧 **Revise & Polish** | Paste your draft text | Improved text with annotated changes |
| ✍️ **Draft from Notes** | Provide raw data / bullet points / claims | Structured section draft following generic models |
| 🔍 **Diagnostic Review** | Ask for a review | Audit report with severity ratings + specific fixes |
| 🧪 **Reverse-Engineer** | Provide published article text | Reusable writing model + vocabulary bank |
| 🗺️ **Interactive Guide** | "Help me write my [section]" | Step-by-step walk-through for each component |

### 🎯 Covers All Paper Sections

Abstract · Introduction · Methods · Results · Discussion · Conclusion · Title

### 🧠 Key Frameworks Applied

- **Generic Writing Models** — proven sentence-function templates for each section
- **Certainty Continuum** — match verb strength to evidence level (never overclaim or underclaim)
- **Verb Tense Strategy** — tense as a signal of information status and confidence
- **Narrative Wrap** — scaffold your data with meaning so readers can't misunderstand
- **Achievement vs. Contribution** — trackable internal success + outward-facing impact
- **Sentence Linking** — this/these + noun, repetition linkage, signal words
- **Evaluative Comments** — no naked numbers; every data point gets commentary
- **Pre-submission Checklist** — 10-point audit before you submit

---

## 📦 Installation

### Claude Code

Copy the `Science-Research-Writing-Skills/` subdirectory into your Claude Code skills directory. `<repository-root>` is the repository root containing this README:

```bash
# Windows (PowerShell) — replace <repository-root> with your repository location
$skillSource = "<repository-root>\Science-Research-Writing-Skills"
$skillDestination = "$env:USERPROFILE\.claude\skills\Science-Research-Writing-Skills"
New-Item -ItemType Directory -Force -Path $skillDestination | Out-Null
Copy-Item -Recurse -Force "$skillSource\*" $skillDestination

# macOS / Linux
mkdir -p ~/.claude/skills/Science-Research-Writing-Skills
cp -R "/path/to/repository/Science-Research-Writing-Skills/." ~/.claude/skills/Science-Research-Writing-Skills/
```

Then restart Claude Code.

### CodeX

Copy the `Science-Research-Writing-Skills/` subdirectory into your CodeX skills directory. `<repository-root>` is the repository root containing this README:

```bash
# Windows (PowerShell) — replace <repository-root> with your repository location
$skillSource = "<repository-root>\Science-Research-Writing-Skills"
$skillDestination = "$env:USERPROFILE\.codex\skills\Science-Research-Writing-Skills"
New-Item -ItemType Directory -Force -Path $skillDestination | Out-Null
Copy-Item -Recurse -Force "$skillSource\*" $skillDestination

# macOS / Linux
mkdir -p ~/.codex/skills/Science-Research-Writing-Skills
cp -R "/path/to/repository/Science-Research-Writing-Skills/." ~/.codex/skills/Science-Research-Writing-Skills/
```

---

## 🚀 Usage

Invoke the skill with `/Science-Research-Writing-Skills` followed by your request. The assistant auto-detects what you need:

### 🔧 Revise & Polish

```
/Science-Research-Writing-Skills
Here's my Introduction — polish it.
```

### ✍️ Draft from Notes

```
/Science-Research-Writing-Skills
Write the Results section. Here's what we found:
- XRD showed crystalline phase at 600°C
- Tensile strength increased by 40% with 5wt% filler
- SEM images showed uniform dispersion
```

### 🔍 Diagnostic Review

```
/Science-Research-Writing-Skills
Review my Discussion section.
```

### 🧪 Reverse-Engineer a Target Article

```
/Science-Research-Writing-Skills
Analyze this Introduction from a Nature Materials paper.
```

### 🗺️ Interactive Guide

```
/Science-Research-Writing-Skills
Help me write my Abstract. My paper is about...
```

> 💡 **Pro tip**: You can also use shorthand — just describe what you need. The assistant figures out the right mode.

---

## 📂 Project Structure

```
Science-Research-Writing-Skills/
├── Science-Research-Writing-Skills/
│   ├── SKILL.md                    # Main skill definition + operating instructions
│   ├── cheatsheet.md               # Quick audit checklists + fix guides
│   ├── patterns.md                 # 8 writing patterns with application steps
│   ├── glossary.md                 # Key terms defined
│   └── references/                 # Detailed reference files (read on demand)
│       ├── 00-introduction-writing-for-a-reader.md
│       ├── 01-writing-the-introduction.md
│       ├── 02-writing-about-methods.md
│       ├── 03-writing-about-results.md
│       ├── 04-writing-the-discussion.md
│       ├── 05-writing-the-conclusion.md
│       ├── 06-writing-the-abstract.md
│       ├── 07-writing-the-title.md
│       ├── 08-checklist-and-tips.md
│       ├── appendix-a-prefixes-in-science-writing.md
│       └── appendix-b-research-verbs.md
├── README.md                   # This file
└── README_zh.md                # 中文说明
```

---

## 📖 Based On

**Glasman-Deal, H.** (2021). *Science Research Writing: For Native and Non-Native Speakers of English* (2nd ed.). Imperial College Press.

The book's frameworks, models, and techniques have been extracted, organized, and transformed into an interactive AI assistant. All writing principles are grounded in the analysis of thousands of successfully published STEMM research articles.

---

## 🎓 Who This Is For

- 📝 **Graduate students** writing their first paper
- 🔬 **Postdocs & researchers** who want to write faster and better
- 🌍 **Non-native English speakers** navigating English-language science publishing
- 📊 **Anyone in STEMM** (Science, Technology, Engineering, Mathematics, Medicine) who wants their papers accepted at higher rates

---

## ⚙️ Platform Support

| Platform | Status |
|----------|--------|
| 🖥️ Claude Code (CLI) | ✅ Full support |
| 🖥️ Claude Code (Desktop App) | ✅ Full support |
| 💻 Claude Code (IDE extensions) | ✅ Full support |
| 🔧 CodeX | ✅ Full support |

---

<p align="center">
  <sub>🤖 Built for the AI-assisted science writing era. Based on evidence, not guesses.</sub>
</p>
