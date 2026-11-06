# Awesome Neural Network Formal Verification [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

<p align="center">
  <img src="assets/banner.svg" alt="Awesome Neural Network Formal Verification Banner" width="100%">
</p>

<p align="center">
  <a href="https://github.com/giovanni-norbedo/awesome-nn-formal-verification/stargazers"><img src="https://img.shields.io/github/stars/giovanni-norbedo/awesome-nn-formal-verification?style=flat-square&logo=github&color=blue" alt="GitHub Stars"></a>
  <a href="https://github.com/giovanni-norbedo/awesome-nn-formal-verification/pulls"><img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square" alt="PRs Welcome"></a>
  <a href="https://creativecommons.org/publicdomain/zero/1.0/"><img src="https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg?style=flat-square" alt="License: CC0-1.0"></a>
  <a href="#contents"><img src="https://img.shields.io/badge/Curated%20Resources-30+-orange.svg?style=flat-square" alt="Curated Resources"></a>
  <a href="https://www.vnnlib.org/"><img src="https://img.shields.io/badge/Standard-VNN--LIB-purple.svg?style=flat-square" alt="VNN-LIB Standard"></a>
</p>

> A curated list of awesome tools, benchmarks, papers, and resources for the formal verification of neural networks.

Formal neural network verification is a set of techniques used to mathematically prove that a neural network satisfies specific properties, such as safety, robustness, or fairness, under all possible inputs within a given range. This is critical for deploying deep learning models in safety-critical domains like autonomous driving, aerospace, robotics, and medicine, where empirical testing is insufficient to guarantee correctness.

## Contents

- [Exact and complete solvers](#exact-and-complete-solvers)
- [Abstract interpretation and reachability](#abstract-interpretation-and-reachability)
- [Branch-and-bound and accelerated verifiers](#branch-and-bound-and-accelerated-verifiers)
- [Closed-loop and cyber-physical systems](#closed-loop-and-cyber-physical-systems)
- [Benchmarks and competitions](#benchmarks-and-competitions)
- [Literature](#literature)
  - [Surveys](#surveys)
  - [Seminal papers](#seminal-papers)
- [Community](#community)

## Exact and complete solvers

- [Marabou](https://github.com/NeuralNetworkVerification/Marabou) - An SMT-based framework for verifying deep neural networks, supporting properties specified via the VNN-LIB format.
- [MIPVerify.jl](https://github.com/vtjeng/MIPVerify.jl) - A Julia-based verification tool that formulates the neural network robustness certification problem as a mixed-integer linear programming (MILP) optimization problem.
- [Reluplex](https://github.com/guykatzz/ReluplexCav2017) - A foundational SMT-based solver algorithm designed to verify neural networks with ReLU activations by extending the Simplex method (predecessor to Marabou).
- [Venus](https://github.com/vas-group-imperial/venus) - A sound and complete MILP-based verification toolkit utilizing symbolic interval propagation and input domain splitting.

## Abstract interpretation and reachability

- [auto_LiRPA](https://github.com/Verified-Intelligence/auto_LiRPA) - A library for automatic linear relaxation-based perturbation analysis (LiRPA) on general computational graphs, serving as a core bound-propagation backend.
- [ERAN](https://github.com/eth-sri/eran) - The ETH Robustness Analyzer for Neural Networks, leveraging abstract interpretation with custom domains (such as DeepPoly and RefineZ) to certify neural network safety.
- [Neurify](https://github.com/tcwangshiqi-columbia/Neurify) - A symbolic interval analysis verifier with directed constraint refinement for efficient tight bounds.
- [NNV](https://github.com/verivital/nnv) - A MATLAB toolbox performing set-based reachability analysis (using Star sets, ImageStars, and zonotopes) for feedforward, convolutional, and recurrent architectures.
- [pyNeVer](https://github.com/NeVerTools/pyNeVer) - A library for the design, training, and formal verification of neural networks using star-set-based reachability analysis algorithms.

## Branch-and-bound and accelerated verifiers

- [alpha-beta-CROWN](https://github.com/Verified-Intelligence/alpha-beta-CROWN) - A GPU-accelerated neural network verifier combining efficient linear bound propagation with branch-and-bound search.
- [MN-BaB](https://github.com/eth-sri/mn-bab) - A GPU-based branch-and-bound verifier employing multi-neuron relaxation constraints within DeepPoly abstract domains.
- [nnenum](https://github.com/stanleybak/nnenum) - A high-performance verification tool utilizing multiple abstraction levels including zonotopes, star sets, and LP relaxation.
- [VeriNet](https://github.com/vas-group-imperial/VeriNet) - A complete branch-and-bound verification toolkit based on symbolic interval propagation and external LP/MIP optimization.

## Closed-loop and cyber-physical systems

- [POLAR](https://github.com/BU-DEPEND-Lab/POLAR) - A tool for reachability analysis of neural-network-controlled continuous and hybrid systems using Taylor model flowpipes.
- [Verisig](https://github.com/verisig/verisig) - A tool for the formal verification of closed-loop systems with neural network controllers using hybrid automata reachability.

## Benchmarks and competitions

- [VNN-COMP](https://github.com/VNN-COMP) - The official repository for the international Verification of Neural Networks Competition, hosting standardized benchmarks (in VNN-LIB and ONNX formats) and performance results.

## Literature

### Surveys

- [Adversarial Robustness of Deep Neural Networks: A Survey from a Formal Verification Perspective](https://ieeexplore.ieee.org/document/9672049) (IEEE TDSC, 2022) - A security-centric review of verification methods designed to prove network robustness against adversarial attacks.
- [Algorithms for Verifying Deep Neural Networks](https://arxiv.org/abs/1903.06758) (Liu et al., 2019) - A comprehensive survey that provides a unified mathematical framework for neural network verification.
- [Introduction to Neural Network Verification](https://verifieddeeplearning.com/) (A. Albarghouthi, 2021) - A foundational textbook-style survey covering key mathematical models, abstractions, and algorithms.

### Seminal papers

- [AI2: Safety Verification of Deep Neural Networks with Abstract Interpretation](https://doi.org/10.1109/SP.2018.00058) (Gehr et al., IEEE S&P 2018) - Pioneered the application of abstract interpretation to deep feedforward and convolutional neural networks.
- [An Abstraction-Refinement Approach to Verification of Artificial Neural Networks](https://doi.org/10.1007/978-3-642-14295-6_24) (Pulina and Tacchella, CAV 2010) - Formulated early SMT-based verification of neural networks using a counter-example guided abstraction refinement loop.
- [An MIP-Based Approach for Evaluating the Robustness of Deep Neural Networks](https://arxiv.org/abs/1711.07356) (Tjeng et al., ICLR 2019) - Showed how mixed-integer programming (MIP) can perform exact robustness verification.
- [Certified Adversarial Robustness via Randomized Smoothing](https://arxiv.org/abs/1902.02918) (Cohen et al., ICML 2019) - Established scalable certified robustness guarantees against adversarial perturbations using randomized smoothing.
- [DeepPoly: An Abstract Domain for Proving Safety of Deep Neural Networks](https://files.sri.inf.ethz.ch/website/papers/DeepPoly.pdf) (Singh et al., POPL 2019) - Introduced the DeepPoly abstract domain for scalable and precise abstract interpretation of neural networks.
- [Intriguing Properties of Neural Networks](https://arxiv.org/abs/1312.6199) (Szegedy et al., ICLR 2014) - Uncovered the vulnerability of deep neural networks to adversarial examples, motivating the field of certified robustness.
- [Provable Defenses against Adversarial Examples via the Convex Outer Adversarial Polytope](https://arxiv.org/abs/1711.00851) (Wong and Kolter, ICML 2018) - Formulated certified defense training by bounding the convex outer adversarial polytope via linear programming duality.
- [Reluplex: An Efficient SMT Solver for Verifying Deep Neural Networks](https://arxiv.org/abs/1702.01135) (Katz et al., CAV 2017) - Introduced the Reluplex algorithm, extending the Simplex method to handle ReLU activation functions.
- [Towards Fast Computation of Certified Robustness for ReLU Networks](https://arxiv.org/abs/1804.09699) (Weng et al., ICML 2018) - Formulated the linear relaxation bounds (CROWN) that underpin many modern accelerated verifiers.

## Community

- [Neural Verification Community](https://neuralverification.org/) - Portal hosting community forums, links to competitions, and collaborative projects.
- [VNN-LIB](https://www.vnnlib.org/) - The standardized property specification language and network metadata standards for formal verification.

## Contributing

Contributions are welcome! Please read the [contributing guidelines](CONTRIBUTING.md) first.
