# Low-N Protein Engineering
This repository contains a complete, open-source, end-to-end re-implementation of the Church Lab's eUniRep in silico protein engineering pipeline as presented in Biswas et al. Details on our implementation can be read [here](https://www.authorea.com/users/320912/articles/472051-new-evaluating-eunirep-and-other-protein-feature-representations-for-in-silico-directed-evolution), with the supplementary information [here](https://github.com/ivanjayapurna/low-n-protein-engineering/blob/master/paper/Supplementary%20Information%20-%20Evaluating%20eUniRep%20and%20other%20protein%20feature%20representations%20for%20in%20silico%20directed%20evolution.pdf). The original Church lab paper can be read [here](https://www.biorxiv.org/content/10.1101/2020.01.23.917682v1), with their repository [here](https://github.com/churchlab/UniRep). The JAX-unirep re-implementation we use in our implementation can be found [here](https://github.com/ElArkk/jax-unirep).

## How to use:
Each in silico step in the protein engineering pipeline has a jupyter notebook that will execute that step as well as an individual README file. The pipeline steps have been broken down as follows:

1. Training UniRep: either use the weights provided by the [Church lab](https://github.com/churchlab/UniRep) or use the JAX-unirep reimplementation to re-train from scratch, which is well documented [here](https://github.com/ElArkk/jax-unirep)
2. Generate input file of characterized mutants: [seq_mutator](https://github.com/ivanjayapurna/low-n-protein-engineering/tree/master/seq_mutator)
3. Curating pre-training set for evotuning: [pre-evotuning](https://github.com/ivanjayapurna/low-n-protein-engineering/tree/master/pre-evotuning)
4. Evotuning: we pushed an [example script](https://github.com/ElArkk/jax-unirep/blob/master/examples/evotuning.py) to the jax-unirep repo.
5. Top model selection and hyperparamter tuning: [top-model](https://github.com/ivanjayapurna/low-n-protein-engineering/tree/master/top-model)
6. Markov Chain Monte Carlo (MCMC) directed evolution: [directed-evo](https://github.com/ivanjayapurna/low-n-protein-engineering/tree/master/directed-evo)
7. Additional: scripts to do further analysis such as PCA and epistasis evaluation: [analysis](https://github.com/ivanjayapurna/low-n-protein-engineering/tree/master/analysis)

If you want to request any modifications / additions or want to collaborate feel free to start an issue / PR!

## License:
All the model weights are licensed under the terms of Creative Commons Attribution-NonCommercial 4.0 International License. To view a copy of this license, visit http://creativecommons.org/licenses/by-nc/4.0/ or send a letter to Creative Commons, PO Box 1866, Mountain View, CA 94042, USA.

Otherwise the code in this repository is licensed under the terms of GPL v3.
