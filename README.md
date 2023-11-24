## Intrinsic evaluation
Code: gensim\
Corpus: https://mattmahoney.net/dc/text8.zip\

### Pre-processing:
- Punctuation, lower case, etc.

### Choices:
- Training sizes, window sizes, CBOW vs Skip-Gram.

### Evaluation:
- Analogies using https://github.com/nicholas-leonard/word2vec/blob/master/questions-words.txt
- Input three words, pick the returned word, compute the distance to the correct word
- Repeat and average.

The hyperparameters for the Word2Vec model are optimized using the Optuna library. The objective is to find the combination of hyperparameters that maximizes the model's performance in analogical reasoning.

- **Vector size (`vector_size`):** The number of dimensions to represent each word.
- **Window size (`window_size`):** The number of words around a central word that are considered in a context.
- **Minimum count (`min_count`):** The minimum number of times a word must appear in the corpus to be included in the model.
- **Number of Workers (`workers`):** The number of CPU cores to use for training.
- **Skip-Gram (`sg`):** 0 for CBOW, 1 for Skip-Gram.
