# K-Means-for-Banknote-Authentication
K-means clustering is an unsupervised machine learning algorithm used to find groups of observations (clusters) that share similar characteristics. 
First of all we have to download dataset of Banknote Authentication which consists of 6 columns (id, V1, V2, V3, V4, Class). In this dataset we have data of original and Fake Bank notes. We will try to build a Machine learning model which will help us to classify notes as Authentic [1] or Fake [2].
We can build a plot to visualize relationship between pairs of variables. 

From the plot we can see than relationships between variables are unclear. So we need to use other methods. For example, K-means clustering. But before it is necessary  to standardize variables as far as scale of them is different and reduse dimension of the dataset. 

Standardizing variables might be done by using StandardScaler from sklearn.preprocessing library.

For linear dimensionality reduction might to be used Principal component analysis (PCA). 

After using PCA we will receive dataset with 3 columns: PC 1 and PC 2 (the linear combination of initial columns V1,V2, V3, V4) and Class as target variable.

Since final dataset includes NaN values in some rows and the number of these rows is not much, we can remove these rows by dropna.

Next step should be dividing data into train and test subsets. The main goal of this step is to use train subset to fit model and then to use test subset to estimate quality of this model.

If K-Means clustering method is used we will see the next plot. We can see division of the train subset into 2 clusters. The centers of 2 clusters are shown by black circles.

To visualize how the model works let is try to run the model with the test data. The results are shown at the final scatter plot.

It is obvious that the model is not very good. It divides data into 2 clusters but the predicted classes differ from the initial classes. 

So I would recommend further analyzing the dataset and looking for other models which can help predict if a banknote authentic or fake.
That is why I am going to implement Decision Tree and Random Forest methods to solve banknote authentication problem.

