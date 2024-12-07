# Chain or Channel? Payment Optimization with Heterogeneous Flow

This repository contains the code used to generate the figures and examples for the paper *"Chain or Channel? Payment Optimization with Heterogeneous Flow"* by Paolo Guasoni and Nazem Khan, which can be accessed [here](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=5046421).

## Figures

Each notebook in this directory provides the code for generating the corresponding figure in our paper.

Start by reading [General Method](GeneralMethod.ipynb). This notebook describes our approach for computing the optimal channel deposits and determining the optimal policy for a general transaction stream with continuously distributed payments. Excluding [Figure 2](figures/figure2.ipynb), this is the only prerequisite required for running and understanding the code in the notebooks located in the [figures](figures) directory. To understand and run the code in [Figure 2](figures/figure2.ipynb), one must also read [Evolution of Channel Balance](EvolutionOfChannelBalance.ipynb).

## Examples

The notebooks in the [examples](examples) directory adapt the [General Method](GeneralMethod.ipynb). Each one provides the code for generating the corresponding example in our paper.
