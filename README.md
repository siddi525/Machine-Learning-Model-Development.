Description of the Project
In this experiment, data was collected from a group of 30 volunteers, aged between 19 and 48 years. Each participant performed six different activities while wearing a smartphone on
their waist. The activities included:
• WALKING
• WALKING UPSTAIRS
• WALKING DOWNSTAIRS
• SITTING
• STANDING
• LAYING
The smartphone was equipped with an accelerometer and a gyroscope, which captured the following data at a constant
sampling rate of 50Hz:
• 3-axial linear acceleration (from the accelerometer)
• 3-axial angular velocity (from the gyroscope)
In addition to the sensor data, the experiments were video recorded to manually label the data. The dataset was randomly
split into two sets:
70% of the data was used for training the machine learning models.
30% of the data was used for testing the model's performance.

Data Preprocessing

Before using the raw data for analysis, several preprocessing steps were applied to ensure high-quality input data for model training: Feature Extraction For each window of data, a feature vector was created by computing various statistical variables from both the time domain
and frequency domain. These features were then used to train machine learning models to classify the different activities.


Dataset Variables

Each record in the dataset contains the following data attributes:
• Triaxial Acceleration: The accelerometer readings representing the total acceleration (which includes both body acceleration and gravitational components) as well as the estimated body acceleration.
• Triaxial Angular Velocity: The gyroscope readings that represent the angular velocity along the three axes (X, Y, and Z).

These features form the basis for classifying the activities performed by the participants. 

Training and Evaluating Models

Once the dataset is pre-processed and the features are extracted, the next step is to train machine learning models to classify the different activities based on the sensor data.

Splitting the Data:
The first step in training the model is to divide the dataset into features (X) and labels (y). Features represent the sensor data, and labels represent the activities to be classified.

• Training Set (70% of the dataset): This set is used to train the machine learning model.
• Testing Set (30% of the dataset): This set is used to evaluate the model's performance after training.

Machine Learning Models Used

The following models were used for classification:
Logistic Regression
K-Nearest Neighbors (KNN)
Support Vector Classifier (SVC) with RBF Kernel
Support Vector Classifier (SVC) with Linear Kernel
Random Forest Classifier
Decision Tree Classifier


Model Training and Evaluation

Model Training and Evaluation
To train and evaluate the models, the following steps were followed:

Splitting Data: The data was split into training and testing sets. The training set contained 70% of the data, while the test set contained 30% of the data. This split ensures that we can assess
how well the model generalizes to new, unseen data. 

Model Initialization: Each model was instantiated, trained, and evaluated. The training process involves fitting the model to the training data (X_train and y_train), and performance was evaluated
using the test data (X_test and y_test).

Model Evaluation: After training the models, the performance of each model is evaluated using metrics such as accuracy, precision, recall, and F1-score. These metrics help assess how well each model performs on the test data
