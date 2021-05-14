---
layout: post
title:  "Neural Network"
date:   2020-12-28 00:00:00 -0000
categories: PZ update
---
<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>

<!-- Mathjax Support -->
<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

## Feedforward

Feedforward is the process neural networks use to turn the input into an output. The following 

$$
\hat{y}=\sigma\circ W^{(3)}\circ\sigma\circ W^{(2)}\circ\sigma\circ W^{(1)}(x)
$$

\begin{align}
    g &= \int_a^b f(x)dx \label{eq1} \\
    a &= b + c \label{eq2}
\end{align}

<p align="center">
  <img width="222" alt="Screen Shot 2020-12-30 at 6 43 58 PM" src="https://user-images.githubusercontent.com/41249426/103389941-0e16e800-4acf-11eb-984e-ef583124e562.png">
  <figcaption align="center">Fig.1 Illustration of neural network.</figcaption>
</p>


$$
\begin{align*}
  & \phi(x,y) = \phi \left(\sum_{i=1}^n x_ie_i, \sum_{j=1}^n y_je_j \right)
  = \sum_{i=1}^n \sum_{j=1}^n x_i y_j \phi(e_i, e_j) = \\
  & (x_1, \ldots, x_n) \left( \begin{array}{ccc}
      \phi(e_1, e_1) & \cdots & \phi(e_1, e_n) \\
      \vdots & \ddots & \vdots \\
      \phi(e_n, e_1) & \cdots & \phi(e_n, e_n)
    \end{array} \right)
  \left( \begin{array}{c}
      y_1 \\
      \vdots \\
      y_n
    \end{array} \right)
\end{align*}
$$
## Backpropogation
