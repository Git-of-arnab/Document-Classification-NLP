# Document Classification-NLP

## Classification of Botany books in PDF format into Animal species, Plant Species or Mixed type using NLP toolkit~nltk.
1.   Training Data and Test data contains 3 columns - 'File_ID', 'Is_Mixed','Topic'
2.   Each File ID is unique and contains details of a topic with varied number of pages
3.   Each PDF needs to be read, identify the topic and determine whether it focuses on animals, plants or both
4.   For each PDF file we shall check the highest probability of a word occuring and identify the topic

Training Data Topic Distribution

![Training_data_topic_Distribution](https://github.com/Git-of-arnab/NLP-Classification/assets/138995898/f468b20d-8232-4d6c-a5f9-61e30911760f)

This is a supervised multi-class classification problem where we will be finding the topic of the document based on high probabilty word occurence.

From the training data we have the content of each File ID and the label informing whether it belongs to animal, plant or mixed type.

1.   If the word occurence probability is high for both plant & animal species then, classify it as 'Not Applicable'
2.   If the word occurence probability is high for plant species then, classify it as 'Plant Species'
3.   If the word occurence probability is high for animal species then, classify it as 'Animal Species'
4.   Once, the classification is done, we can provide the 'Is_Mixed' value column based on condition

**A comparative study on the output after TF-IDF and counterVectorizer is provided, where we see CV outperform TF-IDF**

**Confusion matrix on TF-IDF vectorized inputs**
![TF-IDF-Confusion_Matrix](https://github.com/Git-of-arnab/NLP-Classification/assets/138995898/30609a04-4f37-4124-965b-2ab86ab2b661)

**Confusion matrix on CounterVector vectorized inputs**
![CV-Confusion_Matrix](https://github.com/Git-of-arnab/NLP-Classification/assets/138995898/8d438451-ba99-4687-a1f1-d1a3308e51ef)

***AUC_ROC Score for TF-IDF = 0.9288***

***AUC_ROC Score for CounterVector = 0.9864***
