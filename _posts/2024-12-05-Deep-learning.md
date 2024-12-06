---
title: "From deep learning to Bayesian neural network: 1 - Deep learning and its theoretical framework"
date: 2024-12-05
---

## Basic concepts
Deep learning has become a prominent research field, with numerous architectures and training algorithms proposed. We start with the simplest case: training multi-layer perceptrons (feedforward neural networks) using the stochastic gradient descent (SGD) algorithm for supervised learning tasks. 

A feed-forward neural network (NN) consisting of \\\(L\\\) layers, each defined by weight matrices \\\(W^1,...,W^L\\\) and post-activation vectors \\\(x^1,...,x^L\\\), with \\\(N_l\\\) neurons per layer. Then the network dynamics, starting from the input \\\(x^0\\\), are described by 
\\\[x^l=\phi(h^l), h^l=Wx^{l-1}+b^l, \text{ for }l=1,...,L,\tag{1}\\\]
where \\\(b^l\\\) denotes the bias vector, \\\(h^l\\\) represents the linear pre-activations, and \\\(\phi\\\) is a non-linear activation function. A complete set of NN parameters is \\\(\theta=\\\{W^l,b^l\\\}_{l=1}^L\\\), and the output for input \\\(x^0\\\) is \\\(\hat{y}=h^L=f(x^0,\theta)\\\), where the mapping function \\\(f\\\) is recursively defined by Eq. [1]. 

<p align="center">
<img src="https://github.com/icarusunimelb/skills-github-pages/blob/main/_posts/figures/perceptron.png?raw=true" alt="Perceptron" title="The k-th perceptron of layer l" width="60%" height="60%">
<div style="text-align: center;">Fig.1. The k-th perceptron of layer l</div>
</p>

Figure 1 illustrates the structure of a single perceptron, which functions as a linear binary classifier but cannot handle non-linearly separable data. To address this limitation, multi-layer perceptrons were developed, as shown in Figure 2.

<p align="center">
<img src="https://github.com/icarusunimelb/skills-github-pages/blob/main/_posts/figures/MLP.png?raw=true" alt="MLP" title="Multi-layer preceptron" width="60%" height="60%">
<div style="text-align: center;">Fig.2. Multi-layer preceptron</div>
</p>




## References
[1] Rubinstein, B.I. (2020, August). Statistical machine learning [PowerPoint slides]. School of Computing and Information Systems, The University of Melbourne. \
[2] Bengio, Y., Goodfellow, I., & Courville, A. (2017). Deep learning (Vol. 1). Cambridge, MA, USA: MIT press.