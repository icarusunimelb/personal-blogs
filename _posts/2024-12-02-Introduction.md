---
title: "From deep learning to Bayesian neural network: 0 - Introduction"
date: 2024-12-02
---

While deep learning models have seen significant success across various domains, their black-box learning nature and lack of interpretability affect their reliability in safety-critical applications. In response to these limitations, the Bayesian paradigm offers a promising alternative by incorporating uncertainty estimation into model predictions, enhancing transparency and decision-making.

<ul>
  {% for post in site.posts reversed %}
    <li>
      <h4><a href="{{ post.url }}">{{ post.title }}</a></h4>
    </li>
  {% endfor %}
</ul>