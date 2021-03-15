# Transformations and Exceptions

[TOC]

## Distributions of Functions of a Random Variable

**Theorem:** Let $X$ have *cdf* $F_X(x)$, let $Y=g(X)$, and let $\mathcal{X}$ and $\mathcal{Y}$ be defined as $\mathcal{X}=\{x|f_X(x)>0\}$ and $\mathcal{Y}=\{y|y=g(x) \;\mathrm{for\;some\;}x\in\mathcal{X}\}$

1. If $g$ is an increasing function on $\mathcal{X}$, $F_Y(y)=F_X(g^{-1}(y))$ for $y\in\mathcal{Y}$
2. If $g$ is a decreasing function on $\mathcal{X}$ and $\mathcal{X}$ is a continuous random variable, $F_Y(y)=1-F_X(g^{-1}(y))$ for $y\in\mathcal{Y}$