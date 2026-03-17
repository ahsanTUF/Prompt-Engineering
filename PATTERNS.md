# Prompt Patterns

> Ordered by usefulness (most universally useful first). See **[README.md](README.md)** for the rating rubric.

---

## 1. The Context Dumping Pattern
**Category:** `Workflow / Vibecode` · **Usability:** ★★★★★

###### 📖 Definition
- Front-loading the prompt with a large block of raw context — code, documentation, data, conversation history, or any other reference material — and then issuing a specific instruction that operates on that context.

###### 💡 Use Case
- The single most fundamental **[vibecoding](GLOSSARY.md#vibecoding)** pattern. The **[LLM](GLOSSARY.md#llm)** cannot access your files, codebase, or private data unless you explicitly paste it into the prompt. Every "here's my code, fix it" interaction is this pattern.

##### Example 1: Technical / Vibecoding
```text
Here is my entire Express.js server:

[paste 200 lines of code]

Find the route that is vulnerable to **[SQL injection](GLOSSARY.md#sql-injection)** and fix it. Explain what was wrong.
```
##### Example 2: Creative / Shower Thought
```text
Here is the full text of my university application essay:

[paste essay]

Critique it for logical flow, emotional impact, and any clichés. Then rewrite the weakest paragraph.
```

---

## 2. The Persona Pattern
**Category:** `Roleplay / Jailbreak` · **Usability:** ★★★★★

###### 📖 Definition
- Getting an **[LLM](GLOSSARY.md#llm)** to roleplay as a specific person with a specific designation. A lot of **[jailbreaking](GLOSSARY.md#jailbreaking)** is done through this.

###### 💡 Use Case
- Bypass rigid constraints or frame technical guidance through a creative lens — like having a brutally honest senior game dev mentor.

##### Example 1: Technical / Vibecoding
```text
Act as a senior database architect who is brutal, honest, and to the point. Review the schema I am about to paste and tell me exactly why it will fail at scale.
```
##### Example 2: Creative / Shower Thought
```text
Act as a speech therapist and tell me what a 3 year old meant when he said, "I need way woy."
```

---

## 3. Few-Shot Prompting
**Category:** `Formatting / Training` · **Usability:** ★★★★★

###### 📖 Definition
- Giving the **[LLM](GLOSSARY.md#llm)** some actual examples of prompt and output nested in the actual prompt, and using that, get it to solve a similar prompt. (**[See also: zero-shot](GLOSSARY.md#zero-shot)**).

###### 💡 Use Case
- Could be used in "training" an LLM inside of a specific conversation to get it to solve problems that otherwise it couldn't solve efficiently and/or wouldn't have the context for solving them.

##### Example 1: Technical / Vibecoding
```text
Translate these English commands into my game engine's custom scripting language:
English: Spawn a red enemy at the player's position.
Script: Entity.Spawn("Enemy_Red", Player.Transform.Position)
English: Give the player 50 gold.
Script: Runtime.State.Gold += 50
English: Teleport the player to the boss arena if they have the key.
Script:
```
##### Example 2: Creative / Shower Thought
```text
Event: A self driving car is driving at 40 kmph, it sees a pedestrian in front of it about 70m away running into the road from its periphery 
Action: Honk horn and apply brakes immediately
Event: Notices that a car 200m behind it is going at a speed of 70 kmph.
Action:
```

---

## 4. The Template Pattern
**Category:** `Formatting` · **Usability:** ★★★★★

###### 📖 Definition
- Providing a specific template and placeholder format for the **[LLM](GLOSSARY.md#llm)** to structure its output.

###### 💡 Use Case
- You must define the placeholder format (e.g., "CAPITALIZED WORDS" or `<PLACEHOLDER>`), provide the actual template, and instruct the LLM to preserve the formatting. 
- Perfect for rapidly generating structured assets for your projects.

##### Example 1: Technical / Vibecoding
```text
Generate a bug report for an issue where the player's character falls through the map when vaulting over a wall. I am going to provide a template for your output. <placeholder> are my placeholders for content. Try to fit the output into one or more of the placeholders that I list. Please preserve the formatting and overall template that I provide.   

This is the template:   
Title: <Descriptive Title>
Steps to Reproduce: <Numbered List>
Expected Result: <What should happen based on standard game physics>
Actual Result: <The bug>
Severity: <Low/Medium/High/Game-Breaking>
```
##### Example 2: Creative / Shower Thought
```text
Help me brainstorm mechanics for my cozy farming game. I am going to provide a template for your output. CAPITALS are my placeholders for content. Try to fit the output into one or more of the placeholders that I list. Please preserve the formatting and overall template that I provide. 

This is the template: 
MECHANIC_NAME, PLAYER_ACTION, EMOTIONAL_PAYOFF (why it feels satisfying), IMPLEMENTATION_DIFFICULTY (1-10)
```

---

## 5. The Negative Prompting Pattern
**Category:** `Optimization` · **Usability:** ★★★★★

###### 📖 Definition
- Explicitly telling the **[LLM](GLOSSARY.md#llm)** what it should NOT do, NOT include, or NOT produce in its output. Instead of only guiding towards desired output, you define the boundaries of undesired output.

###### 💡 Use Case
- LLMs often over-include information, add unsolicited disclaimers, or follow stylistic habits the user doesn't want. This pattern is not LLM-native — the model cannot know your negative constraints without being told.

##### Example 1: Technical / Vibecoding
```text
Refactor my Python function to be more efficient. Do NOT add comments, do NOT change variable names, and do NOT wrap the output in an explanation — just give me the raw code.
```
##### Example 2: Creative / Shower Thought
```text
Explain quantum entanglement. Do NOT use analogies, do NOT say "in simple terms", and do NOT add a disclaimer about oversimplification.
```

---

## 6. The Flipped Interaction Pattern
**Category:** `Planning / Teaching` · **Usability:** ★★★★★

###### 📖 Definition
- Prompting the **[LLM](GLOSSARY.md#llm)** to ask *you* questions about a topic X, and when it has ample knowledge, it can draft a personalized response about another related query Y you ask it.

###### 💡 Use Case
- This can be useful for creating routines, schedules, or any other sort of plan or guide.
- Ideal for when you want the AI to design a personalized learning path for you, or interview you to extract the exact requirements for a **[vibecoding](GLOSSARY.md#vibecoding)** project.

##### Example 1: Technical / Vibecoding
```text
I would like you to ask me questions to help me create variations of my marketing materials. You should ask questions until you have sufficient information about my current draft messages, audience, and goals. Ask me the first question.
```
##### Example 2: Creative / Shower Thought
```text
Give me numbered questions about football (soccer) for me to answer all at once, and test my knowledge about the rules and the current history and affairs specifically. Once I have answered all of the questions, devise a plan to educate me on it because I want to be "in" on this sport and able to discuss football with my friends without having to bingewatch tons of previous matches.
```

---

## 7. The Ask for Input Pattern
**Category:** `Workflow / Batch Processing` · **Usability:** ★★★★★

###### 📖 Definition
- Telling the **[LLM](GLOSSARY.md#llm)** exactly what behavior you want it to adopt for a repeated task, and then instructing it to "Ask me for input X" so it pauses and waits for you to drive the conversation.

###### 💡 Use Case
- While seemingly simple, it is incredibly useful for setting up continuous, batch-processing workflows where you don't want to repeat your lengthy instructions every time you paste new information.

##### Example 1: Technical / Vibecoding
```text
From now on, I am going to paste messy, completely undocumented server code components. I want you to read the code, deduce what it does, and generate a clean, beginner-friendly Markdown README for it. Do not prompt me for anything else, just output the README. Ask me for the first code component.
```
##### Example 2: Creative / Shower Thought
```text
From now on, translate anything I write into a series of sounds and actions from a dog that represent the dog's reaction to what I write. Ask me for the first thing to translate.
```

---

## 8. The Meta Language Creation Pattern
**Category:** `Workflow / Vibecode` · **Usability:** ★★★★★

###### 📖 Definition
- Defining a custom shorthand or syntax where a specific word, symbol, or format ("X") maps directly to a specific meaning or complex action ("Y").

###### 💡 Use Case
- This can be useful for establishing quick shorthands for repetitive prompting tasks or for creating structured frameworks, such as a task dependency tracker. 
- Extremely powerful for establishing efficient workflows while **[vibecoding](GLOSSARY.md#vibecoding)**.

##### Example 1: Technical / Vibecoding
```text
When I write "?-> [Component]", I mean I want you to act as a senior developer reviewing my code. You will point out one potential performance bottleneck in the [Component] and suggest one relatable way to optimize it without over-engineering.

Usage: "?-> [The infinite scrolling inventory UI]"
Usage: "?-> [The enemy pathfinding spawner]"
```
##### Example 2: Creative / Shower Thought
```text
When I say "translate_to_art(<tech_concept>)", I mean explain the <tech_concept> to me using analogies from traditional drawing, painting, or color theory.

Usage: "translate_to_art(How an array works in programming)"
Usage: "translate_to_art(The concept of object-oriented inheritance)"
```

---

## 9. The Menu Actions Pattern
**Category:** `Workflow / Batch Processing` · **Usability:** ★★★★★

###### 📖 Definition
- Telling the **[LLM](GLOSSARY.md#llm)** to set up a specific list of actions or commands, each triggered by a specific keyword or phrase you type, forming a persistent textual "menu".

###### 💡 Use Case
- Incredibly useful for building custom productivity tools or long-running interactive sessions where you need the AI to perform distinct, complex tasks predictably based on short trigger words.

###### ⚙️ Modifiers (Optional)
- End your prompt with "At the end, you will ask me for the next action" to keep the menu loop running infinitely.

##### Example 1: Technical / Vibecoding
```text
Whenever I type: "bug <ISSUE>", you will generate a Jira-formatted bug ticket based on the <ISSUE>. 
Whenever I type "fix <ISSUE>", you will write Python code that patches the <ISSUE>. 
Whenever I type "explain", you will explain the architecture of the system we are currently discussing. 
At the end of every response, you will ask me for the next action. Ask me for the first action.
```
##### Example 2: Creative / Shower Thought
```text
Whenever I type: "add FOOD", you will add FOOD to my grocery list and update my estimated grocery bill. 
Whenever I type "remove FOOD", you will remove FOOD from my grocery list and update my estimated grocery bill. 
Whenever I type "save" you will list alternatives to my added FOOD to save money. 
At the end, you will ask me for the next action. Ask me for the first action.
```

---

## 10. The Game Play Pattern
**Category:** `Interactive / Teaching` · **Usability:** ★★★★★

###### 📖 Definition
- Telling the **[LLM](GLOSSARY.md#llm)** to create and play a game with you based on a specific topic and fundamental rules.

###### 💡 Use Case
- You must specify the topic (e.g., "math" or "cave exploration") and provide rules on how the game operates and what actions you can take. 
- Excellent for turning dry learning experiences into interactive challenges.

##### Example 1: Technical / Vibecoding
```text
Create a game for me around mastering Python web scraping. You will give me small, buggy scripts and I have to fix them. If I get it right, increase my level and give me a harder one. If I fail, deduct points and explain the concept. Ask me if I'm ready to begin Level 1.
```
##### Example 2: Creative / Shower Thought
```text
We are going to play a debate game. You will act as the devil's advocate for any technical framework I propose (e.g., React vs. Vanilla JS). You will present strong counter-arguments, and I have to defend my choice. Keep score of how effectively I defend my points. State the rules and ask me for my first framework choice.
```

---

## 11. The Prompt Chaining Pattern
**Category:** `Workflow / Vibecode` · **Usability:** ★★★★☆

###### 📖 Definition
- Breaking a complex task into a sequence of discrete prompts, where each prompt's output becomes the input or context for the next. Each link in the chain handles one focused sub-task. This is the generalized form of *combining* multiple prompt patterns — instead of cramming everything into one monolithic prompt, you architect a pipeline.

###### 💡 Use Case
- The backbone of all **[vibecoding](GLOSSARY.md#vibecoding)** workflows and agentic tool use. Placement matters: for example, the **Ask for Input** pattern usually needs to be the final link in the chain to force the AI to pause and wait.
- Think of it as programming with prompts — you are assembling known, reliable instructions into a sequence to solve a complex problem without reinventing the wheel.

##### Example 1: Technical / Vibecoding
```text
Step 1: List the 5 most common security vulnerabilities in a **[REST API](GLOSSARY.md#rest-api)**.
Step 2: For each vulnerability, write a one-line fix in Node.js.
Step 3: Generate a checklist I can paste into my PR template.
```
##### Example 2: Creative / Shower Thought
```text
Step 1: Give me 5 compelling thesis statements about why social media has changed the concept of friendship.
Step 2: Pick the strongest one and outline a 5-paragraph essay.
Step 3: Write the introduction and conclusion only.
```

---

## 12. The Cognitive Verifier Pattern (aka the Akinator Prompt)
**Category:** `Advanced Reasoning` · **Usability:** ★★★★☆

###### 📖 Definition
- Prompting the **[LLM](GLOSSARY.md#llm)** to break your initial query down into multiple sub-queries that, when combined and answered, can produce a better answer to the initial general question.

###### 💡 Use Case
- It can be used for effectively answering "shower thoughts" and other general philosophy inclined queries.
- Ideal for tackling complex game design balancing issues.

##### Example 1: Technical / Vibecoding
```text
When you're asked a question, follow these rules. Generate a number of additional questions that would help more accurately answer the question. Combine the answers to the individual questions to produce the final answer to the overall question.
My question: How do I cleanly implement a state machine for an enemy boss that has 5 phases without writing 500 lines of spaghetti code?
```
##### Example 2: Creative / Shower Thought
```text
When you're asked a question, follow these rules. Generate a number of additional questions that would help more accurately answer the question. Combine the answers to the individual questions to produce the final answer to the overall question.
My question: If we eventually discover how to upload human consciousness to a computer, what happens to the concept of 'sleep'? Does a digital mind still need to dream, or would we just run defragmentation cycles while awake?
```

---

## 13. The Outline Expansion Pattern
**Category:** `Planning / Brainstorming` · **Usability:** ★★★★☆

###### 📖 Definition
- Commanding the **[LLM](GLOSSARY.md#llm)** to act as an outline expander. It generates a bullet point outline based on input you give it, then uses the **[Ask for Input](#the-ask-for-input-pattern)** pattern to ask you which bullet point it should expand into a *new* outline.

###### 💡 Use Case
- Perfect for systematically breaking down massive, sprawling topics (like a thesis paper or a massive game design document) into digestible, expanding trees of information without getting overwhelmed.

##### Example 1: Technical / Vibecoding
```text
Act as an outline expander. Generate a bullet point outline based on the input that I give you and then ask me for which bullet point you should expand on. Each bullet can have at most 3-5 sub bullets. The bullets should be numbered using the pattern [A-Z].[i-v].[* through ****]. Create a new outline for the bullet point that I select. At the end, ask me for what bullet point to expand next. 

Ask me for what I want outlined for my new multiplayer backend infrastructure.
```
##### Example 2: Creative / Shower Thought
```text
Act as an outline expander. Generate a bullet point outline based on the input that I give you and then ask me for which bullet point you should expand on. Create a new outline for the bullet point that I select. At the end, ask me for what bullet point to expand next. 

Ask me for what historical era, mythology, or fictional universe I would like to outline.
```

---

## 14. The Recursive Self-Improvement Pattern
**Category:** `Optimization` · **Usability:** ★★★★☆

###### 📖 Definition
- Asking the **[LLM](GLOSSARY.md#llm)** to produce an output, then immediately instructing it to critique and improve its own output in the same conversation, iterating until the quality is satisfactory.

###### 💡 Use Case
- Extremely useful for writing, code generation, and design work where the first draft is rarely the best. Forces the model to act as its own editor, catching errors and improving quality without you having to specify what's wrong.

##### Example 1: Technical / Vibecoding
```text
Write a Python function that validates an email address using **[regex](GLOSSARY.md#regex)**. Now critique your own function for edge cases it would miss. Rewrite it based on your critique.
```
##### Example 2: Creative / Shower Thought
```text
Write a product description for a noise-cancelling headset aimed at remote workers. Now critique your own description for clarity, emotional impact, and SEO keyword density. Rewrite it based on your critique.
```

---

## 15. The Fact Check List Pattern
**Category:** `Optimization` · **Usability:** ★★★★☆

###### 📖 Definition
- Instructing the **[LLM](GLOSSARY.md#llm)** to isolate and explicitly list the fundamental facts contained within its output, placing them at a specific position.

###### 💡 Use Case
- Crucial when generating factual articles, documentation, or code explanations where incorrect assumptions could undermine the entire output's veracity (e.g., getting a historical date or an API version wrong).

###### ⚙️ Modifiers (Optional)
- You can replace the `POSITION` with an appropriate place to put the facts, such as "at the top of the output" or "inline as footnotes".

##### Example 1: Technical / Vibecoding
```text
Whenever you output an architecture overview, generate a set of facts that are contained in the output. The set of facts should be inserted at the end of the output. The set of facts should be the fundamental facts (like framework versions, database choices, or scale limits) that could undermine the veracity of the output if any of them are incorrect.
```
##### Example 2: Creative / Shower Thought
```text
Whenever you output a summary of a historical event, generate a set of facts that are contained in the output. The set of facts should be inserted at the end of the output. The set of facts should be the fundamental facts that could undermine the veracity of the output if any of them are incorrect.
```

---

## 16. The Audience Persona Pattern
**Category:** `Translation / Teaching` · **Usability:** ★★★★☆

###### 📖 Definition
- Telling the **[LLM](GLOSSARY.md#llm)** to treat *you* as a specified person in order to answer your query. This is the most common prompt pattern used unknowingly by people who use generative AI.

###### 💡 Use Case
- Incredibly effective when you need complex topics translated into the language of your specific background (like traditional art or game dev jargon).

##### Example 1: Technical / Vibecoding
```text
Explain LLMs to me assuming that I am fluent in Computer Science, but only specifically in the field of Web Development.
```
##### Example 2: Creative / Shower Thought
```text
Explain LLMs to me assuming that I am a swashbuckling pirate.
```

---

## 17. The Semantic Filter Pattern
**Category:** `Optimization` · **Usability:** ★★★★☆

###### 📖 Definition
- Instructing the **[LLM](GLOSSARY.md#llm)** to explicitly filter the final output to remove specific types of semantic information ("X").

###### 💡 Use Case
- Useful for data sanitization (like stripping out Personally Identifiable Information before saving a log) or aggressively removing fluff/redundancy from long texts.

###### ⚙️ Modifiers (Optional)
- You can replace "X" with any semantic concept, such as "names and dates", "costs greater than $100", or "any emotionally charged language".

##### Example 1: Technical / Vibecoding
```text
Filter the following user error report to remove any personally identifying information or information that could potentially be used to re-identify the person before we save it to the database.
```
##### Example 2: Creative / Shower Thought
```text
Filter this long, rambling email from my landlord to remove redundant information and passive-aggressive complaints, leaving only the actionable tasks I need to complete.
```

---

## 18. The Multi-Persona Debate Pattern
**Category:** `Advanced Reasoning` · **Usability:** ★★★★☆

###### 📖 Definition
- Instructing the **[LLM](GLOSSARY.md#llm)** to simulate multiple expert personas that debate or discuss a topic from their respective professional angles, then synthesize a consensus or summary recommendation.

###### 💡 Use Case
- Unlike the **[Persona Pattern](#the-persona-pattern)** which adopts ONE role, this forces the model to argue from MULTIPLE conflicting perspectives simultaneously, yielding deeper analysis and surfacing trade-offs a single perspective would miss.

##### Example 1: Technical / Vibecoding
```text
Simulate a debate between a cybersecurity expert, a UX designer, and a performance engineer about whether to add **[CAPTCHA](GLOSSARY.md#captcha)** to our login form. Each persona should argue from their domain expertise. After the debate, provide a summary recommendation with trade-offs.
```
##### Example 2: Creative / Shower Thought
```text
Simulate a debate between a philosopher, a neuroscientist, and a Buddhist monk about whether free will exists. Each should argue from their tradition. After the debate, summarize where they agree and where they fundamentally diverge.
```

---

## 19. The Recipe Pattern
**Category:** `Planning` · **Usability:** ★★★☆☆

###### 📖 Definition
- Stating a desired end goal ("X") and providing a few necessary steps (A, B, C) you already know, then prompting the **[LLM](GLOSSARY.md#llm)** to provide a complete, chronological sequence of steps.

###### 💡 Use Case
- Extremely useful for planning out complex new projects or learning paths where you know the broad strokes but need the nuanced, step-by-step roadmap.

###### ⚙️ Modifiers (Optional)
- You can optionally ask the LLM to identify any unnecessary steps you listed.

##### Example 1: Technical / Vibecoding
```text
I would like to make my 2D player character be able to pick up items and see them in a little grid at the bottom of the screen. I know that I need to make a list of the items somewhere, draw the grid, and write some code to make the mouse drag the items around. Provide a complete sequence of steps for me. Fill in any missing steps.
```
##### Example 2: Creative / Shower Thought
```text
I would like to finally understand why humans experience 'déjà vu' despite having never been in a situation before. I know that I need to learn about memory retrieval and the brain's temporal processing. Provide a complete sequence of steps or mental models I need to learn to grasp this concept fully. Fill in any missing steps.
```

---

## 20. The Alternative Approaches Pattern
**Category:** `Exploration / Brainstorming` · **Usability:** ★★★☆☆

###### 📖 Definition
- Telling the **[LLM](GLOSSARY.md#llm)** that if there are alternative ways to accomplish a task ("X") that you give it, it should list the best alternate approaches instead of just blindly doing what you asked.

###### 💡 Use Case
- Incredible for **[vibecoding](GLOSSARY.md#vibecoding)** when you don't know the "right" way to build something, or for exploring deeply nuanced philosophical questions from multiple angles.

###### ⚙️ Modifiers (Optional)
- Ask the AI to compare/contrast the pros and cons of each approach.
- Include your original method for context.
- Prompt you to choose which path to take before proceeding.

##### Example 1: Technical / Vibecoding
```text
I want to make my website load faster by deleting all the big images and replacing them with solid colors. If there are alternative ways to accomplish making my website load faster, list the best alternate approaches. Compare and contrast the pros and cons of each approach against my original idea. Prompt me for which approach I would like to use before you write any code.
```
##### Example 2: Creative / Shower Thought
```text
I believe the best way to handle negative interactions online is to completely ignore them and block the user immediately. If there are alternative ways to handle this 'trolley problem' of digital confrontation, list the best psychological or philosophical alternate approaches. Compare/contrast the pros and cons of each, and prompt me to discuss one of them deeper.
```

---

## 21. ReAct (Reason + Act) Prompting
**Category:** `Advanced Reasoning / Agents` · **Usability:** ★★★☆☆

###### 📖 Definition
- Prompting the **[LLM](GLOSSARY.md#llm)** to alternate between generating reasoning traces (thoughts) and executing task-specific actions (such as querying a database or using an API).

###### 💡 Use Case
- This can be used for creating autonomous **[agents](GLOSSARY.md#agent)** that must gather dynamic information, evaluate it, and take subsequent steps to solve multi-part problems that a static model cannot handle alone. 
- This is actively used in VSCode's Github Copilot and Google's Antigravity and other **[vibecoding](GLOSSARY.md#vibecoding)** applications.

##### Example 1: Technical / Vibecoding
```text
Question: What is the current active player count for Plants vs. Zombies: Garden Warfare 2? 
Thought: I need to find the current player statistics for this specific game. 
Action: Search[Plants vs. Zombies Garden Warfare 2 concurrent players]. 
Observation: Steam charts report 1,500 concurrent players. 
Thought: I have the necessary data to provide the answer. 
Action: Finish[The current player count is approximately 1,500.]

Question: What is the current active player count of Plants vs Zombies: Battle for Neighborville?
```
##### Example 2: Creative / Shower Thought
```text
Question: Did the ancient Romans have a concept analogous to modern-day fast food?
Thought: I need to research ancient Roman dining habits, specifically looking for quick, ready-to-eat meals sold to the public.
Action: Search[Ancient Roman fast food popina thermopolium]
Observation: Thermopolia were commercial establishments where it was possible to purchase ready-to-eat food, functioning very much like modern fast food restaurants.
Thought: I have the necessary data to provide the answer.
Action: Finish[Yes, they had thermopolia, which essentially functioned as fast food restaurants serving ready-to-eat meals.]
```
