# Prompt Patterns I learnt in Coursera

## The Persona Pattern
- It involves getting an LLM to roleplay as a specific person having a specific designation.
- Usually a lot of jailbreaking is done through Persona Prompting.
- **Example:** `Act as a speech therapist and tell me what a 3 year old meant when he said, "I need way woy."`

## The Audience Persona Pattern
- It involves telling the LLM to treat you as a specified person in order to answer your query.
- This is the most common prompt pattern used unknowingly by people who use generative AI.
- **Example 1:** `Explain LLMs to me assuming that I am a swashbuckling pirate`
- **Example 2:** `Explain LLMs to me assuming that I am fluent in Computer Science, but only specifically in the field of Web Development.`

## The Question Refinement Pattern
- It usually involves giving a root prompt to an LLM to refine your question for you and then optionally proceed with that improved query as input.
- You can uncover some unasked for but useful information with this technique. It's purpose is to improve interaction with the specific LLM.
- **Example 1:** `From now on, whenever I ask you a question, refine/improve that question for me and then ask me to optionally proceed with that improved query instead.`
- **Example 2:** `Whenever I ask a question about who is the greatest of all time (GOAT), suggest a better version of the question that puts multiple players unique accomplishments into perspective Ask me for the first question to refine.`

## The Cognitive Verifier Pattern (aka the Akinator Prompt)
- It involves prompting the LLM to break your initial query down into multiple queries that when combined and answered can produce a better answer to the initial general question.
- It can be used for effectively answering "shower thoughts" and other general philosophy inclined queries.
- **Example:** `When you're asked a question, follow these rules. Generate a number of additional questions that would help more accurately answer the question. Combine the answers to the individual questions to produce the final answer to the overall question.`, followed by `How many mosquitoes could probably be in my front yard?`

## The Flipped Interaction Pattern
- It involves prompting the LLM to ask YOU questions about a topic X, and when it has ample knowledge, it can draft a personalized response about another related query Y you ask it.
- This can be useful for creating routines, schedules, or any other sort of plan or guide.
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
