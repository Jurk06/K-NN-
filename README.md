# K-NN (Theory and Application)
It is used for classification and regression. In both cases, the input consists of the k closest training examples in data set. The output depends on whether k-NN is used for classification or regression

*   In k-NN classification, the output is a class membership. An object is classified by a plurality vote of its neighbors, with the object being assigned to the class most common among its k nearest neighbors (k is a positive integer, typically small). If k = 1, then the object is simply assigned to the class of that single nearest neighbor.
*   In k-NN regression, the output is the property value for the object. This value is the average of the values of k nearest neighbors.
*   k-NN is a type of classification where the function is only approximated locally and all computation is deferred until function evaluation. Since this algorithm relies on distance for classification, if the features represent different physical units or come in vastly different scales then normalizing the training data can improve its accuracy dramatically
*   Both for classification and regression, a useful technique can be to assign weights to the contributions of the neighbors, so that the nearer neighbors contribute more to the average than the more distant ones. For example, a common weighting scheme consists in giving each neighbor a weight of 1/d, where d is the distance to the neighbor
*   The neighbors are taken from a set of objects for which the class (for k-NN classification) or the object property value (for k-NN regression) is known. This can be thought of as the training set for the algorithm, though no explicit training step is required
# Parameters 
1.  n_neighbors:- Number of neighbors to use by default for kneighbors queries
2.  weights{‘uniform’, ‘distance’} or callable, default=’uniform’
   *  ‘uniform’ : uniform weights. All points in each neighborhood are weighted equally
   *  ‘distance’ : weight points by the inverse of their distance. in this case, closer neighbors of a query point will have a greater influence than neighbors which are further away
   *  [callable] : a user-defined function which accepts an array of distances, and returns an array of the same shape containing the weights.
3.  algorithm{‘auto’, ‘ball_tree’, ‘kd_tree’, ‘brute’}, default=’auto’:- "Algorithm used to compute the nearest neighbors:"
   *  ‘ball_tree’ will use BallTree
   *   ‘kd_tree’ will use KDTree
   *   ‘brute’ will use a brute-force search.
   *   ‘auto’ will attempt to decide the most appropriate algorithm based on the values passed to fit method.
4.  metricstr or callable, default=’minkowski’
the distance metric to use for the tree. The default metric is minkowski, and with p=2 is equivalent to the standard Euclidean metric. See the documentation of DistanceMetric for a list of available metrics. If metric is “precomputed”, X is assumed to be a distance matrix and must be square during fit. X may be a sparse graph, in which case only “nonzero” elements may be considered neighbors.

