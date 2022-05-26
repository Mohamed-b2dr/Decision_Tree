# Decision_Tree
* Like SVMs, Decision Trees are versatile Machine Learning algorithms that can perform both classification and regression tasks, and even multioutput tasks.
#### Decision Tree Classification 
![Decision_Tree Classification](https://github.com/Mohamed-b2dr/Decision_Tree/blob/main/download%20(1).png)
#### Decision Tree Regression 
![Decision_Tree Regression](https://github.com/Mohamed-b2dr/Decision_Tree/blob/main/download.png)
## Concepts covered
* Training and Visualizing a Decision Tree
* Optimize max_depth

# Note
* One of the many qualities of Decision Trees is that they require very little data preparation. In fact, they don’t require feature scaling or centering at all.
* Scikit-Learn uses the CART algorithm, which produces only binary trees: nonleaf nodes always have two children (i.e., questions only have yes/no answers). However, other algorithms such as ID3 can produce Decision Trees with nodes that have more than two children.

# Model Interpretation: White Box Versus Black Box
Decision Trees are intuitive, and their decisions are easy to interpret. 
Such models are often called white box models. In contrast, as we will see, Random Forests or neural networks are generally considered black box models. 
They make great predictions, and you can easily check the calculations that they performed to make these predictions; nevertheless, it is usually hard to explain in simple terms why the predictions were made. For example, if a neural network says that a particular person appears on a picture, it is hard to know what contributed to this prediction: did the model recognize that person’s eyes? Their mouth? Their nose? Their shoes? Or even the couch that they were sitting on? Conversely, Decision Trees provide nice, simple classification rules that can even be applied manually if need be (e.g., for flower classification).

# Note
CART algorithm is a greedy algorithm: it greedily searches for an optimum split at the top level, then repeats the process at each subsequent level. It does not check whether or not the split will lead to the lowest possible impurity several levels down. A greedy algorithm often produces a solution that’s reasonably good but not guaranteed to be optimal. Unfortunately, finding the optimal tree is known to be an NPComplete problem:2 it requires O(exp(m)) time, making the problem intractable even for small training sets. This is why we must settle for a “reasonably good” solution

# Regularization Hyperparameters
To avoid overfitting the training data, you need to restrict the Decision Tree’s freedom during training. As you know by now, this is called regularization.The regularization hyperparameters depend on the algorithm used, but generally you can at least restrict the maximum depth of the Decision Tree. In Scikit-Learn, this is controlled by the max_depth hyperparameter (the default value is None, which means unlimited). Reducing max_depth will regularize the model and thus reduce the risk of overfitting
