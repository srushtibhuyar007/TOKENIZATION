# Current State and Future Trends

Today, subword methods (BPE, WordPiece, Unigram) are dominant in state-of-the-art models like Transformers (BERT, GPT-3, T5).

## SentencePiece
A popular open-source library that implements both BPE and Unigram LM tokenization.

* **Key Feature:** It treats the input as raw character sequences, including spaces (often represented as _ or special characters), making it language-independent.
* **Pipeline:** It handles normalization, sentence splitting, and tokenization directly from raw text.

> **Infographic: Modern Tokenization Landscape**
> (See visual below)
