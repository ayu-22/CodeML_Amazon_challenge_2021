# Code_ml_Amazon_challenge_2021

We approached this problem as a multi-class text categorization task.

## Text Preprocessing :
1. Removing special characters, numbers and converting them in lowercase form.
2. Removing stopwords ( using 'nltk' Library)
3. Tokenization followed by Lemmatization

## Classical ML Approaches :

1. SVM:
We tried classical ML approaches, for example, SVM (after converting the text into TF-IDF features). Given the vast number of samples, it took us many hours but not a good place on the private leaderboard.

2. fastText Library
This Library is used to learn text representations and text classifiers. We format the data as required to feed it in a fastText classifier. By manual tuning of its hyperparameters, we were able to get ~0.63 in a private leaderboard.

## Deep Learning Approachers :

We used the BERT model to train the data. We used the transformer library for this. But, this was consuming too much RAM. So, we used Tez Library.

We trained the model on different splits of data for few epochs. We also tried to ensemble the predictions and implemented Monte Carlo Dropout to improve the scores.
The method which gave the best score on the private leaderboard -
Preprocessed and concatenated all features 
Trained BERT on entire data for three epochs ( 80:20 train:Val split) for three epochs.

We have added our code in a code_ml_notebook file (jupyter notebook).