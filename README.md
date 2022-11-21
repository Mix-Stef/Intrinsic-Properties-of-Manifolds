# Intrinsic-Properties-of-Manifolds
Using SymPy (Python's symbolic computation package) to compute as many intrinsic properties of a manifold as possible.

#### Goal:

Given a Riemannian Metric defined on a manifold, compute as many *intrinsic* properties, meaning properties that can be derived by only knowning the metric and the respective coordinate system. Intuitively, "intrinsic" means that a blind observer could measure these properties by only moving along the manifold, without being aware of the ambient space in which the manifold might be embedded.\\


The metric is a symmetric bilinear form that when restricted on the tangent space of the manifold defines an inner product.
 $g: T_{p}\mathcal{M} \times T_{p} \mathcal{M} \rightarrow \mathbb{R}$. Essentially, it is a $n \times n$ symmetric matrix, where $n$ is the dimension of the manifold (or, equivalently, of the tangent space).
 
 
 
