# English-Spelling-Corrector


#### Concept

Objective: To build a basic spelling corrector from scratch that suggests the most probable correct word for a given misspelled input word, without using external NLP libraries.

Approach: The algorithm is based on a probabilistic model of language and edit distance, inspired by the Noisy Channel Model. The correct word is assumed to be the one with the highest likelihood.

Methodology:

1. Corpus-Based Language Model:
Extract words from a large text corpus and compute their frequencies to estimate word probabilities.

2. Error Modeling using Edits:
Generate candidate corrections that are one or two edits (insert, delete, replace, transpose) away from the input word —         approximating Damerau-Levenshtein distance.

3. Candidate Filtering:
Retain only those candidates that exist in the known vocabulary.

4. Best Candidate Selection:
From the filtered set, choose the word with the highest probability according to the language model.

Outcome: The corrector works well for common spelling mistakes and chooses corrections based on both proximity (edit distance) and word frequency (likelihood of occurrence).
