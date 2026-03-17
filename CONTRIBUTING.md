# Contributing

All contributions must follow the guidelines below to maintain consistency across the repository.

---

## 1. Tone

- Keep it brief and direct. Avoid jargon beyond the concept being explained.
- Every pattern needs two examples: one **Technical / Vibecoding**, one **Creative / Shower Thought**.
- Vibecoding examples should be written from the perspective of someone who knows *what* they want but not the technical words for it.

---

## 2. Pattern Template (Mandatory)

Every pattern entry in `PATTERNS.md` must follow this exact structure to ensure cross-platform aesthetics (GitHub + Obsidian):

```markdown
---

## The [Pattern Name] Pattern
**Category:** `[Tag]` · **Usability:** [1-5 Stars]

###### 📖 Definition
- [Core explanation. Link technical terms to GLOSSARY.md, e.g. [LLM](GLOSSARY.md#llm).]

###### 💡 Use Case
- [Relatable scenario explaining why you would use this pattern.]
- [Optional second scenario.]

###### ⚙️ Modifiers (Optional)
- [Optional variations or toggles the user can add to the base pattern.]

##### Example 1: Technical / Vibecoding
```text
[Prompt goes here]
```
##### Example 2: Creative / Shower Thought
```text
[Prompt goes here]
```
```

### Rules

1. Use `######` (h6) for Definition, Use Case, and Modifiers labels.
2. Use `#####` (h5) for Example labels.
3. Body text under Definition, Use Case, and Modifiers must be formatted as **bullet points** (`- `) to ensure proper indentation and readability without adopting faded blockquote styles.
4. Prompts must be inside ` ```text ``` ` code blocks for 1-click copying on GitHub.
5. Separate each pattern with `---`.

---

## 3. Glossary

If your pattern introduces a technical term not already in `GLOSSARY.md`, add it in **alphabetical order** using this format:

```markdown
### [Term Name]
> **Definition:** [Clear, accessible definition.]
> **Context:** [How it relates to prompt engineering.]
```

Link the term on its first use in your pattern's definition:
```markdown
- Getting an [LLM](GLOSSARY.md#llm) to roleplay...
```

---

## 4. File Reference

| File | Purpose |
|------|---------|
| `PATTERNS.md` | All active prompt pattern entries |
| `OBSOLETE_PATTERNS.md` | Archived patterns now baked into modern LLMs |
| `GLOSSARY.md` | Technical term definitions |
| `CONTRIBUTING.md` | This file — formatting rules |
| `README.md` | Repository overview and pattern index |
