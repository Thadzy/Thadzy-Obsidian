---
tags:
  - Calculus2
  - Series
date: 2025-04-14
---
## Introduction 
A Fourier series is a mathematical tool that decomposes periodic functions into an infinite sum of sine and cosine functions.


$$f(x) = a_0 + \sum_{n=1}^{\infty} \left( a_n \cos \frac{n\pi x}{L} + b_n \sin \frac{n\pi x}{L} \right)$$

$$a_0 = \frac{1}{2L} \int_{-L}^{L} f(x) \, dx$$

$$a_n = \frac{1}{L} \int_{-L}^{L} f(x) \cos \frac{n\pi x}{L} \, dx, \quad n \geq 1$$

$$b_n = \frac{1}{L} \int_{-L}^{L} f(x) \sin \frac{n\pi x}{L} \, dx, \quad n \geq 1$$
