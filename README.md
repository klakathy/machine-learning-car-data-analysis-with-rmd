# Prediction of risks of auction used cars
*An analysis about judging whether a car from auctions has issues by fitting multiple machine learning models based on R.*
<br/><br/>
The purpose of this project is to learning the philosophy between cars tradings. It is a practise of employing machine learning methods. 

## Getting started

### Data
The original data is collected from kaggle [Don't get kicked!](https://www.kaggle.com/c/DontGetKicked), which is the same as csv files in orinigal_data folder. The original kaggle test has already closed the evaluation access, thus there is no specific rank for this project.  
<br/>
**Entity:**  


### Setup
- Environment: R (R Markdown), Tableau  
- Data resource: kaggle [Don't get kicked!](https://www.kaggle.com/c/DontGetKicked)  
- Models: classification tree model, Random Forest, XGBoost, support vector machine, neutral network  
- Libraries: caret, randomForest, xgboost, nnet, pROC, etc.  
- Other: PCA knowledge is also needed.  
  <br/>
- Import all `.rmd` files and install libraries as needed.  
  The files is currently set to knit to word document.  
<br/><br/>

## Content
In this project, data is first cleaned with preprocessing and feature selection methods, and second analyzed with multiple machine learning models, and then evaluated considering roc when applying different models.  
<br/>

### Preprocessing
![img](readme_img/pre4.jpg) 
![img](readme_img/pre5.jpg)
![img](readme_img/pre6.jpg)

### Model applying
- **Tree model**  
  ![img](readme_img/tree1.jpg)  
  Five variables are chosen for classification tree model according to gini index. After and additional cross-validation check, further improvement is made by changing model complexity to pruning the tree.
- **Random forest**  
  ![img](readme_img/forest1.jpg)  
  
- **XGBoost**  
  ![img](readme_img/xgb1.jpg)  
  
- **SVM**  
  ![img](readme_img/svm1.jpg)  
  
- **NNet**  
  ![img](readme_img/nnet1.jpg)  

### Evaluation ROC
![img](readme_img/roc1.jpg)  
![img](readme_img/result1.jpg)  

In terms of the auc and recall rate, the best current model is nnet, which gives a 59.48% recall rate, this is based on cutoff value where having the J statistic (Sensitivity+Specificity-1) maximal.  

## Constribution
This is a group project for a course. My teammate Wendy, Nina, Andi and I worked together to accomplish this work.  
<br/>
