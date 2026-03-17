# Prompt Engineering Glossary

Definitions for technical terms used across the **[Prompt Patterns](PATTERNS.md)** repository. All terms are listed alphabetically.

---

### Agent
> **Definition:** An AI system configured to autonomously use tools, search the web, or execute code to achieve a given goal, rather than just generating static text.
> **Context:** ReAct prompting is fundamental for building functioning agents that can 'Reason' and 'Act' in a loop.

### CAPTCHA
> **Definition:** "Completely Automated Public Turing test." A challenge-response test used in computing to determine whether or not the user is human.
> **Context:** Often used in examples of security considerations or system architecture debates.

### Few-Shot
> **Definition:** Providing the AI with a few concrete examples of the input-output pattern you want before asking it to solve your actual query.
> **Context:** Contrasted with zero-shot prompting. Used to "train" an AI's behavior within a single conversation.

### Jailbreaking
> **Definition:** Using complex prompt structures or assumed personas to bypass an AI's safety filters, constraints, or default conversational tone.
> **Context:** Often achieved through the Persona Pattern. The ethics and legality of jailbreaking vary by platform and use case.

### LLM
> **Definition:** Large Language Model. The underlying AI engine (like ChatGPT, Claude, or Gemini) that processes your prompts and generates text.
> **Context:** The foundational technology that all prompt engineering patterns are designed to interact with.

### Regex
> **Definition:** Short for "Regular Expression." A sequence of characters that specifies a search pattern in text, mostly used for string matching and validation.
> **Context:** Often used in coding-related prompts (like email validation) where precision is required.

### REST API
> **Definition:** A set of rules and conventions that allow different software applications to communicate with each other over the internet.
> **Context:** A common architectural concept when giving an LLM full-stack or backend code instructions.

### SQL Injection
> **Definition:** A cyberattack technique where malicious SQL statements are inserted into data entry fields, tricking the backend database into executing them.
> **Context:** A classic example of a security vulnerability that you might prompt an LLM to identify or fix.

### State Machine
> **Definition:** A programming construct that transitions between different defined "states," such as a game character switching from `Idle` to `Running` to `Jumping`.
> **Context:** Often referenced in game development examples. State machines can be complex to debug, which makes them a good candidate for AI-assisted reasoning patterns.

### Vibecoding
> **Definition:** The act of writing software using natural language by interacting with an AI, rather than typing traditional code syntax.
> **Context:** The user acts more like a designer or director, describing the desired functionality and logic in plain English, while the AI handles syntax and implementation.

### Zero-Shot
> **Definition:** Asking an AI to perform a task without providing it any prior examples or training data within the prompt itself.
> **Context:** The default mode of most AI interactions. Contrasted with few-shot prompting, where examples are provided.
