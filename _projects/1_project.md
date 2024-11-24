---
layout: page
title: String-Local QFT
description: Quantum Fields Localized along Half-Infinite Strings
img:
importance: 1
category: work
---

Hilbert space positivity, covariant quantum fields, and locality - These three properties are the cornerstones of a quantum field theory. Sacrifices of a few of the above properties are to be made when dealing with spin$$\geq1$$ states associated to their respective p-loc quantum fields. With the canonical approach, one has to work on saving the Hilbert space positivity, while the Wigner representation makes us worry about causality and covariance of the associated p-loc quantum field.

String localized fields jumps in, thanks to the flexibility in the choice of coefficient functions when writing the quantum field in Wigner-Weinberg representation, and liberates us from all the woes of ensuring positivity, covariance and locality of quantum fields. These s-loc quantum fields exist directly on the Hilbert space, having their own well-defined notions of covariance and locality.


<div class="row">
    <div class="col">
    </div>
    <div class="col-6">
        {% include figure.html path="assets/img/string.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col">
    </div>
</div>

Operating $$\partial_\kappa$$ on a p-loc field amounts to multiplying the intertwiners with $$\pm ik_\kappa$$. Now one can ask, what can be the inverse operation for this? The answer to this question brings us to the 'string-localization' (s-loc).\\ 
Integrating the point local (p-loc) field along a "string" $$x+\mathbb{R}_{+} e$$ multiplies the intertwiner with $$\frac{-i}{(p e)_{\mp}}$$. e is some spacelike direction and normalized, $e^{2}=-1$. We denote by $I_{e}$, the operation of string integration:

$$
\left(I_{e} \Phi\right)(x) \equiv \int_{0}^{\infty} d s\; \Phi(x+s e)
$$

One can see that $$(e \partial) I_{e} \Phi=-\Phi,$$ and hence, $$I_{e}$$ is minus the inverse of $$(e \partial)=e^{\kappa} \partial_{\kappa}$$.
$$I_{e} \Phi$$ is a string-local field.

$$\begin{equation}
\int_{0}^{\infty} d s e^{-i p(x\pm s e)}=\lim _{\varepsilon \searrow 0} \frac{-i}{(p e)\mp i \varepsilon} \cdot e^{-i p x} \equiv \frac{1}{i(p e)_{\mp}} \cdot e^{-i p x}
\end{equation}$$

