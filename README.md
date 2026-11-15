# Enhancement of the Topological Regime in Elongated Josephson Junctions

This repository contains the numerical code and data associated with the following publication:

**Enhancement of the Topological Regime in Elongated Josephson Junctions**

D. Kuiri, P. Wójcik, and M. P. Nowak  
*Physical Review B* **111**, 085416 (2025).

[Read the paper](https://doi.org/10.1103/PhysRevB.111.085416)

## 1. Overview

Planar Josephson junctions are promising platforms for realizing topological superconductivity and Majorana bound states. In this work, we theoretically investigate how the length of a planar Josephson junction influences its topological properties.

We show that increasing the junction length enhances the Zeeman-induced phase shift of Andreev bound states (ABSs). This leads to a substantial increase in the range of superconducting phase differences over which the junction can support Majorana bound states.

However, elongating the junction also introduces additional in-gap states that can suppress the induced superconducting gap and prevent the formation of Majorana modes.

We demonstrate that these unwanted states can be removed by introducing two additional superconducting contacts at the top and bottom of the junction. We also show that the topological transition can be identified through measurements of the critical current.

## 2. Physical Model

We consider a planar superconductor-normal-superconductor (SNS) Josephson junction based on a two-dimensional electron gas (2DEG).

The model includes Rashba spin-orbit coupling, Zeeman interaction and proximity-induced superconductivity. The superconducting electrodes have a phase difference $\phi$, which can be controlled using magnetic flux.

The system is described by the Bogoliubov-de Gennes Hamiltonian:

$$
\begin{aligned}
H_0 ={}&
\left(
\frac{\hbar^2 k_x^2}{2m^*}
+
\frac{\hbar^2 k_y^2}{2m_\parallel^*}
-\mu
\right)
\sigma_0\otimes\tau_z
\\
&+\frac{1}{2}g\mu_B B
\sigma_y\otimes\tau_0
\\
&+\alpha(x)(\sigma_x k_y-\sigma_y k_x)
\otimes\tau_z .
\end{aligned}
$$

Here, $\sigma_i$ and $\tau_i$ are Pauli matrices acting on spin and electron-hole degrees of freedom, respectively. The magnetic field and spin-orbit coupling are included in the normal region of the junction.

The superconducting pairing potential is spatially dependent:

$$
\Delta(x)=
\begin{cases}
\Delta_0, & x<-L_j/2,\\
0, & |x|\leq L_j/2,\\
\Delta_0 e^{i\phi}, & x>L_j/2.
\end{cases}
$$

where $L_j$ is the junction length and $\Delta_0$ is the superconducting gap.

## 3. Analytical Description of Andreev Bound States

To understand the effect of junction elongation, we first consider a perfectly transparent Josephson junction.

The spin-resolved Andreev bound-state energies can be written as

$$
E_\sigma(\phi)
=
\pm\Delta
\left|
\cos\left(
\frac{\phi}{2}+\varphi_\sigma
\right)
\right|.
$$

The Zeeman-induced phase shift is given by

$$
\varphi_\sigma
=
\frac{\sigma E_Z L_j}{\hbar v_F},
$$

where

$$
E_Z=\frac{g\mu_B B}{2},
\qquad
v_F=\sqrt{\frac{2\mu}{m^*}}.
$$

Here, $\sigma=\pm1$ denotes the two spin components.

The zero-energy solutions determine the boundaries of the topological phase:

$$
\phi_\pm
=
\pm\chi B L_j+\pi(1+2n),
$$

where $n\in\mathbb{Z}$ and

$$
\chi=\frac{g\mu_B}{\hbar v_F}.
$$

Consequently, the phase span of the topological regime becomes

$$
\boxed{
\Delta\phi=2\chi B L_j
}
$$

This is the central result of the analytical model. The topological phase span increases linearly with both the magnetic field and the junction length.

## 4. Numerical Approach

We use two complementary approaches to investigate the junction properties.

### 4.1 Green's Function Model

First, we calculate the induced superconducting gap using a Green's function description.

The Green's function is obtained from

$$
G^{-1}(\omega)
=
\omega-H_0-\Sigma(\omega),
$$

where the self-energy due to coupling with the parent superconductor is

$$
\Sigma(\omega)
=
-\gamma
\frac{
\omega\sigma_0\otimes\tau_0
+\Delta(x)\tau_+
+\Delta^*(x)\tau_-
}{
\sqrt{\Delta(x)^2-\omega^2}
}.
$$

Here, $\gamma$ describes the coupling strength between the semiconductor and the parent superconductor, and

$$
\tau_\pm=\frac{\tau_x\pm i\tau_y}{2}.
$$

The density of states is calculated as

$$
\rho(\omega)
=
-\frac{1}{\pi}
\operatorname{Im}
\left[
G(\omega)
\right].
$$

This approach allows us to investigate the induced gap and the appearance of additional in-gap states as the junction length increases.

### 4.2 Tight-Binding Model

For finite-size junctions, we use an effective Hamiltonian in which the proximity-induced superconductivity is integrated into the surrounding regions.

The Hamiltonian is discretized on a square lattice with lattice spacing

$$
a=10\ \mathrm{nm}.
$$

The numerical calculations are performed using Python and the Kwant package.

We investigate the energy spectrum, Andreev bound states, wave-function localization and critical current as functions of junction length, magnetic field and superconducting phase difference.

## 5. Results and Discussion

### 5.1 Enhancement of the Topological Phase

The Zeeman interaction lifts the spin degeneracy of the Andreev bound states and shifts their phase dependence.

As the junction becomes longer, the phase shift increases. Consequently, the zero-energy crossings extend over a wider range of superconducting phase differences.

The analytical model predicts a linear dependence of the topological phase span on junction length.

### 5.2 Induced Gap and In-Gap States

We compare the energy dispersion for junction lengths of 100 nm and 500 nm.

For shorter junctions, a clear induced superconducting gap is present throughout the momentum range.

For longer junctions, additional states appear inside the induced gap at larger transverse momenta. These states are mainly localized in the normal region and are weakly affected by the superconducting phase difference.

Their presence can couple the two edges of the junction and prevent the formation of Majorana bound states.

### 5.3 Proximity-Induced Removal of In-Gap States

To overcome this limitation, we introduce two additional superconducting contacts at the top and bottom of the junction.

These contacts provide additional proximity-induced superconductivity and modify the spectrum of the in-gap states.

The additional superconducting contacts remove the unwanted phase-independent states and restore the induced superconducting gap.

This allows zero-energy Majorana bound states to emerge at the junction edges, even for elongated junctions.

### 5.4 Longer Junctions and Majorana Bound States

We further investigate a junction with length

$$
L_j=1000\ \mathrm{nm}.
$$

For this configuration, the junction length becomes comparable to the superconducting coherence length.

The calculated spectrum shows a pronounced topological gap and nearly zero-energy states over a large range of superconducting phase differences, even at a relatively small magnetic field.

### 5.5 Critical Current and Topological Transition

We also investigate how the topological transition can be detected through the critical current.

The Josephson current is calculated from the Andreev bound-state energies:

$$
I(\phi)
=
-\frac{e}{\hbar}
\sum_{E_i>0}
\frac{\partial E_i}{\partial\phi}.
$$

The critical current is defined as

$$
I_c=\max_\phi |I(\phi)|.
$$

We find that the transition between the trivial and topological ground states is accompanied by a minimum in the critical current.

The analytical model gives the transition magnetic field as

$$
\boxed{
B_c=
n\frac{\hbar v_F}{4L_j g\mu_B}
}
$$

where $n\in\mathbb{Z}$.

This expression shows that the critical magnetic field decreases inversely with junction length.

Therefore, elongating the junction not only increases the topological phase span but also reduces the magnetic field required to reach the topological transition.

## 6. Repository Contents

The repository contains the Jupyter notebooks and numerical data used in the calculations.

| File | Description |
|---|---|
| `long_junction_paper.ipynb` | Main numerical calculations for the elongated Josephson junction |
| `S_N_S_translational_invariant_paper.ipynb` | Calculations for translationally invariant SNS junctions |
| `Self_energy_S_N_S_1D_paper.ipynb` | Green's function and self-energy calculations |
| `analytical_ABS.ipynb` | Analytical calculations of Andreev bound states |
| `E_junction_L_N_100.pkl` | Junction energy data |
| `I_c_values_L_N_100.pkl` | Critical current data for N = 100 |
| `I_c_values_L_N_500.pkl` | Critical current data for N = 500 |
| `energies_L_N_100.pkl` | Energy spectrum data for N = 100 |
| `energies_L_N_500.pkl` | Energy spectrum data for N = 500 |
| `dos_values_L_N_100_pi_gamma_07.pkl` | Density of states data |
| `dos_values_L_N_500_pi_gamma_07.pkl` | Density of states data |

Additional `.pkl` files contain numerical results used in the analysis and preparation of the figures in the paper.

## 7. Software and Requirements

The calculations use the following scientific computing tools:

- Python
- NumPy
- SciPy
- Matplotlib
- Kwant
- Jupyter Notebook

## 8. Publication

If you use the numerical code or data from this repository, please cite:

D. Kuiri, P. Wójcik, and M. P. Nowak, "Enhancement of the topological regime in elongated Josephson junctions," *Physical Review B* **111**, 085416 (2025).

[https://doi.org/10.1103/PhysRevB.111.085416](https://doi.org/10.1103/PhysRevB.111.085416)

## 9. Acknowledgements

This work was supported by the National Science Centre (NCN), Poland, under Agreement No. UMO-2020/38/E/ST3/00418.

Computational resources were provided by the PLGrid infrastructure at ACK Cyfronet AGH.

## Author

**Dibyendu Kuiri**

[Personal Website](https://dkuiri.github.io/) | [Google Scholar](https://scholar.google.com/citations?user=K1jTqmYAAAAJ) | [LinkedIn](https://www.linkedin.com/in/dkuiri) | [GitHub](https://github.com/dkuiri)
