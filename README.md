# K-Means-Clustering
K-Means is an algorithm used in partitioning grouping which separates data into different groups based on the distance of each cluster from a predetermined point. This algorithm is able to minimize the distance between the data to its cluster. In this code we are using pandas and numpy library to process the data. For modelling, we are using TensorFlow and Scikit library.

The dataset that we use to conduct the training is obtained from https://www.kaggle.com/c/predict-west-nile-virus.

## Documentation

### data_cleaning function
The first step is to create a data_cleaning function. Here, we cluster the location points with variables in the form of latitude and longitude. So, it is necessary to clean the data to remove the NA data and only take the Latitude and Longitude variables.

### clustering function
We form a clustering function with one parameter called data and the output is a dataframe containing cluster points (latitude and longitude) and radius.
1. The first thing to do is to determine the optimal number of clusters from the known data. The determination method we use is elbow. We use the sckit library for that.
2. After obtaining the optimum number of clusters, we form variables using the Tensorflow library which will later be used to determine cluster points. In addition, the data needs to be converted into data in tensorflow format so that the input_fn function is formed.
3. Next, we determine the location points for each cluster, and the results are assigned to the centroid variable. The centroid variable is a dataframe with 2 variables, namely latitude and longitude.
4. The last thing to do is measure the radius for each cluster using the sckit library.
