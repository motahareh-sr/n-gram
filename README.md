# N-Gram Language Model

## Overview

This project implements an N-Gram language model using Python. The model is trained on a text corpus and generates sentences based on bigram, trigram, and five-gram probabilities.

## Features

- Custom tokenizer to preprocess text and add start/end tokens for sentences.
- Implementation of bigram, trigram, and five-gram probability models.
- Sentence generation using the trained N-Gram models.Installation



## Usage

1. **Preprocessing**

   - The text is read from a file and tokenized.
   - A custom tokenizer adds `<START>` and `<END>` tokens to sentences.

2. **Bigram Model**

   - Computes the probability of the next word based on the previous word.
   - Generates text based on bigram probabilities.

3. **Trigram Model**

   - Computes the probability of the next word based on the last two words.
   - Generates more contextually relevant sentences.

4. **Five-Gram Model**

   - Uses the last four words to predict the next word.
   - Provides more accurate predictions but requires more training data.

### Example Usage

```python
# Generating a sentence using the bigram model
sentence = "Knowing well the windings of the trail he"
print(generate_sentence(bigram, sentence, 10))
```

```python
# Generating a sentence using the trigram model
sentence = "For half a day he lolled on the huge back and"
print(generate_sentence_3gram(trigram, sentence, 10))
```

```python
# Generating a sentence using the five-gram model
sentence = "Knowing well the windings of the trail he"
print(generate_sentence_5gram(fivegram, sentence, 25))
```

## File Structure

- `main.py`: Main script for training and generating sentences.
- `README.md`: Project documentation.

## Limitations

- Requires sufficient training data to generate coherent sentences.
- The model assumes a closed vocabulary and may struggle with out-of-vocabulary words.

## Future Improvements

- Implement smoothing techniques for better probability estimation.
- Extend to a larger dataset for improved performance.
- Add interactive input for user-generated text predictions.

## License

This project is open-source and available under the MIT License.

