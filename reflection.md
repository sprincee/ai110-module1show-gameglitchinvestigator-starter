# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?

  The game seemed normal, as if it wer fully functional.
  Yet, I quickly ran into bugs.
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").

  The hints were off: '99' was given a 'Go Higher' Hint, 
  yet '100' was given a 'Go Lower' hint.

  The hints were also wrong: the answer was 4.

  I also noted an incorrect amount of hints, I as given 6 rather than the displayed 7.

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?

  I used Claude for this project.
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).

  Using AI as a 'pair programmer' I asked it what may be wrong with the game. It suggested to look closely at the bounds for my guesses.
  It led me to finding the glitch with '99' being too low, '100' being too high, yet '4' being the answer.
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).

  The AI told me to look at front-end bugs, but, seeing as that I cannot edit that for this assignment, I did not listen to the AI. It did      mislead me though, enough to ask a TF about front-end bug considerations.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?

  Every time you interact with the app — clicking a button, typing something — Streamlit reruns the entire Python script from top to bottom. Session state is basically a dictionary that persists between those reruns so you don't lose things like your score, attempts, or game history each time the page refreshes.

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.

  Adding # FIXME comments before touching any code. It forced me to actually understand where the bug was before trying to fix it.
- What is one thing you would do differently next time you work with AI on a coding task?

  Test the game manually earlier instead of waiting until after all the fixes — would've caught the swapped hint messages sooner.
- In one or two sentences, describe how this project changed the way you think about AI generated code.

  AI generated code can look completely fine on the surface but have subtle logic bugs that only show up when you actually run it. You still have to read and test everything yourself.
