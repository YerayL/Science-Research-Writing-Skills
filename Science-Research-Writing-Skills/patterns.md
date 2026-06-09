# Patterns & Techniques — With Application Instructions

Each pattern below includes: **when to trigger it**, **step-by-step instructions for the model to apply it**, and **output format**.

---

## 1. Reverse-Engineering Pattern

**Trigger**: User provides text from a published article or asks "analyze this paper's writing"

**How to apply**:
1. Take the user's provided text and split into sentences/paragraphs
2. For each unit, write what it is DOING (function), not what it is SAYING (content)
3. Generalize by replacing content-specific words with placeholders: "polymer" → "[this material]", "37°C" → "[temperature]"
4. Extract the exact vocabulary used for each function into a vocabulary bank
5. Note the verb tense used for each function
6. Map the extracted structure onto the relevant generic model — note matches and deviations
7. Test: can this model describe another article from the same journal?

**Output format**:
```
### Reverse-Engineered Model

| Sentence | Function | Vocabulary Used | Tense |
|----------|----------|----------------|-------|
| 1 | [function] | [key phrases] | [tense] |
| 2 | [function] | [key phrases] | [tense] |
...

### Vocabulary Bank (by function)
- Establishing significance: [phrases from article]
- Identifying gap: [phrases from article]
- Presenting the paper: [phrases from article]
...

### Comparison to Generic Model
- Matches: [components present]
- Deviations: [components absent or reordered]
```

---

## 2. The 4-Step Writing Strategy

**Trigger**: User is starting a new paper or new section from scratch

**How to apply**:
1. **Build the model**: Ask the user for 3-5 target articles in their field/journal. If they don't have them, use the generic model for their section. Help them identify sentence functions.
2. **Mine vocabulary**: From the target articles or the reference files, extract vocabulary for each function needed.
3. **Master grammar**: Identify the verb tense choices, passive/active patterns, and linking strategies used. Explain each choice's communicative function.
4. **Reinforce**: Remind the user to update their model as they read more papers in their field.

**Output**: A customized writing model + vocabulary bank for the user's specific field and target journal.

---

## 3. Narrative Wrap Application

**Trigger**: User's draft feels like a data dump; sentences lack commentary; text is hard to follow

**How to apply**:
For each sentence or data point, add three layers:

1. **Function layer** — Add a clause that tells the reader what function this information serves:
   - "To assess whether X affects Y, we..."
   - "A key question is whether..."
   - "This result suggests that..."

2. **Evaluation layer** — Add commentary on what the data means:
   - Instead of "The yield was 43%" → "The yield was only 43%, indicating that..."
   - Instead of "X increased" → "X increased substantially, reaching..."

3. **Direction layer** — Add language that shows where the argument is going:
   - "This finding raises the question of whether..."
   - "To explore this further, we..."
   - "Taken together, these results suggest that..."

**Trade-off**: Dense narrative wrap can feel heavy-handed. Calibrate to your target journal's style — reverse-engineer their narrative density.

---

## 4. Verb Tense Strategy — Application

**Trigger**: User's draft has inconsistent tenses; user unsure which tense to use

**How to apply**:
Go through the text sentence by sentence and apply this decision tree:

```
Is this sentence about...
├── An established fact or permanent truth?
│   → Present Simple ("PLA is biodegradable")
├── Something you or others did (a specific, completed action)?
│   → Past Simple ("We measured..." / "Smith et al. found...")
├── A trend or area of research linking past to present?
│   → Present Perfect ("Recent studies have investigated...")
├── What the paper/section/figure does?
│   → Present Simple ("This paper presents..." / "Figure 1 shows...")
├── A method step?
│   → Past Simple ("Cells were incubated at 37°C")
├── A result you want to present tentatively?
│   → Past Simple ("The temperature increased by 15%")
├── A result you are confident is a permanent finding?
│   → Present Simple ("X is linearly related to Y")
└── An achievement or contribution?
    → Present Perfect or Present Simple ("We have demonstrated...")
```

**Critical check**: Using Present Simple for your own results = asserting they are permanent truths. Make sure this is warranted. When in doubt, check what your target articles do.

---

## 5. Certainty Continuum — Application

**Trigger**: User overclaims or underclaims; language doesn't match evidence strength

**How to apply**:
For each claim in the Results/Discussion, run this audit:

```
1. What is the actual evidence?
   ├── Randomized controlled experiment → can support causal claims
   ├── Observational study → can support associations
   ├── Correlation analysis → correlation only
   └── Exploratory analysis → speculation only

2. What verb does the user use?
   ├── demonstrate, prove → requires proof-level evidence
   ├── show, indicate, reveal → requires strong evidence
   ├── suggest, imply, point to → moderate evidence OK
   ├── may, might, could → any evidence level OK (explicitly tentative)
   └── be linked to, be associated with → explicitly non-causal

3. Does the verb match the evidence?
   ├── Match → keep
   └── Mismatch → replace with appropriate-level verb
```

**Critical distinction**: "X produced Y" (directional cause) ≠ "X is linked to Y" (no direction) ≠ "X originated in Y" (reverse direction). Mismatches here are among the most common reviewer criticisms.

---

## 6. Achievement-Contribution Pattern

**Trigger**: Discussion or Conclusion doesn't clearly state what the study accomplished

**How to apply**:

1. **Locate the aim statement** from the Introduction (Component 4). Identify the exact verb used: "The aim of this study was to [VERB] X"

2. **Check the Discussion/Conclusion**: Does it use the SAME verb to state achievement?
   - If the aim was "to identify X" → achievement should say "We identified X" (not "We found X" or "We discovered X")
   - Trackability is the goal. The reader should not have to guess.

3. **Separate achievement from contribution**:
   - Achievement (internal): "We [same verb from aim] X"
   - Contribution (outward): "This [advances/opens/extends/enables] Y"

4. **Verify specificity**: "This study makes an important contribution to the field" is too generic. What specifically advances? What specifically opens up?

---

## 7. Sentence-Linking Patterns — Application

**Trigger**: Paragraphs feel choppy; text doesn't flow

**How to apply** (in order of effectiveness):

1. **This/These + noun** (most effective in science writing):
   - Before: "The nanoparticles were characterized by TEM. The images showed uniform size distribution."
   - After: "The nanoparticles were characterized by TEM. **These images** showed a uniform size distribution."

2. **Repetition linkage** (end one sentence with key term, start next with same term):
   - "...the reaction yielded predominantly the para isomer. **The para isomer** was then..."

3. **Connector words** (use sparingly — overuse feels mechanical):
   - However, Therefore, In addition, Furthermore, Consequently, Moreover

4. **Signal words** (flag what's coming):
   - problem, issue, challenge, gap, limitation, question, opportunity

**Audit process**: Read each sentence-initial word. If consecutive sentences start with unrelated nouns, insert linking. Aim for ~70% of sentences to have a visible link to the previous sentence.

---

## 8. Title Reverse-Engineering — Application

**Trigger**: User needs to write or improve a title

**How to apply**:
1. Collect 10-20 titles from the user's target journal (or ask the user to provide them)
2. Analyze each for:
   - Word count
   - Structure: noun phrase vs. full sentence vs. question
   - Content elements present: topic, method, finding, application, material, system
   - Information order: what comes first?
3. Identify the dominant pattern
4. Map the user's paper onto this pattern
5. Verify: does the title's promise match what the paper actually delivers?
6. Check against the Title Quality Checklist (see Writing the Title):
   - Keywords present?
   - Acronyms justified?
   - Unambiguous?
   - Searchable?

**Output**: 2-3 title options following the target journal's convention, with annotations.
