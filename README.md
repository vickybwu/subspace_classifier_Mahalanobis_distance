# subspace_classifier_Mahalanobis_distance

Three parts of this project: iterate feature selection, subspace selection and feature projection (equivalent of a PCA), Mahalanobis distance classifier. Each part is implemented with a tuning parameter to control the desired output so that the classifier can be optimized.

Iterating feature selection works by calculating the degree of assiciation between every feature and every class. If feature i is determined to be strongly associated with class c then feature i can be used for classification for class c. Here it works by taking one feature at a time to fit into a classifier and test the proabbility of correct assignment using that single feature. 

Subspace projection works like a principal component analysis, where a desired variance/number of principal componenets is selected for each class of the dataset. The training and testing set is then transformed by projecting their features onto the selected subspace. It helps to reduce data dimension/noise in the dataset so that only essential information is passed through the classifier in theory.

Mahalanobis distance is a distance measure that measures how far a vector is from a distribution, aka a point from a cluster of points. When used as a classifier, the idea is simply to measure the distance from a point (an x in the test set) to a distribution (a distribution of all the points in class c in the training set) and evaluate if the distance is close enough for the point x to be assigned to the class c. 

A detailed explaination can be found in the Latex report 

Implementation in Python can be found here https://colab.research.google.com/drive/18J4tp375uM305tfL6MYicGOQtDXroawu#scrollTo=vRhr5nuoekX0

