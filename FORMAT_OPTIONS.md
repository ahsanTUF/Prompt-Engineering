# The Standard Format

This is the final, approved structure for every prompt pattern entry in this repository. Contributors must follow this template exactly.

---

## The Persona Pattern
`Roleplay / Jailbreak` · `★★★★★`

> [!NOTE] Definition
> Getting an [LLM](GLOSSARY.md#llm) to roleplay as a specific person with a specific designation. A lot of [jailbreaking](GLOSSARY.md#jailbreaking) is done through this.

> [!TIP] Use Case
> Bypass rigid constraints or frame technical guidance through a creative lens — like having a brutally honest senior game dev mentor.

##### Example 1: Vibecoding
```text
Act as a senior database architect who is brutal, honest, and to the point. Review the schema I am about to paste and tell me exactly why it will fail at scale.
```
##### Example 2: Shower Thought
```text
Act as a speech therapist and tell me what a 3 year old meant when he said, "I need way woy."
```

---

## The Alternative Approaches Pattern
`Exploration / Brainstorming` · `★★★★☆`

> [!NOTE] Definition
> Telling the [LLM](GLOSSARY.md#llm) that if there are alternative ways to accomplish a task you give it, it should list the best alternate approaches instead of just blindly doing what you asked.

> [!TIP] Use Case
> Incredible for [vibecoding](GLOSSARY.md#vibecoding) when you don't know the "right" way to build something, or for exploring philosophical questions from multiple angles.

> [!CAUTION] Modifiers
> - Ask the AI to compare/contrast the pros and cons of each approach.
> - Include your original method for context.
> - Prompt you to choose which path to take before proceeding.

##### Example 1: Vibecoding
```text
I want to make my website load faster by deleting all the big images and replacing them with solid colors. If there are alternative ways to accomplish making my website load faster, list the best alternate approaches. Compare and contrast the pros and cons of each approach against my original idea. Prompt me for which approach I would like to use before you write any code.
```
##### Example 2: Shower Thought
```text
I believe the best way to handle negative interactions online is to completely ignore them and block the user immediately. If there are alternative ways to handle this 'trolley problem' of digital confrontation, list the best psychological or philosophical alternate approaches. Compare/contrast the pros and cons of each, and prompt me to discuss one of them deeper.
```
