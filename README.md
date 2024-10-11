# Film_Junky_Union_Negative_Review_Model
The Film Junky Union, a new edgy community for classic movie enthusiasts, is developing a system for filtering and categorizing movie reviews. The goal is to train a model to automatically detect negative reviews.


## Data Description

The data is stored in the `imdb_reviews.tsv` file. Download the dataset.

The data was provided by Andrew L. Maas, Raymond E. Daly, Peter T. Pham, Dan Huang, Andrew Y. Ng, and Christopher Potts. (2011). Learning Word Vectors for Sentiment Analysis. The 49th Annual Meeting of the Association for Computational Linguistics (ACL 2011).

Here's the description of the selected fields:

`review`: the review text
`pos`: the target, '0' for negative and '1' for positive
`ds_part`: 'train'/'test' for the train/test part of dataset, correspondingly

## Conclusions
After normalizing and vectorized 3 models with a dummy model alongside for a baseline, we have successfully created 3 models and evaluated their performances.

 Model 2:

Model 2 used the Natural Language Toolkit with TF-IDF vectorization fit to a Logistic Regression model showed to be an effective model.

- Accuracy :   0.94  0.88
- F1 :         0.94  0.88
- APS :        0.98  0.95
- ROC AUC :    0.98  0.95
 
 Model 3:

Model 3 used spaCY library for NLP in addition to TF-IDF vectorization, fit to Logistic Regression model also performed well.

- Accuracy :   0.93  0.88
- F1 :         0.93  0.88
- APS :        0.98  0.95
- ROC AUC :    0.98  0.95

Model 4:

Model 4 used the spaCY library for NLP in addition to TF-IDF vectorization as well, fit to a gradient boosted decision tree model resulted in an F1 score of 0.98 after tuning some of the hyper parameters.

- Accuracy: 0.98 0.87
- F1 Score: 0.98 0.87
- APS:      1.00 0.94
- ROC AUC:  1.00 0.94

Model 2 and 3's results seem nearly identical, this could be due to the fact that the Logisitic Regression model was used for both, as a NLP library used between each of them could likely made the nearly identical results.

Although Model 4 training model results were higher than Model 2 and 3's results, the test results we still lower even after 
