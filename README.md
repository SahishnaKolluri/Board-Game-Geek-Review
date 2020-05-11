BoardGameGeek is a popular site where different types of board games like Settlers of Catan, Through the Ages: A Story of Civilization etc are discussed and reviewed. There are seven major data types. Each of these types has subtypes which differ by the various domains of this collection of sites. But the ID numbers are unique for any given type. For example [boardgames] and [rpgitems] are subtypes of [thing]; the ID numbers for [things] are unique and shared between its subtypes, such that any one [thing] could have the [boardgame] or [rpgitem] subtype, but different [boardgames] and [rpg items] will never have the same ID number.
Objective
The objective of this notebook to analyze the given review data and predict the rating. Let's use our analysis skills to predict the ratings.

Dataset
The dataset contains data on 80000 board games. The dataset contains several data points about each board game. Here’s a list of the interesting ones:

name – name of the board game.
playingtime – the playing time (given by the manufacturer).
minplaytime – the minimum playing time (given by the manufacturer).
maxplaytime – the maximum playing time (given by the manufacturer).
minage – the minimum recommended age to play.
users_rated – the number of users who rated the game.
average_rating – the average rating given to the game by users. (0-10)
total_weights – Number of weights given by users. Weight is a subjective measure that is made up by BoardGameGeek. It’s how “deep” or involved a game is. Here’s a full explanation.
average_weight – the average of all the subjective weights (0-5).
Machine Learning Algorithms Used For Predicting The Rating
We have used the following 3 Machine Learning Algorithms in this project:

k-means clustering
Linear Regression
RandomForest Regression
k-means clustering
K-means clustering is one of the simplest and popular unsupervised machine learning algorithms. Typically, unsupervised algorithms make inferences from datasets using only input vectors without referring to known, or labelled, outcomes. The objective of K-means is simple: group similar data points together and discover underlying patterns. To achieve this objective, K-means looks for a fixed number (k) of clusters in a dataset.” A cluster refers to a collection of data points aggregated together because of certain similarities. You’ll define a target number k, which refers to the number of centroids you need in the dataset. A centroid is the imaginary or real location representing the center of the cluster. Every data point is allocated to each of the clusters through reducing the in-cluster sum of squares. In other words, the K-means algorithm identifies k number of centroids, and then allocates every data point to the nearest cluster, while keeping the centroids as small as possible. The ‘means’ in the K-means refers to averaging of the data; that is, finding the centroid. How the K-means algorithm works To process the learning data, the K-means algorithm in data mining starts with a first group of randomly selected centroids, which are used as the beginning points for every cluster, and then performs iterative (repetitive) calculations to optimize the positions of the centroids It halts creating and optimizing clusters when either:

The centroids have stabilized — there is no change in their values because the clustering has been successful.
The defined number of iterations has been achieved.
Linear Regression
Linear Regression is a machine learning algorithm based on supervised learning. It performs a regression task. Regression models a target prediction value based on independent variables. It is mostly used for finding out the relationship between variables and forecasting. Different regression models differ based on – the kind of relationship between dependent and independent variables, they are considering and the number of independent variables being used. Linear regression performs the task to predict a dependent variable value (y) based on a given independent variable (x). So, this regression technique finds out a linear relationship between x (input) and y(output). Hence, the name is Linear Regression.
RandomForest Regression¶
Random forest is a Supervised Learning algorithm which uses ensemble learning method for classification and regression. Random forest is a bagging technique and not a boosting technique. The trees in random forests are run in parallel. There is no interaction between these trees while building the trees. It operates by constructing a multitude of decision trees at training time and outputting the class that is the mode of the classes (classification) or mean prediction (regression) of the individual trees. A random forest is a meta-estimator (i.e. it combines the result of multiple predictions) which aggregates many decision trees, with some helpful modifications:

The number of features that can be split on at each node is limited to some percentage of the total (which is known as the hyperparameter). This ensures that the ensemble model does not rely too heavily on any individual feature, and makes fair use of all potentially predictive features.
Each tree draws a random sample from the original data set when generating its splits, adding a further element of randomness that prevents overfitting. The above modifications help prevent the trees from being too highly correlated.
Conclusion
From the above analysis we can see that the error rate of random forest is less when compared to linear regression.The random forest algorithm can find nonlinearities in data that a linear regression wouldn’t be able to pick up on. A linear regression algorithm wouldn’t be able to pick up on this because there isn’t a linear relationship between the predictor and the target. Predictions made with a random forest usually have less error than predictions made by a linear regression.

The challenges I faced for this project were selecting the Machine algorithms for handling the data, choosing the columun to find the correlation and also handling the huge sample datasets. I have choosen "average_rating" for correlation because our final project was based on predicting rating. However, we can try predicting a different column, such as average_weight. Regarding handling of datasets, I was able to divide the dataset as test and train, which could be easily handled by Kaggle Server.

Finally, we were able to find which machine algorithms were best suited for this dataset.
