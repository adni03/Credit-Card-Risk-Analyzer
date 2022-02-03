# Credit Card Risk Analyzer

In this project, I used my knowledge of the following to predict if a certain customer's credit card
application will be approved or not.

	1. EDA or Exploratory Data Analysis:
		I looked through the dataset to understand the various kinds of features present
		and their data types, statistics etc.

	2. Missing Data:
		Upon inspection, there was data missing from the dataset. Using the data as it will
		severly affect the accuracy of the model and hence, this must be taken care of.

		1. Replaced all the '?' or missing values with NaN
		2. Imputed all the NaN values with the mean of the dataset.
		3. To take care of the non-numeric data, I replaced the missing values with the 
		   most frequent observation in the dataset for that feature.
	
	3. Labelling Data:
		The non-numeric data were encoded using LabelEncoder to numbers.

	4. Scaling:
		It is a well known fact that scaling the data improves the performance of the model
		as it is computationally less expensive. Hence, I chose to apply MinMaxScaling to 
		the data, to bring it down to the [0-1] range.

	5. Train-Test split:
		Split the dataset into training and testing sets to train and later, evaluate
		model performance.

	6. Logistic Regression:
		The model I chose to use was LogisticRegression as I need a probability of credit card
		approval. From sklearn.linear_model, I imported LogisticRegression and fit the scaled data
		to it.

		The accuracy from fitting a vanilla logistic regressor to the data was 0.4824.

	7. Hyperparameter Tuning:
		To improve the accuracy of the model, I used GridSearchCV to find the optimum
		parameters to use for the regressor.
		Apart from that, to fairly evaluate the model, I used cross-validation.
		
		Cross validation works by splitting the training data into k folds and fitting the data
		to the model. (k-1) sets are used to train and the last set is used to calculate the 
		performance.
		This is repeated k times to get performance scores that are more credible.	
