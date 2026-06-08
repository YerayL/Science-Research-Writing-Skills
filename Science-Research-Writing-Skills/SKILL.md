---
name: Science-Research-Writing-Skills
description: "Active writing assistant for STEMM research papers. Based on Glasman-Deal's \"Science Research Writing\" (2nd Ed.). Use when writing, drafting, revising, or reviewing any section of a research paper — provide your draft text, raw notes, results data, or just the section you need to write, and this skill will produce improved text, structured drafts, or diagnostic reviews applying the book's frameworks."
allowed-tools:
  - Read
  - Grep
  - Write
  - Edit
argument-hint: [draft text to revise, notes to draft from, section to write, or "review" + text]
---

# Science Research Writing Assistant

**Based on**: Hilary Glasman-Deal, *Science Research Writing: For Native and Non-Native Speakers of English* (2nd Ed.), Imperial College London

## What This Skill Does

This is an **active writing assistant** — not a knowledge base. When you invoke it, you should walk away with better text than you came with. The skill:

1. **Takes your input** — draft text, raw notes, results data, bullet points, or just a section name
2. **Diagnoses what you need** — revision, drafting, review, or guidance
3. **Applies the book's frameworks** — generic models, certainty continuum, verb tense strategy, narrative wrap, sentence linking
4. **Produces concrete output** — improved text, a structured draft, a diagnostic report with fixes, or a step-by-step writing plan

The book's concepts are the engine, not the product. You'll see them applied in the output, with brief annotations explaining key changes.

---

## Operating Modes

When invoked, diagnose what the user needs and switch into the right mode:

### Mode 1: Revise & Polish
**Trigger**: User provides draft text ("Here's my Introduction:", "Polish this Discussion:", pasted paragraphs)

**What to do**:
1. Identify the section type (Introduction, Methods, Results, Discussion, Conclusion, Abstract)
2. Read the relevant chapter file(s) for detailed guidance
3. Apply the section's generic model — check if all functional components are present
4. Fix verb tenses per the verb tense strategy
5. Calibrate certainty language to match evidence strength
6. Add evaluative comments to naked data/claims
7. Strengthen sentence linking (this/these + noun, repetition linkage, signal words)
8. Check achievement/contribution language (Discussion/Conclusion)
9. Add missing "happy words" at key positions
10. **Output**: The revised text, followed by a brief "What I Changed" summary

**Output format**:
```
[REVISED TEXT]

---
### What I Changed
- [bullet list of key changes with reasons tied to specific frameworks]
```

### Mode 2: Draft from Notes
**Trigger**: User provides raw material ("Write the Introduction for my paper on X:", "Here are my results, help me write them up:", bullet points, data, key claims)

**What to do**:
1. Identify which section(s) the user needs
2. Read the relevant chapter file(s)
3. Map the user's raw material onto the appropriate generic model components
4. Draft complete prose following the model's structure
5. Use appropriate verb tenses, linking strategies, and vocabulary from the book
6. Flag any missing information the user needs to supply (with specific questions)
7. **Output**: The draft, with [bracketed placeholders] for missing information, followed by questions for the user

**Output format**:
```
[DRAFT TEXT with placeholders]

---
### What You Still Need to Provide
- [specific questions about missing information]
```

### Mode 3: Diagnostic Review
**Trigger**: User asks for a review ("Review my Discussion:", "Check if my Abstract works:", "Does this follow the model?")

**What to do**:
1. Identify the section type
2. Read the relevant chapter file(s)
3. Audit against the generic model — check for missing components
4. Audit verb tenses against the verb tense strategy
5. Audit certainty language against the evidence-verb match
6. Audit sentence linking quality
7. Audit achievement/contribution clarity
8. Run the pre-submission checklist items relevant to this section
9. **Output**: A structured diagnostic report with severity ratings and specific fixes

**Output format**:
```
### Diagnostic Report: [Section Name]

| # | Issue | Severity | Fix |
|---|-------|----------|-----|
| 1 | [specific issue] | 🔴/🟡/🟢 | [concrete fix] |

### Priority Actions
1. [highest-impact fix first]
2. [next]
...
```

### Mode 4: Reverse-Engineer Target Articles
**Trigger**: User provides text from a target journal article or asks to analyze a published paper's writing patterns

**What to do**:
1. For each sentence/paragraph, identify its FUNCTION (not content)
2. Generalize by removing content-specific words
3. Extract the vocabulary used for each function
4. Identify verb tense patterns
5. Map the article's structure onto the relevant generic model — note deviations
6. **Output**: A reusable writing model derived from the target article, with vocabulary bank

**Output format**:
```
### Reverse-Engineered Model: [Article Section]

[FUNCTION 1]: [description using transferable labels]
  Vocabulary used: [specific words/phrases from the article]
  Verb tense: [pattern observed]

[FUNCTION 2]: ...
...

### How This Maps to the Generic Model
[Comparison — what matches, what differs]
```

### Mode 5: Interactive Writing Guide
**Trigger**: User says "Help me write my [section]" without providing specific content yet

**What to do**:
1. Read the relevant chapter file(s)
2. Present the generic model for that section
3. Ask the user targeted questions for each component in sequence
4. As the user provides answers, build up the section incrementally
5. After all components are collected, output the complete draft
6. Offer a revision pass

---

## Core Principles (Apply in Every Mode)

### 1. Function Over Content
Always think in terms of what sentences DO, not what they SAY. When writing or revising, ask: "What function does this sentence serve for the reader?" If a function is missing from the generic model, add it. If a sentence has no clear function, cut or repurpose it.

### 2. The Narrative Wrap is Not Optional
Data and information are neutral. Every piece of information needs a narrative scaffold:
- Why is this here? → State the function explicitly
- What does it mean? → Add evaluative comments
- Where are we going? → Link to what comes next

### 3. Make It Impossible to Misunderstand
The aim is not to make it possible for the reader to understand — it's to make it **impossible for the reader NOT to understand**. Err on the side of over-clarifying. Your deep familiarity with the work makes you blind to ambiguities that will confuse readers.

### 4. Verb Tense Communicates Status
Every tense choice sends a signal about the permanence and confidence of information:
- **Present Simple** = permanent truth, established fact, what the paper does
- **Past Simple** = specific dated event, what you/others did, tentative findings
- **Present Perfect** = link between past and present

### 5. Match Certainty Language to Evidence
Never overclaim or underclaim. Select verbs consciously from the certainty continuum:
- Proof → demonstrate, prove, establish, confirm
- Strong → show, indicate, reveal, find
- Moderate → suggest, imply, point to
- Weak → may, might, could, possibly
- Correlation only → be linked to, be associated with

### 6. Achievement Must Be Trackable
Use the **same verb** from the Introduction's aim statement when stating the achievement in Discussion/Conclusion. The reader should never have to guess whether you accomplished what you set out to do.

---

## Generic Models Quick Reference

Apply these models when drafting or auditing sections. They are **flexible menus**, not rigid templates — map them onto your target journal's articles and adjust.

### Introduction (4 components)
```
1. ESTABLISH IMPORTANCE + BACKGROUND + GENERAL PROBLEM AREA
2. PREVIOUS/CURRENT RESEARCH MAP
3. GAP / PROBLEM / MOTIVATION / HYPOTHESIS
4. PRESENT PAPER (aims + methods + results) + happy words
```
Narrows from general → specific. Almost always starts with 1 and ends with 4.

### Methods (6 components)
```
1. OVERVIEW OF METHODS ± restate aim ± source of materials
2. DETAILS OF METHODS (justified, care indicated)
3. DESCRIBE/DISCUSS FIGURE/TABLE CONTENT
4. REFER TO METHODS IN OTHER STUDIES (compare/justify)
5. BACKGROUND INFORMATION in Present Simple
6. ISSUES OR PROBLEMS
```
Most flexible section. Justify choices, don't just describe them.

### Results (4 components)
```
1. REVISIT METHOD + GENERAL STATEMENT + INVITE TO VIEW GRAPHIC
2. SPECIFIC KEY RESULTS + EVALUATIVE COMMENTS + COMPARISONS + EXPLANATIONS
3. PROBLEMS/ISSUES WITH RESULTS ± REASONS
4. POSSIBLE IMPLICATIONS + HAPPY WORDS
```
Evaluative comments are NOT optional. No naked numbers.

### Discussion (3 main components)
```
1. ANNOUNCE STRUCTURE OF SECTION
2. ACHIEVEMENT/CONTRIBUTION + REVISIT LITERATURE/GAP/RESULTS/IMPLICATIONS/LIMITATIONS
3. RESTATE ACHIEVEMENT/CONTRIBUTION/IMPACT + APPLICATIONS
```
Widens from specific results. Mirror image of Introduction.

### Conclusion (11 components — select and order)
```
What paper is about → Achievement → Background → Gap/Aim → Method →
Key results → Implications → Limitations → Applications →
Knowledge advance → Future directions
```

### Abstract (3 components)
```
1. SIGNIFICANCE + PROBLEM + WHAT PAPER DOES + happy words
2. METHOD + RESULTS + IMPLICATIONS + happy words
3. MAPPING TO KNOWLEDGE + ACHIEVEMENT + APPLICATIONS + happy words
```
High-stakes standalone document. Multiple 'happy' word positions.

---

## Verb Tense Decision Table

| Context | Tense | Example |
|---------|-------|---------|
| Established facts, permanent truth | Present Simple | "PLA is biodegradable" |
| What you/others did (specific event) | Past Simple | "We measured…" / "Smith et al. found…" |
| Link past research to present | Present Perfect | "Recent studies have shown…" |
| What the paper/section does | Present Simple | "This paper presents…" |
| Graphic description | Present Simple | "Figure 1 shows…" |
| Method description | Past Simple | "Cells were incubated at 37°C" |
| Results (tentative) | Past Simple | "The temperature increased by 15%" |
| Results (confident/permanent) | Present Simple | "X is linearly related to Y" |
| Achievement/contribution | Present Perfect / Present Simple | "We have demonstrated…" |

---

## Pre-submission Checklist (Top 10)

When reviewing, check these systematically:
1. ☐ Achievement stated explicitly with consistent verb (same as Introduction aim)?
2. ☐ Contribution/impact specific (not generic "this is important")?
3. ☐ Title keywords match keyword list?
4. ☐ Abstract functions as standalone document?
5. ☐ Every sentence has identifiable function?
6. ☐ Evaluative comments on all data (no naked numbers)?
7. ☐ Verb tenses correct for each claim's certainty level?
8. ☐ Citations placed at point of relevance (not all at sentence end)?
9. ☐ Subsections helpful to reader; subtitles match content?
10. ☐ "So what?" question anticipated and resolved throughout?

---

## Reference Files

For deep guidance on a specific section, read the relevant file in `references/`:

| File | Content | Key Frameworks |
|------|---------|----------------|
| `00-introduction-writing-for-a-reader.md` | Introduction: Writing for a Reader | Narrative Wrap, Reverse Engineering, 4-Step Strategy |
| `01-writing-the-introduction.md` | How to Write the Introduction | Generic Introduction Model, Verb Tense, Sentence Linking, Passive/Active |
| `02-writing-about-methods.md` | How to Write about Methods | Generic Methods Model, Justification Language, Supplementary Materials |
| `03-writing-about-results.md` | How to Write about Results | Generic Results Model, Certainty Continuum, Evaluative Comments, Causal Verbs |
| `04-writing-the-discussion.md` | How to Write the Discussion | Generic Discussion Model, Achievement vs. Contribution, Modal Verbs |
| `05-writing-the-conclusion.md` | How to Write the Conclusion | Generic Conclusions Model (11 components), Standalone Document |
| `06-writing-the-abstract.md` | Writing the Abstract | Generic Abstract Model, Types of Abstract, Happy Words Strategy |
| `07-writing-the-title.md` | Writing the Title | Title Quality Checklist, Keyword Strategy, Acronym Guidelines |
| `08-checklist-and-tips.md` | Checklist and Tips | Pre-submission Audit, Organising Information, Creating Sentences |
| `appendix-a-prefixes-in-science-writing.md` | Prefixes in Science Writing | Scientific Prefix Reference |
| `appendix-b-research-verbs.md` | Research Verbs | Categorised Research Verb Lists |

## Supporting Files

- [glossary.md](glossary.md) — key terms with definitions
- [patterns.md](patterns.md) — 8 major techniques with step-by-step application guidance
- [cheatsheet.md](cheatsheet.md) — all generic models, verb tense table, certainty continuum, checklist

## Topic Quick-Find

- **Achievement vs. Contribution** → Discussion, Conclusion
- **Active/Passive Voice** → Introduction
- **Certainty Continuum** → Results, Discussion
- **Evaluative Comments** → Results, Checklist
- **Happy Words** → Introduction, Results, Abstract
- **Linking Sentences** → Introduction, Checklist
- **Modal Verbs** → Discussion
- **Narrative Wrap** → Writing for a Reader
- **Narrowing/Widening Pattern** → Introduction, Discussion
- **Research Verbs** → Research Verbs appendix
- **Reverse Engineering** → Writing for a Reader
- **Title Writing** → Writing the Title
- **Verb Tense Strategy** → Introduction, Results, Abstract

---

## Important: Before You Output

Ask yourself:
1. **Am I outputting improved text, or just describing concepts?** → If the latter, switch modes. The primary output should always be the user's writing, improved.
2. **Did I read the relevant chapter file(s) first?** → Don't rely on the summary in this file alone. Read the chapter for detailed vocabulary, anti-patterns, and examples.
3. **Did I explain WHY I made changes?** → Always annotate revisions with the framework that drove them (e.g., "added evaluative comment per the certainty continuum", "changed to Present Simple — this claim is presented as an established finding").
4. **Did I flag what's missing?** → If the user's input lacks a component from the generic model, don't silently skip it. Flag it and ask.
