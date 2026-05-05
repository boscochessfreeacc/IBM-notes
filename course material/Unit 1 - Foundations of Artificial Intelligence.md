v # Unit 1 - Foundations of Artificial Intelligence

## Evolution of AI Systems

### From rule-based to learning systems

Classical AI systems (often called **symbolic AI**) relied on explicit rule encoding. These systems operate on deterministic logic:

- A rule base ( $R = {r_1, r_2, ..., r_n}$ )
- Each rule maps conditions → actions

Formally:  
$$
[  
y = f(x) \quad \text{where } f \text{ is explicitly defined by humans}  
]
$$
Limitations:
- Combinatorial explosion of rules
- Inability to generalize beyond encoded conditions
- Fragility to noise or unseen inputs

Machine Learning replaces explicit rule construction with **statistical function approximation**:
$$
[  
\hat{y} = f_\theta(x)  
]
$$
Where:
- ( $\theta$ ) = parameters learned from data
- ( $f_\theta$ ) is not manually defined but optimized

Learning objective:  
$$
[  
\theta^* = \arg\min_\theta \mathcal{L}(f_\theta(x), y)  
]
$$
This shift transforms programming into **optimization over data distributions**.

---
## Core Learning Paradigms

### Supervised learning

Supervised learning operates on labeled datasets:
$$
[  
D = {(x_i, y_i)}_{i=1}^N  
]
$$
Goal: 
$$
[  
f_\theta(x) \rightarrow y  
]
$$

Optimization:  
$$
[  
\min_\theta \frac{1}{N} \sum_{i=1}^{N} \mathcal{L}(f_\theta(x_i), y_i)  
]
$$
Common loss functions:
- Classification → Cross-entropy
- Regression → Mean Squared Error

Feature learning:
- Model extracts discriminative features ( \phi(x) )
- Decision boundary learned in feature space

Generalization:
- Performance depends on ability to minimize empirical risk while controlling overfitting

Key properties:
- Requires labeled data
- Strong inductive bias from training distribution

---
### Unsupervised learning

Dataset:  
$$
[  
D = {x_i}_{i=1}^N  
]
$$

Objective:
- Discover latent structure without labels

Clustering formulation:  
$$
[  
\min \sum_{i=1}^{N} |x_i - \mu_{c_i}|^2  
]
$$

Where:
- ( $\mu_{c_i}$ ) = centroid of cluster assignment

Latent variable models:  
$$
[  
p(x) = \sum_z p(x|z)p(z)  
]
$$

Key mechanisms:
- Similarity metrics (Euclidean, cosine)
- Density estimation
- Dimensionality reduction (PCA)

Interpretation:

> System builds its own representation space and partitions data accordingly

Limitations:
- No explicit objective tied to human-defined labels
- Ambiguity in cluster interpretation

---
### Reinforcement learning

Formalized as a **Markov Decision Process (MDP)**:
$$
[  
(S, A, P, R, \gamma)  
]
$$

Where:
- ( $S$ ): states
- ( $A$ ): actions
- ( $P(s'|s,a)$ ): transition probabilities
- ( $R(s,a)$ ): reward function
- ( $\gamma$ ): discount factor

Objective: 
$$
[  
\max_\pi \mathbb{E}\left[\sum_{t=0}^{\infty} \gamma^t R_t\right]  
]
$$

Policy:  
$$
[  
\pi(a|s)  
]
$$

Value function:  
$$
[  
V^\pi(s) = \mathbb{E}[ \text{future reward} ]  
]
$$

Learning methods:
- Q-learning
- Policy gradients

Exploration vs exploitation:
- Balance between trying new actions and maximizing known rewards

---
## Neural Networks and Deep Learning

### Network structure

A neural network is a composition of functions:
$$
[  
f(x) = f_L(f_{L-1}(...f_1(x)))  
]
$$
Each layer:  
$$[  
h^{(l)} = \sigma(W^{(l)} h^{(l-1)} + b^{(l)})  
]$$

Where:
- ( $W$ ): weights
- ( $b$ ): bias
- ( $\sigma$ ): activation function

Depth:
- Number of layers ( L )
- Enables hierarchical representation learning

---
### Neurons and activation functions

Neuron computation:  
$$[  
z = \sum w_i x_i + b  
]$$

Activation:  
$$[  
a = \sigma(z)  
]$$

Common activation functions:
- ReLU: ( $\max(0, x)$ )
- Sigmoid: ( $\frac{1}{1 + e^{-x}}$ )
- $Tanh$

Role:
- Introduce non-linearity
- Allow network to approximate complex functions

Universal Approximation:
- Neural networks can approximate any continuous function given sufficient capacity
- 
---
### Feature extraction

Feature hierarchy:
- Layer 1 → edges
- Layer 2 → textures
- Layer 3 → shapes
- Layer N → objects

Representation learning:  
$$[  
\phi(x) = h^{(L-1)}  
]$$

Deep networks transform raw input into **high-level abstractions**

This reduces dependence on manual feature engineering.

---
## Computer Vision and Generative AI

### Shape recognition classification generation

Computer vision pipeline:
1. Input:  $$[  
    X \in \mathbb{R}^{H \times W \times C}  
    ]$$
2. Convolution:  $$[  
    (X * K)  
    ]$$
3. Feature maps:
    - Detect edges, gradients, textures
4. Classification:  $$[  
    \hat{y} = \text{Softmax}(f(X))  
    ]$$
CNN properties:
- Spatial locality
- Weight sharing
- Translation invariance

---
### Image generation

Generative models learn data distribution:
$$[  
p(x)  
]$$

Approaches:
- GANs:  $$[  
    \min_G \max_D V(D,G)  
    ]$$
- Diffusion models:
    - Add noise → learn reverse process
- Variational Autoencoders:  $$[  
    z \sim \mathcal{N}(0, I)  
    ]$$
Key idea:

> Generate samples that approximate training distribution

---
## AI in real-world applications

### Daily integration

AI systems operate as:$$
[  
f(x_{user}) \rightarrow action  
]$$
Examples:
- Recommendation systems:  $$
    [  
    \hat{r}_{ui} = u^T v_i  
    ]$$
- Speech recognition:  $$
    [  
    P(text | audio)  
    ]$$
- Smart systems:
    - Predict next state from historical data

---
### Predictive and generative systems

Predictive:  $$
[  
y = f(x)  
]$$
Generative:  $$
[  
x \sim p(x)  
]$$
Differences

|Type|Goal|
|---|---|
|Predictive|Estimate output|
|Generative|Model data distribution|

Applications:
- Autonomous systems
- Fraud detection
- Content generation
- Scientific discovery

---
## Final synthesis

All systems can be abstracted as:$$

[  
\text{Input} \rightarrow \text{Representation} \rightarrow \text{Optimization} \rightarrow \text{Output}  
]$$
This is the unifying computational model across:
- Supervised learning
- Unsupervised learning
- Reinforcement learning
- Neural networks
- Generative systems

Understanding this abstraction is essential before moving into implementation-level detail.