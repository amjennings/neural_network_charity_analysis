# neural_network_charity_analysis

## **Overview of the analysis:** 
###### The purpose of this analysis was to create a binary classifier capable of predicting whether applicants will be successful if funded by the Charity  Alphabet Soup. The data analyzed included information about each organization such as the organization type, the income classification, how much the organization asked for, and whether the money was used effectively.

## **Results**
###### Data Preprocessing
- The target variable for the model was 'IS_SUCCESSFUL' - the data reflecting whether or not organizations had effectively used the money.
- The feature variables included: 
  -STATUS
  -ASK_AMT
  -APPLICATION_TYPE
  -AFFILIATION
  -CLASSIFICATIONN
  -USE_CASE
  -ORGANIZATION
  -INCOME_AMT
  -SPECIAL_CONSIDERATIONS
  
- The variables that were removed included: 
  -EIN & NAME - Identification columns

###### Compiling, Training, and Evaluating the Model
- Originally there were 110 neurons across two layers with the ReLU activation function used for both hidden layers and the Sigmoid activation function used for the output layer. 
- In the attempted optimization (which was not successful to achieve accuracy greater than 75%), there were still 110 neurons, this time split across three hidden layers. The activation functions were kept as ReLU for hidden layers and Sigmoid for the output. The ReLU was retained for hidden layers as this is ideal for nonlinear output data for classification. The Sigmoid was used for the output layer because this was a binary classification with the prediction to indicate whether an applicant successfully used the money or not.
- In addition to adding a third hidden layer to increase model performance, the STATUS column was dropped and the number of epochs were increased to 300. However, these were not effective to increase performance.

## **Summary**
###### The predictive accuracy of the model to determine whether or not an applicant would be successful if funded by Alphabet Soup was about 73%. A support vector machine (SVM) may be a better model to use for this prediction. SVMs are also used for classification and perform similar to deep learning models, however, they require less code. 
