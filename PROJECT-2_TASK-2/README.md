Objective:
  To perform a binary classification task using logistic regression on the Titanic dataset. The goal is to predict whether a passenger survived or not based on various features such as age, fare, gender, and embarked location.

Importing Libraries:
  "numpy and pandas" for data manipulation.
  "seaborn and matplotlib.pyplot" for data visualization.
  "LogisticRegression" from scikit-learn for building a logistic regression model.
  "train_test_split" for splitting the dataset into training and testing sets.
  "accuracy_score" for evaluating the model's accuracy.

Reading the Dataset:
  The Titanic dataset is read from a CSV file into a Pandas DataFrame (df).
  Initial exploration using df.head(), df.shape, df.describe(), and df.isnull().sum() to check the structure, dimensions, summary statistics, and missing values in the dataset.

Data Preprocessing:
  Handling missing values by filling NaN values in the 'Age' and 'Fare' columns with their respective means.
  Converting categorical variables ('Embarked' and 'Sex') into numerical format.
  Dropping unnecessary columns ('PassengerId', 'Name', 'Cabin', 'Ticket') from the DataFrame.

Data Visualization:
  Creating histograms to visualize the distribution of 'Age' and 'Fare' with respect to survival.
  Creating a bar chart to show the count of passengers who survived and those who did not.

Data Splitting:
  Separating the dataset into training and testing sets using train_test_split.

Logistic Regression Model:
  Creating a logistic regression model (LR) using scikit-learn's LogisticRegression with specific parameters.
  Fitting the model on the training data.

Model Evaluation:
  Making predictions on the test set (x_test) using the trained model.
  Calculating the accuracy of the logistic regression model using accuracy_score.
  Printing the accuracy in percentage format.
