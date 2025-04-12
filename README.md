A **Decision tree** is a popular machine learning algorithm used for both classification and regression tasks. 
It works by splitting data into subsets based on the value of input features.
These splits form a tree-like structure, hence the name.

**Decision Tree Process:**

1. Start with the full dataset.

2. Pick the best feature to split the data (based on highest Information Gain or lowest Gini Impurity).

3. Split the data into smaller subsets using the chosen feature.

4. For each subset, repeat the process by picking the next best feature to split on.

5. Stop when:

                   All data in a node is the same class (pure).

                   There are no more features to split on.

                   A stopping condition is met (e.g., max depth or minimum samples per leaf).




