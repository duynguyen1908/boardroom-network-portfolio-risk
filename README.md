# Boardroom Network & Portfolio Risk

*Team project · University of Adelaide · Nov 2026*

**Question:** Do companies with the most connected boards make better investments?

**What we did** (team of 3)
- **I** built a network of the 500 largest US firms linked by shared directors, and ranked them by influence
- **We** compared two portfolios (most connected vs next tier) under the same risk limit
- **We** stress-tested both with Monte Carlo simulation to measure downside risk
- **We** checked that the result wasn't just firm size

**Methods**
- **Network analysis:** firm-to-firm graph from shared directors; ranked by **eigenvector centrality**, which rewards links to well-connected firms, with weighted centrality as a robustness check
- **Mean-variance optimisation (SLSQP):** long-only, fully invested, volatility cap. The cap's **feasibility was tested first** (minimum achievable volatility)
- **Monte Carlo VaR:** 10,000 multivariate-normal scenarios for 95% and 99% one-day Value at Risk
- **Robustness:** Student's and Welch's t-tests on firm size, with IQR outlier removal
- **Text analytics:** stemming and keyword dictionaries on director role titles, with a dictionary sensitivity check

**Result:** The most connected boards did **not** win: the next tier returned **24.17% vs 22.53%** with less downside risk. The original risk limit also turned out to be impossible to meet in 2020.

**Tools:** Python (pandas, NetworkX, SciPy)

---
📂 **Full notes, code and results are available on request.** Message me on [LinkedIn](https://www.linkedin.com/in/duynguyen1908/) and I can share access to the private project repo.
