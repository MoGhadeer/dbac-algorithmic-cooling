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

## Repository Layout
