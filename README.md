#Multiple Sclerosis Disease Prediction
This project focuses on predicting the conversion of Clinically Isolated Syndrome (CIS) to Multiple Sclerosis (MS) using a dataset from Kaggle. The goal is to build models that can accurately classify patients based on various predictors and identify those at risk of developing MS.

#Dataset
The dataset used for this project is obtained from Kaggle and is named conversion_predictors_of_clinically_isolated_syndrome_to_multiple_sclerosis.csv. It contains information related to patients diagnosed with CIS and includes several features that can be used to predict the conversion to MS. Some of the important features in the dataset are:

Age: The age of the patient at the time of diagnosis.
Gender: The gender of the patient.
Initial_Symptom: The initial symptom observed in the patient.
Schooling: The education level of the patient.
MRI_Lesion_Count: The count of lesions observed in the brain MRI.
#oneAPI and oneDAL Library
This project utilizes the oneAPI framework and optimizes the code using the oneDAL (oneAPI Data Analytics Library) library. The oneAPI initiative from Intel aims to provide a unified and efficient programming model for heterogeneous architectures.

The oneDAL library, a component of the oneAPI toolkit, is specifically designed for efficient data analysis and machine learning tasks. It provides a collection of highly optimized algorithms and functions that can be used to accelerate data preprocessing, model training, and inference.

#Code Explanation
The code begins by importing the necessary libraries, including pandas, numpy, and sklearn. It then loads the dataset into a pandas DataFrame using the read_csv function.

##Data Preprocessing:

Missing Values: The code checks for missing values in the dataset and fills any missing values in the 'Schooling' and 'Initial_Symptom' columns with 0.
Next, the code splits the data into training and testing sets using the train_test_split function from sklearn. The input features are split into X_train and X_test, while the target variable is split into y_train and y_test.

##Model Training and Evaluation:

The code trains two classification models: GradientBoostingClassifier and Random Forest Classifier.

For the GradientBoostingClassifier model, it fits the model to the training data, makes predictions on the test data, and calculates the accuracy and classification report using the accuracy_score and classification_report functions from sklearn.metrics.

For the Random Forest Classifier model, the same steps are performed to train the model, make predictions, and evaluate its performance.

#Results
The trained models were evaluated on the test set, and the following results were obtained:

GradientBoostingClassifier Results:
Accuracy: 0.8181818181818182

Random Forest Classifier Results:
Accuracy: 0.7818181818181819

The GradientBoostingClassifier achieved an accuracy of approximately 0.8182, while the Random Forest Classifier achieved an accuracy of approximately 0.7818. This indicates that the GradientBoostingClassifier performed slightly better in predicting the conversion of CIS to MS compared to the Random Forest Classifier.



#Conclusion
In this project, multiple models were developed to predict the conversion of Clinically Isolated Syndrome to Multiple Sclerosis. By utilizing the GradientBoostingClassifier and Random Forest Classifier, the models achieved reasonable levels of accuracy.


