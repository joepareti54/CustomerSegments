# CustomerSegments
Identify customer segments to increase sales. It is based on a demographic file containing ~900K records, and a ~200K customers’ records file.

This is an application of unsupervised learning techniques such as k-means clustering and of Principal Components Analysis. 

Each row of the demographics files represents a single person, but also includes information outside of individuals, including information about their household, building, and neighborhood. This information is used to cluster the general population into groups with similar demographic properties. Then, the people in the customers dataset are mapped into those created clusters. The result is that certain clusters are over-represented in the customers data, as compared to the general population; The information can then be used for further applications, such as targeting for a marketing campaign.


