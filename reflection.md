# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
    - hints were wrong, could not start a new game
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").
  
    - changing difficulty did not change the secret number to be in range
    - hints kept saying go lower when it should be higher
    - attempts don't reach max allowed
    - hard mode isn't actually harder than normal

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
    -  used claude
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
    - the go higher and go lower messages were wrong and I verified by playing the game
        and looking at the developer debug 
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).
    - claude gave me wrong cmd to run pytest but then self corrected. It was 
    pytest tests/test_game_logic.py vs python -m pytest tests/test_game_logic.py

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
    - by running pytest and manual test in the streamlit app
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
    - It showed me the hints was correct
- Did AI help you design or understand any tests? How?
    - It told me that the tuple returned by check_guess should be unpacked
---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
    - Streamlit reruns the whole app.py script on every input - click, type, button press, etc. To prevent variables getting reset to their default values, session state comes in to preserve it.

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
    - To use AI to generate tests to double check if requirements are met / bugs are fixed
- What is one thing you would do differently next time you work with AI on a coding task?
    - To understand more of the generated code before using it
- In one or two sentences, describe how this project changed the way you think about AI generated code.
    - It makes you focus less on syntax, more on high level program decisions