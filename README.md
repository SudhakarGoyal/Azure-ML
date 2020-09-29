# Optimizing an ML Pipeline in Azure

## Overview
This project is part of the Udacity Azure ML Nanodegree.
In this project, we build and optimize an Azure ML pipeline using the Python SDK and a provided Scikit-learn model.
This model is then compared to an Azure AutoML run.

## Summary
**In this project we use the Bank Marketing dataset to showcase how you can use AutoMLm and differentiate between hyperdrive and automl training process and subsequents outputs for a classification problem. The classification goal is to predict if the client will subscribe to a term deposit with the bank on the basis of client specific festueres like age, job, marital status, education, housing, loan etc"**

**We got our best performing model through AutoML. VotingEnsemble performed the best giving an accuracy of 94.99. The accuracy received from hyperdrive was approximately 91% whihc is not bad and in my opinion can be improved further considering many more hyperprameter iptimization**

## Scikit-learn Pipeline
**The data was read in a tabular form and was on hot encoded in a way that yes and no were converted to 1's and 0's respectively. As this was a classification task, scikit learn is currently just using Logistic regression for binary classification. The model needs to predict whether the client will subscribe to term deposit based on several features.**

**The parameter sampler chosen is really simple. We just wish to check wich optimizer works better than the other given the same hyperparameters. Not much of a differecne has been noted though between Adam and SGD for the specfic dataset in contention**

**The major benefit of The Median Stopping policy is that it computes running averages across all runs and cancels runs whose best performance is worse than the median of the running averages which ultimately helps out to iron out worst performing models.**

## AutoML
**votingclassifier/  voting ensemble was the best model returned by automl. Thought the accuracy of other models was also very similar. Some of the parameters computed  max_depth=3,
         min_child_weight=1,
         missing=nan,
         n_estimators=100,
         n_jobs=1,
         nthread=None,
         objective='binary:logistic',
         random_state=0,
         reg_alpha=0,
         reg_lambda=1,
         scale_pos_weight=1,
         seed=None,
         silent=None,
         subsample=1,
         tree_method='auto**

## Pipeline comparison
**AutoMl performs better than the manual training using hyperdrive for hyperparameters optimization. The differecne in accuracy is aprox 4 percentage points with AutoMl acheiving 94.99% accuracy. Different models bing used to check the performance along with numerous hyperparamters not even considered in hyperdrive actually play major role and that is why automl performed better. Though hyperdrive can still include more hyperparameters for tuning but in my opinion, the accuracy will be similar in the end **

## Future work
**Improvement in terms more n_cross_validations can also help to train and test the data differently which might help in improving the model. Moreover feature tuning and transformation and creation of more features has not been taken into consideration during the data exploration process which will play an integral part in understanding data and improve training **

## Proof of cluster clean up
**I had stopped the cluster instance in use. After the 2hrs of demo session, the cluster got deleted automtically as the session was over.**
