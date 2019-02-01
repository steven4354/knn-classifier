# KNN Classifiers

So far we've covered learning via probability (naive Bayes) and learning via errors (regression). Here we'll cover learning via similarity. This means we look for the datapoints that are most similar to the observation we are trying to predict.

Nearest neighbor - grab the point that is closest and return the "Y" value of that

K Nearest neighbor - grab K nearest points and return the "Y" that appears the most frequently out of the K points

Improving on KNN classifiers

- normalization

It can be a more obvious challenge if you were dealing with something where the relative scales are strikingly different. For example, if you were looking at buildings and you have height in floors and square footage, you'd have a model that would really only care about square footage since distance in that dimension would be a far greater number of units than the number of floors.

Turn all the values to be between 0 and 1 or -1 to 1 (same thing)

- weighing 

There is one more thing to address when talking about distance, and that is weighting. In the vanilla version of KNN, all k of the closest observations are given equal votes on what the outcome of our test observation should be. When the data is densely populated that isn't necessarily a problem.

However, sometimes the k nearest observations are not all similarly close to the test. In that case it may be useful to weight by distance. Functionally this will weight by the inverse of distance, so that closer datapoints (with a low distance) have a higher weight than further ones.

(sample is in the notebook)
