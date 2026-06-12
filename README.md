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

### 🛠 Project Ideas
1. **Word Embedding Explorer** — Load GloVe/Word2Vec embeddings, visualize vector arithmetic (`king - man + woman`), project to 2D with PCA, and plot clusters interactively with Plotly.
2. **SVD Image Compressor** — Decompose images using SVD and build a slider UI showing rank-k approximations vs file size vs visual quality loss in real time.
3. **LoRA Simulator** — Implement LoRA weight decomposition from scratch on a small linear layer; visualize how rank affects parameter count and approximation error.
4. **Attention Matrix Visualizer** — Build a heatmap renderer that shows the full $QK^T / \sqrt{d_k}$ matrix for a toy sentence — before and after softmax.
5. **Eigenface Face Recognizer** — Apply PCA to a face dataset (LFW), reconstruct faces from top-k eigenfaces, and plot how reconstruction error changes with k.
6. **Matrix Factorization Recommender** — Implement collaborative filtering with gradient descent on a movie-rating matrix; plot loss curves and compare with SVD-based factorization.

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

### 🛠 Project Ideas
1. **Backprop from Scratch** — Implement a 2-layer MLP with hand-coded forward pass, chain-rule backpropagation, and gradient descent — no PyTorch autograd.
2. **Gradient Flow Visualizer** — Animate gradient vectors on a 3D loss surface for simple functions; show how different learning rates cause divergence or slow convergence.
3. **Jacobian Explorer** — Compute and visualize Jacobian matrices for small neural networks; show how they change during training.
4. **Taylor Approximation Playground** — Interactive web app that shows nth-order Taylor expansions of `sin`, `exp`, and `log` converging to the true function as n grows.
5. **Hessian Landscape Analyzer** — Compute eigenvalues of the Hessian of a small network's loss; visualize sharp vs flat minima and their connection to generalization.
6. **Automatic Differentiation Engine** — Build a miniature autograd library (like Andrej Karpathy's `micrograd`) supporting `+`, `*`, `relu`, `tanh` with a computation graph renderer.

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

### 🛠 Project Ideas
1. **LLM Token Probability Inspector** — Hook into a model's logits (via Hugging Face) and visualize the full probability distribution over the vocabulary at each generation step.
2. **Markov Chain Text Generator** — Build an n-gram Markov chain on any text corpus; animate state transitions and compare outputs at different orders (n=1,2,3,4).
3. **Bayesian Spam Classifier** — Implement Naive Bayes from scratch on an email dataset; plot posterior probability updates as new words are observed.
4. **Monte Carlo Pi Estimator** — Visualize the geometric Monte Carlo method for estimating π, showing convergence rate as sample count grows.
5. **Distribution Playground** — Interactive dashboard where changing parameters updates live plots for Gaussian, Poisson, Beta, and Exponential distributions side by side.
6. **Central Limit Theorem Animator** — Sample from any distribution (uniform, exponential, skewed) repeatedly and animate how the distribution of sample means converges to Gaussian.

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

### 🛠 Project Ideas
1. **Bias-Variance Decomposition Dashboard** — Fit polynomial regressors of varying degree to noisy data; plot bias², variance, and total error decomposition as degree increases.
2. **A/B Test Simulator** — Simulate online A/B tests with configurable effect sizes; show p-value evolution over time and false positive rate under repeated peeking.
3. **MLE vs MAP Visualizer** — Fit a Gaussian to data using both MLE and MAP; animate how the MAP estimate shifts with different prior strengths.
4. **Bootstrap Confidence Interval Explorer** — Apply bootstrap resampling to any small dataset; compare bootstrap CIs vs theoretical CIs for different statistics.
5. **Regression Diagnostics Tool** — Build a full residual analysis dashboard (Q-Q plot, heteroscedasticity check, Cook's distance) for linear regression outputs.
6. **Model Calibration Plotter** — Plot reliability diagrams (confidence vs actual accuracy) for classifiers; implement Platt scaling and isotonic regression to recalibrate.

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

### 🛠 Project Ideas
1. **LLM Loss Landscape** — Track cross-entropy loss per token during GPT-2 inference on different text types (code, poetry, random); visualize which tokens are hardest to predict.
2. **KL Divergence Animator** — Animate KL divergence between a fixed target distribution and a learnable Gaussian as its parameters optimize toward the target.
3. **Entropy-Based Text Analyzer** — Compute and compare per-character and per-word entropy of different languages, code, and random text; visualize information density.
4. **Information Bottleneck Visualizer** — Implement the IB method on a small classification network; plot the information plane (I(X;T) vs I(T;Y)) across training epochs.
5. **Huffman Coding Demonstrator** — Build an interactive Huffman tree builder that shows compression ratio vs entropy for any input text in real time.
6. **Mutual Information Feature Selector** — Compute MI between each feature and the target in a tabular dataset; compare MI-based selection vs correlation-based selection visually.

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

### 🛠 Project Ideas
1. **Optimizer Race Visualizer** — Animate SGD, Momentum, RMSProp, and Adam simultaneously on the same 2D loss surface (Rosenbrock, Beale, saddle point); compare convergence paths.
2. **Learning Rate Finder** — Implement the LR range test (Smith 2017); plot loss vs learning rate and highlight the optimal range automatically.
3. **Loss Surface Explorer** — Interpolate between two trained model checkpoints and visualize the 1D or 2D loss landscape slice between them.
4. **Lagrange Multiplier Solver** — Interactive tool that visualizes constrained optimization problems; animate the constraint surface and gradient alignment at the optimum.
5. **Adam vs SGD Generalization Study** — Train the same network with Adam and SGD, compare training/validation curves, and visualize sharpness of found minima using Hessian eigenvalues.
6. **Second-Order Optimizer from Scratch** — Implement Newton's method and L-BFGS on small problems; compare convergence rate with gradient descent in iterations vs wall-clock time.

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

### 🛠 Project Ideas
1. **Numerical vs Analytical Gradient Checker** — Implement gradient checking (finite differences) and visualize the error gap between numerical and autograd gradients across network layers.
2. **Iterative Solver Comparator** — Compare Jacobi, Gauss-Seidel, and Conjugate Gradient on large sparse linear systems; animate residual decay per iteration.
3. **Root Finding Visualizer** — Animate bisection, Newton-Raphson, and secant methods converging on the same function; plot error per step on a log scale.
4. **Floating Point Error Propagator** — Visualize how FP16 vs BF16 vs FP32 accumulate rounding errors during deep network forward passes.
5. **Numerical Integration Comparator** — Implement and compare Riemann, Trapezoidal, Simpson's, and Gaussian quadrature; plot error vs number of evaluation points.

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

### 🛠 Project Ideas
1. **Tokenization Combinatorics Explorer** — Visualize how BPE tokenization merges character pairs; plot vocabulary growth as a function of merge operations and corpus size.
2. **SAT Solver Visualizer** — Implement DPLL or CDCL and animate the search tree as it solves Boolean satisfiability problems of increasing complexity.
3. **Recurrence Relation Solver** — Build a tool that takes a recurrence relation, plots its growth, and compares it to common complexity classes (O(n), O(n log n), O(2^n)).
4. **Combinatorial Reasoning Benchmark** — Create a dataset of combinatorics problems and probe LLM accuracy; compare to exact computation and visualize failure modes.

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

### 🛠 Project Ideas
1. **GNN from Scratch** — Implement a Graph Convolutional Network on Cora/Citeseer; visualize node embeddings with UMAP before and after training, colored by class.
2. **Knowledge Graph Builder** — Extract entities and relations from text using an LLM; render the resulting knowledge graph interactively with D3.js or Pyvis.
3. **Agent Workflow DAG Visualizer** — Parse LangChain/LangGraph agent execution traces and render the DAG of tool calls, decisions, and results with timing annotations.
4. **Spectral Graph Clustering** — Implement spectral clustering using graph Laplacian eigenvectors; animate how the Fiedler vector partitions graph communities.
5. **PageRank Visualizer** — Animate the PageRank power iteration on a small web graph; show how authority scores converge across iterations.

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

### 🛠 Project Ideas
1. **Neural ODE Classifier** — Implement a Neural ODE (torchdiffeq) on a 2D classification problem; animate the continuous-depth transformation of the input point cloud.
2. **Diffusion Forward Process Animator** — Visualize the forward noise schedule of a DDPM; animate how a clean image degrades to Gaussian noise across 1000 timesteps.
3. **Lorenz Attractor Explorer** — Simulate the Lorenz system and visualize chaotic trajectories; show sensitive dependence on initial conditions interactively.
4. **Phase Portrait Plotter** — Build an interactive ODE phase portrait tool; plot vector fields and trajectories for common dynamical systems (pendulum, predator-prey, Van der Pol).

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

### 🛠 Project Ideas
1. **Kernel SVM Visualizer** — Implement SVM with RBF, polynomial, and linear kernels; animate the decision boundary and support vectors in 2D as the kernel parameters change.
2. **Reproducing Kernel Hilbert Space (RKHS) Demo** — Visualize function regression in RKHS; show how the kernel determines the smoothness of the fitted function.
3. **Neural Tangent Kernel Explorer** — Compute the NTK for small networks analytically; compare NTK predictions vs actual gradient descent dynamics on simple regression tasks.
4. **Operator Spectrum Visualizer** — Compute and visualize the spectrum of common linear operators (Laplacian, convolution kernels) and their effect on input signals.

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

### 🛠 Project Ideas
1. **Riemann vs Lebesgue Integration Visualizer** — Animate the difference between Riemann (slice vertically) and Lebesgue (slice horizontally) integration on discontinuous functions.
2. **Probability Space Simulator** — Build an interactive tool that lets users define sample spaces, events, and measures; verify sigma-algebra axioms visually.
3. **Measure-Theoretic Probability Bridge** — Show how discrete probability distributions, PDFs, and mixed distributions are all unified under measure theory with visual examples.

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

### 🛠 Project Ideas
1. **Posterior Update Animator** — Animate Bayesian posterior updates for a Beta-Binomial model as coin flip data arrives sequentially; show prior → likelihood → posterior.
2. **MCMC Sampler Comparator** — Implement Metropolis-Hastings, Gibbs, and Hamiltonian Monte Carlo; visualize sample trajectories on a 2D posterior and compare mixing rates.
3. **Variational Inference from Scratch** — Implement mean-field VI on a Gaussian mixture model; animate the ELBO optimization and compare the VI approximation to the true posterior.
4. **Bayesian Neural Network Uncertainty** — Train a BNN (using PyMC or Pyro) on a small regression task; plot predictive mean ± uncertainty bands and compare to a standard NN.
5. **Prior Sensitivity Analyzer** — Show how different priors (uninformative, weakly informative, strong) affect the posterior on the same dataset; visualize the prior-likelihood-posterior triad.

---

## 14. Convex Analysis

### Topics
- Convex sets and functions
- Fenchel duality
- Subgradients
- KKT conditions

### Applications
Optimization theory

### 🛠 Project Ideas
1. **Convexity Checker and Visualizer** — Build a tool that takes a 2D function and checks convexity numerically; visualize the epigraph, supporting hyperplanes, and subgradients.
2. **KKT Conditions Visualizer** — Animate KKT conditions for constrained 2D optimization problems; show primal feasibility, dual feasibility, and complementary slackness geometrically.
3. **Fenchel Duality Explorer** — Plot a convex function and its Fenchel conjugate side by side; animate the Legendre-Fenchel transform geometrically.
4. **Proximal Operator Playground** — Implement proximal operators for L1, L2, and nuclear norms; visualize how they shrink or project input vectors.

---

## 15. Stochastic Processes

### Topics
- Markov processes
- Hidden Markov Models (HMMs)
- Brownian motion
- Martingales

### Applications
Reinforcement learning · Sequential modeling

### 🛠 Project Ideas
1. **Brownian Motion Simulator** — Simulate and animate 2D Brownian motion paths; show how variance grows linearly with time and compare to fractional Brownian motion.
2. **HMM Part-of-Speech Tagger** — Build an HMM from scratch using the Viterbi algorithm; visualize the trellis diagram and state transition probabilities on a sentence.
3. **Markov Reward Process Visualizer** — Animate value function convergence under Bellman backup on a small grid MDP; show how values propagate from terminal states.
4. **Martingale Betting Strategy Simulator** — Simulate the Martingale, Kelly criterion, and fixed-fraction betting strategies; plot wealth trajectories and ruin probability over many trials.

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

### 🛠 Project Ideas
1. **Nash Equilibrium Finder** — Implement support enumeration to find Nash equilibria in 2-player normal form games; visualize best-response correspondences and equilibrium points.
2. **Multi-Agent RL Arena** — Train two RL agents in a zero-sum grid game (e.g., Blotto, Pursuit-Evasion) using self-play; plot Elo ratings and strategy evolution over training.
3. **Mechanism Design Simulator** — Simulate Vickrey (second-price) vs first-price auctions with different bidder types; plot revenue and efficiency outcomes across many trials.
4. **RLHF Reward Hacking Visualizer** — Build a toy reward model and show how a policy can exploit Goodhart's Law — optimizing the proxy while diverging from true human preferences.

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

### 🛠 Project Ideas
1. **PID Controller Tuner** — Implement a PID controller on a simulated cart-pole; animate the system response and show how changing K_p, K_i, K_d affects stability and overshoot.
2. **LQR vs RL Agent Comparison** — Control a linear dynamical system with both an LQR optimal controller and a trained PPO agent; compare trajectory efficiency and robustness to noise.
3. **Dynamic Programming Value Iteration** — Implement value iteration on a continuous control problem (e.g., mountain car); visualize the value function surface and greedy policy as they converge.
4. **Model Predictive Control (MPC) Demo** — Implement MPC on a 2D navigation task; animate the receding horizon plan and compare to a reactive policy.

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

### 🛠 Project Ideas
1. **Bellman Backup Visualizer** — Animate synchronous and asynchronous Bellman backups on a gridworld; show value function convergence iteration by iteration with a color heatmap.
2. **Q-Learning vs SARSA on Cliff Walking** — Implement both algorithms; animate their learned paths and plot Q-value surface evolution — highlighting on-policy vs off-policy differences.
3. **Policy Gradient Ascent Visualizer** — Implement REINFORCE on CartPole; plot policy entropy, average return, and gradient variance across training; show variance reduction with baselines.
4. **Advantage Function Analyzer** — Train an Actor-Critic on a continuous control task; plot the advantage function A(s,a) and show its role in reducing policy gradient variance.
5. **Discount Factor Sensitivity Study** — Train the same agent with γ = 0.9, 0.95, 0.99, 1.0; visualize how planning horizon depth affects policy behavior and value estimates.
6. **Reward Shaping Experiment** — Compare sparse vs dense vs potential-based reward shaping on a maze; animate exploration patterns and plot sample efficiency curves.

---

## 19. Signal Processing

### Topics
- Fourier Transform and FFT
- Wavelets
- Convolution
- Spectral analysis

### Applications
Audio AI · Speech models · Time-series AI

### 🛠 Project Ideas
1. **Spectrogram Explorer** — Build a live audio visualizer that computes and displays FFT, mel-spectrogram, and MFCC for microphone input or uploaded audio files.
2. **CNN as Signal Filter Visualizer** — Visualize learned CNN kernels as frequency filters; apply them to audio signals and show which frequencies each filter passes or blocks.
3. **Wavelet vs Fourier Comparator** — Decompose a non-stationary signal (chirp, speech) using both methods; animate the time-frequency representation and compare localization.
4. **Convolution Animation** — Animate 1D and 2D convolution operations (with padding, stride, dilation) step by step; show how different kernels affect signal and image outputs.

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

### 🛠 Project Ideas
1. **Embedding Space Topology Analyzer** — Project LLM embeddings (BERT, GloVe) to 2D/3D with t-SNE, UMAP, and PCA; compare manifold shapes and neighborhood preservation.
2. **Geodesic vs Euclidean Distance on Manifolds** — Simulate a Swiss Roll dataset; compare Euclidean shortest path vs geodesic (Isomap) distance for nearest neighbor retrieval.
3. **Hyperbolic Embedding Visualizer** — Embed hierarchical data (WordNet, org charts) in the Poincaré disk model; compare to Euclidean embeddings and measure distortion.
4. **t-SNE Parameter Sensitivity Study** — Run t-SNE on the same embedding dataset with varying perplexity and learning rate; animate the optimization and show how parameters change cluster shapes.

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

### 🛠 Project Ideas
1. **Attention Head Microscope** — Extract and visualize all attention heads of GPT-2 on a sentence; identify syntactic heads (subject-verb), positional heads, and rare patterns.
2. **RoPE vs Sinusoidal Positional Encoding Comparator** — Visualize attention score decay with distance for RoPE vs sinusoidal; test extrapolation to sequences longer than training length.
3. **Sparse Attention Pattern Designer** — Implement sliding window, strided, and global attention patterns; visualize their attention masks and measure speedup vs full attention.
4. **Mixture of Experts Router Visualizer** — Build a toy MoE layer and animate which experts receive which tokens; plot load balancing distributions and collapse behavior.
5. **Scaling Laws Reproducer** — Train character-level transformers at scales 1M–100M parameters on TinyShakespeare; reproduce the Chinchilla-style compute-optimal scaling curves.
6. **Flash Attention Memory Analyzer** — Profile standard attention vs Flash Attention memory usage and speed at different sequence lengths; plot the quadratic vs near-linear memory scaling.

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

### 🛠 Project Ideas
1. **DDPM Forward/Reverse Process Visualizer** — Animate the full forward noising and reverse denoising process on MNIST; plot the learned noise predictions at each timestep.
2. **Score Function Estimator** — Visualize the score function (∇ log p(x)) for 2D toy distributions; animate how a denoising network learns to approximate the score field.
3. **Noise Schedule Comparator** — Compare linear, cosine, and sigmoid noise schedules; plot signal-to-noise ratio curves and show how schedule choice affects sample quality.
4. **Langevin Dynamics Sampler** — Implement Langevin MCMC with the learned score function on a 2D distribution; animate particle trajectories converging to the target density.
5. **Classifier-Free Guidance Strength Study** — Run diffusion inference at guidance scales w=1, 3, 7, 15; show the quality-diversity tradeoff using FID and sample grids.

---

## 23. Information Geometry

### Topics
- Fisher Information
- Natural gradients
- Statistical manifolds

### Applications
Advanced optimization · Theoretical ML

### 🛠 Project Ideas
1. **Natural Gradient vs SGD Visualizer** — Compare SGD and Natural Gradient Descent on the same loss landscape; show how the Fisher metric warps the parameter space and speeds convergence.
2. **Fisher Information Matrix Heatmap** — Compute and visualize the FIM for a small Bayesian network; show which parameters carry the most information about the data.
3. **Statistical Manifold Plotter** — Plot the manifold of Gaussian distributions parameterized by (μ, σ); visualize geodesics, KL-divergence contours, and the Fisher-Rao metric.

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

### 🛠 Project Ideas
1. **VC Dimension Visualizer** — Demonstrate shattering for linear classifiers, polynomials, and neural networks on 2D point sets; animate the boundary between shatterable and non-shatterable configurations.
2. **PAC Learning Sample Complexity Calculator** — Build an interactive tool that computes required sample size given ε, δ, and VC dimension; visualize how each parameter affects the bound.
3. **Double Descent Curve Reproducer** — Train linear models and neural networks on a synthetic classification task at varying model sizes; reproduce the bias-variance-double-descent curve.
4. **Generalization Gap Tracker** — Train models with different regularization strengths; plot train/test loss gap vs model complexity and overlay the PAC-Bayes generalization bound.

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

### 🛠 Project Ideas
1. **Optimal Transport for Distribution Alignment** — Implement Sinkhorn iterations to compute Wasserstein distance between two 2D point clouds; animate the optimal transport plan and use it for domain adaptation between datasets.
2. **Random Matrix Theory for Network Initialization** — Analyze weight matrix spectra of randomly initialized networks; show how the Marchenko-Pastur law predicts bulk eigenvalue distribution and why it matters for signal propagation.
3. **Causal Inference with Do-Calculus** — Build a causal graph (DAG) over a tabular dataset; compare observational correlation vs interventional P(Y | do(X)) and visualize backdoor adjustment.
4. **Mean Field Theory for Neural Networks** — Simulate signal propagation through deep random networks; reproduce the edge-of-chaos phase diagram (ordered, chaotic, critical) as a function of weight variance.
5. **Persistent Homology for Embedding Analysis** — Compute topological features (Betti numbers, persistence diagrams) of LLM embedding spaces; compare topology across model sizes and training stages.
6. **Spectral Analysis of Trained Weights** — Plot singular value spectra of weight matrices across all layers of a trained transformer; compare to random baselines and track spectral changes during fine-tuning.
7. **Wasserstein GAN Training Dynamics** — Implement WGAN with gradient penalty; plot the Wasserstein distance estimate during training and compare stability and mode coverage vs standard GAN.
8. **Statistical Physics of Neural Scaling** — Reproduce scaling law experiments (loss vs parameters, loss vs data) on a small language model; fit power law exponents and compare to Chinchilla predictions.

---

*Last updated: 2026*
