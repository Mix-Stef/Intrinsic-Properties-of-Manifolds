# Intrinsic-Properties-of-Manifolds
Using SymPy (Python's symbolic computation package) to compute as many intrinsic properties of a manifold as possible.

#### Goal:

Given a Riemannian Metric defined on a manifold, compute as many *intrinsic* properties, meaning properties that can be derived by only knowning the metric and the respective coordinate system. Intuitively, "intrinsic" means that a blind observer could measure these properties by only moving along the manifold, without being aware of the ambient space in which the manifold might be embedded.


The metric is a symmetric bilinear form that when restricted on the tangent space of the manifold defines an inner product.
 $g: T_{p}\mathcal{M} \times T_{p} \mathcal{M} \rightarrow \mathbb{R}$. Essentially, it is a $n \times n$ symmetric matrix, where $n$ is the dimension of the manifold (or, equivalently, of the tangent space).
 
 
 Given a Riemannian Metric, one can compute -using local coordinates on a manifold- the following quantities:
 
* Christoffel Symbols: Functions that describe how the basis vectors change. They are not tensors. In local coordinates they can be computed by using the metric as follows $\displaystyle \Gamma_{ij}^{k} = \frac{1}{2} \sum_{m=1}^{n} g^{km} \Big( \frac{\partial g_{jm}}{\partial x^{i}} + \frac{\partial g_{mi}}{\partial x^{j}} - \frac{\partial g_{ij}}{\partial x^{k}}       \Big)$
* Riemann Curvature Tensor: A tensor field that measures the failure of parallel transport along a vector field defined on the manifold. In local coordinates, the contravariant Riemann Curvature Tensor, $R_{\sigma \mu \nu}^{\rho}$, is given by: $R_{\sigma \mu \nu}^{\rho} = \partial_{\mu} \Gamma_{\nu \sigma}^{\rho} - \partial_{\nu} \Gamma_{\mu \sigma}^{\rho} + \Gamma_{\mu \lambda}^{\rho} \Gamma_{\nu \sigma}^{\lambda} - \Gamma_{\nu \lambda}^{\rho} \Gamma_{\mu \sigma}^{\lambda}$. In order to lower the upper index to get the covariant Riemann tensor we have to multiply by the metric as follows: $R_{\rho \sigma \mu \nu} = g_{\rho \lambda} R_{\sigma \mu \nu}^{\lambda}$

 
 
 
