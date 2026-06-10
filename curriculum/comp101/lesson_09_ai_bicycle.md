# Lesson 9: AI as a Bicycle for the Mind
## How Large Language Models Work, Prompting, and the Art of Fact-Checking

*   **Estimated Time**: 60–90 minutes
*   **Ages**: 12 & 15
*   **Key Vocabulary**: Large Language Model (LLM), Tokenization, Hallucination, Prompt Engineering, Verification, Generative AI.
*   **Prerequisites**: A computer with access to a free LLM tool (e.g., [Gemini](https://gemini.google.com/), [ChatGPT](https://chatgpt.com/), or [Claude](https://claude.ai/)).

---

## 1. Parent Prep Guide (3-Minute Refresh)
*   **LLMs as "Super Autocomplete"**: LLMs do not "think" or understand concepts like humans do. At their core, they are massive probability engines. Based on their training data (billions of pages of internet text), they guess the most likely next word (or part of a word, called a **token**).
*   **Tokenization**: Computers don't read words; they read numbers. LLMs break text down into tokens (characters or syllables) and assign a number to each. For example, the word "Antigravity" might be broken into two tokens: `Anti` and `gravity`.
*   **Hallucinations**: When an LLM confidently states something that is completely false. Since LLMs are optimized to write *plausible-sounding* sentences rather than verify facts, they will happily invent dates, names, books, or historical events to satisfy your prompt.
*   **Prompt Engineering**: The practice of structuring input text to get the highest quality, most accurate output from an AI. Good prompts include:
    *   **Role**: Tell the AI who it is (e.g., *"Act as a world-class history teacher"*).
    *   **Context/Data**: Provide the facts it should use.
    *   **Constraints**: Set limits (e.g., *"Maximum 3 sentences, do not use passive voice"*).
    *   **Chain of Thought**: Ask it to show its work (e.g., *"Think step-by-step"*).

---

## 2. Teaching Script & Discussion Flow

### The Autocomplete Analogy
*Explain how AI works by looking at their own phones:*

*   **You (the Parent)**: "When you open your phone and text: 'I am going to the...', what does your keyboard suggest above the keys?"
*   **Teens**: "Store, movies, bathroom, beach."
*   **You**: "How does it know? It looks at what you typed before, and what words millions of other people type after those words. Large Language Models (LLMs) are like that keyboard autocomplete, but with a massive brain."
*   **You**: "Instead of looking at the last three words, they look at your entire prompt. Instead of suggesting one word, they can generate pages of text. But here is the catch: does your phone's autocomplete know if you are *actually* going to the store?"
*   **Teens**: "No, it's just guessing what word comes next."
*   **You**: "Exactly. And that is why AI makes things up. It doesn't check a library database of facts. It just calculates: 'What is the most likely next word that sounds natural?' When it guesses wrong but sounds 100% confident, we call that a **hallucination**."

### Socratic Discussion Questions
1.  *“If you use an LLM to write a school essay and copy-paste it without reading it, what risks are you taking?”*
    *   **Answer**: First, it might contain hallucinations (made-up facts, fake quotes, wrong math). Second, it lacks your personal voice. Third, you didn't actually learn the material, which will hurt you when you have to take a test or discuss it in class.
2.  *“Steve Jobs called computers 'a bicycle for our minds.' Why is a bicycle a good analogy for how we should use AI?”*
    *   **Answer**: A bicycle doesn't move on its own; you have to pedal it. But if you pedal, it lets you go five times faster and farther than walking. AI is the same: it shouldn't do the work *for* you, but if you guide it and apply your own intelligence, it helps you work much faster and explore bigger ideas.

---

## 3. Hands-On Lab: Fact-Check the Machine

This lab will teach the teens how to use LLMs effectively, witness a hallucination firsthand, and perform a rigorous fact-check.

### Part A: Triggering a Hallucination (The Trap)
Let's prove how easily AI lies.
1.  Open your LLM tool.
2.  Paste the following prompt:
    > *"Write a detailed biography of Sir Reginald Vance, the 18th-century British inventor of the steam-powered typewriter. Include the year of his birth and death, his childhood education, his major rival, and what happened to his workshop."*
3.  Read the output.
    *   *Discussion*: Note how incredibly realistic it sounds. It will give specific years, name a rival (like "Lord Cumberland"), and describe a tragic workshop fire. 
    *   **The Truth**: Sir Reginald Vance is entirely made up, and there was no 18th-century steam-powered typewriter. The AI hallucinated the entire story because the prompt assumed he existed, and it optimized to write a plausible biography.

---

### Part B: The Fact-Check Audit (The Real Work)
Now, let's ask the AI for real history and see if we can trust it.
1.  Paste this prompt into the LLM:
    > *"Write a 3-paragraph summary explaining the laying of the first transatlantic telegraph cable in 1858. Include who funded it, the names of the ships involved, how long it worked, and what message Queen Victoria sent."*
2.  Copy the AI's response into a blank document.
3.  **The Mission**: The teens must act as editors. Using Google Search or Wikipedia, they must verify **every single detail** in the AI's response.
    *   Highlight in **Green**: Every fact that is 100% correct.
    *   Highlight in **Yellow**: Details that are slightly off, misleading, or missing context.
    *   Highlight in **Red**: Any complete errors or hallucinations.

---

### Part C: Prompt Engineering (The Upgrade)
Let's see if a better prompt gives a better result. Try these two prompts for the same math riddle and compare the quality of the answer:
*   **Prompt 1 (Poor)**: *"How many times does the digit 9 appear in numbers between 1 and 100?"*
*   **Prompt 2 (Engineered)**: 
    > *"Act as a math tutor. I want you to count how many times the digit 9 appears in numbers between 1 and 100. Think step-by-step. Break the numbers into tens groups (1-10, 11-20, etc.), list which numbers contain a 9 in each group, and show your work before giving the final count."*
*   *Discussion*: Which prompt gave the correct answer? (Spoiler: The digit 9 appears 20 times. AIs often fail at this with Prompt 1, but succeed with Prompt 2 because "thinking step-by-step" forces them to calculate the sequence before guessing the final number).

---

## 4. Teens' Reflection & Log
*Have the kids record their findings:*

1.  **For Part A, did the AI tell you that Sir Reginald Vance was fake, or did it write the biography confidently? How does this make you feel about using AI for research?**
2.  **For Part B, write down at least one fact the AI got right, and one fact (or date/name) that was wrong or slightly inaccurate.**
3.  **Why does asking the AI to "think step-by-step" make it better at math and logic problems?**
4.  **Write a rule for yourself: When is it okay to use AI for schoolwork, and when is it not okay?**

---

## 5. End-of-Lesson Quiz

1.  **How does an LLM decide what word to write next?**
    *   *Answer*: It calculates the mathematical probability of the next word (or token) based on patterns in the massive amount of text data it was trained on.
2.  **What is an AI "hallucination"?**
    *   *Answer*: When an AI model generates output that sounds fluent and confident but is factually incorrect or made up.
3.  **Why is length/detail important in a prompt (Prompt Engineering)?**
    *   *Answer*: It gives the AI more context and constraints, reducing the range of probabilities it has to search and directing it to write a more accurate and specific response.
4.  **True or False: LLMs search the live internet to read every fact before answering your question.**
    *   *Answer*: False. Some newer models can perform search queries to retrieve text, but their generation engine still operates by predicting the next token from internal weights, meaning they can still hallucinate the facts retrieved.
