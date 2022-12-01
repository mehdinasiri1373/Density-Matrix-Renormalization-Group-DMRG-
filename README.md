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
The major issue in quantum many-body physics is that the Hilbert space expands exponentially with size. It is obvious that these matrix sizes will quickly become unmanageable by current computers. The DMRG is a variational, iterative strategy for reducing effective degrees of freedom to those that are most significant for a goal state. The ground state is often the goal state. This model is ideal for us since our model is one-dimensional, we lack long-range interaction, and our system has a gap. This is a highly strong and sophisticated approach, and we spent most of the project time writing the code and tactics for this section.

In this strategy, our system is made up of two subsystems (A and B) and two sites in between. The superblock consists of the left block Plus two sites Plus the right block. The Hilbert space of the superblock will be obtained by the tensor product of the Hilbert spaces of the two subsystems $H_{A+B} = H_A ⊗ H_B$ and will have the dimension $D_{A+B} = D_A × D_B$.

![img 4](https://user-images.githubusercontent.com/51785162/204970920-2d99e2cb-b890-4bba-85d4-8a50cbe20d9d.png)

At each stage, we add one site to the right of the left block and one to the left of the right block. The Hilbert spaces will eventually become too vast to handle. So we set m as the maximum number of states we wish to maintain. The base dimension will grow greater than m at some point throughout the operation. We start applying the density matrix truncation as follows:
1. Using a suitable library routine (Lanczos, Davidson), diagonalize the super-Hamiltonian to obtain the ground state $|\Psi>=\sum_{\mathrm{ij}} \Psi_{\mathrm{ij}}| \mathbf{i}>\mid \mathbf{j}>$.

2. Calculate the reduced density matrix of the left block and right blocks. 

$$\begin{aligned}
&\rho_A=\operatorname{Tr}_B|\Psi><\boldsymbol{\Psi}| \\
&\rho_B=\operatorname{Tr}_A|\Psi><\boldsymbol{\Psi}|
\end{aligned}$$

3. For each of the blocks, diagonalize the density matrix to obtain the full spectrum and eigenvectors.

4. Build a Truncation matrix or basis by keeping only the m eigenvectors with the largest eigenvalues.

5. Rotate the Hamiltonian and the operators involved in the interactions between blocks to the new basis.

6. Add a new site to the left and right blocks, to build new blocks and reiterate the diagonalization and truncation steps.

## Results:
### Many-zone chain:
As previously stated, when N regions are present, we expect a $2^N$ detergency for ground in a system with $Z_2$ symmetry. We examined this problem using the DMRG computational approach for the number of regions N = 1, 2, 3 and discovered that it is as predicted. This conclusion indicates that we will have N qubits for N areas, each with zero-mode pairings at both ends of the FM regions.

![img 5](https://user-images.githubusercontent.com/51785162/204972007-45a7147a-7acf-412f-9483-ac981e5f135f.png)

### Finite length effects:
The conclusions shown above are for scenarios with large lengths or thermodynamic limitations. We might be curious about what happens at the order of finite length. Is the ground state's degeneracy impacted by length? If so, can an effective length for the system be determined? to provide answers to these questions. Examining the DMRG findings for various systems reveals that two effective lengths, one for the FM area and the other for the PM region, can be defined as follows, depending on the values of J and h:

$$
\xi_{P M} \sim \frac{1}{\left|J_{P M}-h_{P M}\right|} \quad \xi_{F M} \sim \frac{1}{\left|J_{F M}-h_{F M}\right|}
$$

$𝜉_{FM}$ means that as long as the distance between the two zero modes at the end of each FM region $(L_{FM})$ is significantly greater than $𝜉_{FM}$, the two zero modes cannot be combined.

But $𝜉_{PM}$ means that as long as the distance between the zero-mode at the end of the first FM region and the zero modes at the beginning of the second FM region $(L_{PM})$ is significantly bigger than $𝜉_{PM}$, these two zero modes cannot be combined and eliminated.

To test this assertion, we will use the DMRG technique on a chain with N = 2 and $Z_2$ symmetry to determine the effective length of the FM and PM regions. Assume $L_{FM} = L_{PM} = 10$ for the sake of simplicity. First, assuming that the variables in the PM area are constant, examine the impact of modifying the FM region (and hence $𝜉_{FM}$) parameters on degeneracy. Second, assuming that the variables in the FM area remain fixed, the impact of altering the parameters of the PM region (and hence $𝜉_{PM}$) on the degeneracy will be seen.

![img 6](https://user-images.githubusercontent.com/51785162/204973244-8f7cb2c8-f4fa-44fa-90b3-e9acbdade4e8.png)

![img 7](https://user-images.githubusercontent.com/51785162/204973364-d81c34e6-81cb-4abe-93e5-7bd443a9374c.png)

All of the conclusions we got and discussed for $Z_2$ symmetry hold true for greater symmetries. So, in general, we assume the detergency state's (is equal to): $n^N$ for a system with the symmetry of $Z_n$ and N regions (FM+PM) as long as the effective length is substantially less than the system's length.

## Conclusion:
1. We presented a paradigm in which more than one pair of zero-boundary modes may be generated spontaneously (equivalent to one qubit). Theoretical studies show that if we have N pairs of zero modes, then the ground state degeneracy for the $Z_n$ symmetries must be $n^N$. We used the DMRG computational approach to evaluate this and found that the findings were as predicted.

2. Using computational studies, We discover that the effective length can be defined for the FM and PM areas. If we do not wish to mix zero modes, the effective length must be less than the system length. The effective lengths are determined by the problem variables. As a result, we may regulate the number of zero modes by adjusting these variables.

3. Because zero-mode couples can be utilized to create qubits in quantum computing, we can give the controllable number of qubits we need. Our computational studies have also helped us grasp the zero-mode pairing requirements.

## Application user interface

[**Through this link, you can access and download the application we wrote for this project.**](https://drive.google.com/file/d/1LaWCg4rv01eqy5gcObYKgny-KsIxdUrb/view?usp=share_link)

![img 8](https://user-images.githubusercontent.com/51785162/204976102-59ac4bd8-1f34-4a04-bd2c-44a54d8c7643.png)

## Authors
- Mohammad Mahdi Nasiri Fatmehsari
- Supervisor: [Seyyed Mohammad Sadegh Vaezi](https://scholar.google.com/citations?hl=en&user=6Pr-lFEAAAAJ)


