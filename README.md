# Double-Bracket Algorithmic Cooling (DBAC)

This repository accompanies the manuscript:

**Double-Bracket Algorithmic Cooling**  
Mohammed Alghadeer, Khanh Uyen Giang, Shuxiang Cao, Simone D. Fasciati,  
Michele Piscitelli, Nelly Ng, Peter J. Leek, Marek Gluza, Mustafa Bakr (2025)

---

## Summary

Algorithmic cooling is a framework for redistributing entropy in a closed quantum register so that a subset of qubits reach a lower effective temperature.  
In this work we extend the concept from *entropy* to *quantum coherence*.  

We introduce **Double-Bracket Algorithmic Cooling (DBAC)**, a dynamic quantum algorithm that suppresses phase-coherent excitations of pure states by simulating imaginary-time evolution. The protocol is implemented through **recursive unitary flows** constructed via **density-matrix exponentiation (DME)**, relying only on native two-qubit interactions.  

Key features of DBAC:
- Operates **obliviously**: no prior knowledge of the state is required.  
- Avoids mid-circuit measurements, unlike traditional algorithmic cooling.  
- Compatible with standard superconducting qubit architectures through simple Heisenberg ($ZZ$) interactions.  
- Recursion improves cooling but, in direct analogy to Nernst’s principle, perfect ground-state preparation requires infinite resources.  

We experimentally demonstrate DBAC on a 16-qubit superconducting lattice, showing Pauli transfer matrix (PTM) characterization of DME compilation and cooling curves across different circuit depths.  

---

## Highlights from the Paper

- **Conceptual advance:** Extends algorithmic cooling from entropy reduction to coherence suppression.  
- **Theoretical underpinning:** Connects double-bracket flows, Riemannian steepest-descent, and quantum imaginary-time evolution.  
- **Implementation:** Compiled using the Stark-induced ZZ by level excursions (**siZZle**) protocol to boost native ZZ interactions.  
- **Experimental results:**  
  - PTM fidelities around 90–92% across a range of interaction angles.  
  - Cooling performance improves with more instruction qubits and recursive DBAC steps.  
  - Robustness to imperfect calibration due to the continuous nature of ZZ interactions.  
- **Thermodynamic analogy:** Demonstrates a quantum manifestation of Nernst’s unattainability principle.  

---

## Experimental Control Code (LeeQ)

While this repository hosts the data, processed results, and analysis pipelines for the DBAC study, the **experimental orchestration code** used to run the superconducting qubit experiments is developed and maintained in a separate repository: [LeeQ](https://github.com/ShuxiangCao/LeeQ).

**LeeQ** is a Python package designed for orchestrating quantum computing experiments, with a specific focus on superconducting circuit–based systems. It provides a streamlined syntax for experiment definition, calibration, and live feedback, enabling rapid development of complex protocols like DBAC. The package integrates both hardware control and simulation/theory modules, making it suitable for full-stack quantum experimentation.

### Key Features of LeeQ
- **Easy-to-use orchestration**: Abstracted syntax for defining, scheduling, and running superconducting qubit experiments.  
- **Calibration framework**: Built-in routines for common calibration tasks such as frequency tuning, drive optimization, and gate calibration.  
- **Experiment library**: Ready-to-use implementations of common experimental protocols, with extendable modules for custom routines.  
- **Simulation and theory support**: Interfaces for running numerical simulations alongside experiments, enabling theory–experiment comparison.  
- **Dockerized environment**: Pre-built Docker images provide reproducible setups for Jupyter notebooks and live plotting servers.  
- **Extensive documentation**: Includes quick start guides, in-depth tutorials, conceptual explanations, and API references.  

### Documentation and Resources
- **Quick Start Guide**: Run your first superconducting qubit experiment within minutes.  
- **Tutorials**: Comprehensive hands-on material covering experiment orchestration, calibration, and data acquisition.  
- **User Guides**: Conceptual documentation describing LeeQ’s architecture, experiment workflows, and calibration strategies.  
- **API Docs**: Detailed references for core modules, built-in experiments, calibration classes, and theory/simulation functions.  
- **Advanced Topics**: Deployment of LeeQ as a gRPC service (EPII), architectural overviews, and developer contributions.  
- **Examples**: A collection of configuration examples and sample notebooks to help new users quickly replicate and extend experiments.  

### Relevance to DBAC
For the DBAC experiments described in our manuscript, LeeQ was used as the **control layer** to:  
1. Schedule multi-qubit experiments across the 16-qubit superconducting lattice.  
2. Implement calibrations of native ZZ interactions via the siZZle protocol.  
3. Acquire and process raw measurement counts for Pauli Transfer Matrix (PTM) tomography.  
4. Interface with theoretical modules to benchmark observed results against simulated DBAC dynamics.  

LeeQ was originally developed by [Shuxiang Cao](https://github.com/ShuxiangCao) at the University of Oxford [Quantum Superconducting Circuits Research Group](https://leeklab.org/).  
Its modular design ensures that future DBAC-related experiments and other multi-qubit protocols can be implemented with minimal overhead.

---

## Citation

If you use this repository, please cite as: 
  author       = {Mohammed Alghadeer and Khanh Uyen Giang and Shuxiang Cao and
                  Simone D. Fasciati and Michele Piscitelli and Nelly Ng and
                  Peter J. Leek and Marek Gluza and Mustafa Bakr},
  title        = {Double-Bracket Algorithmic Cooling (DBAC): code and data},
  year         = {2025},
  publisher    = {GitHub},
  journal      = {GitHub repository},
  howpublished = {\url{https://github.com/MoGhadeer/dbac-algorithmic-cooling}},
  version      = {v1.0.0}
}
