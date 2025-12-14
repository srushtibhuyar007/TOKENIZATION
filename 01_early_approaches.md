# The Dawn of Tokenization: Early Approaches

In the early days of NLP, tokenization was relatively straightforward and often rule-based.

## 1. Word-based Tokenization
This was one of the simplest and most common approaches. Text was split into tokens based on whitespace and punctuation.

* **Introduction:** Imagine a sentence like "Hello, world!"
* **Process:** Split by spaces and remove punctuation.
* **Tokens:** ["Hello", "world"]

**Challenges:**
* **Contractions:** "don't" would be split into ["don", "'t"], losing its original meaning.
* **Hyphenated words:** "state-of-the-art" might become ["state", "of", "the", "art"].
* **Languages without spaces:** Languages like Chinese or Japanese don't use spaces to separate words, making this method ineffective.

> **Infographic: Word-Based Tokenization**
> (See visual below)

## 2. Character-based Tokenization
In this approach, each character becomes a token.

* **Introduction:** For "Hello"
* **Tokens:** ["H", "e", "l", "l", "o"]
* **Advantages:** Handles out-of-vocabulary (OOV) words naturally; suitable for Asian languages.
* **Disadvantages:** Results in very long sequences; loses semantic meaning at the word level; increases computational cost.

> **Infographic: Character Tokenization**
> (See visual below)
