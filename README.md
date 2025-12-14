# TOKENIZATION
# TOKENIZATION: The Foundation of NLP

Tokenization is a fundamental concept in natural language processing (NLP) and plays a crucial role in how computers understand and process human language.

## What is Tokenization?
At its core, tokenization is the process of breaking down a sequence of text into smaller units called "tokens." These tokens can be words, subwords, or even individual characters, depending on the specific tokenization strategy employed. 

The goal is to transform raw text into a format that can be easily understood and processed by machine learning models.

#The Dawn of Tokenization: Early Approaches
In the early days of NLP, tokenization was relatively straightforward and often rule-based.
Word-based Tokenization: This was one of the simplest and most common approaches. Text was split into tokens based on whitespace and punctuation.
#Introduction: Imagine a sentence like "Hello, world!"
#Process: Split by spaces and remove punctuation.
#Tokens: ["Hello", "world"]
#Challenges:
#Contractions: "don't" would be split into ["don", "'t"], losing its original meaning.
#Hyphenated words: "state-of-the-art" might become ["state", "of", "the", "art"].
#Languages without spaces: Languages like Chinese or Japanese don't use spaces to separate words, making this method ineffective.
Here's an infographic illustrating early word-based tokenization: 



#Character-based Tokenization: In this approach, each character becomes a token.
#Introduction: For "Hello"
#Tokens: ["H", "e", "l", "l", "o"]
#Advantages: Handles out-of-vocabulary (OOV) words naturally and is suitable for languages without clear word boundaries.
#Disadvantages: Results in very long sequences, losing semantic meaning at the word level, and increasing computational cost.
Here's an infographic illustrating character tokenization: 

#The Rise of Statistical and Subword Tokenization
As NLP models became more sophisticated, the limitations of simple word and character tokenization became apparent. This led to the development of subword tokenization methods, which strike a balance between word and character-level approaches.
#Byte Pair Encoding (BPE): Introduced in 2015, BPE was initially used for data compression and later adapted for NLP.
Process: It iteratively merges the most frequent pairs of bytes (characters or subwords) into new, longer subwords. It starts with a vocabulary of individual characters and builds up a vocabulary of common subwords.
Example: If "low" and "er" are frequent, BPE might merge them into "lower". If "low" appears frequently with "est", it might form "lowest".
Advantages:
Handles OOV words by breaking them into known subwords.
Reduces vocabulary size compared to character-level tokenization.
Captures morphological variations (e.g., "running", "ran", "runs" might share the "run" subword).
Disadvantages: Can sometimes create less intuitive subwords.
#WordPiece: Developed by Google for its neural machine translation system, WordPiece is similar to BPE but uses a slightly different merging strategy. It selects the pair of subwords that, when merged, maximizes the likelihood of the training data.
Process: Similar to BPE, but focuses on statistical likelihood for merging.
Advantages: Widely used in popular models like BERT.
Disadvantages: Requires a pre-trained model to learn the merges.
#Unigram Language Model (ULM) Tokenization: This method, used in models like SentencePiece, treats each subword as an independent unit and learns their probabilities from the training data. It aims to find the most probable segmentation of a sentence into subwords.
Process: Starts with a large vocabulary of subwords (characters, common words, and subwords) and iteratively removes subwords that reduce the overall likelihood of the training data.
Advantages: Offers more flexibility in segmentation, can handle multiple possible segmentations, and often results in more uniform subword lengths.
Disadvantages: Computationally more intensive than BPE or WordPiece.
#Current State and Future Trends
Today, subword tokenization methods like BPE, WordPiece, and Unigram LM are the dominant approaches in state-of-the-art NLP models. They are essential for models like Transformers (BERT, GPT-3, T5) to handle vast amounts of text data efficiently and effectively.
#SentencePiece: A popular open-source library that implements both BPE and Unigram LM tokenization. It's language-independent and treats the input as raw character sequences, making it suitable for various languages, especially those without explicit word delimiters.
#Key Feature: It handles the entire tokenization pipeline, including text normalization and sentence splitting, directly from raw text.
Here's an infographic summarizing the modern landscape of tokenization:



