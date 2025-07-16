# Validation

This folder reports the results from two sets of additional experiments: 
- Embedding another non-parametric model within MAML
- Applying transfer learning instead of meta-learning

# MAML + nonparametric
The folder contains the MFDs estimated with another non-parametric model with literature, with and without the meta-learning component. The esperiments are reported with two sets of hyperparameters (150/300 meta iterations for MAML and 50/1000 epochs for the non-parametric model). The non-parametric model is from literature: Bramich, D. M., Menéndez, M., & Ambühl, L. (2022). Fitting empirical fundamental diagrams of road traffic: A comprehensive review and comparison of models using an extensive data set. IEEE Transactions on Intelligent Transportation Systems, 23 (9), 14104–14127.

# comparison with transfer learning
The folder contains 4 folders (one for each LD configuration). The results report the MSE and RRSE across experiments and tested combinations of meta/transfer-learning strategies and non-parametric models