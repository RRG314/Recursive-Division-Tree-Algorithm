# Recursive-Division-Tree-A-Log-Log-Algorithm-for-Integer-Depth
Recursive Division Tree (RDT): a log–log integer-depth algorithm showing Θ(log log n) growth and structure across primes, perfect numbers, and additive partitions.
 Recursive Division Tree (RDT) Algorithm

Author: Steven Reid  
ORCID: [0009-0003-9132-3410](https://orcid.org/0009-0003-9132-3410)  
DOI: [10.5281/zenodo.17487651](https://doi.org/10.5281/zenodo.17487651)  
Published: October 30, 2025  
License: MIT (code) and CC BY 4.0 (paper and figures)



## Overview

The Recursive Division Tree (RDT) algorithm is a mathematical process for measuring the logarithmic height of positive integers.  
For any integer \( n \ge 2 \), it recursively divides by logarithm-based factors, producing a depth value that grows on the order of Θ(log log n).  
This ultra-slow growth defines a new invariant that is independent of prime factorization yet reveals consistent structures across primes, perfect numbers, and additive partitions.

This repository contains:
- The complete LaTeX preprint and figures  
- The Python implementation (`rdt.py`)  
- Benchmark data, plots, and reproducibility scripts  



## Mathematical Definition

For parameter \( \alpha = 1.5 \):

\[
x_{i+1} = \left\lfloor \frac{x_i}{\max(2,(\ln x_i)^{1.5})} \right\rfloor, \quad x_0 = n.
\]
Terminate when \( x_k \le 1 \); define \( RDT(n) = k \).

Empirical asymptotic law:
\[
RDT(n) \sim c\,\ln\ln n, \qquad c \approx 2.24 \pm 0.22.
\]




Key Results

Property	Observation

Asymptotic Growth	Θ(log log n)
Empirical Constant	c ≈ 2.24 ± 0.22
Factorization Independence	RDT depends only on magnitude
Twin Prime Property	Approximately 95% of twin primes share equal depth
Perfect and Mersenne Numbers	Linear fits to ln ln n
Goldbach Inequality	RDT(p) + RDT(q) ≥ RDT(p + q) (empirically strict)
Runtime	Approximately 4×10⁻⁵ seconds per evaluation


Benchmark data and figures are provided in the benchmarks directory.



Citation

Please cite this work as:

Steven Reid (2025). Recursive Division Tree: A Log-Log Algorithm for Integer Depth. Zenodo.
DOI: 10.5281/zenodo.17487651

BibTeX entry:

@article{reid2025rdt,
  title     = {Recursive Division Tree: A Log-Log Algorithm for Integer Depth},
  author    = {Reid, Steven},
  year      = {2025},
  doi       = {10.5281/zenodo.17487651},
  publisher = {Zenodo},
  url       = {https://doi.org/10.5281/zenodo.17487651}
}

Acknowledgments
All concepts, mathematical formulations, and empirical studies in this work were conceived and conducted by the author, Steven Reid. 
Artificial intelligence tools were used to assist with documentation, LaTeX editing, and computational organization, 
but the underlying theory, algorithms, and results presented are original contributions by the author. 
This research was performed independently, without institutional affiliation or external financial support.




License

Code: MIT License

Paper and Figures: Creative Commons Attribution 4.0 International (CC BY 4.0)




"The Recursive Division Tree demonstrates how logarithmic structure reveals hidden order in the integers."
Steven Reid (2025)
