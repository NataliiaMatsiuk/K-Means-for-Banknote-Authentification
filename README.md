# K-Means-for-Banknote-Authentification
The goal of this assignment is to use the Banknote authentication dataset to train a model that can predict if a banknote is genuine or not.

First of all we have downloaded dataset of Banknote Authentification which consists of 6 columns (id, V1, V2, V3, V4, Class). As far as scale of variables is different we need to use StandardScaler from sklearn.preprocessing library.

When the features have scaled they should be transformed into 2 new principal component. In order to do this we can use PCA from sklearn.decomposition with n_components=2. 

After that we receive final dataset which consists of 3 columns: Principal Component 1, Principal Component 2 and Class. Principal Component 1, Principal Component 2 are X and Class is Y for K-Means Clusterisation. 

If final dataset includes NaN values in some rows and the number of these rows is not much, we can remove these rows by dropna.

Then we can visualize the data with the scatter plot. At the plot 2 clusters are shown: the first with value of variable Class which equals 1 and the second with value of variable Class which equals 2. That is why K-Means clustering from sklearn.cluster should be used. 

The final plot depicts the results of dividing data by 2 clusters with the centers of them.
