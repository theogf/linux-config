@def title = "Variational Message Passing"
@def hasmath = true
@def comment_section = true
@def blog_post = true
@def hascode = true

# Variational Message Passing

Variational inference (VI) is one of the most popular methods in Bayesian machine thanks to its usual speed of convergence. Its principle is quite simple, given a target distribution $p(x)$ one tries to find the distribution $q(x)$ belonging to a certain family which minimizes a given metric. The most known instance if the KL-divergence, defined by 

$$\text{KL}(q||p) = \int q(x) \log (q(x) - p(x)) dx$$

In other terms we try to solve the following optimization problem

$$\arg_{q \in \mathcal{Q}} \max \text{KL}(q||p)$$

Typically $\mathcal{Q}$ is a class of distribution parametrized by its parameters $\theta$. A concrete example of that would be to take $\mathcal{Q}$ 