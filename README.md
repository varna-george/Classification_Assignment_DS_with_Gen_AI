Classification Assignment

Classification Assignment Objective: The objective of this assessment is to evaluate the understanding and ability to apply supervised learning techniques to a real-world dataset.

Dataset: Used breast cancer dataset available in the sklearn library.

Key Components fulfilled:

Loading and Preprocessing:

● Loaded the breat cancer dataset using the load_breast_cancer function from sklearn. ● Converted the dataset into a pandas DataFrame for easier handling. ● All the features are float, int and there are no categorical feature. ● No missing values found. ● Scaling is done only for  Logistic Regression, SVM and k-NN. Logistic Regression: Scaling ensures that each feature contributes equally to the model’s learning process. Support Vector Machine (SVM): SVM relies on distances and inner products → scaling is crucial to avoid bias from feature magnitude.k-Nearest Neighbors (k-NN): Since k-NN uses distance to find neighbors, scaling ensures that all features contribute equally to that distance. Decision Tree, Random Forest: These models split data by feature thresholds, scaling has no effect on their performance.

Classifier Algorithm Implementation: Implemented the following classification algorithms:

○ Logistic Regression: A linear model that estimates the probability of a sample belonging to a class using the logistic (sigmoid) function. It fits a linear decision boundary by optimizing weights via gradient descent. The Breast Cancer dataset is mostly linearly separable, meaning a straight line (or plane) can divide the classes well. Performs very well after feature scaling. Fast, interpretable, and accurate (97%).

○ Decision Tree Classifier: A tree-like structure that recursively splits data based on feature thresholds that best separate the classes. Uses metrics like Gini impurity or entropy to choose the best splits. Can capture non-linear relationships between features and labels. Easy to visualize and interpret. No need for feature scaling since it works on thresholds.

○ Random Forest Classifier: An ensemble of many Decision Trees trained on random subsets of data and features. Final prediction is made by majority voting among the trees. Reduces overfitting compared to a single Decision Tree. Handles high-dimensional data and correlated features well. Very robust and usually achieves high accuracy (96%) on this dataset.

○ Support Vector Machine (SVM): Finds the best separating hyperplane that maximizes the margin between classes. Uses kernels (like RBF) to handle non-linear relationships by projecting data into higher dimensions. The dataset has clear separation and not much noise → perfect for SVM. With RBF kernel + scaling, it can achieve excellent accuracy (98%). Works well in moderate dimensions like this dataset (30 features).

○ k-Nearest Neighbors (k-NN): A distance-based algorithm: for a new sample, it finds the k nearest training points and assigns the majority class among them. Commonly uses Euclidean distance. Works well on clean, well-separated datasets. Intuitive and simple — makes few assumptions about data. Needs scaling because distance should treat all features equally. 

Models Evaluation and Comparison:

SVM (0.98) → Highest accuracy; works great with scaling and non-linear boundary. [Top performance]

Logistic Regression (0.97) → Strong linear model; great baseline.

Random Forest (0.96) → Very reliable ensemble method.

Decision Tree & k-NN (0.95) → Still good, but slightly less generalizable. [Lowest performance]
