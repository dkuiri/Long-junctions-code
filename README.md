# Enhancement of the Topological Regime in Elongated Josephson Junctions

This repository contains the numerical code and data used in our theoretical study of topological superconductivity in elongated planar Josephson junctions.

The work investigates how increasing the separation between superconducting electrodes affects the Andreev bound-state spectrum and the topological superconducting phase.

We show that elongating the junction enhances the Zeeman-induced phase shift of Andreev bound states, resulting in a wider topological phase region. However, longer junctions also support additional trivial in-gap states that can destroy the induced superconducting gap and prevent the formation of Majorana bound states.

We show that introducing additional superconducting contacts at the top and bottom of the junction suppresses these unwanted states. We also show that the topological transition can be probed through measurements of the critical current.

**Publication:** Physical Review B 111, 085416 (2025)

**Authors:** D. Kuiri, P. Wójcik, and M. P. Nowak

[Read the paper](https://doi.org/10.1103/PhysRevB.111.085416)

---

## 1. Overview

Planar superconductor-normal-superconductor (SNS) Josephson junctions are promising platforms for realizing topological superconductivity and Majorana bound states.

In this work, we theoretically investigate the effect of junction elongation on the topological properties of planar Josephson junctions.

Our main findings are:

- Increasing the junction length enhances the Zeeman-induced phase shift of Andreev bound states.
- The phase span of the topological regime increases linearly with junction length.
- Elongated junctions support additional transverse modes that appear as trivial in-gap states.
- These in-gap states can prevent the formation of Majorana bound states and close the induced superconducting gap.
- Additional superconducting contacts at the top and bottom of the junction suppress these unwanted states and restore the topological gap.
- The topological transition can be identified through a minimum in the critical current.
- The critical magnetic field required to reach the topological regime decreases with increasing junction length.

## 2. Physical Model

We consider a two-dimensional semiconductor forming a planar SNS Josephson junction.

The system consists of two superconducting regions separated by a normal semiconductor region. The model includes Rashba spin-orbit coupling and an in-plane magnetic field acting on the normal region.

The superconducting phase difference between the two electrodes is denoted by $\phi$.

The system is described by the Bogoliubov-de Gennes Hamiltonian:

$$
\begin{aligned}
H_0 ={}&
\left(
\frac{\hbar^2 k_x^2}{2m^{\ast}}
+
\frac{\hbar^2 k_y^2}{2m_{\parallel}^{\ast}}
-\mu
\right)
\sigma_0\otimes\tau_z
\\
&+\frac{1}{2}g\mu_B B_y
\sigma_y\otimes\tau_0
\\
&+\alpha(x)(\sigma_x k_y-\sigma_y k_x)
\otimes\tau_z .
\end{aligned}
$$

Here, $\sigma_i$ and $\tau_i$ are Pauli matrices acting on spin and electron-hole degrees of freedom, respectively.

The momentum operators are defined as

$$
k_x=-i\frac{\partial}{\partial x},
$$

while $k_y$ is a good quantum number for a translationally invariant junction.

The magnetic field and spin-orbit coupling are included only in the normal region.


### 2.1 Analytical Model of Andreev Bound States

To understand the effect of junction elongation, we first consider a perfectly transparent Josephson junction.

The spin-resolved Andreev bound-state energies are given by:

$$
E_{\sigma}(\phi)=\pm\Delta\left|\cos\left(\frac{\phi}{2}+\varphi_{\sigma}\right)\right|
$$

The Zeeman-induced phase shift is:

$$\varphi_{\sigma}= \frac{\sigma E_Z L_j}{\hbar v_F}$$

where:

$$
E_Z=\frac{g\mu_B B}{2}
$$

Here, $\sigma=\pm1$ denotes the two spin components.

The Fermi velocity is:

$$
v_F=\sqrt{\frac{2\mu}{m^{\ast}}}
$$

Here, $L_j$ is the junction length, $g$ is the effective g-factor and $\mu_B$ is the Bohr magneton.

The zero-energy solutions of the Andreev bound-state spectrum determine the boundaries of the topological phase:

$$\phi_{\pm}= \pm\chi B L_j+\pi(1+2n)$$

where:

$$
\chi=\frac{g\mu_B}{\hbar v_F}
$$

Consequently, the phase span of the topological regime is:

$$
\Delta\phi=2\chi B L_j
$$

This is the central result of the analytical model. It shows that the topological phase span increases linearly with junction length at a fixed magnetic field.

## 3. Induced Gap: Green's Function Model

We first investigate the dispersion relation of an SNS junction to understand how elongation affects the induced superconducting gap.

We consider a system that is finite along the junction direction and translationally invariant in the perpendicular direction.

The excitations are obtained from the system's Green's function:

$$G^{-1}(\omega) = \omega-H_0-\Sigma(\omega).
$$

Here, $\Sigma(\omega)$ is the self-energy resulting from the uniform coupling of the semiconductor to the parent superconductor:

$$ \Sigma(\omega) =
-\gamma
\frac{
\omega\sigma_0\otimes\sigma_0
+\Delta(x)\tau_+
+\Delta^{\ast}(x)\tau_-
}{
\sqrt{\Delta(x)^2-\omega^2}
}.
$$

The superconducting pairing potential is spatially dependent:

$$
\Delta(x)=
\begin{cases}
\Delta_0, & x<-L_j/2,\\
0, & |x|\leq L_j/2,\\
\Delta_0 e^{i\phi}, & x>L_j/2.
\end{cases}
$$

The pairing matrices are defined as

$$ \tau_{\pm} =
\frac{\tau_x\pm i\tau_y}{2}.
$$

The density of states is calculated using

$$ \rho(\omega) = -\frac{1}{\pi}
\operatorname{Im}[G(\omega)].
$$

This approach allows us to investigate the induced superconducting gap and the appearance of additional in-gap states as the junction length increases.

### 3.1 Parameters

The calculations use parameters corresponding to an InSb semiconductor coupled to an aluminium superconductor.

| Parameter | Value |
|---|---:|
| Effective mass | $0.014m_e$ |
| Chemical potential | 5 meV |
| Superconducting gap | 0.2 meV |
| Rashba coupling | 50 meV nm |
| Zeeman g-factor | 50 |
| Semiconductor-superconductor coupling | 0.7 meV |
| Lattice spacing | 10 nm |
| Superconducting contact length | 2000 nm |

The superconducting coherence length is estimated to be approximately 1 micrometre.

## 4. Integrated Superconductivity Model

For further analysis of the in-gap states and finite-size junctions, we use an effective Hamiltonian in which the proximity-induced superconductivity is integrated into the regions surrounding the normal part of the junction.

The Hamiltonian becomes

$$
\begin{aligned}
H={}&
\left(
\frac{\hbar^2 k_x^2}{2m^{\ast}}
+
\frac{\hbar^2 k_y^2}{2m^{\ast}}
-\mu
\right)
\sigma_0\otimes\tau_z
\\
&+g(x)\mu_B B\sigma_y\otimes\tau_0
\\
&+\alpha(x)(\sigma_x k_y-\sigma_y k_x)
\otimes\tau_z
\\
&+\Delta(x)\tau_+
+\Delta^{\ast}(x)\tau_- .
\end{aligned}
$$

Here, the Zeeman interaction, spin-orbit coupling and superconducting pairing are spatially dependent.

The Hamiltonian is discretized on a square lattice with lattice constant

$$
a=10\ \mathrm{nm}.
$$

For a proper description of Andreev scattering at the normal-superconductor interface, an anisotropic effective mass is introduced in the proximitized contacts:

$$
m_{\parallel}^{\ast}=1000m^{\ast}.
$$

The numerical calculations are performed using Python and the Kwant quantum transport package.

### 4.1 Wave-function Weight in the Normal Region

To distinguish states localized in the normal region from states residing in the superconducting contacts, we calculate the wave-function weight:

$$ W_N = \int_{-L_j/2}^{L_j/2}
|\Psi(x,k_y)|^2\,dx.
$$

This quantity allows us to identify the origin of the different quasiparticle bands and investigate the localization of the in-gap states.

## 5. Results and Discussion

### 5.1 Enhancement of the Topological Phase

The Zeeman interaction lifts the spin degeneracy of the Andreev bound states and shifts their phase dependence.

The magnitude of this phase shift increases with junction length.

Consequently, the region around $\phi=\pi$ where Majorana bound states appear becomes wider as the junction is elongated.

For the same magnetic field, a longer junction can support the topological regime over a significantly larger phase interval.

The analytical model predicts a linear dependence:

$$
\Delta\phi\propto B L_j.
$$

### 5.2 Induced Gap and Trivial In-Gap States

We compare the dispersion relations for junction lengths of 100 nm and 500 nm.

For the shorter junction, a pronounced induced superconducting gap is present throughout the Brillouin zone.

For the elongated junction, additional states appear inside the induced gap at larger transverse momenta.

These states are mainly localized in the normal region and are weakly affected by changes in the superconducting phase difference.

Their presence has an important consequence for the Andreev bound-state spectrum: they couple the two edges of the junction and prevent the formation of Majorana bound states.

Thus, although elongation enhances the topological phase span, it can simultaneously suppress the induced gap.

### 5.3 Proximitizing the In-Gap States

To overcome the problem of trivial in-gap states, we introduce two additional superconducting contacts at the top and bottom edges of the junction.

These contacts provide additional proximity-induced superconductivity.

The additional superconducting contacts force Andreev reflections of quasiparticles propagating in the transverse direction and remove the unwanted phase-independent in-gap states.

As a result, the induced superconducting gap reopens, allowing Majorana bound states to form at the junction edges.

### 5.4 Majorana Bound States in Longer Junctions

We further investigate an elongated junction with length

$$
L_j=1000\ \mathrm{nm}.
$$

At this length, the junction becomes comparable to the superconducting coherence length.

The Andreev bound-state spectrum undergoes a transition towards a linear configuration.

We observe a pronounced topological gap and nearly degenerate zero-energy states over almost the entire superconducting phase range, even at a relatively small magnetic field of

$$
B=0.2\ \mathrm{T}.
$$

This demonstrates that elongation, together with additional proximity-induced superconductivity, provides an effective route towards enlarging the topological regime.

### 5.5 Critical Current and Topological Transition

The presence of additional superconducting contacts prevents conventional local or nonlocal tunnelling spectroscopy of the junction spectrum.

However, the topological transition can still be investigated through the critical current.

The Josephson current is calculated from the Andreev bound-state energies:

$$ I(\phi) = -\frac{e}{\hbar} \sum_{E_i>0} \frac{\partial E_i}{\partial\phi}.$$

The critical current is defined as

$$
I_c=\max_{\phi} I(\phi).
$$

The ground-state phase is determined by minimizing the total energy of the junction:

$$ E_j(\phi) = \sum_{E_i<0}E_i(\phi).$$

We find that the topological transition is accompanied by a minimum in the critical current. At the same transition, the ground-state phase switches from a value close to zero to a value close to $\pi$.

The analytical model allows us to estimate the magnetic field at which this transition occurs:

$$
\boxed{
B_c=
\frac{n\hbar v_F}
{4L_j g\mu_B}
}
$$

where $n\in\mathbb{Z}$.

This expression shows that the critical magnetic field decreases inversely with junction length:

$$
B_c\propto\frac{1}{L_j}.
$$

Therefore, elongating the junction increases the topological phase span while reducing the magnetic field required to reach the topological transition.

## 6. Repository Contents

The repository contains the Jupyter notebooks and numerical datasets used in the calculations.

| File | Description |
|---|---|
| `long_junction_paper.ipynb` | Main numerical calculations for elongated Josephson junctions |
| `S_N_S_translational_invariant_paper.ipynb` | Calculations for translationally invariant SNS junctions |
| `Self_energy_S_N_S_1D_paper.ipynb` | Green's function and self-energy calculations |
| `analytical_ABS.ipynb` | Analytical calculations of Andreev bound states |
| `E_junction_L_N_100.pkl` | Junction energy data |
| `I_c_values_L_N_100.pkl` | Critical current data for N = 100 |
| `I_c_values_L_N_500.pkl` | Critical current data for N = 500 |
| `energies_L_N_100.pkl` | Energy spectrum data for N = 100 |
| `energies_L_N_500.pkl` | Energy spectrum data for N = 500 |
| `energies_W_SC_0.pkl` | Energy data for the corresponding superconducting configuration |
| `energies_W_SC_2000_L_N_1000.pkl` | Energy data for an elongated junction with additional superconducting contacts |
| `energies_short_junction.pkl` | Short-junction energy data |
| `energies_with_top_SC_n_200.pkl` | Energy data with additional top superconducting contact |
| `dos_values_for_L_N_100_pi_gamma_07.pkl` | Density of states data for N = 100 |
| `dos_values_for_L_N_500_pi_gamma_07.pkl` | Density of states data for N = 500 |
| `phi_values_max_L_N_100.pkl` | Phase values associated with the maximum energy for N = 100 |
| `phi_values_max_L_N_500.pkl` | Phase values associated with the maximum energy for N = 500 |
| `phi_values_E_j_max_L_N_100.pkl` | Phase-dependent energy data for N = 100 |
| `phi_values_Ej_max_L_N_500.pkl` | Phase-dependent energy data for N = 500 |

Additional numerical datasets are included for analysing the energy spectra, phase dependence and critical current.

## 7. Software and Requirements

The calculations use Python and the following scientific computing packages:

- NumPy
- SciPy
- Matplotlib
- Kwant
- Jupyter Notebook

Some calculations involve large sparse matrices and may require substantial computational resources.

## 8. Running the Notebooks

Clone the repository:

```bash
git clone https://github.com/dkuiri/Long-junctions-code.git
cd Long-junctions-code
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

The main calculations can be explored through the following notebooks:

- `long_junction_paper.ipynb`
- `S_N_S_translational_invariant_paper.ipynb`
- `Self_energy_S_N_S_1D_paper.ipynb`
- `analytical_ABS.ipynb`

The saved numerical datasets can also be loaded for post-processing and figure generation without repeating the full simulations.

## 9. Publication and Citation

If you use the numerical code or data from this repository, please cite our paper:

D. Kuiri, P. Wójcik, and M. P. Nowak, "Enhancement of the topological regime in elongated Josephson junctions," *Physical Review B* **111**, 085416 (2025).

DOI: [10.1103/PhysRevB.111.085416](https://doi.org/10.1103/PhysRevB.111.085416)

The numerical code associated with this work is also archived on Zenodo:

[https://zenodo.org/records/13740205](https://zenodo.org/records/13740205)

## 10. Acknowledgements

This work was supported by the National Science Centre (NCN), Poland, under Agreement No. UMO-2020/38/E/ST3/00418.

Computational resources were provided by the PLGrid infrastructure at ACK Cyfronet AGH under Computational Grant No. PLG/2024/017374.

---

**Dibyendu Kuiri**

Theoretical Condensed Matter Physics

[Personal Website](https://dkuiri.github.io/) | [Google Scholar](https://scholar.google.com/citations?user=K1jTqmYAAAAJ) | [LinkedIn](https://www.linkedin.com/in/dkuiri) | [GitHub](https://github.com/dkuiri)
