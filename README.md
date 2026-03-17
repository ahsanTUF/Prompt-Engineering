# Prompt Engineering Patterns

A structured, open-source guide to prompt engineering patterns — from beginner-friendly techniques to advanced reasoning strategies.

Based on the [Prompt Engineering for ChatGPT](https://www.coursera.org/learn/prompt-engineering) course by Vanderbilt University on Coursera, and expanded with modern techniques.

---

## Repository Structure

| File | Purpose |
|------|---------|
| [prompt_patterns.md](prompt_patterns.md) | The core collection of all prompt patterns |
| [GLOSSARY.md](GLOSSARY.md) | Definitions for technical jargon used across the patterns |
| [CONTRIBUTING.md](CONTRIBUTING.md) | Strict formatting and style guidelines for contributors |

---

## How to Read the Patterns

Each pattern entry follows a rigid scientific template:

- **Category** — A tag describing the pattern's primary domain (see table below).
- **Usability** — A 1–5 star rating reflecting how broadly useful the pattern is across different tasks.
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

| Rating | Meaning |
|--------|---------|
| ★★★★★ | Universal — useful in almost any prompting scenario |
| ★★★★☆ | Broadly useful — fits many common tasks |
| ★★★☆☆ | Situational — powerful when applicable, niche otherwise |
| ★★☆☆☆ | Specialized — requires specific context to be effective |
| ★☆☆☆☆ | Experimental — cutting-edge or highly domain-specific |

---

## Pattern Index

| # | Pattern | Category | Usability |
|---|---------|----------|-----------|
| 0 | [Combining Patterns](prompt_patterns.md#combining-patterns) | *Meta-concept* | — |
| 1 | [The Persona Pattern](prompt_patterns.md#the-persona-pattern) | `Roleplay / Jailbreak` | ★★★★★ |
| 2 | [The Audience Persona Pattern](prompt_patterns.md#the-audience-persona-pattern) | `Translation / Teaching` | ★★★★★ |
| 3 | [The Question Refinement Pattern](prompt_patterns.md#the-question-refinement-pattern) | `Optimization` | ★★★☆☆ |
| 4 | [The Cognitive Verifier Pattern](prompt_patterns.md#the-cognitive-verifier-pattern-aka-the-akinator-prompt) | `Advanced Reasoning` | ★★★★☆ |
| 5 | [The Flipped Interaction Pattern](prompt_patterns.md#the-flipped-interaction-pattern) | `Planning / Teaching` | ★★★★☆ |
| 6 | [Few-Shot Prompting](prompt_patterns.md#few-shot-prompting) | `Formatting / Training` | ★★★★☆ |
| 7 | [Chain of Thought Prompting](prompt_patterns.md#chain-of-thought-prompting) | `Advanced Reasoning` | ★★★☆☆ |
| 8 | [ReAct Prompting](prompt_patterns.md#react-reason--act-prompting) | `Advanced Reasoning / Agents` | ★★★★☆ |
| 9 | [The Game Play Pattern](prompt_patterns.md#the-game-play-pattern) | `Interactive / Teaching` | ★★★★★ |
| 10 | [The Template Pattern](prompt_patterns.md#the-template-pattern) | `Formatting` | ★★★★★ |
| 11 | [The Meta Language Creation Pattern](prompt_patterns.md#the-meta-language-creation-pattern) | `Workflow / Vibecode` | ★★★★★ |
| 12 | [The Recipe Pattern](prompt_patterns.md#the-recipe-pattern) | `Planning` | ★★★★☆ |
| 13 | [The Alternative Approaches Pattern](prompt_patterns.md#the-alternative-approaches-pattern) | `Exploration / Brainstorming` | ★★★★☆ |
| 14 | [The Ask for Input Pattern](prompt_patterns.md#the-ask-for-input-pattern) | `Workflow / Batch Processing` | ★★★★★ |
| 15 | [The Outline Expansion Pattern](prompt_patterns.md#the-outline-expansion-pattern) | `Planning / Brainstorming` | ★★★★☆ |

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for the mandatory formatting template, tone guidelines, and glossary rules. All contributions must adhere strictly to the established scientific template.

---

## License

This repository is open-source and intended for educational purposes. Based on course material from Vanderbilt University's Prompt Engineering specialization on Coursera.
