# internet-customers
This work example is on analyzing a dataset related to internet service churn, aiming to help internet providers understand which customers might cancel their service, known as churn. The code begins by loading the dataset and performing data cleaning and preprocessing steps, such as handling missing values and scaling numerical data for machine learning. It then delves into building a neural network model using TensorFlow and fine-tuning its hyperparameters using Keras Tuner, a tool for automating the search for optimal model configurations. The code concludes by training the neural network with the best hyperparameters and evaluating its performance, showcasing an effort to enhance customer retention strategies for internet providers in a highly competitive market. 

1. **Data Loading and Cleaning:**
   - A dataset ('internet_service_churn.csv') is loaded using pandas, containing information about customers.
   - NaN values are identified and handled by imputing the most frequent value for each column with missing data.
   - Non-beneficial columns ('id', 'remaining_contract') are dropped from the dataset.

2. **Data Preprocessing:**
   - The data is preprocessed by standardizing numerical features using StandardScaler.
   - The target variable 'churn' is separated from the features, and the dataset is split into training and testing sets.

3. **Model Creation and Hyperparameter Tuning:**
   - A neural network model is defined using Keras.
   - Hyperparameters for the model are tuned using Hyperband, a hyperparameter tuning library, to optimize the model's performance.
   - The top-performing models' hyperparameters and their evaluation metrics are displayed.

4. **Alternative Model:**
   - An alternative neural network model is defined with a fixed architecture (16 units in each of the two hidden layers).
   - The model is trained and evaluated using the dataset.

Overall, the goal of the code is to predict customer churn for an internet service provider, allowing them to target potential churners with promotions or interventions to retain customers. The models are evaluated based on their accuracy in predicting churn.
