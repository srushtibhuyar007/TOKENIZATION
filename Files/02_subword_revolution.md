# The Rise of Statistical and Subword Tokenization

As NLP models became more sophisticated, the limitations of simple word and character tokenization became apparent. This led to **Subword Tokenization**, striking a balance between word and character-level approaches.

## 1. Byte Pair Encoding (BPE)
*Introduced in 2015, adapted for NLP.*

* **Process:** Iteratively merges the most frequent pairs of bytes (characters or subwords) into new, longer subwords. Starts with a vocabulary of individual characters.
* **Example:** If "low" and "er" are frequent, BPE merges them to "lower".
* **Advantages:** Handles OOV words, reduces vocabulary size, captures morphological variations (e.g., "running", "runs").
* **Disadvantages:** Can sometimes create less intuitive subwords.

## 2. WordPiece
*Developed by Google (used in BERT).*

* **Process:** Similar to BPE, but selects the pair of subwords that, when merged, **maximizes the likelihood of the training data**.
* **Advantages:** Widely used in popular models like BERT.
* **Disadvantages:** Requires a pre-trained model to learn the merges.

## 3. Unigram Language Model (ULM)
*Used in SentencePiece, T5, ALBERT.*

* **Process:** Starts with a large vocabulary and iteratively removes (prunes) subwords that reduce the overall likelihood of the training data.
* **Advantages:** Flexible segmentation, handles multiple possible segmentations (regularization).
* **Disadvantages:** Computationally more intensive.
