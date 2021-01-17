# CustomerSegments
Identify customer segments to increase sales. It is based on a demographic file containing ~900K records, and a ~200K customers’ records file.

This is an application of unsupervised learning techniques such as k-means clustering and of Principal Components Analysis. 

Each row of the demographics files represents a single person, but also includes information outside of individuals, including information about their household, building, and neighborhood. This information is used to cluster the general population into groups with similar demographic properties. Then, the people in the customers dataset are mapped into those created clusters. The result is that certain clusters are over-represented in the customers data, as compared to the general population; The information can then be used for further applications, such as targeting for a marketing campaign.

The jupyter notebook performs the following functions:

- read the population dataset, which is Udacity_AZDIAS_Subset.csv
- read the feature description file, AZDIAS_Feature_Summary.csv
- clean the data by removing rows, columns with missing data, deal with NaN occurrences, transform specific features (all this is described in the notebook)
- the rows are customers, the columns are products customers buy
- apply Principal Components Analysis to reduce the number of features
- apply k-means to determine the cluster which each customer belongs to
- read the customer dataset, Udacity_CUSTOMERS_Subset.csv and apply the same 'cleaning' actions as for the population data
- apply the same pca model determined on the population data
- apply the same k-means model determined on the population data
- evaluate the results in terms of over/under representation in the cluster of individuals by comparing the population with customer base
- translate the principal components back into original features to draw conclusions.

The insight is that the following group is over-represented in the customer dataset than in the general population, and it coukd be the traget for a marketing action:
male, approx 60 years old, german, interested in financial matters, money saver, investor, etc (more details in the notebook)

Note: if you repeat the run YOU WILL NOT GET THE SAME DIAGRAM AS IN paragraph 3.3, however the conclusions hold. 
To illustrate this point I have created a simpler notebook that reproducs the behavior.

In addition, many assumptions were made on which data to drop. Those may affect the final results. The data preparation step was by far the most challenging task.
