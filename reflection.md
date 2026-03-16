# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the secret number kept changing" or "the hints were backwards").

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
  I used Copilot for this project mainly.
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
  Something good the AI did was fixing the New Game problem. One thing I had notice while doing my code was that New Game button would work if the game was still ongoing, but not if it was finished. When I asked the AI about that, it identified the problem as the session state not resetting when the new game button was clicked, meaning that when the game reset, it was not in the playing state and thus immediately stopped, and I allowed the AI to change it so that it properly reset, and when I tested it myself, the New Game button worked as it should.

- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).
  One weird thing the AI did was change the session state attempts to reset to 1. I asked it to explain why it did that, but its explanation did not make a lot of sense, and when I actually tried to run the game, I saw it made the game start with the incorrect number of attempts, so I undid that specfic change.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
  Generally, what I did is I tried out the steps that lead to a bug, then saw if the bug still happened. Then I tried again. Then I tried a different variation of the steps. I tried situtions where the code had previously worked correctly to see if the bug happened there. If I never then saw the bug again, I decided it was fixed.
- Describe at least one test you ran (manual or using pytest)  
   and what it showed you about your code.
  When the AI said it fixed the new game bug, I decided to test it by using all my attempts so I was in a non-playing state and then clicke new game to see if the bug reappeared. I then tested it in a playing state. Then I tested it when I had 0 attempts. Then I spam clicked the button to make sure it could handle multiple new games. It worked for all of them.
- Did AI help you design or understand any tests? How?
  While I did my own tests mostly, the AI also did its own. That being said those tests did not seem that robust, so in general I did not rely on them.

---

## 4. What did you learn about Streamlit and state?

- In your own words, explain why the secret number kept changing in the original app.
- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
- What change did you make that finally gave the game a stable secret number?

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.
