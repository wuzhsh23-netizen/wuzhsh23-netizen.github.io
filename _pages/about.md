---
permalink: /
title: ""
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

# Hi, I am Zheshun Wu 👋

I am currently a Ph.D. student in the School of Computer Science and Technology at Harbin Institute of Technology, Shenzhen, where I am fortunate to be advised by Prof. Jie Liu (IEEE Fellow) and Prof. Zenglin Xu. Prior to this, I received my Master's degree in Information and Communication Engineering from Sun Yat-sen University in 2023, and my Bachelor's degree in Information and Interaction Design from South China University of Technology in 2020.

My research interests lie broadly in **Trustworthy AI, Edge Intelligence, and Efficient Training and Inference**, with a particular focus on:

* **Efficient Training and Inference:** Distributed machine learning, progressive training, MoE training, and edge collaborative inference.
* **Online Learning and Reinforcement Learning:** Robust multi-armed bandits and provably sample-efficient reinforcement learning.
* **Wireless Communications and Networking:** AI for communications, wireless sensing, and localization.

## 🔥 News

* **[Feb 2026]** One paper was accepted by Neural Networks!
* **[Jan 2026]** One paper was accepted by ICLR 2026!

## Publications

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

{% if site.publication_category %}
  {% for category in site.publication_category %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
        <h2>{{ category[1].title }}</h2><hr />
        {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}
