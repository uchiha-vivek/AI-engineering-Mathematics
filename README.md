# Mathematics for AI

A comprehensive reference of mathematical foundations used in deep learning, machine learning, and frontier AI research.

---

## 1. Linear Algebra *(Most Important)*

Used everywhere in deep learning.

### Topics
- Vectors and vector spaces
- Matrices and tensors
- Matrix multiplication
- Dot products
- Norms (L1, L2)
- Orthogonality
- Eigenvalues and eigenvectors
- Singular Value Decomposition (SVD)
- Principal Component Analysis (PCA)
- Matrix factorization
- Rank and null space
- Positive definite matrices
- Kronecker products
- Tensor decomposition
- Low-rank approximations

### Applications
Embeddings · Transformers · Attention · PCA · LoRA · Quantization

---

## 2. Calculus

Required for optimization and backpropagation.

### Topics
- Limits
- Differentiation
- Partial derivatives
- Chain rule
- Multivariable calculus
- Jacobian matrices
- Hessian matrices
- Gradient
- Directional derivatives
- Taylor series
- Vector calculus
- Implicit differentiation

### Applications
Backpropagation · Neural network training · Gradient descent

---

## 3. Probability Theory

The language of uncertainty.

### Topics
- Random variables
- Probability distributions
- Joint distributions
- Conditional probability
- Bayes' theorem:

$$P(A \mid B) = \frac{P(B \mid A)\, P(A)}{P(B)}$$

- Expectation
- Variance
- Covariance
- Correlation
- Law of total probability
- Markov chains
- Stochastic processes
- Gaussian, Poisson, Bernoulli, and Exponential distributions

### Applications
Bayesian AI · Reinforcement learning · Generative models · LLM token prediction

---

## 4. Statistics

Used to evaluate models.

### Topics
- Estimation theory
- Maximum likelihood estimation (MLE)
- MAP estimation
- Hypothesis testing
- Confidence intervals
- Statistical significance
- Regression
- ANOVA
- Bias-variance tradeoff
- Sampling theory
- Bootstrap methods
- A/B testing

### Applications
Model evaluation · Experiment design

---

## 5. Information Theory

Foundation of LLMs and generative models.

### Topics
- Entropy:

$$H(X) = -\sum_{x} p(x) \log p(x)$$

- Cross entropy
- KL divergence
- Mutual information
- Channel capacity
- Coding theory
- Information bottleneck

### Applications
LLM loss functions · Compression · Representation learning

---

## 6. Optimization Theory

Core of model training.

### Topics
- Convex and non-convex optimization
- Gradient descent
- SGD, Adam, RMSProp, Momentum
- Newton's method and Quasi-Newton methods
- Constrained optimization
- Lagrange multipliers
- Duality theory
- Trust region methods

### Applications
Neural network training · RL optimization

---

## 7. Numerical Methods

Used when exact solutions are impossible.

### Topics
- Numerical differentiation and integration
- Root finding
- Matrix inversion
- Iterative solvers
- Stability analysis
- Error propagation

### Applications
Large-scale training · Scientific ML

---

## 8. Discrete Mathematics

Important for algorithms and reasoning.

### Topics
- Logic
- Set theory
- Relations and functions
- Recurrence relations
- Combinatorics and counting
- Graph theory
- Boolean algebra

### Applications
Search · Agents · Knowledge graphs

---

## 9. Graph Theory

Huge area in modern AI.

### Topics
- Graphs, trees, and DAGs
- Network flow
- Graph traversal
- Spectral graph theory
- Random graphs

### Applications
Graph Neural Networks · Knowledge graphs · Agent workflows

---

## 10. Differential Equations

Used in advanced AI research.

### Topics
- ODEs
- PDEs
- Dynamical systems
- Stability analysis
- Chaos theory

### Applications
Neural ODEs · Diffusion models

---

## 11. Functional Analysis

Research-level deep learning.

### Topics
- Hilbert spaces
- Banach spaces
- Function spaces
- Linear operators
- Spectral theory

### Applications
Kernel methods · Theoretical deep learning

---

## 12. Measure Theory

Necessary for advanced probability.

### Topics
- Sigma algebras
- Measurable functions
- Lebesgue integration
- Probability spaces

### Applications
Advanced Bayesian ML · RL theory

---

## 13. Bayesian Mathematics

### Topics
- Bayesian inference
- Posterior distributions
- Priors
- Variational inference
- MCMC
- Gibbs sampling
- Hamiltonian Monte Carlo

### Applications
Bayesian neural networks · Probabilistic AI

---

## 14. Convex Analysis

### Topics
- Convex sets and functions
- Fenchel duality
- Subgradients
- KKT conditions

### Applications
Optimization theory

---

## 15. Stochastic Processes

### Topics
- Markov processes
- Hidden Markov Models (HMMs)
- Brownian motion
- Martingales

### Applications
Reinforcement learning · Sequential modeling

---

## 16. Game Theory

Important for multi-agent systems.

### Topics
- Nash equilibrium
- Zero-sum games
- Cooperative games
- Mechanism design

### Applications
RLHF · Multi-agent AI

---

## 17. Control Theory

Increasingly important.

### Topics
- State space models
- Feedback systems
- Stability
- Optimal control
- Dynamic programming

### Applications
Robotics · Agent planning

---

## 18. Reinforcement Learning Mathematics

### Topics
- Bellman equations:

$$V(s) = \max_{a} \left( R(s,a) + \gamma \sum_{s'} P(s' \mid s, a)\, V(s') \right)$$

- Markov Decision Processes (MDPs)
- Policy gradients
- Q-learning
- Temporal difference learning
- Actor-critic methods

### Applications
RL agents · Robotics · Reasoning systems

---

## 19. Signal Processing

### Topics
- Fourier Transform and FFT
- Wavelets
- Convolution
- Spectral analysis

### Applications
Audio AI · Speech models · Time-series AI

---

## 20. Geometry & Manifold Learning

### Topics
- Euclidean geometry
- Differential geometry
- Riemannian manifolds
- Geodesics
- Curvature

### Applications
Embedding spaces · Representation learning

---

## 21. Transformer-Specific Mathematics

### Topics
- Attention mechanisms:

$$\text{Attention}(Q, K, V) = \text{softmax}\!\left(\frac{QK^T}{\sqrt{d_k}}\right) V$$

- Positional encodings
- Rotary embeddings (RoPE)
- Low-rank approximations
- Sparse attention
- Mixture of Experts

### Applications
GPT · Claude · Gemini · Llama

---

## 22. Diffusion Model Mathematics

### Topics
- Stochastic differential equations
- Reverse diffusion
- Score matching
- Langevin dynamics
- Fokker-Planck equations

### Applications
Image generation · Video generation

---

## 23. Information Geometry

### Topics
- Fisher Information
- Natural gradients
- Statistical manifolds

### Applications
Advanced optimization · Theoretical ML

---

## 24. Theoretical Computer Science

### Topics
- Computational complexity
- VC Dimension
- PAC Learning
- Learning theory
- Approximation algorithms

### Applications
Understanding model generalization

---

## 25. Frontier AI Research Mathematics

Used in papers from OpenAI, Anthropic, Google DeepMind, and Meta AI:

| Topic | Rarity |
|---|---|
| Random Matrix Theory | Common |
| Spectral Theory | Common |
| Category Theory | Common |
| Topology | Common |
| Optimal Transport | Common |
| Wasserstein Geometry | Common |
| Causal Inference | Common |
| Statistical Physics | Common |
| Mean Field Theory | Common |
| Dynamical Systems | Common |
| Knot Theory | Rare |
| Algebraic Geometry | Rare |
| Homotopy Theory | Research |
