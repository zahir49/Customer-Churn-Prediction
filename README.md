# Customer_Churn_Prediction

1. Let us understand what customer churn is. Customer churn is the loss of clients or customers.
2. It is the most common issue that any company faces. So, understanding customer churn behaviour would help in providing better offers and recommendations to customers so that the company can retain its customers.
3. So, for this project I had taken a telecom dataset which consists of around 7000 entries.
4. I analysed the customer behaviour and build a model to identify the churners. So, for this I have done data pre-processing, EDA and at last I build the model.
5. To get started, I had imported all the required libraries like numpy, pandas, matplotlib, seaborn, sklearn and smote module.
6. Then, I had loaded the dataset into a pandas dataframe and had a look at the dataframe to understand the data. 
7. I checked the shape of the data. It had 7043 entries and 21 columns.

Data Pre-Processing:
1.	I dropped the column ‘customer_id’ as it has no significance.
2.	Then I converted datatype of column total_charges from object to float data type.
3.	I checked index of rows with any spaces. I found 11 blank spaces in total charges.
4.	So, I replaced blank spaces with nan values and further replaced nan values with median value of total charges.
5.	I then mapped senior citizen to yes and no as other categorical features has values like yes and no.
6.	I also created a ‘tenure grp’ column from tenure column of each group having range 12 and dropped the tenure column.

Exploratory Data Analysis:
1.	I checked the data distribution of target variable with countplot. It was an imbalanced data as the number of 'No' is far greater than the number of 'Yes' in our dataset. 73% data is for 'No'.
2.	So, I balanced the data while building the model.
3.	I separated categorical features and plotted the impact of categorical features on churn.
4.	I then plotted a countplot of tenure group w.r.t churn. Tenure group 0-12 has the highest churn rate.
5.	Then I converted all categorical variables to dummy variables so that I can plot a correlation bar plot. And for the model building part.

Model Building:
1.	As the dataset was imbalanced, I used SMOTE technique to resample the data. It upsampled the data.  
2.	I then splited the data to train and test data.
3.	For model building I decided to use Random Forest Algorithm and created an object of Random Forest Classifier and called the fit function on the training data.
4.	After the training, I called the predict function on test data and then calculated the accuracy. It was 81.28%.
