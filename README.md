# Prompt Engineering Patterns

A structured, open-source guide to prompt engineering patterns — from beginner-friendly techniques to advanced reasoning strategies.

Based on the [Prompt Engineering for ChatGPT](https://www.coursera.org/learn/prompt-engineering) course by Vanderbilt University on Coursera, and expanded with modern techniques.

---

## Repository Structure

| File | Purpose |
|------|---------|
| [PATTERNS.md](PATTERNS.md) | The core collection of all active prompt patterns |
| [OBSOLETE_PATTERNS.md](OBSOLETE_PATTERNS.md) | Archived patterns now largely baked into modern LLMs |
| [GLOSSARY.md](GLOSSARY.md) | Definitions for technical jargon used across the patterns |
| [CONTRIBUTING.md](CONTRIBUTING.md) | Formatting and style guidelines for contributors |

---

## How to Read the Patterns

Each pattern entry follows a rigid scientific template:

- **Category** — A tag describing the pattern's primary domain (see table below).
- **Usability** — A 1–5 star rating (see [Usability Scale](#usability-scale)).
- **Definition** — A concise mechanical explanation of what the pattern does.
- **Use Case** — Relatable scenarios explaining *why* you would use it.
- **Modifiers** *(optional)* — Extra toggles or variations you can add to the base pattern.
- **Examples** — Two copy-able prompts: one Technical/Vibecoding, one Creative/Shower Thought.

---

## Categories

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

## Usability Scale

The rating reflects three combined factors:

| Factor | Question |
|--------|----------|
| **Productive Value** | Does explicitly using this pattern unlock meaningfully better output than a naive prompt? |
| **LLM-Native?** | Is this behavior already baked into modern LLMs (2024+), reducing the need to explicitly prompt it? |
| **Breadth** | How many different domains/tasks does this pattern apply to? |

| Rating | Criteria |
|--------|----------|
| ★★★★★ | High productive value + NOT LLM-native + broad applicability |
| ★★★★☆ | High productive value + may be partially LLM-native OR slightly narrower applicability |
| ★★★☆☆ | Moderate productive value OR substantially LLM-native (diminished returns from explicit use) |
| ★★☆☆☆ | Mostly LLM-native now OR requires very specific context to provide value |
| ★☆☆☆☆ | Fully LLM-native / obsolete — explicit prompting provides negligible improvement |

> Patterns rated ★★☆☆☆ or ★☆☆☆☆ are archived in [OBSOLETE_PATTERNS.md](OBSOLETE_PATTERNS.md).

---

## Pattern Index

| # | Pattern | Category | Usability |
|---|---------|----------|-----------|
| 0 | [Combining Patterns](PATTERNS.md#combining-patterns) | *Meta-concept* | — |
| 1 | [The Persona Pattern](PATTERNS.md#the-persona-pattern) | `Roleplay / Jailbreak` | ★★★★★ |
| 2 | [The Audience Persona Pattern](PATTERNS.md#the-audience-persona-pattern) | `Translation / Teaching` | ★★★★☆ |
| 3 | [The Cognitive Verifier Pattern](PATTERNS.md#the-cognitive-verifier-pattern-aka-the-akinator-prompt) | `Advanced Reasoning` | ★★★★☆ |
| 4 | [The Flipped Interaction Pattern](PATTERNS.md#the-flipped-interaction-pattern) | `Planning / Teaching` | ★★★★★ |
| 5 | [Few-Shot Prompting](PATTERNS.md#few-shot-prompting) | `Formatting / Training` | ★★★★★ |
| 6 | [ReAct Prompting](PATTERNS.md#react-reason--act-prompting) | `Advanced Reasoning / Agents` | ★★★☆☆ |
| 7 | [The Game Play Pattern](PATTERNS.md#the-game-play-pattern) | `Interactive / Teaching` | ★★★★★ |
| 8 | [The Template Pattern](PATTERNS.md#the-template-pattern) | `Formatting` | ★★★★★ |
| 9 | [The Meta Language Creation Pattern](PATTERNS.md#the-meta-language-creation-pattern) | `Workflow / Vibecode` | ★★★★★ |
| 10 | [The Recipe Pattern](PATTERNS.md#the-recipe-pattern) | `Planning` | ★★★☆☆ |
| 11 | [The Alternative Approaches Pattern](PATTERNS.md#the-alternative-approaches-pattern) | `Exploration / Brainstorming` | ★★★☆☆ |
| 12 | [The Ask for Input Pattern](PATTERNS.md#the-ask-for-input-pattern) | `Workflow / Batch Processing` | ★★★★★ |
| 13 | [The Outline Expansion Pattern](PATTERNS.md#the-outline-expansion-pattern) | `Planning / Brainstorming` | ★★★★☆ |
| 14 | [The Menu Actions Pattern](PATTERNS.md#the-menu-actions-pattern) | `Workflow / Batch Processing` | ★★★★★ |
| 15 | [The Fact Check List Pattern](PATTERNS.md#the-fact-check-list-pattern) | `Optimization` | ★★★★☆ |
| 16 | [The Semantic Filter Pattern](PATTERNS.md#the-semantic-filter-pattern) | `Optimization` | ★★★★☆ |

### Archived Patterns

| Pattern | Category | Usability | Why Archived |
|---------|----------|-----------|--------------|
| [The Question Refinement Pattern](OBSOLETE_PATTERNS.md#the-question-refinement-pattern) | `Optimization` | ★★☆☆☆ | LLMs routinely clarify questions by default |
| [Chain of Thought Prompting](OBSOLETE_PATTERNS.md#chain-of-thought-prompting) | `Advanced Reasoning` | ★★☆☆☆ | Reasoning models do this natively |
| [The Tail Generation Pattern](OBSOLETE_PATTERNS.md#the-tail-generation-pattern) | `Workflow / Batch Processing` | ★☆☆☆☆ | LLMs repeat context and ask follow-ups by default |

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for the mandatory formatting template, tone guidelines, and glossary rules.

---

## License

This repository is open-source and intended for educational purposes. Based on course material from Vanderbilt University's Prompt Engineering specialization on Coursera.
