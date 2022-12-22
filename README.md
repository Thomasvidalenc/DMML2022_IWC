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

At the beggining of our project we decided to proceed as the T.A told us, which is to work with a dataset without using any data cleaning. In order to do that we vectorized the sentences using TDIF and apply the different models, Logistic regression, kNN, Decision Tree and Random Forests, on the obtained data. After seeing the results, we realized that it wasn't precise at all. So we decided to use the LinearSVC and once again the result was not convincing at all. Then we tried another approach, we used the multilanguage. The result was the worst we got, so here again we decided to abandon this solution. 

After many hours fighting with the code, we found CamenBert.

- Work in the dataset without using any data cleaning
- Work in the dataset with cleaning
- Use the french version of "Bert", "Camembert"


## Summary of results table

- Without Data Cleaning

|  | Logistic regression |kNN	| Decision Tree | Random Forests |
| ------------- | ------------- |----------| ------------- | ------------- |
| Precision |||  |  |
| Recall |||  |  |
| F1-score | ||  |  |
| Accuracy |  ||  |  |


- Final result

|| LinearSVC | CamemBERT | 
| --- | --- |---|
| Precision |  |  |
| Recall |  |  | 
| F1-Score |  |  | 
| Accuracy | |  |  


## Video link 🎥 



[Our Demo](https://www.youtube.com/watch?v=H1HdZFgR-aA)

## Sources
