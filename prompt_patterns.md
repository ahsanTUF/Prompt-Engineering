# Prompt Patterns I learnt in Coursera

## The Persona Pattern
- It involves getting an LLM to roleplay as a specific person having a specific designation.
- Usually a lot of jailbreaking is done through Persona Prompting.
  - *Useful for bypassing rigid constraints or framing technical guidance through a creative lens (like a demanding senior game dev mentor).*
- **Example:** `Act as a speech therapist and tell me what a 3 year old meant when he said, "I need way woy."`

## The Audience Persona Pattern
- It involves telling the LLM to treat you as a specified person in order to answer your query.
- This is the most common prompt pattern used unknowingly by people who use generative AI.
  - *Incredibly effective when you need complex topics translated into the language of your specific background (like traditional art or game dev jargon).*
- **Example 1:** `Explain LLMs to me assuming that I am a swashbuckling pirate`
- **Example 2:** `Explain LLMs to me assuming that I am fluent in Computer Science, but only specifically in the field of Web Development.`

## The Question Refinement Pattern
- It usually involves giving a root prompt to an LLM to refine your question for you and then optionally proceed with that improved query as input.
- You can uncover some unasked for but useful information with this technique. It's purpose is to improve interaction with the specific LLM.
- **Example 1:** `From now on, whenever I ask you a question, refine/improve that question for me and then ask me to optionally proceed with that improved query instead.`
- **Example 2:** `Whenever I ask a question about who is the greatest of all time (GOAT), suggest a better version of the question that puts multiple players unique accomplishments into perspective Ask me for the first question to refine.`

## The Cognitive Verifier Pattern (aka the Akinator Prompt)
- It involves prompting the LLM to break your initial query down into multiple queries that when combined and answered can produce a better answer to the initial general question.
- It can be used for effectively answering "shower thoughts" and other general philosophy inclined queries, or for tackling complex game design balancing issues.
- **Example:** `When you're asked a question, follow these rules. Generate a number of additional questions that would help more accurately answer the question. Combine the answers to the individual questions to produce the final answer to the overall question.`, followed by `If we eventually discover how to upload human consciousness to a computer, what happens to the concept of 'sleep'? Does a digital mind still need to dream, or would we just run defragmentation cycles while awake?`

## The Flipped Interaction Pattern
- It involves prompting the LLM to ask YOU questions about a topic X, and when it has ample knowledge, it can draft a personalized response about another related query Y you ask it.
- This can be useful for creating routines, schedules, or any other sort of plan or guide.
  - *Ideal for when you want the AI to design a personalized learning path for you, or interview you to extract the exact requirements for a vibecoding project.*
- **Example 1:** `Give me numbered questions about football (soccer) for me to answer all at once, and test my knowledge about the rules and the current history and affairs specifically. Once I have answered all of the questions, devise a plan to educate me on it because I want to be "in" on this sport and able to discuss football with my friends without having to bingewatch tons of previous matches.`
- **Example 2:** `I would like you to ask me questions to help me create variations of my marketing materials. You should ask questions until you have sufficient information about my current draft messages, audience, and goals. Ask me the first question.`

## Few-Shot Prompting
- It means to give the LLM some examples of prompt and output nested in the actual prompt, and using that, get it to solve a similar prompt.
- Could be used in "training" an LLM inside of a specific conversation to get it to solve problems that otherwise it couldn't solve efficiently and/or wouldn't have the context for solving them.
- **Example:**
  ```text
  Event: A self driving car is driving at 40 kmph, it sees a pedestrian in front of it about 70m away running into the road from its periphery 
  Action: Honk horn and apply brakes immediately
  Event: Notices that a car 200m behind it is going at a speed of 70 kmph.
  Action:
  ```

## Chain of Thought Prompting
- It is a type of few-shot prompting, but instead of making rules, and answering them in the prompt, we use developed queries, answer them along with provided reasoning, and then prompt the LLM to answer a different query with reasoning attached to it.
- Probably obsolete in the current era of reasoning LLMs, but a use could still be found for this technique.
  - *Still an excellent pattern when you want to force the AI to document its exact logical steps when debugging intricate state machines or story lore inconsistencies.*
- **Example:** `Q: Roger has 5 tennis balls. He buys 2 more cans of tennis balls. Each can has 3 tennis balls. How many tennis balls does he have now? A: Roger started with 5 balls. 2 cans of 3 tennis balls each is 6 tennis balls. 5 + 6 = 11. The answer is 11. Q: The cafeteria had 23 apples. If they used 20 to make lunch and bought 6 more, how many apples do they have?`

## ReAct (Reason + Act) Prompting
- It involves prompting the LLM to alternate between generating reasoning traces (thoughts) and executing task-specific actions (such as querying a database or using an API).
- This can be used for creating autonomous agents that must gather dynamic information, evaluate it, and take subsequent steps to solve multi-part problems that a static model cannot handle alone. This is actively used in VSCode's Github Copilot and Google's Antigravity and other vibecoding applications.
- **Example:** 
  ```text
  Question: What is the current active player count for Plants vs. Zombies: Garden Warfare 2? 
  Thought: I need to find the current player statistics for this specific game. 
  Action: Search[Plants vs. Zombies Garden Warfare 2 concurrent players]. 
  Observation: Steam charts report 1,500 concurrent players. 
  Thought: I have the necessary data to provide the answer. 
  Action: Finish[The current player count is approximately 1,500.]
  ```
  followed by `Question: What is the current active player count of Plants vs Zombies: Battle for Neighborville?`

## The Game Play Pattern
- It involves telling the LLM to create and play a game with you based on a specific topic and fundamental rules.
- You must specify the topic (e.g., "math" or "cave exploration") and provide rules on how the game operates and what actions you can take. Excellent for turning dry learning experiences into interactive challenges.
- **Example 1:** `We are going to play a debate game. You will act as the devil's advocate for any technical framework I propose (e.g., React vs. Vanilla JS). You will present strong counter-arguments, and I have to defend my choice. Keep score of how effectively I defend my points. State the rules and ask me for my first framework choice.`
- **Example 2:** `Create a game for me around mastering Python web scraping. You will give me small, buggy scripts and I have to fix them. If I get it right, increase my level and give me a harder one. If I fail, deduct points and explain the concept. Ask me if I'm ready to begin Level 1.`

## The Template Pattern
- It involves providing a specific template and placeholder format for the LLM to structure its output.
- You must define the placeholder format (e.g., "CAPITALIZED WORDS" or `<PLACEHOLDER>`), provide the actual template, and instruct the LLM to preserve the formatting. Perfect for rapidly generating structured assets for your projects.
- **Example 1:** `Help me brainstorm mechanics for my cozy farming game. I am going to provide a template for your output. CAPITALS are my placeholders for content. Try to fit the output into one or more of the placeholders that I list. Please preserve the formatting and overall template that I provide. This is the template: MECHANIC_NAME, PLAYER_ACTION, EMOTIONAL_PAYOFF (why it feels satisfying), IMPLEMENTATION_DIFFICULTY (1-10)`
- **Example 2:**
  ```text
  Generate a bug report for an issue where the player's character falls through the map when vaulting over a wall. I am going to provide a template for your output. <placeholder> are my placeholders for content. Try to fit the output into one or more of the placeholders that I list. Please preserve the formatting and overall template that I provide.   

  This is the template:   
  Title: <Descriptive Title>
  Steps to Reproduce: <Numbered List>
  Expected Result: <What should happen based on standard game physics>
  Actual Result: <The bug>
  Severity: <Low/Medium/High/Game-Breaking>
  ```

## The Meta Language Creation Pattern
- It involves defining a custom shorthand or syntax where a specific word, symbol, or format ("X") maps directly to a specific meaning or complex action ("Y").
- This can be useful for establishing quick shorthands for repetitive prompting tasks or for creating structured frameworks, such as a task dependency tracker. Extremely powerful for establishing efficient workflows while vibecoding.
- **Example 1:**
  ```text
  When I say "translate_to_art(<tech_concept>)", I mean explain the <tech_concept> to me using analogies from traditional drawing, painting, or color theory.

  Usage: "translate_to_art(How an array works in programming)"
  Usage: "translate_to_art(The concept of object-oriented inheritance)"
  ```
- **Example 2:**
  ```text
  When I write "?-> [Component]", I mean I want you to act as a senior developer reviewing my code. You will point out one potential performance bottleneck in the [Component] and suggest one relatable way to optimize it without over-engineering.

  Usage: "?-> [The infinite scrolling inventory UI]"
  Usage: "?-> [The enemy pathfinding spawner]"
  ```

## The Recipe Pattern
- It involves stating a desired end goal ("X") and providing a few necessary steps (A, B, C) you already know, then prompting the AI to provide a complete, chronological sequence of steps.
  - *Extremely useful for planning out complex new projects or learning paths where you know the broad strokes but need the nuanced, step-by-step roadmap.*
- You can optionally ask the LLM to identify any unnecessary steps you listed.
- **Example 1:** `I would like to make my 2D player character be able to pick up items and see them in a little grid at the bottom of the screen. I know that I need to make a list of the items somewhere, draw the grid, and write some code to make the mouse drag the items around. Provide a complete sequence of steps for me. Fill in any missing steps.`
- **Example 2:** `I would like to finally understand why humans experience 'déjà vu' despite having never been in a situation before. I know that I need to learn about memory retrieval and the brain's temporal processing. Provide a complete sequence of steps or mental models I need to learn to grasp this concept fully. Fill in any missing steps.`

## The Alternative Approaches Pattern
- It involves telling the AI that if there are alternative ways to accomplish a task ("X") that you give it, it should list the best alternate approaches instead of just blindly doing what you asked.
  - *Incredible for vibecoding when you don't know the "right" way to build something, or for exploring deeply nuanced philosophical questions from multiple angles.*
- You can optionally ask the AI to compare/contrast the pros and cons of each approach, include your original method for context, and prompt you to choose which path to take before proceeding.
- **Example 1:** `I want to make my website load faster by deleting all the big images and replacing them with solid colors. If there are alternative ways to accomplish making my website load faster, list the best alternate approaches. Compare and contrast the pros and cons of each approach against my original idea. Prompt me for which approach I would like to use before you write any code.`
- **Example 2:** `I believe the best way to handle negative interactions online is to completely ignore them and block the user immediately. If there are alternative ways to handle this 'trolley problem' of digital confrontation, list the best psychological or philosophical alternate approaches. Compare/contrast the pros and cons of each, and prompt me to discuss one of them deeper.`
