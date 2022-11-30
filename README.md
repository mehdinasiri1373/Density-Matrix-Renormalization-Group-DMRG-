# Investigation of the emergence of more than one Qubit in a quantum chain, comprising ferromagnetic and paramagnetic regions, by using the Density Matrix Renormalization Group (DMRG) method
A quantum computer is a device that does computations using quantum events and principles directly. In many cases, quantum-based algorithms outperform traditional algorithms in terms of power and speed. Technology behemoths like Microsoft, Google, and others are investing heavily in research on this subject.

The qubit is the fundamental variable in quantum computers. Classical bits have a fixed state: they are either 0 or 1 at all times throughout a calculation. This limitation does not apply to quantum bits. It may or may not be fully 0 or entirely 1.

However, we are still in the early phases of constructing such a computer, and there are several challenges ahead. One of the main problems of decoherence is due to environmental errors that cause the information to be lost. The collapse of a quantum wave function into one of its potential states is referred to as "decoherence. This is precisely what occurs as a consequence of quantum measurement. Isolating the system from its environment is one potential method. Because this may be difficult, we may consider another option.

To solve this problem, scientists looked to materials with topological phases. Because the quantum information contained in a qubit is impermeable to local measurement, local measurement cannot remove this qubit's state. Tiny, cumulative perturbations may cause quantum states to decohere and induce mistakes in computing, although such small perturbations have no effect on the system's topological features.

## Kitaev model:
Alexei Kitaev was among the first to investigate such systems in terms of their potential applicability in quantum computing. Kitaev's model is a one-dimensional chain of spineless electrons ci as follows:

![equation number 1](https://latex.codecogs.com/svg.image?H=-h&space;\sum_i&space;c_i^{\dagger}&space;c_i-\frac{1}{2}&space;\sum_i\left(\mathrm{Jc}_i^{\dagger}&space;c_{i&plus;1}&plus;\Delta&space;c_i&space;c_{i&plus;1}&plus;\text&space;{&space;h.&space;}&space;c\right))

Where h.c. means Hermitian conjugate, h is the chemical potential, ci is the electron annihilation operator for site i, and $c_i^{\dagger}$ is the creation operator. J is the intensity of the hopping and Δ is the intensity of the pairing or superconducting gap.

He demonstrated that one electron is equal to two Majorana fermions wherever they are in the system. MFs are created by dividing a fermion into real and imaginary parts. Majorana fermions are particles that are antiparticles to themselves. This indicates that the creation operator equals the destruction operator in physical terms $γ=γ^†$.

Therefore, we can rewrite the Dirac operator c using a pair of Majorana operators, and vice versa for the Majorana operators using the Dirac operator. As a result, with a few computations, we can rewrite Hamilton in the Majorana fermion language.

![equation number 2](https://user-images.githubusercontent.com/51785162/204788914-0ab1a7bd-6ab2-4092-b5f4-db1cc333e848.JPG)

We are seeking Majorana fermions that are spatially isolated yet have the same cumulative behavior as a non-localized Dirac fermion. This allows us to store data non-locally and use it in quantum computing.
Each blue oval in the image below includes two kinds of Majorana fermions, each of which is equal to one electron. The Majorana fermions may be linked locally or nonlocally, depending on the couplings used. When we are in the topological phase in a special case when h=0 and J=∆≠0 two separated Majorana fermions are left. These two Majorana operators can equivalently be described by a single fermionic state with an operator $\tilde{c}$ which can be used to encode information in them non-locally and make a qubit out of them. Therefore resistant to the issue of Decoherence. 

We name these Majorana fermions zero-edge modes because they are at the border of the topological phase and vacuum, which is a trivial phase, and they carry no energy.

![img 1](https://user-images.githubusercontent.com/51785162/204790842-747ab2ec-8a69-45bd-972a-020422e2e0aa.png)

## Ising quantum chain:
Using the Jordan-Wigner transformation, the above model is equivalent to a quantum Ising chain with the number of spins equal to the number of Majorana fermions.

![equation number 3](https://user-images.githubusercontent.com/51785162/204791482-c67fd30c-a6ca-4801-9772-6b0e67ccab0f.JPG)

Where the $𝜎^a$ Pauli matrices are:

![equation number 4](https://user-images.githubusercontent.com/51785162/204792032-db7dfcc9-14c2-4d0b-8475-0aa996d43b12.JPG)

And J>0 is the intensity of interaction of close neighbors, and h>0 is the intensity of the magnetic field

A magnetic ordering parameter may be specified in this language. It can be shown that the magnetism in the irregular phase is zero and that when it is moving to the regular phase, its value shifts away from zero.
Because we will be using the spin language for our investigations later, it is important to understand these three points:
1. The system is in the ferromagnetic phase or topological order when |h|<|J|. Except for the two modes at the beginning and end of the chain, the zero modes are coupled with each other and vanish.
2. When we are in the paramagnetic phase  |h|>|J| without topological order, all modes are coupled and annihilated, therefore no zero-edge mode exists and the ground state has no degeneracy.
3. The critical state is also the case |J|=|h|.

## Model:
We suggest the following approach for obtaining more than one pair of zero-edge modes or one qubit.
Consider an Ising chain. We may specify the variables in the problem such that a part of the chain with a length of LFM is in the ferromagnetic phase (with topological order and ground state degeneracy) and another part with a length of LFM is in the paramagnetic phase (irregular and without degeneracy).
We anticipate that the paramagnetic areas will act as an insulator between the two zero modes of the ferromagnetic regions, allowing us to obtain the requisite number of Qubits.

Since the zero-edge modes can only live at the boundaries, where topological and trivial phases meet (green diamonds), we expect the number of boundaries to determine the number of zero-edge modes or qubits.

![img 2](https://user-images.githubusercontent.com/51785162/204792777-02ad830d-2233-4124-8c63-9e4ac2435c02.png)

If we have N number of these regions (FM+PM), then the total length of the system L will be equal to:

![equation number 5](https://latex.codecogs.com/svg.image?L&space;=&space;N(L_F_M&space;&plus;&space;L_P_M))

IF N = 1. We anticipate to observe one pair of zero-mode since there is only one FM zone close to a PM zone. This is due to the fact that there are no zero modes in the PM phase.

![img 3](https://user-images.githubusercontent.com/51785162/204794492-716f5de6-cd9b-4bbc-955b-ab4dae295e28.png)

We may wonder how we may determine the number of zero modes. It is simple to demonstrate this by examining the degeneracy of the ground state.

This is what we should anticipate theoretically when we are in the ferromagnetic phase (topological order) zero-edge modes occur and affect the ground state's degeneracy. Assume that the Hamiltonian of the system is $H_1$ for N = 1. If we place a copy of this chain next to it, we will have a chain with N = 2. When there is no interaction between the first chain and its duplicate, the Hamiltonian as a whole looks like this.

![equation number 6](https://user-images.githubusercontent.com/51785162/204795213-b1e748bf-7b1e-4342-a7bb-d685e56ead05.JPG)

Because $H_1$ has a ground state with double degeneracy in $Z_2$ and we assume that there is no interaction between the two blocks, we can describe the ground state of the whole system as the tensor product of each block. 

![equation number 7](https://user-images.githubusercontent.com/51785162/204795888-6a380d6f-0f73-477e-8cf8-320608ceaf3f.JPG)

As you can see, the system will be four-fold degenerate in $Z_2$.  So we expect that for a system with the symmetry of $Z_2$ and N number of regions, the detergency of the ground state is equal to $2^N$.

How can we verify this now? We employ the numerical DMRG approach since doing it analytically is very challenging.

## DMRG Method:

