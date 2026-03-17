<div align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Geist+Mono&size=36&duration=3000&pause=1000&color=0EA5E9&center=true&vCenter=true&width=700&lines=Prompt+Engineering+Patterns;From+Beginner+to+Advanced;21+Battle-Tested+Patterns" alt="Typing Animation" />
</div>

<p align="center">
  A structured, open-source guide to prompt engineering patterns — from beginner-friendly techniques to advanced reasoning strategies.
</p>

<p align="center">
  <a href="https://github.com/ahsanTUF/Prompt-Engineering/releases/latest/download/PDF.pdf"><img src="https://img.shields.io/badge/Download-PDF_Handbook-FF4154?style=for-the-badge&logo=pdf&logoColor=white" /></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Patterns-21_Active-0EA5E9?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Archived-3_Obsolete-6B7280?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Source-Vanderbilt_+_Research-8B5CF6?style=for-the-badge" />
</p>

<p align="center">
  Based on the <a href="https://www.coursera.org/learn/prompt-engineering">Prompt Engineering for ChatGPT</a> course by Vanderbilt University on Coursera, and expanded with modern techniques.
</p>

---

## 📁 Repository Structure

| File | Purpose |
|------|---------|
| [PATTERNS.md](PATTERNS.md) | All active prompt patterns, ordered by usefulness |
| [OBSOLETE_PATTERNS.md](OBSOLETE_PATTERNS.md) | Archived patterns now largely baked into modern LLMs |
| [GLOSSARY.md](GLOSSARY.md) | Definitions for technical jargon used across the patterns |
| [CONTRIBUTING.md](CONTRIBUTING.md) | Formatting and style guidelines for contributors |

---

## 📖 How to Read the Patterns

Each pattern entry follows a rigid scientific template:

- **#** — Patterns are numbered by usefulness (most useful first).
- **Category** — A tag describing the pattern's primary domain (see table below).
- **Usability** — A 1–5 star rating (see [Usability Scale](#-usability-scale)).
- **Definition** — A concise mechanical explanation of what the pattern does.
- **Use Case** — Relatable scenarios explaining *why* you would use it.
- **Modifiers** *(optional)* — Extra toggles or variations you can add to the base pattern.
- **Examples** — Two copy-able prompts: one Technical/Vibecoding, one Creative/Shower Thought.

---

## 🏷️ Categories

| Tag | Description |
|-----|-------------|
| `Roleplay / Jailbreak` | Patterns that involve the AI adopting a persona or bypassing default behavior |
| `Translation / Teaching` | Patterns that adapt the AI's output to a specific audience or knowledge level |
| `Optimization` | Patterns that improve the quality of your interaction with the AI |
| `Advanced Reasoning` | Patterns that force the AI through structured logical steps |
| `Advanced Reasoning / Agents` | Patterns that combine reasoning with external actions (search, API calls) |
| `Planning / Teaching` | Patterns where the AI interviews you to build a personalized plan |
| `Planning / Brainstorming` | Patterns for breaking down large topics into structured outlines |
| `Planning` | Patterns for generating step-by-step plans from partial knowledge |
| `Exploration / Brainstorming` | Patterns that surface multiple approaches to a single problem |
| `Formatting / Training` | Patterns that train the AI's behavior using in-prompt examples |
| `Formatting` | Patterns that control the structure and layout of the AI's output |
| `Interactive / Teaching` | Patterns that turn learning into a game or interactive challenge |
| `Workflow / Vibecode` | Patterns for creating custom shorthands and efficient prompting workflows |
| `Workflow / Batch Processing` | Patterns for setting up repeatable, input-driven workflows |

---

## ⚖️ Usability Scale

Rate each pattern by answering 3 questions:

| Question | +1 if YES |
|----------|-----------|
| Does explicitly using this unlock meaningfully better output than a naive prompt? | **Productive** |
| Is this behavior NOT baked into modern LLMs (2024+)? | **Not-native** |
| Does it apply across 3+ different domains/tasks? | **Broad** |

| Score | Rating |
|-------|--------|
| 3/3 | ★★★★★ |
| 2/3 | ★★★★☆ |
| 1/3 | ★★★☆☆ |
| 0/3 | ★★☆☆☆ or ★☆☆☆☆ → archive to [OBSOLETE_PATTERNS.md](OBSOLETE_PATTERNS.md) |

Within the same star tier, patterns are ordered by how *frequently* a typical user would reach for them in daily use.

---

## 📋 Pattern Index

<details>
<summary><b>★★★★★ — Essential (10 patterns)</b></summary>
<br>

| # | Pattern | Category |
|---|---------|----------|
| 1 | [The Context Dumping Pattern](PATTERNS.md#1-the-context-dumping-pattern) | `Workflow / Vibecode` |
| 2 | [The Persona Pattern](PATTERNS.md#2-the-persona-pattern) | `Roleplay / Jailbreak` |
| 3 | [Few-Shot Prompting](PATTERNS.md#3-few-shot-prompting) | `Formatting / Training` |
| 4 | [The Template Pattern](PATTERNS.md#4-the-template-pattern) | `Formatting` |
| 5 | [The Negative Prompting Pattern](PATTERNS.md#5-the-negative-prompting-pattern) | `Optimization` |
| 6 | [The Flipped Interaction Pattern](PATTERNS.md#6-the-flipped-interaction-pattern) | `Planning / Teaching` |
| 7 | [The Ask for Input Pattern](PATTERNS.md#7-the-ask-for-input-pattern) | `Workflow / Batch Processing` |
| 8 | [The Meta Language Creation Pattern](PATTERNS.md#8-the-meta-language-creation-pattern) | `Workflow / Vibecode` |
| 9 | [The Menu Actions Pattern](PATTERNS.md#9-the-menu-actions-pattern) | `Workflow / Batch Processing` |
| 10 | [The Game Play Pattern](PATTERNS.md#10-the-game-play-pattern) | `Interactive / Teaching` |

</details>

<details>
<summary><b>★★★★☆ — High Value (8 patterns)</b></summary>
<br>

| # | Pattern | Category |
|---|---------|----------|
| 11 | [The Prompt Chaining Pattern](PATTERNS.md#11-the-prompt-chaining-pattern) | `Workflow / Vibecode` |
| 12 | [The Cognitive Verifier Pattern](PATTERNS.md#12-the-cognitive-verifier-pattern-aka-the-akinator-prompt) | `Advanced Reasoning` |
| 13 | [The Outline Expansion Pattern](PATTERNS.md#13-the-outline-expansion-pattern) | `Planning / Brainstorming` |
| 14 | [The Recursive Self-Improvement Pattern](PATTERNS.md#14-the-recursive-self-improvement-pattern) | `Optimization` |
| 15 | [The Fact Check List Pattern](PATTERNS.md#15-the-fact-check-list-pattern) | `Optimization` |
| 16 | [The Audience Persona Pattern](PATTERNS.md#16-the-audience-persona-pattern) | `Translation / Teaching` |
| 17 | [The Semantic Filter Pattern](PATTERNS.md#17-the-semantic-filter-pattern) | `Optimization` |
| 18 | [The Multi-Persona Debate Pattern](PATTERNS.md#18-the-multi-persona-debate-pattern) | `Advanced Reasoning` |

</details>

<details>
<summary><b>★★★☆☆ — Situational (3 patterns)</b></summary>
<br>

| # | Pattern | Category |
|---|---------|----------|
| 19 | [The Recipe Pattern](PATTERNS.md#19-the-recipe-pattern) | `Planning` |
| 20 | [The Alternative Approaches Pattern](PATTERNS.md#20-the-alternative-approaches-pattern) | `Exploration / Brainstorming` |
| 21 | [ReAct Prompting](PATTERNS.md#21-react-reason--act-prompting) | `Advanced Reasoning / Agents` |

</details>

<details>
<summary><b>🗃️ Archived — Obsolete (3 patterns)</b></summary>
<br>

| Pattern | Usability | Why Archived |
|---------|-----------|--------------|
| [The Question Refinement Pattern](OBSOLETE_PATTERNS.md#the-question-refinement-pattern) | ★★☆☆☆ | LLMs routinely clarify questions by default |
| [Chain of Thought Prompting](OBSOLETE_PATTERNS.md#chain-of-thought-prompting) | ★★☆☆☆ | Reasoning models do this natively |
| [The Tail Generation Pattern](OBSOLETE_PATTERNS.md#the-tail-generation-pattern) | ★☆☆☆☆ | LLMs repeat context and ask follow-ups by default |

</details>

---

## 🤝 Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for the mandatory formatting template, tone guidelines, and glossary rules.

---

## 📄 License

This repository is open-source and intended for educational purposes. Based on course material from Vanderbilt University's Prompt Engineering specialization on Coursera.

---

<p align="center">
  <i>⭐ If you find this useful, consider giving the repo a star — it keeps the patterns coming!</i>
</p>
