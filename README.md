# Movie Review Sediment Analysis
## Project Description
The Film Junky Union, a fictive new edgy community for classic movie enthusiasts, is developing a system for filtering and categorizing movie reviews.   
For those functionalities this project a model to automatically detect  negative reviews has been built.  
This model has been trained on a dataset of IMBD movie reviews with polarity labelling. The model must be at least provide an F1 score of 0.85.

## Content
In this project the following steps have been carried out:

- load and inspect the data
- Exploratory Data Analysis
- Data preprocessing (multiple text normalization approaches)
- Developing different approaches and ML models incl. hyperparameter tuning:
	- Approach 1: Dummy Classifier
	- Approach 2: NLTK + TF-IDF + Logistic Regression
	- Approach 3: spaCy + TF-IDF + Logistic Regression
	- Approach 4: spaCy + TF-IDF + LGBMClassifier
	- Approach 5: BERT + Logistic Regression
- Evaluation of the 5 approaches

- It needs to be noted here, that the Transformer model (BERT) was only trained with 2000 reviews and tested with 1000 entries due to its heavy computation power. Thus the general perfomance of the model is expected to be much lower than the other models. This could be resolved by moving to a GPU based training


## Outcome
- Approaches 1-4 have achieved F1 Scores on the test data up to 88% which could not significant improved by hyperparameter tuning
- The normalization using NLTK takes significant shorter than the normalization using spacy
- The transformer model is with 83% worse than approaches 1-4 but considering the small training dataset, the results are surprisingly good. Using the full dataset i expect approach 5 to perform equally or even outperfom approaches 1-4.
