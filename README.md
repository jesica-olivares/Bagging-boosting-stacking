# Bagging-boosting-stacking

## Ensemble Learning: 
### <center> Introduction, investigation and analysis of various techniques 

### Ensemble Learning Fundamentals  


# %% [markdown]
# Ensemble learning refers to the procedures employed to train multiple learning machines and combine their outputs, treating them as a “committee” of decision makers. The principle is that the decision of the committee, with individual predictions combined appropriately, should have better overall accuracy, on average, than any individual committee member.  
# 
# The members of the ensemble might be predicting real-valued numbers, class labels, posterior probabilities, rankings, clusterings, or any other quantity. Therefore, their decisions can be combined by many methods, including averaging, voting, and probabilistic methods. 
# 
# Ensemble learning can be represented through the following mathematical formulations for point and probability estimates respectively: 

# %% [markdown]
# Point estimate:
# $f(y|x, π)=\sum_{m=1}^{M} w_m f_m(y|x)$

# %% [markdown]
# Probability estimate: 
# $p(y|x, \boldsymbol{\pi}) = \sum_{m=1}^{M} \pi_m p(y|x, m)$

# %% [markdown]
# where:
# 
# *   $w_m$ is the tunable parameter (i.e. weight assigned to the m-th base model), which can be determined using accuracy/performance indicators or uniformly 
# 
# *   $f_m$ is the prediction of the m-th base model in the ensemble for the input variable $x$ and the target variable $y$,  
# 
# *   $π$ is the ensemble model hyperparameter, which depends on the type of ensemble model being used.  (E.g. for a bagging ensemble, which trains multiple base models on random subsets of the training data, π might represent the number of base models to include in the ensemble and the random seed used to generate the subsets, while for a boosting ensemble, which trains multiple base models sequentially, π might represent the learning rate or the maximum depth of the base models). 
# 
# *   $p(y|x, m)$ is the m-th model that estimates the probability of y given the input $x$ 

# %% [markdown]
# Ensemble learning is closely related to learning adaptive-basis function models and can be even claimed to be a neural net where $f_m$ represents the m-th hidden unit and $w_m$ are the output layer weights. 
# 
# The most important characteristics of Ensemble Learning is that is corresponds to enlarging the model scope by defining single new model which is a convex combination of base models. 
# 
# However, it is important to note that Ensemble Learning is not equivalent to BMA (Bayes Model Averaging), which is a weighted average of the predictions made by each model given by: 
#  

