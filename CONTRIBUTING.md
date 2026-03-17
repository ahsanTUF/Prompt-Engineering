# Contributing to the Prompt Patterns Repository

Thank you for your interest in contributing! Our goal is to create a robust, open-source, and easy-to-read "simple-to-advanced" guide for prompt engineering. 

To maintain a professional, scientific, and cohesive aesthetic across the repository, **all contributions must strictly adhere to the guidelines below.**

---

## 1. Tone and Scope
- **Keep it brief and direct:** Use simple, easily understandable vocabulary. Avoid unnecessary fluff or jargon beyond the immediate concept you are explaining.
- **The "Golden Mix":** We aim for a perfect balance between technical utility and creative relatability. Every pattern should ideally have one Technical/Vibecoding example and one Creative/Shower Thought example.
- **Vibecoding Perspective:** When writing technical examples, frame them from the perspective of someone who knows *what* they want functionally, but doesn't necessarily know the technical jargon to ask for it.

---

## 2. The Clean Scientific Template (MANDATORY)

Every single pattern must rigidly follow this exact markdown format to ensure cross-platform aesthetics (it renders beautifully on both GitHub and Obsidian). Do not use custom HTML or exotic markdown.

```markdown
---

## The [Pattern Name] Pattern
**Category:** `[Tag]` · **Usability:** [1-5 Stars]

###### 📖 Definition
> [Core explanation. Any highly technical word MUST link to `GLOSSARY.md`, e.g., `[LLM](GLOSSARY.md#llm)`].

###### 💡 Use Case
> - [Relatable Spark 1]
> - [Relatable Spark 2]

###### ⚙️ Modifiers (Optional)
> - [Bullet points for modifiers like "Ask the AI to compare/contrast..."]

##### Example 1: Technical / Vibecoding
```text
[Prompt goes here for easy 1-click copying]
```
##### Example 2: Creative / Shower Thought
```text
[Prompt goes here for easy 1-click copying]
```
```

### Template Rules:
1. **Headings:** Use `######` (h6) for the Definition, Use Case, and Modifiers labels. Use `#####` (h5) for the Example labels.
2. **Blockquotes:** The text for Definition, Use Case, and Modifiers must be wrapped in standard `>` blockquotes.
3. **Spacing:** Do *not* put a blank line between the `##### Example` heading and the code block below it.
4. **Code Blocks:** Prompts must be placed inside standard markdown code blocks tagged as `text`.

---

## 3. The Glossary System

If your pattern introduces a highly technical term (e.g., *LLM*, *Jailbreaking*, *State Machine*, *Vibecoding*), you **must** link it to the Glossary on its first use in the definition.

**How to link:**
```markdown
Getting an [LLM](GLOSSARY.md#llm) to roleplay...
```

**How to update the Glossary:**
If the term does not exist in `GLOSSARY.md`, you must add it. Add new terms in alphabetical order using the following format:

```markdown
### [Term Name]
> **Definition:** [Clear, accessible definition of the term]
> **Context:** [Brief explanation of how it relates to prompt engineering]
```

*Example:*
```markdown
### Vibecoding
> **Definition:** The act of writing software using natural language by interacting with an AI, rather than typing traditional code syntax.
> **Context:** Focuses on expressing the "vibe" or desired architectural outcome and letting the LLM generate the rigid boilerplate.
```
