# forex-density-estimation
## 1. K-Means Clustering

- Partitions data into K clusters by minimizing within-cluster squared distances (SSE / inertia).
- Model selection based on Silhouette Score.
- Used to identify structural groupings in return space.

---

## 2. Gaussian Mixture Model (GMM)

Models data as a mixture of Gaussian distributions:

p(x) = sum over k=1 to K of [ pi_k * N(x | mu_k, Sigma_k) ]

Where:
- pi_k = mixture weight of component k
- mu_k = mean of component k
- Sigma_k = covariance matrix of component k
- N(x | mu_k, Sigma_k) = Gaussian distribution

- Parameters are estimated using the Expectation–Maximization (EM) algorithm.
- Model selection is performed using AIC and BIC.
- Provides probabilistic cluster membership and full density estimation.

---

## Key Concepts Explained

Clustering  
Partitioning data into groups based on similarity.

Density Estimation  
Modeling the probability distribution that generates the data.

EM Algorithm (Expectation–Maximization)  

- E-step: Estimate component membership probabilities.
- M-step: Update Gaussian parameters (means, covariances, weights).
- Repeat until convergence.

---

## Results Discussion

Results indicate that FX log-returns are better described by multiple Gaussian components rather than a single normal distribution.

The presence of multiple mixture components suggests regime-like behavior in return dynamics (for example, lower-volatility vs higher-volatility states).

GMM provides a richer probabilistic interpretation compared to K-Means, which only performs geometric partitioning.
