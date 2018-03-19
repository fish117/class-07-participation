# class-07-participation
cm 07 in class exercise

1.Bagging is a special case of random forests under which case?
Yes,because bagging means use all predictors instead of just a part of predictors.Then choose a part of samples to build the trees. Then, we will combine the results to get a model with lower variance and high variance.

2.What are the hyperparameters we can control for random forests?
We choose m predictors out of the total p predictors as our hyperparameters to make the trees decorrelated. By using these different combination of hyperparameters,we could get different trees. If we combine them together, in general it will generate a better result than bagging because these trees are decorrelated.



3.Suppose you have the following paired data of (x,y): (1,2), (1,5), (2,0). Which of the following are valid bootstrapped data sets? Why/why not?
(1,0), (1,2), (1,5)
(1,2), (2,0)
(1,2), (1,2), (1,5)

The 3rd one are the valid bootstrapped data sets because bootstrap means they will choose b observations randomly with replacement.
The 1st has (1,0) which doesn’t appear in the data set.
(1,2)(2,0) choose only 2 observations but we need 3 observations.
(1,2), (1,2), (1,5) choose 3 observations and (1,2) are chosen twice.


4.For each of the above valid bootstapped data sets, which observations are out-of-bag (OOB)?

For (1,2), (1,2), (1,5),the OOB is (2,0).
 



5.You make a random forest consisting of four trees. You obtain a new observation of predictors, and would like to predict the response. What would your prediction be in the following cases?
Regression: your trees make the following four predictions: 1,1,3,3.
Classification: your trees make the following four predictions: "A", "A", "B", "C".
For regression: it will be 2 because the average is 2.
For classification: it will be A
