# Chain or Channel? Payment Optimization with Heterogeneous Flow

This repository contains the code used to generate the figures and examples for the paper "Chain or Channel? Payment Optimization with Heterogeneous Flow" by Paolo Guasoni and Nazem Khan (2024). To fully understand it, you should be familiar with the notation and jargon in the aforementioned paper. 

## Requirements

To run the code, you need the following Python libraries:

- numpy
- scipy
- matplotlib

## General Example

### Inputs

- Cost of an on-chain transaction $C > 0$
- Channel reset cost $D > 0$
- Discount factor $\alpha \in (0,1)$ 
- Payment size probability density function $g:\mathbb{R} \to \mathbb{R}_+$
- Fine-tuning parameter $n \in \mathbb{N}$

### Outputs 

- Optimal channel deposits $l_A^{\*}$ and $l_B^{\*}$
- Optimal policy $f^{\*}$

There are three steps in getting the outputs from the inputs. First you need to be able to compute the expected cost in transactions $T(0  |  l_A, l_B)$ for a fixed pair of channel deposits $l_A, l_B \in R_n := \{ \tfrac{k}{2n} : 0 \leq k \leq \tfrac{2n\alpha C}{1-\alpha} \textnormal{ and } k \in \mathbb{N} \}$. You then minimize the function $\mathbb{R}^2 \ni (l_A, l_B) \mapsto l_A + l_B + T(0  |  l_A, l_B)$ in order to find optimal channel deposits $l_A^{\*}$ and $l_B^{\*}$. Finally, you use $T(\cdot  |  l_A, l_B)$ to compute the optimal policy $f^{\*}$.

### Step 1 Computing $T(0 | l_A, l_B)$

![Quadratic Formula](images/equation.png)
















