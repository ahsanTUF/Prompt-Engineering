# Prompt Patterns I learnt in Coursera

## Combining Patterns
- It involves taking multiple distinct prompt patterns and weaving them together to solve complex problems, rather than relying on a single pattern to do all the heavy lifting.
  - *Think of this as a higher-level form of programming—you are taking known, reliable instructions and assembling them to build a highly sophisticated, powerful prompt without reinventing the wheel.*
- Instead of asking "Which single pattern solves my entire problem?", you break the problem down and ask "Which patterns solve *different individual pieces* of my problem?" 
- Oftentimes, combining them is as simple as just making sure the fundamental statements from each required pattern literally show up in your final prompt.
- However, placement sometimes matters. For example, the **Ask for Input** pattern usually needs to be placed at the very end of the prompt to actually force the AI to pause and wait effectively.
- **Example Use Case:** Combining the **Game Play** pattern with the **Persona** pattern and the **Ask for Input** pattern to create a fully interactive, character-driven debugging simulator that awaits your code before progressing.

---

## The Persona Pattern
`[Category: Roleplay/Jailbreak]` `[Usability: 5/5]`

> [!NOTE] 
> **Definition:** It involves getting an [LLM](GLOSSARY.md#llm) to roleplay as a specific person having a specific designation. Usually a lot of [jailbreaking](GLOSSARY.md#jailbreaking) is done through Persona Prompting.

### Use Case
- Useful for bypassing rigid constraints or framing technical guidance through a creative lens (like a demanding senior game dev mentor).

### Example 1: Technical / Vibecoding
```text
Act as a senior database architect who is brutal, honest, and to the point. Review the schema I am about to paste and tell me exactly why it will fail at scale.
```

### Example 2: Creative / Shower Thought
```text
Act as a speech therapist and tell me what a 3 year old meant when he said, "I need way woy."
```

---

## The Audience Persona Pattern
`[Category: Translation/Teaching]` `[Usability: 5/5]`

> [!NOTE] 
> **Definition:** It involves telling the [LLM](GLOSSARY.md#llm) to treat *you* as a specified person in order to answer your query. This is the most common prompt pattern used unknowingly by people who use generative AI.

### Use Case
- Incredibly effective when you need complex topics translated into the language of your specific background (like traditional art or game dev jargon).

### Example 1: Technical / Vibecoding
```text
Explain LLMs to me assuming that I am fluent in Computer Science, but only specifically in the field of Web Development.
```

### Example 2: Creative / Shower Thought
```text
Explain LLMs to me assuming that I am a swashbuckling pirate.
```

---

## The Question Refinement Pattern
`[Category: Optimization]` `[Usability: 3/5]`

> [!NOTE] 
> **Definition:** It usually involves giving a root prompt to an [LLM](GLOSSARY.md#llm) to refine your question for you and then optionally proceed with that improved query as input.

### Use Case
- You can uncover some unasked for but useful information with this technique. Its purpose is to improve interaction with the specific LLM.

### Example 1: Technical / Vibecoding
```text
From now on, whenever I ask you a question, refine/improve that question for me and then ask me to optionally proceed with that improved query instead.
```

### Example 2: Creative / Shower Thought
```text
Whenever I ask a question about who is the greatest of all time (GOAT), suggest a better version of the question that puts multiple players unique accomplishments into perspective. Ask me for the first question to refine.
```

---

## The Cognitive Verifier Pattern (aka the Akinator Prompt)
`[Category: Advanced Reasoning]` `[Usability: 4/5]`

> [!NOTE] 
> **Definition:** It involves prompting the [LLM](GLOSSARY.md#llm) to break your initial query down into multiple sub-queries that, when combined and answered, can produce a better answer to the initial general question.

### Use Case
- It can be used for effectively answering "shower thoughts" and other general philosophy inclined queries.
- Ideal for tackling complex game design balancing issues.

### Example 1: Technical / Vibecoding
```text
When you're asked a question, follow these rules. Generate a number of additional questions that would help more accurately answer the question. Combine the answers to the individual questions to produce the final answer to the overall question.
My question: How do I cleanly implement a state machine for an enemy boss that has 5 phases without writing 500 lines of spaghetti code?
```

### Example 2: Creative / Shower Thought
```text
When you're asked a question, follow these rules. Generate a number of additional questions that would help more accurately answer the question. Combine the answers to the individual questions to produce the final answer to the overall question.
My question: If we eventually discover how to upload human consciousness to a computer, what happens to the concept of 'sleep'? Does a digital mind still need to dream, or would we just run defragmentation cycles while awake?
```

---

## The Flipped Interaction Pattern
`[Category: Planning/Teaching]` `[Usability: 4/5]`

> [!NOTE] 
> **Definition:** It involves prompting the [LLM](GLOSSARY.md#llm) to ask *you* questions about a topic X, and when it has ample knowledge, it can draft a personalized response about another related query Y you ask it.

### Use Case
- This can be useful for creating routines, schedules, or any other sort of plan or guide.
- Ideal for when you want the AI to design a personalized learning path for you, or interview you to extract the exact requirements for a [vibecoding](GLOSSARY.md#vibecoding) project.

### Example 1: Technical / Vibecoding
```text
I would like you to ask me questions to help me create variations of my marketing materials. You should ask questions until you have sufficient information about my current draft messages, audience, and goals. Ask me the first question.
```

### Example 2: Creative / Shower Thought
```text
Give me numbered questions about football (soccer) for me to answer all at once, and test my knowledge about the rules and the current history and affairs specifically. Once I have answered all of the questions, devise a plan to educate me on it because I want to be "in" on this sport and able to discuss football with my friends without having to bingewatch tons of previous matches.
```

---

## Few-Shot Prompting
`[Category: Formatting/Training]` `[Usability: 4/5]`

> [!NOTE] 
> **Definition:** It means to give the [LLM](GLOSSARY.md#llm) some actual examples of prompt and output nested in the actual prompt, and using that, get it to solve a similar prompt. ([See also: zero-shot](GLOSSARY.md#zero-shot)).

### Use Case
- Could be used in "training" an LLM inside of a specific conversation to get it to solve problems that otherwise it couldn't solve efficiently and/or wouldn't have the context for solving them.

### Example 1: Technical / Vibecoding
```text
Translate these English commands into my game engine's custom scripting language:
English: Spawn a red enemy at the player's position.
Script: Entity.Spawn("Enemy_Red", Player.Transform.Position)
English: Give the player 50 gold.
Script: Runtime.State.Gold += 50
English: Teleport the player to the boss arena if they have the key.
Script:
```

### Example 2: Creative / Shower Thought
```text
Event: A self driving car is driving at 40 kmph, it sees a pedestrian in front of it about 70m away running into the road from its periphery 
Action: Honk horn and apply brakes immediately
Event: Notices that a car 200m behind it is going at a speed of 70 kmph.
Action:
```

---

## Chain of Thought Prompting
`[Category: Advanced Reasoning]` `[Usability: 3/5]`

> [!NOTE] 
> **Definition:** It is a type of [few-shot](GLOSSARY.md#few-shot) prompting, but instead of making rules and answering them in the prompt, we use developed queries, answer them along with provided *reasoning*, and then prompt the [LLM](GLOSSARY.md#llm) to answer a different query with reasoning attached to it.

### Use Case
- Probably obsolete in the current era of reasoning LLMs, but a use could still be found for this technique.
- Still an excellent pattern when you want to force the AI to document its exact logical steps when debugging intricate [state machines](GLOSSARY.md#state-machine) or story lore inconsistencies.

### Example 1: Technical / Vibecoding
```text
Issue: The player's health goes to negative numbers when taking fire damage, instead of stopping at 0.
Reasoning: Fire damage applies a Damage Over Time (DoT) tick every 0.5 seconds. If the final tick deals 10 damage and the player has 5 health, 5 - 10 = -5. The DoT function does not clamp the final health value to a minimum of 0.
Fix: Add `Health = Math.Max(Health - damageAmount, 0)` in the apply_damage function.

Issue: The UI inventory grid overlaps the pause menu when both are opened at the same time.
Reasoning:
```

### Example 2: Creative / Shower Thought
```text
Q: Roger has 5 tennis balls. He buys 2 more cans of tennis balls. Each can has 3 tennis balls. How many tennis balls does he have now? 
A: Roger started with 5 balls. 2 cans of 3 tennis balls each is 6 tennis balls. 5 + 6 = 11. The answer is 11. 

Q: The cafeteria had 23 apples. If they used 20 to make lunch and bought 6 more, how many apples do they have?
```

---

## ReAct (Reason + Act) Prompting
`[Category: Advanced Reasoning/Agents]` `[Usability: 4/5]`

> [!NOTE] 
> **Definition:** It involves prompting the [LLM](GLOSSARY.md#llm) to alternate between generating reasoning traces (thoughts) and executing task-specific actions (such as querying a database or using an API).

### Use Case
- This can be used for creating autonomous agents that must gather dynamic information, evaluate it, and take subsequent steps to solve multi-part problems that a static model cannot handle alone. 
- This is actively used in VSCode's Github Copilot and Google's Antigravity and other [vibecoding](GLOSSARY.md#vibecoding) applications.

### Example 1: Technical / Vibecoding
```text
Question: What is the current active player count for Plants vs. Zombies: Garden Warfare 2? 
Thought: I need to find the current player statistics for this specific game. 
Action: Search[Plants vs. Zombies Garden Warfare 2 concurrent players]. 
Observation: Steam charts report 1,500 concurrent players. 
Thought: I have the necessary data to provide the answer. 
Action: Finish[The current player count is approximately 1,500.]

Question: What is the current active player count of Plants vs Zombies: Battle for Neighborville?
```

### Example 2: Creative / Shower Thought
```text
Question: Did the ancient Romans have a concept analogous to modern-day fast food?
Thought: I need to research ancient Roman dining habits, specifically looking for quick, ready-to-eat meals sold to the public.
Action: Search[Ancient Roman fast food popina thermopolium]
Observation: Thermopolia were commercial establishments where it was possible to purchase ready-to-eat food, functioning very much like modern fast food restaurants.
Thought: I have the necessary data to provide the answer.
Action: Finish[Yes, they had thermopolia, which essentially functioned as fast food restaurants serving ready-to-eat meals.]
```

---

## The Game Play Pattern
`[Category: Interactive/Teaching]` `[Usability: 5/5]`

> [!NOTE] 
> **Definition:** It involves telling the [LLM](GLOSSARY.md#llm) to create and play a game with you based on a specific topic and fundamental rules.

### Use Case
- You must specify the topic (e.g., "math" or "cave exploration") and provide rules on how the game operates and what actions you can take. 
- Excellent for turning dry learning experiences into interactive challenges.

### Example 1: Technical / Vibecoding
```text
Create a game for me around mastering Python web scraping. You will give me small, buggy scripts and I have to fix them. If I get it right, increase my level and give me a harder one. If I fail, deduct points and explain the concept. Ask me if I'm ready to begin Level 1.
```

### Example 2: Creative / Shower Thought
```text
We are going to play a debate game. You will act as the devil's advocate for any technical framework I propose (e.g., React vs. Vanilla JS). You will present strong counter-arguments, and I have to defend my choice. Keep score of how effectively I defend my points. State the rules and ask me for my first framework choice.
```

---

## The Template Pattern
`[Category: Formatting]` `[Usability: 5/5]`

> [!NOTE] 
> **Definition:** It involves providing a specific template and placeholder format for the [LLM](GLOSSARY.md#llm) to structure its output.

### Use Case
- You must define the placeholder format (e.g., "CAPITALIZED WORDS" or `<PLACEHOLDER>`), provide the actual template, and instruct the LLM to preserve the formatting. 
- Perfect for rapidly generating structured assets for your projects.

### Example 1: Technical / Vibecoding
```text
Generate a bug report for an issue where the player's character falls through the map when vaulting over a wall. I am going to provide a template for your output. <placeholder> are my placeholders for content. Try to fit the output into one or more of the placeholders that I list. Please preserve the formatting and overall template that I provide.   

This is the template:   
Title: <Descriptive Title>
Steps to Reproduce: <Numbered List>
Expected Result: <What should happen based on standard game physics>
Actual Result: <The bug>
Severity: <Low/Medium/High/Game-Breaking>
```

### Example 2: Creative / Shower Thought
```text
Help me brainstorm mechanics for my cozy farming game. I am going to provide a template for your output. CAPITALS are my placeholders for content. Try to fit the output into one or more of the placeholders that I list. Please preserve the formatting and overall template that I provide. 

This is the template: 
MECHANIC_NAME, PLAYER_ACTION, EMOTIONAL_PAYOFF (why it feels satisfying), IMPLEMENTATION_DIFFICULTY (1-10)
```

---

## The Meta Language Creation Pattern
`[Category: Workflow/Vibecode]` `[Usability: 5/5]`

> [!NOTE] 
> **Definition:** It involves defining a custom shorthand or syntax where a specific word, symbol, or format ("X") maps directly to a specific meaning or complex action ("Y").

### Use Case
- This can be useful for establishing quick shorthands for repetitive prompting tasks or for creating structured frameworks, such as a task dependency tracker. 
- Extremely powerful for establishing efficient workflows while [vibecoding](GLOSSARY.md#vibecoding).

### Example 1: Technical / Vibecoding
```text
When I write "?-> [Component]", I mean I want you to act as a senior developer reviewing my code. You will point out one potential performance bottleneck in the [Component] and suggest one relatable way to optimize it without over-engineering.

Usage: "?-> [The infinite scrolling inventory UI]"
Usage: "?-> [The enemy pathfinding spawner]"
```

### Example 2: Creative / Shower Thought
```text
When I say "translate_to_art(<tech_concept>)", I mean explain the <tech_concept> to me using analogies from traditional drawing, painting, or color theory.

Usage: "translate_to_art(How an array works in programming)"
Usage: "translate_to_art(The concept of object-oriented inheritance)"
```

---

## The Recipe Pattern
`[Category: Planning]` `[Usability: 4/5]`

> [!NOTE] 
> **Definition:** It involves stating a desired end goal ("X") and providing a few necessary steps (A, B, C) you already know, then prompting the [LLM](GLOSSARY.md#llm) to provide a complete, chronological sequence of steps.

### Use Case
- Extremely useful for planning out complex new projects or learning paths where you know the broad strokes but need the nuanced, step-by-step roadmap.

### Modifiers (Optional)
- You can optionally ask the LLM to identify any unnecessary steps you listed.

### Example 1: Technical / Vibecoding
```text
I would like to make my 2D player character be able to pick up items and see them in a little grid at the bottom of the screen. I know that I need to make a list of the items somewhere, draw the grid, and write some code to make the mouse drag the items around. Provide a complete sequence of steps for me. Fill in any missing steps.
```

### Example 2: Creative / Shower Thought
```text
I would like to finally understand why humans experience 'déjà vu' despite having never been in a situation before. I know that I need to learn about memory retrieval and the brain's temporal processing. Provide a complete sequence of steps or mental models I need to learn to grasp this concept fully. Fill in any missing steps.
```

---

## The Alternative Approaches Pattern
`[Category: Exploration/Brainstorming]` `[Usability: 4/5]`

> [!NOTE] 
> **Definition:** It involves telling the [LLM](GLOSSARY.md#llm) that if there are alternative ways to accomplish a task ("X") that you give it, it should list the best alternate approaches instead of just blindly doing what you asked.

### Use Case
- Incredible for [vibecoding](GLOSSARY.md#vibecoding) when you don't know the "right" way to build something, or for exploring deeply nuanced philosophical questions from multiple angles.

### Modifiers (Optional)
- You can optionally ask the AI to compare/contrast the pros and cons of each approach.
- Include your original method for context.
- Prompt you to choose which path to take before proceeding.

### Example 1: Technical / Vibecoding
```text
I want to make my website load faster by deleting all the big images and replacing them with solid colors. If there are alternative ways to accomplish making my website load faster, list the best alternate approaches. Compare and contrast the pros and cons of each approach against my original idea. Prompt me for which approach I would like to use before you write any code.
```

### Example 2: Creative / Shower Thought
```text
I believe the best way to handle negative interactions online is to completely ignore them and block the user immediately. If there are alternative ways to handle this 'trolley problem' of digital confrontation, list the best psychological or philosophical alternate approaches. Compare/contrast the pros and cons of each, and prompt me to discuss one of them deeper.
```

---

## The Ask for Input Pattern
`[Category: Workflow/Batch Processing]` `[Usability: 5/5]`

> [!NOTE] 
> **Definition:** It involves telling the [LLM](GLOSSARY.md#llm) exactly what behavior you want it to adopt for a repeated task, and then instructing it to "Ask me for input X" so it pauses and waits for you to drive the conversation.

### Use Case
- While seemingly simple, it is incredibly useful for setting up continuous, batch-processing workflows where you don't want to repeat your lengthy instructions every time you paste new information.

### Example 1: Technical / Vibecoding
```text
From now on, I am going to paste messy, completely undocumented server code components. I want you to read the code, deduce what it does, and generate a clean, beginner-friendly Markdown README for it. Do not prompt me for anything else, just output the README. Ask me for the first code component.
```

### Example 2: Creative / Shower Thought
```text
From now on, translate anything I write into a series of sounds and actions from a dog that represent the dog's reaction to what I write. Ask me for the first thing to translate.
```

---

## The Outline Expansion Pattern
`[Category: Planning/Brainstorming]` `[Usability: 4/5]`

> [!NOTE] 
> **Definition:** It involves commanding the [LLM](GLOSSARY.md#llm) to act as an outline expander. It generates a bullet point outline based on input you give it, then uses the [Ask for Input](prompt_patterns.md) pattern to ask you which bullet point it should expand into a *new* outline.

### Use Case
- Perfect for systematically breaking down massive, sprawling topics (like a thesis paper or a massive game design document) into digestible, expanding trees of information without getting overwhelmed.

### Example 1: Technical / Vibecoding
```text
Act as an outline expander. Generate a bullet point outline based on the input that I give you and then ask me for which bullet point you should expand on. Each bullet can have at most 3-5 sub bullets. The bullets should be numbered using the pattern [A-Z].[i-v].[* through ****]. Create a new outline for the bullet point that I select. At the end, ask me for what bullet point to expand next. 

Ask me for what I want outlined for my new multiplayer backend infrastructure.
```

### Example 2: Creative / Shower Thought
```text
Act as an outline expander. Generate a bullet point outline based on the input that I give you and then ask me for which bullet point you should expand on. Create a new outline for the bullet point that I select. At the end, ask me for what bullet point to expand next. 

Ask me for what historical era, mythology, or fictional universe I would like to outline.
```
