<img src='https://upload.wikimedia.org/wikipedia/commons/7/77/Logo_HEC_Lausanne.png' width="250">

# DMML2022 - Team IWC

## Detecting the difficulty level of french texts
### Team IWC members : 

- Ismael Tewfik
- Thomas Vidalenc


## Project description - the idea 💎

In this project, we wanted to detect the difficulty level of the french texts. To be more precise the objective was to predict the difficulty level of the text given in French. Most of the time when someone wants to improve his language skill, they need to read sin order to be familiar with the language. These texts have to be at the reader’s language level. This is why we try to build a model that helps us predict the difficulty level which range between A1 to C2. After the model is created, it can be used in a recommendation system, to recommend texts. If someone is at an A1 level, giving him a text at B2 level is innapropriat because the person won't be able to understand it. This is why it's is important to build a model that helps to detect the difficulty level. 

## Approach 📂
To construct our model, we used the dataset that was given to us on Kaggle, such as : 

- training_data.csv, the training set.
- unlabelled_test_data.csv, the test file.
- sample_submission.csv, the sample submission file in the correct format.

Regarding the columns we used

- id: Numerical identifier of the sentence.
- sentence: A sentence in French for which you want to predict the difficulty level.
- difficulty: The difficulty level of the sentence (from A1 to C2). This column would be your target variable.

#### Plan :

At the beginning of our project, we decided to proceed as the T.A. told us, which is to work with a dataset without using any data cleaning. In order to do that, we vectorized the sentences using TDIF and applied the different models—logistic regression, kNN, decision trees, and random forests—on the obtained data. After seeing the results, we realized that it wasn't precise at all. So we decided to use the linear SVC, and once again the result was not convincing. Then we tried another approach: we used multilanguage. The result we got with this model was the worst, a precision of 0.243. We understood something was missing in our approach.

Then, after many hours of fighting with the code, we taught about changing our approach and using a text encoding. At the end, we used the French version of Bert, CamemBert.



## Summary of results table

- Without Data Cleaning

|  | Logistic regression |kNN	| Decision Tree | Random Forests |
| ------------- | ------------- |----------| ------------- | ------------- |
| Precision |0.4656|0.4030| 0.3004 | 0.3158 |
| Recall |0.4667|0.3187| 0.2969 | 0.3156 |
| F1-score | 0.4640|0.3022| 0.2952 | 0.3008 |
| Accuracy | 0.4667 |0.3187| 0.2969 | 0.3156 |


- Final result

|| LinearSVC | CamemBERT | 
| --- | --- |---|
| Precision | 0.4992 |  0.59 |
| Recall | 0.5010 |  0.59 | 
| F1-Score | 0.4974 |  0.59 | 
| Accuracy |0.5010 |   0.59|  


## Video link 🎥 



[Our Demo](https://www.youtube.com/watch?v=H1HdZFgR-aA)

## Sources

- [Camembert](https://camembert-model.fr)
- [Huggingface](https://huggingface.co)
- [Towardsdatascience](https://towardsdatascience.com/whats-hugging-face-122f4e7eb11a)
