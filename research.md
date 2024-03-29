---
layout: page
title: Research
---

## Table of Contents
{:.no_toc}
* this unordered seed list will be replaced by toc as unordered list
{:toc}

See also my [Google Scholar](https://scholar.google.de/citations?user=2HpXCQ0AAAAJ) or [Orcid](https://orcid.org/0000-0003-2766-3982) pages. My dissertation is published [here](https://kups.ub.uni-koeln.de/64465/).

## Dynamics of Random Networks

The structure of cortical networks of mammals is only known on a statistical level. Thus, they are typically modeled as random networks with the appropriate connectivity statistics. Conveniently, quite a bit about the dynamics of random networks can be deduced using tools from statistical physics.

For random networks, one can start from the N-dimensional, coupled system of differential equations which describe the dynamics of the network and arrive, through a series of systematic approximations, at an effective lower-dimensional description. This approach, called Dynamic Mean-Field Theory (DMFT) in the pioneering work by [Sompolinsky, Crisanti, and Sommers](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.61.259), relies heavily on techniques from field theory (see the lecture notes [Helias & Dahmen 2020](https://www.springer.com/de/book/9783030464431) for an introduction). Albeit mathematically involved, the final result is intuitive: the recurrent input to a neuron is approximated as a Gaussian process with self-consistent statistics.

#### Large-Deviation Approach to Random Recurrent Neuronal Networks: Parameter Inference and Fluctuation-Induced Transitions

<img src="assets/png/PRL21_Fig3.png" alt="fluctuations" width="350" border="2px solid #555"/>
<img src="assets/png/PRL21_Fig2.png" alt="connectivity inference" width="350" border="2px solid #555"/>

* **Publication**: A. van Meegen, T. Kühn, and M. Helias, [Phys. Rev. Lett. **127**, 158302 (2021)](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.127.158302)
* **Poster**: *COSYNE 2020*, Denver, United States ([pdf](assets/pdf/COSYNE20_pathdeviation.pdf))

A particular realization of a random network leads, through its dynamics, to particular network-averaged observables (think correlation functions). Hence, the ensemble of random networks gives rise to a distribution of observables. We calculated the latter distribution to leading order using field theory and large deviations theory, building on the pioneering work of [Ben-Arous and Guionnet](https://link.springer.com/article/10.1007/BF01198846).

With the distribution of observables at hand, we attacked the inverse problem of determining the statistics of the random network from its dynamics. From this point of view, the distribution is the likelihood of the connectivity statistics. Employing maximum likelihood enabled us to infer the connectivity statistics directly from network-averaged power spectra.

Complementary, the distribution of observables also enabled progress on the forward problem: The maximum of the distribution corresponds to DMFT;  we used the variability about this maximum to calculate beyond-mean-field fluctuations. This lead us to a novel network state featuring two stable mean-field solutions and fluctuation-induced transitions between them.

#### Self-Consistent Correlations of Randomly Coupled Rotators in the Asynchronous State

<img src="assets/png/PRL18_Fig2.png" alt="rotator spectra" width="350" border="2px solid #555"/>
<img src="assets/png/PRL18_Fig4.png" alt="spiking spectra" width="350" border="2px solid #555"/>

* **Publication**: A. van Meegen and B. Lindner, [Phys. Rev. Lett. **121**, 258302 (2018)](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.121.258302)
* **Talk**: *CNS 2019 Main Meeting*, Barcelona, Spain ([pdf](assets/pdf/CNS19_rotators.pdf))

The dynamics of cortical networks in awake, behaving animals are typically asynchronous and irregular. We set out to find a toy model that features such an network state but is still analytically tractable. To this end, we investigated a random network of oscillatory units (rotators).

Using DMFT, we derived an ordinary differential equation determining the network-averaged correlation function. For simple interaction functions, this differential equation could be solved explicitly, leading to closed-form analytical expressions for the correlation functions and power spectra.

Deep in the mean-driven regime, spiking neurons behave similar to oscillators. Thus, we extended our theory to mimic the spike-based coupling of cortical neurons. This allowed us to determine the power spectra of a sparse, heterogeneous network of excitatory and inhibitory exponential integrate-and-fire neurons deep in the mean-driven regime.

#### Microscopic Theory of Intrinsic Timescales in Spiking Neural Networks

<img src="assets/png/PRR21_Fig5.png" alt="brunel glm" width="350" border="2px solid #555"/>
<img src="assets/png/PRR21_Fig4.png" alt="glm parameter scan" width="350" border="2px solid #555"/>

* **Publication**: A. van Meegen and S.J. van Albada, [Phys. Rev. Research **3**, 043077 (2021)](https://journals.aps.org/prresearch/abstract/10.1103/PhysRevResearch.3.043077)
* **Poster**: *CNS 2019*, Barcelona, Spain ([pdf](assets/pdf/CNS19_timescales.pdf))

Neurons communicate predominantly through spikes. How does this spike-based interaction affect the recurrent dynamics of random networks? In particular, how does it affect their temporal correlations (intrinsic timescales)? Are long intrinsic timescales possible despite the white spiking noise?

To address these questions, we built upon the recently developed model-independent DMFT by [Keup et al](https://journals.aps.org/prx/abstract/10.1103/PhysRevX.11.021064). Furthermore, we developed novel approximations and solutions to the colored noise problem - mapping temporal input correlations to temporal output correlations - for LIF and GLM neurons.

The resulting theory allows for parameter scans which revealed that there are regimes with intermediate intrinsic timescales in balanced networks of GLM neurons. Furthermore, the structure of the temporal correlations are fundamentally different in GLM and LIF networks: Longer intrinsic timescales correspond to bursty spiking for the former and to an effective refractory period for the latter.

## Bayesian Supervised Learning in Neural Networks

#### Unified Field Theoretical Approach to Deep and Recurrent Neuronal Networks

<img src="assets/png/JSTAT22_Fig1.png" alt="gp limit" width="350" border="2px solid #555"/>
<img src="assets/png/JSTAT22_Fig3.png" alt="nlo corrections" width="350" border="2px solid #555"/>

* **Publication**: K. Segadlo, B. Epping, A. van Meegen, D. Dahmen, M. Krämer, and M. Helias, [J. Stat. Mech., 103401 (2022)](https://iopscience.iop.org/article/10.1088/1742-5468/ac8e57)

Feedforward and recurrent neuronal networks differ fundamentally due to weight sharing: recurrent networks employ the same weights in every time step while feedforward networks use a new set of weights in every layer. How does this difference affect the mapping from inputs to outputs?

To be able to compare the two network architectures, we developed a unified description based on tools from statistical field theory. We start the comparison in the infinite width / size limit. Already to leading order differences emerge: weight sharing leads to correlations between time steps in recurrent networks. Curiously, these correlations do not affect the prediction if it is based on a single time point.

To uncover differences relevant for the prediction, we calculated finite-size corrections. These next-to-leading-order corrections reveal a clear difference between the architectures: weight sharing in recurrent networks allows fluctuations to build up, leading to larger overall corrections.

<!-- ## Large-Scale Simulations -->
