---
title: "From deep learning to Bayesian neural network: 1 - Deep learning and its theoretical framework"
date: 2024-12-05
category: "Deep Learning"
---

## Basic concepts
Deep learning has become a prominent research field, with numerous architectures and training algorithms proposed. We start with the simplest case: training multi-layer perceptrons (feedforward neural networks) using the stochastic gradient descent (SGD) algorithm for supervised learning tasks. 

A feed-forward neural network (NN) consisting of \\\(L\\\) layers, each defined by weight matrices \\\(W^1,...,W^L\\\) and post-activation vectors \\\(x^1,...,x^L\\\), with \\\(N_l\\\) neurons per layer. Then the network dynamics, starting from the input \\\(x^0\\\), are described by 
\\\[x^l=\phi(h^l), h^l=W^lx^{l-1}+b^l, \text{ for }l=1,...,L,\tag{1}\\\]
where \\\(b^l\\\) denotes the bias vector, \\\(h^l\\\) represents the linear pre-activations, and \\\(\phi\\\) is a non-linear activation function. A complete set of NN parameters is \\\(\theta=\\\{W^l,b^l\\\}_{l=1}^L\\\), and the output for input \\\(x^0\\\) is \\\(\hat{y}=h^L=f(x^0,\theta)\\\), where the mapping function \\\(f\\\) is recursively defined by Eq. [1]. 

<p align="center">
<img src="https://github.com/icarusunimelb/skills-github-pages/blob/main/_posts/figures/perceptron.png?raw=true" alt="Perceptron" title="The k-th perceptron of layer l" width="50%" height="50%">
<div style="text-align: center;">Fig.1. The k-th perceptron of layer l</div>
</p>

Figure 1 illustrates the structure of a single perceptron, which functions as a linear binary classifier but cannot handle non-linearly separable data. To overcome this limitation, multiple perceptrons are combined to form multi-layer perceptrons, as depicted in Figure 2.

<p align="center">
<img src="https://github.com/icarusunimelb/skills-github-pages/blob/main/_posts/figures/MLP.png?raw=true" alt="MLP" title="Multi-layer preceptron" width="50%" height="50%">
<div style="text-align: center;">Fig.2. Multi-layer preceptron</div>
</p>

Optimizing NN parameters typically involves an iterative process, known as "training," to minimize the loss function.
<p align="center">
<img src="https://github.com/icarusunimelb/skills-github-pages/blob/main/_posts/figures/training-loop.png?raw=true" alt="training-loop" title="training-loop" width="80%" height="80%">
<div style="text-align: center;">Fig.3. Training loop</div>
</p>

A common approach for training multi-layer perceptrons is the SGD algorithm, where \\\(L(\hat{y},y)\\\) represents the loss function quantifying the discrepancy between \\\(\hat{y}\\\) and \\\(y\\\).

```
Choose initial guess θ⁰, k=0
For i from 1 to T (epoches) 
    For j from 1 to N (training samples) 
        Consider a sample {xⱼ,yⱼ}\
        Update: θᵏ⁺¹=θᵏ-𝝁∇L(ŷⱼ,yⱼ); k=k+1
```

To compute partial derivatives \\\(\frac{\partial L}{\partial w_i^l}\\\) for updating weights, backpropagation is employed, which is based the chain rule. For example, given \\\(z=g(u)\\\) and \\\(u=f(x)\\\), the chain rule states that the derivative can be expressed as \\\(\frac{dz}{dx} = \frac{dz}{du}\frac{du}{dx}\\\). Similarly, in the context of NNs, the derivatives are computed as:
\\\[\frac{\partial L}{\partial w_i^L} = \frac{\partial L}{\partial h^L}\frac{\partial h^L}{\partial w_i^L} \tag{2}\\\]
\\\[\frac{\partial L}{\partial w_i^{L-1}} = \frac{\partial L}{\partial h^L}\frac{\partial h^L}{\partial x^{L-1}}\frac{\partial x^{L-1}}{\partial h^{L-1}}\frac{\partial h^{L-1}}{\partial w_i^{L-1}} \tag{3}\\\]
and so forth.





## References
[1] Rubinstein, B.I. (2020, August). Statistical machine learning [PowerPoint slides]. School of Computing and Information Systems, The University of Melbourne. \
[2] Bengio, Y., Goodfellow, I., & Courville, A. (2017). Deep learning (Vol. 1). Cambridge, MA, USA: MIT press. \
[3] Chen, Y., Yu, S. S., Li, Z., Eshraghian, J. K., & Lim, C. P. Interplay between Bayesian Neural Networks and Deep Learning: A Survey. Available at SSRN 5009452.