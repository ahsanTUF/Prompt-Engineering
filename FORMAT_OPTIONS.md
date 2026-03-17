# Format Options — Pick Your Favorite

This file demonstrates 3 different visual layouts for our prompt pattern entries. Push this to GitHub, view it there, and pick the one that looks best rendered.

Each option below shows the **Persona Pattern** as a sample entry so you can compare apples to apples.

---
---

# Option A: "The Card Layout"
*Uses blockquote cards + collapsible `<details>` for examples.*

---

## The Persona Pattern
> `Roleplay/Jailbreak` · `Usability: 5/5`
>
> Getting an [LLM](GLOSSARY.md#llm) to roleplay as a specific person with a specific designation. A lot of [jailbreaking](GLOSSARY.md#jailbreaking) is done through this.

**Why use it?** Bypass rigid constraints or frame guidance through a creative lens — like having a brutally honest senior game dev mentor.

<details>
<summary><strong>📋 Example 1: Vibecoding</strong></summary>

```text
Act as a senior database architect who is brutal, honest, and to the point. Review the schema I am about to paste and tell me exactly why it will fail at scale.
```

</details>

<details>
<summary><strong>💭 Example 2: Shower Thought</strong></summary>

```text
Act as a speech therapist and tell me what a 3 year old meant when he said, "I need way woy."
```

</details>

---
---

# Option B: "The Table-Driven Layout"
*Uses a metadata table at the top of each pattern. Very scannable and documentation-like.*

---

## The Persona Pattern

| Category | Usability | Core Idea |
|----------|-----------|-----------|
| `Roleplay/Jailbreak` | ⭐⭐⭐⭐⭐ | Get the AI to *become* someone specific. |

Getting an [LLM](GLOSSARY.md#llm) to roleplay as a specific person with a specific designation. A lot of [jailbreaking](GLOSSARY.md#jailbreaking) is done through this.

**Why use it?** Bypass rigid constraints or frame technical guidance through a creative lens.

#### Example 1: Vibecoding
```text
Act as a senior database architect who is brutal, honest, and to the point. Review the schema I am about to paste and tell me exactly why it will fail at scale.
```

#### Example 2: Shower Thought
```text
Act as a speech therapist and tell me what a 3 year old meant when he said, "I need way woy."
```

---
---

# Option C: "The Minimalist Typographic" (Recommended)
*Relies purely on typography hierarchy — bold, italic, blockquote, and sub-headers. No tables, no icons, no details tags. Just clean and aggressive.*

---

## The Persona Pattern
**`Roleplay / Jailbreak`** · Usability: ★★★★★

> Getting an [LLM](GLOSSARY.md#llm) to roleplay as a specific person with a specific designation. A lot of [jailbreaking](GLOSSARY.md#jailbreaking) is done through this.

*Useful for bypassing rigid constraints or framing technical guidance through a creative lens — like having a brutally honest senior game dev mentor.*

#### Example 1: Vibecoding
```text
Act as a senior database architect who is brutal, honest, and to the point. Review the schema I am about to paste and tell me exactly why it will fail at scale.
```

#### Example 2: Shower Thought
```text
Act as a speech therapist and tell me what a 3 year old meant when he said, "I need way woy."
```

---
---

# Bonus: Combining Patterns — Tighter Rewrite

> The real power of prompt engineering isn't in any single pattern — it's in stacking them. Break your problem into pieces, assign a pattern to each piece, and merge the statements into one prompt. That's it. Sometimes order matters (e.g., **Ask for Input** should go last), but usually, it's as simple as making sure every pattern's core statements show up.

*Think of it as modular programming, but with English.*
