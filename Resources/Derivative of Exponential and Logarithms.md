---
tags:
  - Calculus
Area: "[[Areas/Calculus I]]"
---
link : [[Exponential and Logarithms]] [[Derivative]]
# Derivative of Exponential and Logarithms
## Derivative of Exponential
![[Pasted image 20250628142152.png]]
$$\ln a = \lim_{h \to 0}\frac{a^h-1}{h} $$
$$\frac{d}{dx}2^x=2^x\ln2$$
Therefore the derivative of Exponential is 
$$\frac{d}{dx}b^x= b^x\ln b$$
if there is
$$\frac{d}{dx}b^{f(x)} = f'(x) \ln b^{fx}$$
## Derivative of e
we know that $\frac{d}{dx}b^x= b^x\ln b$ therefore when derivative of e 
$$\frac{d}{dx}e^x = e \ln e^x$$
while $\ln e = 1$ because $e^1 = e$
$log_b b = 1$ because $b^1 = b$
therefore derivative of e
$$\frac{d}{dx}e^x = e^x$$
## Summarize Differentiation of Exponentials
![[Pasted image 20250628145208.png]]
## Derivative of Logarithms
$$ \frac{d}{dx} b^{f(x)} = f'(x) \ln b \cdot b^{f(x)} $$

Differentiation Rule for Logarithms
$$ \frac{d}{dx} \log_b f(x) = f'(x) \cdot \frac{1}{\ln b} \cdot \frac{1}{f(x)} $$
## Summarize Differentiation of Logarithms
![[Pasted image 20250628150423.png]]
# Cues
**Why ln e = 1?**
**Ans**  Because the logarithm tells you **"what power must I raise e to get e?"**
# Summary
```
Derivative of 2^x = 2^x ln x by chain rule and if I derivative e I got the same e and the logarithms Start by converting the base-b logarithm to the natural log then apply the chain rule.
```