---
title: "From deep learning to Bayesian neural network: 0 - Introduction"
date: 2024-12-02
---

While deep learning models have seen significant success across various domains, their black-box learning nature and lack of interpretability affect their reliability in safety-critical applications. In response to these limitations, the Bayesian paradigm offers a promising alternative by incorporating uncertainty estimation into model predictions, enhancing transparency and decision-making. 

<ul>
  {% for post in site.posts reversed %}
    <li>
      <h4><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h4>
    </li>
  {% endfor %}
</ul>

## Reference
If you feel this tutorial is useful, I would appreciate it if you would cite the following paper:
```
@article{chen5009452interplay,
  title={Interplay between Bayesian Neural Networks and Deep Learning: A Survey},
  author={Chen, Yinsong and Yu, Samson S and Li, Zhong and Eshraghian, Jason K and Lim, Chee Peng},
  journal={Available at SSRN: https://ssrn.com/abstract=5009452 or http://dx.doi.org/10.2139/ssrn.5009452}
}
```