# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").

**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|-------|-------------------|-----------------|------------------------|
|Attempts |Attempts should be 8 |Attempts should be 7 |Console Output: None/ |
|Higher/Lower Hints Switched |When guess is > secret, "Go LOWER". When guess is < secret, "Go HIGHER". |When guess is > secret, "Go HIGHER". When guess is < secret, "Go LOWER". |Hints were switched |
|New Game |When New Game is clicked, "CORRECT" and hint messages are removed. |When New Game is clicked, no change. |Does not refreshed. |

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
For this project, I used claude in order to figure out how to fix the mistake in the code I found when it came to switching the hint values.
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
AI suggest that I switched the values of the hint in the code to if guess > secret: return "Too High", "📈 Go LOWER!" else: return "Too Low", "📉 Go HIGHER!". Which made the correct output.
- Give one example of an AI suggestion you did not accept as written (including what the AI suggested, why you rejected or changed it, and how you verified your version). It does not have to be a suggestion that was wrong: over-engineered, out of scope, harder to read, or a poor fit for this codebase all count.
The AI suggested adding some extra error handling, but I felt it was unnecessary and tested the app in Streamlit to verify that it still worked correctly.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
Once implementing the the right code in the app python file, I refreshed the website where the number guesser was located and witnessed the change functioning correctly.
- Describe at least one test you ran (manual or using pytest)
One test I ran was the the number of attempts that were displayed. Intially it was 7 attempts when it should've been 8. I went ahead and changed the code and once I refreshed the website, the display changed from 7 to 8, as it should be.  
  and what it showed you about your code.
  Showed me where certain displays and conditons are located within the code.
- Did AI help you design or understand any tests? How?
Yes, AI helped when it came to solving the START NEW GAME bug, which needed a change in design in order for the display of CORRECT or hints to be removed from the website.
---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
I noticed that Streamlit reruns code when you interact with the app, while session state saves information between reruns.
---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
  I think a testing habit that I would reuse in the future is using an AI agent to assist me in debugging certain aspects of the code or even location where bugs could potentially be.
- What is one thing you would do differently next time you work with AI on a coding task?
  I would use AI to work on one bug at a time, instead of trying to find all issues at once.
- In one or two sentences, describe how this project changed the way you think about AI generated code.
  To me, this project showed me that AI generated code can be helpful, but I shouldn't automatically accept every suggestion. I need to understand the code and test it to make sure it works the way I expect.
