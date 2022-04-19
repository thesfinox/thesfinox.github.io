---
title: "Machine Learning for Complete Intersection Calabi-Yau Manifolds: a Methodological Study"
collection: publications
permalink: /publication/2020-07-machine-learning-calabi-yau
excerpt: "We revisit the question of predicting both Hodge numbers $h^{1,1}$ and $h^{2,1}$ of Complete Intersection Calabi-Yau 3-folds using machine learning."
date: 2021-06-15
venue: "Phys. Rev. D, 103, 12, 126014"
paperurl: "https://doi.org/10.1103/PhysRevD.103.126014"
citation: "H. Erbin, R. Finotello. 'Machine Learning for Complete Intersection Calabi-Yau Manifolds: a Methodological Study'. Phys.Rev.D 103 (2021) 12, 126014"
---
We revisit the question of predicting both Hodge numbers $h^{1,1}$ and $h^{2,1}$ of Complete Intersection Calabi-Yau 3-folds using machine learning, considering both the old and new datasets built respectively by Candelas-Dale-Lutken-Schimmrigk/Green-Hübsch-Lutken and by Anderson-Gao-Gray-Lee. In real world applications, implementing a ML system rarely reduces to feed the brute data to the algorithm. Instead, the typical workflow starts with an exploratory data analysis which aims at understanding better the input data and finding an optimal representation. It is followed by the design of a validation procedure and a baseline model. Finally, several machine learning models are compared and combined, often involving neural networks with a topology more complicated than the sequential models typically used in physics. By following this procedure, we improve the accuracy of machine learning computations for Hodge numbers with respect to the existing literature. First, we obtain $97\%$ (resp. $99\%$) accuracy for $h^{1,1}$ using a neural network inspired by the Inception model for the old dataset, using only $30\%$ (resp. $70\%$) of the data for training. For the new one, a simple linear regression leads to almost $100\%$ accuracy with $30\%$ of the data for training. The computation of $h^{2,1}$ is less successful as we manage to reach only $50\%$ accuracy for both datasets, but this is still better than the $16\%$ obtained with a simple neural network (SVM with Gaussian kernel and feature engineering and sequential convolutional network reach at best $36\%$). This serves as a proof of concept that neural networks can be valuable to study the properties of geometries appearing in string theory.

[Full text](https://doi.org/10.1103/PhysRevD.103.126014)

[preprint](https://arxiv.org/abs/2007.15706)

[Code](https://github.com/thesfinox/ml-cicy)
