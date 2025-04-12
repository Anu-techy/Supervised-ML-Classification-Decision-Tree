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
   
=================================================================

Which feature to use at each node in a decision tree is found by

                            •	Gini
                            •	Information gain (Entropy)

**Entropy (Uncertainty, randomness or Messiness**)

•	Entropy is just a way to measure how mixed up your data is.
•	If your dataset has 50% "Yes" and 50% "No", it's very uncertain — high entropy.
•	If it's 100% "Yes" or 100% "No", there's no uncertainty — low entropy.
•	So, higher entropy = more confusion, lower entropy = more clarity.

**Relationship Between Entropy & Information Gain:**

•	Information Gain is based on Entropy.
•	You start with the entropy of the full dataset and split it using a feature.
•	You check how much the entropy goes down after the split
•	That drop in entropy = Information Gain.
•	The higher the Information Gain, the better the feature is at reducing uncertainty.
•	You want to split the data on features that give the highest Information Gain, because they help you make the most clear, confident decisions.
==================================================
**Gini Index/impurity**

The Gini Index focuses on impurity — how mixed the classes are in your dataset.

In simple terms:

            •	If a group is mostly one class (e.g., mostly "Yes" or mostly "No"), 
              it has low Gini impurity.

            •	If a group has a 50/50 split (like half "Yes" and half "No"), 
              it has high Gini impurity.

**Steps to find best splitting node using Gini index:**

1.	Start with the Gini Index of the full dataset.
                          o	This measures how impure or mixed up the overall dataset is?.
2.	Split the dataset using a feature (like Age, Income, etc.).
                          o	After the split, you’ll get subsets.
3.	Calculate the Gini Index for each subset.
                          o	If a subset is very pure (e.g., mostly "Yes" or mostly "No"), 
                            its Gini index will be low.
                          o	If a subset is very mixed (50% "Yes" and 50% "No"), 
                            its Gini index will be high.
5.	Calculate the weighted average of Gini indices for all the subsets.

  	Weighted average because each subset have different number of records.

  	This tells you the overall impurity after the split.
  	
7.	The feature with the lowest weighted average Gini is the best one to split on.






