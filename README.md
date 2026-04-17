[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)]()

# Vibrational Anharmonicity in a Diatomic Molecule

## Beyond The Harmonic Oscillator
Let's now consider two ways in which the vibrational structure of "real molecules" is more complicated than what we've seen for the harmonic oscillator. 

## Anharmonicity
First, real vibrational motions involve "anharmonicity", e.g., Their potential deviates from a perfect harmonic oscillator quadratic potential energy surfaces. We've already touched on this by looking at the Morse Potential.
<p align='center'>
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/84/Morse-potential.svg/960px-Morse-potential.svg.png" alt="figure" width="400"/>
</p>

<p align='center'>
    $$\mbox{Figure.The Morse Potential (blue) and harmonic oscillator potential (green)}$$
</p>

The harmonic oscillator is a reasonable approximation of this potential near the equilibrium geometry, but deviates substantially for $x$ far from the center of the well. Correspondingly, the vibrational levels of the Morse potential will deviate from those of the HO model. Note that the Morse potential levels grow closer together as energy increases.

## Limitations of the Harmonic Oscillator Model for Molecular Vibrations
The harmonic oscillation is a great approximation of a molecular vibration, but has key limitations:
- Due to equal spacing of energy, all transitions occur at the _same_ frequency (i.e., single line spectrum). However, experimentally, many lines are often observed (called overtones).
- The harmonic oscillator does not predict bond dissociation, you cannot break it, no matter how much energy is introduced.

# Morse Oscillator Breakdown
The Morse oscillator, named after physicist [Philip M. Morse](https://www.nae.edu/28848/Dr-Philip-M-Morse) is a better approximation for the vibrational structure of the molecule than the harmonic oscillator because it explicitly includes

The Morse oscillator is a model for a particle in a one-dimensional anharmonic potential energy surface with a dissociative limit at infinite displacement. It is commonly used for describing the spectroscopy of diatomic molecules and anharmonic vibrational dynamics, and most of its properties can be expressed through analytically expressions. The Morse potential is

<p align='center'>
    $$V(x) = D_e[1-e^{-\alpha x}]^2 \quad (1)$$
</p>

where $x = (r - r_0)$, $D_e$ sets the depth of the energy minimu at $r=r_0$ relative to the dissociation limit as $r \rightarrow \infty$, and $\alpha$ sets the curvature of the potential. If we expand $V$ in powers of $x$ about $x=0$, the parameter $\alpha = \sqrt{k_e /2D_e}$ and $k_e = \left(\frac{d^2 V}{dx^2} \right)_e$ is the bond force constant at the bottom of the potential well.

The Morse oscillator Hamiltonian for a diatomic molecule of reduced mass _mR_ bound by the potential is

<p align='center'>
    $$H = \frac{p^2}{2m_R} + V(x)$$
</p>

and has the eigenvalues
<p align='center'>
    $$E_n = \hbar \omega_0 \left[\left(n + \frac{1}{2} \right) - x_e \left(n + \frac{1}{2} \right)^2 \right] \quad n =0, \ 1, 2, \ 3, \ldots \quad (2)$$
</p>

where
- $\omega_0 = \sqrt{2 D_e \alpha^2 / m_R}$ is the fundamental frequency.
- $x_e = \frac{\hbar \omega_0}{4 D_e}$ is the harmonic constant.
- The frequency $\omega_0$ is equivalent to equating the harmonic for constant $\mathcal{K} = (\partial^2 V/ \partial x^2)_{x=0}$ with $m_R \omega_0^2$.

The harmonic oscillator approximation is convenient to use for diatomic molecules with quantized vibrational energy levels given by the following equation:
<p align='center'>
    $$E_n = \left ( n + \frac{1}{2} \right) \omega_e$$
</p>

The new energy levels of this _anharmonic_ potential can be found using _perturbation theory_. We will just write down the result here that we find higher-order corrections to the energy according to:

<p align ='center'>
    $$G(n) = \omega_e \left(n + \frac{1}{2} \right) - \omega_e x_e \left( n + \frac{1}{2} \right)^2 + \omega_e y_e \left(n + \frac{1}{2} \right)^3 + \ldots \quad (3)$$
</p>

where $\omega_e$ is the anharmonic oscillator frequency, and $x_e$ is the _anharmonic constant_, which is typically much smaller than $\omega_e$.

While it masy seem that the harmonic oscillator and the anharmonic oscillator are closely related, this is in fact not the case. The difference in the wavefunctions leads to a breakdown of selection rules, specifically, $\Delta n = \pm 1$ selection rule can not be applied, and higher order terms must be accounted in the energy calculations. 

On the other note is that anharmonicity also changes the selection rules for IR transitions. For absorption of IR light, we can now have:
<p align='center'>
    $$\Delta n = +1, \ +2, \ +3, + \ldots$$
</p>

where $\Delta n = +1$ are _fundamental transition_ and $\Delta n = +2, \ +3, + \ldots$ are called _overtones_, and can occur but are much weaker in intensity than the _fundamental_. Overtone transitions are not always observed, especially in larger molecules, because the transitions become weaker with increasing $Delta n$.

## Overtones
Based on the harmonic oscillator approximation, the energy of the overtone transition would be $n$ times larger than the energy of the fundamental transition frequency, but the _anharmonic oscillator_ calculations show that the overtones are less than a multiple of the fundamental frequency. This is demonstrated with the vibration of the diatomic in the gas phase:

<p align='center'>
    $\mbox{Table 1. HCl vibrational spectrum}$
</p>

<div align='center'>
  
|Transition | Term | $v_{obs} \ [cm^{-1}]$ | $v_{Harmonic} \ [cm^{-1}]$| $v_{Anharmonic} \ [cm^{-1}]$ |
|:-----------:|:------:|:---------------------:|:-------------------------:|:----------------------------:|
| $0 \rightarrow 1$ | fundamental | 2,885.9 | 2,885.9 | 2,885.3 |
| $0 \rightarrow 2$ | first overtone | 5,668.0 | 5,771.8 | 5,665.0 |
| $0 \rightarrow 3$ | second overtone | 8,347.0 | 8,657.7 | 8,339.0|
| $0 \rightarrow 4$ | third overtone | 10,923.1 | 11,543.6 | 10,907. 4|
| $0 \rightarrow 4$| fourth overtone | 13,396.5 | 14,429.5 | 13,370|

</div>

We can see from Table 1, that the anharmonic frequencies correspond much better with the observed frequencies, especially as the vibrational levels increase.

## The Morse oscillator $Schr\ddot{o} dinger$ equation

Solving the $Schr\ddot{o}dinger$ with the Morse oscillator is not trivial, but can be done analytically in terms of associated __Laguerre polynomials__.

<p align='center'>
    $$\psi (n) = N_n z^{\lambda - n - \frac{1}{2}} e^{-z / 2} L_n^{2 \lambda - 2n - 1} (z) \quad [in \ cm^{-1}] \quad (4)$$
</p>

where 
- $N_n = \sqrt{\frac{n!(2\lambda - 2n - 1)a}{\Gamma (2 \lambda - n)}}, \quad \lambda = \frac{\sqrt{2mD_e}}{a\hbar}$ is normalization constant.
- $\mathcal{L}_n^(\alpha) = \frac{z^{- \alpha} e^z}{v !} \ \frac{d^n}{dz^n} (z^{n + \alpha} e^{-z}), \quad z= 2\lambda e^{-x}$ is a _generalized Laguerre Polynomial_.
- $n = 0, \ 1, \ 2, \ 3, \ldots, \left[ \lambda - \frac{1}{2} \right]$

The code below defines the class Morse representing a Morse oscillator, which can be used to generate depictions of the wavefunctions and energy levels as given in the example for $HCl$.
