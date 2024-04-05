# BeHealthy-Medical-Data-Processing-with-CRF
This project aims to develop a custom Named Entity Recognition (NER) model using Conditional Random Fields (CRF) to identify diseases and treatments in medical text data from the BeHealthy platform.
Data Preprocessing:

Sentence Construction:

Read data files (e.g., train_sent.txt) using functions like process_file.
Identify sentence boundaries using blank lines or label markers.
Construct sentences from individual words.
Data Exploration:

Combine train and test data for concept identification.
Utilize spaCy for Part-of-Speech (PoS) tagging.
Extract nouns (NOUN) and proper nouns (PROPN) from the combined data.
Print the top 25 most frequent noun concepts.
CRF Feature Definition:

Feature Engineering:
Define features for the CRF model, including:
Current word's PoS tag
PoS tag of the preceding word (context)
Indicators for first and last words in a sentence
Feature and Label Extraction:

Feature Generation:

Implement functions to extract feature values for each sentence based on defined features.
Label Processing:

Write code to obtain a list of labels for a preprocessed label line.
Model Building and Evaluation:

Input and Target Variables:

Extract features and labels for both training and testing data sets.
Prepare these as input and target variables for the CRF model.
CRF Model Construction:

Build a CRF model using the scikit-learn library.
Model Performance:

Predict labels for each token in sentences from the test data set.
Calculate the F1 score to evaluate model performance.
Disease and Treatment Identification:

NER for Diseases and Treatments:

Develop logic to identify predicted treatment labels (T) associated with each predicted disease label (D) in the test data set.
Treatment Prediction:

Predict the treatment for a specific disease (e.g., "hereditary retinoblastoma")
