# Intrinsic-Properties-of-Manifolds
Using SymPy (Python's symbolic computation package) to compute as many intrinsic properties of a manifold as possible.

#### Goal:

Given a Riemannian Metric defined on a manifold, compute as many *intrinsic* properties, meaning properties that can be derived by only knowning the metric and the respective coordinate system. Intuitively, "intrinsic" means that a blind observer could measure these properties by only moving along the manifold, without being aware of the ambient space in which the manifold might be embedded. For all the computations we assume a Levi-Civita connection defined on the manifold (i.e. a torsion-less connection that is compatible with the metric).


The Riemannian metric is a symmetric bilinear form of rank 2 that when restricted on the tangent space of the manifold defines an inner product.
 $g: T_{p}\mathcal{M} \times T_{p} \mathcal{M} \rightarrow \mathbb{R}$. Essentially, it is a $n \times n$ symmetric matrix, where $n$ is the dimension of the manifold (or, equivalently, of the tangent space).
 
 
 Given a Riemannian Metric, one can compute -using local coordinates on a manifold- the following quantities:
 
* Christoffel Symbols: Functions that describe how the basis vectors change. They are not tensors. In local coordinates they can be computed by using the metric as follows $\displaystyle \Gamma_{ij}^{k} = \frac{1}{2} \sum_{m=1}^{n} g^{km} \Big( \frac{\partial g_{jm}}{\partial x^{i}} + \frac{\partial g_{mi}}{\partial x^{j}} - \frac{\partial g_{ij}}{\partial x^{k}} \Big)$
* Riemann Curvature Tensor: A tensor field that measures the failure of parallel transport along a vector field defined on the manifold. In local coordinates, the contravariant Riemann Curvature Tensor, $R_{\sigma \mu \nu}^{\rho}$, is given by: $R_{\sigma \mu \nu}^{\rho} = \partial_{\mu} \Gamma_{\nu \sigma}^{\rho} - \partial_{\nu} \Gamma_{\mu \sigma}^{\rho} + \Gamma_{\mu \lambda}^{\rho} \Gamma_{\nu \sigma}^{\lambda} - \Gamma_{\nu \lambda}^{\rho} \Gamma_{\mu \sigma}^{\lambda}$. In order to lower the upper index to get the covariant Riemann tensor we have to multiply by the metric as follows: $R_{\rho \sigma \mu \nu} = g_{\rho \lambda} R_{\sigma \mu \nu}^{\lambda}$
* Ricci Curvature Tensor: The Ricci Curvature Tensor measures how a shape is deformed as we move along geodesics in the manifold. It is a symmetric bilinear form of rank 2. We get it by contracting the covariant Riemann Curvature Tensor by the metric: $R_{ij} = g^{kl}R_{kilj}$
* Scalar Curvature: The scalar curvature is computed by further contracting the Ricci Tensor by the metric: $\mathcal{R} = g^{ij}R_{ij}$. For 2-dimensional surfaces, the scalar curvature is twice the well-known Gaussian Curvature
* Gaussian Curvature: It is defined as the product of the principal curvatures at any given point: $K = k_{1}k_{2}$. A more "Riemannian" definition for a 2-manifold, with respect to the metric, is: $K \frac{\langle(\nabla_{2} \nabla_{1} - \nabla_{1} \nabla_{2})e_{1}, e_{2}\rangle}{\det g}$. An alternative definition, using the first and second fundamental forms, is: $K = \frac{\det(II)}{\det(I)}$. In this notebook we use the "Brioschi formula", which only contains the coefficients of the first fundamental form and their derivatives.
* Euler Characteristic: A very important topological invariant of a manifold. For regular polyhedra we have Euler's polyhedron formula: $V-E+F=2$. For compact manifold with-or-without boundary one can use the Gauss-Bonet formula: $\int_{\mathcal{M}} K dA + \int_{\partial \mathcal{M}} k_{g} ds = 2 \pi \chi$

 
 
 
