## Characterization of Young Accreting Planets

Eduard Bopp, Hubert Klahr (MPIA) & Sebastian Wolf (Uni Kiel)

Supported by DFG Priority Programme 1992

PSF Theory Group Meeting – Dec 14 2017

---

### Observing embedded planets

<img src="images/quanz-hd100546.png" width="600" />

Candidate around HD100546

$$
\mathrm{T} = 932^{+193}\_{-202} \mathrm{K}, \quad
\mathrm{R} = 6.9^{+2.7}\_{-2.9} \mathrm{R}\_\mathrm{Jup}
$$

Source: Quanz et al. (2015)

Note:

if real => object we are interested in


<img src="images/vlt.jpg" height="200" />
<img src="images/eelt.jpg" height="200" />

<img src="images/jwst.jpg" height="200" />
<img src="images/alma.jpg" height="200" />

Credit: ESO, NASA

Note:

Current and next-gen observatories will give us more data

- SPHERE/VLT
- METIS/E-ELT
- MIRI/JWST
- ALMA

Visible, IR, Millimeter

Direct detection of accreting planets?

---

## Interpreting observations

- *Dynamical model of planet-disk system*
- Detailed model of observed radiation (S. Wolf, Uni Kiel)
  - Radiative transfer models
  - Instrument effects


### Numerical models

<img src="images/klahr-kley-midplane-temperature.png" height="350" />
<img src="images/klahr-kley-vertical-cut.png" height="350" />

Source: Klahr & Kley (2006)

Note:

disk thickens around planet, high pressure scale height
donut-shaped structure


### Synthetic observations

<img src="images/ruge-2014-disk-embedded-planet.png" height="300" />
<img src="images/ruge-2014-synthetic-alma-observation.png" height="300" />

Source: Ruge, Wolf, Uribe, Klahr (2014)

Note:

Should show features like

- Accretion onto the planet
- Circumplanetary disk
- Horseshoe orbits
- Ring structures
- Spiral waves

Feasibility of detecting gaps (caused by planets) with ALMA

---

## Dynamical models

- Internal energy of disk is dominated by radiation
- 3D radiation hydrodynamical numerical models

Note:

Treat radiation as accurately as possible in a dynamical setup


### Hydrodynamics

PLUTO (Mignone et al. 2007)

- Godunov-type grid code
- Adaptive mesh refinement
- Many different physics modules

Note:

experience in group
availability of accurate radiation models


### Radiative transfer

<img src="images/radtrans-schematic-plain.svg" width="600" />

Note:

Approximate radiation model used within fluid simulations


Equations for radiative transfer:

$ ∂\_t E\_\mathrm{int} + ∇ \cdot (E\_\mathrm{int} \mathbf{u}) =
\- \mathrm{P} ∇ \cdot \mathbf{u} - Λ $
<!-- .element: class="fragment" -->

$ ∂\_t E\_\mathrm{rad} + ∇ \cdot (E\_\mathrm{rad} \mathbf{u}) =
\- ∇ \cdot \mathbf{F}\_\mathrm{rad} + Λ $
<!-- .element: class="fragment" -->

with $ Λ = ρ c κ\_R (a T^4 - E\_\mathrm{rad}) $
<!-- .element: class="fragment" -->


<img src="images/radtrans-schematic-diffusion.svg" width="600" />

- Flux-limited diffusion: $ \mathbf{F} = - D ∇ E\_\mathrm{rad} $
- Levermore & Pomeraning (1981)
- Implementation in PLUTO: Kuiper et al. (2010)

Note:

gray approximation

fast, thus practical for dynamical simulations

FLD is a strong simplification of radiative transfer

leads to inaccuracies in atmosphere: opt. thin -> opt. thick

maybe M1 closure later?


<img src="images/radtrans-schematic-irradiation.svg" width="600" />

Frequency-dependent ray-tracing (Kuiper et al., 2010 & 2013)

Note:

stellar irradiation using frequency-dependent ray-tracing

refer to Flock et al. (2013) as alternative implementation


<img src="images/kuiper-klessen-2013-radtrans-comparison.png" width="600" />

Kuiper & Klessen (2013)

Note:

midplane T profile compared between

- Monte Carlo (RADMC3D)
- dashed: gray FLD
- dotted: gray FLD + gray ray-tracing
- solid:  gray FLD + frequency-dependent ray-tracing

Flux-limited diffusion not sufficient on its own

caveat not even this is accurate for intermediate optical depths around 10^3


### Full picture

<img src="images/radtrans-schematic.svg" width="600" />

---

### Current state

- 2D axis-symmetric radiation hydro setup
- Next steps: move to 3D, introduce the planet
- Collaboration on modelling real systems

Note:

ppl working on simulations


### Further aspects to study

- Dust opacities
- Gas opacities (Malygin et al., 2014)
- Accretion shock at planet (Marleau et al., 2017)
- Refinement of the region around the planet
- Ionization for hot regions

Note:

AMR is very useful for this type of problem

Radiation treatment not implemented yet for AMR

Some work in that direction by Szulágyi et al. (2017)

---

### Summary

- Dynamical models of planet-disk interaction
- Focus on small-scale structures
- Aim: treat radiation as accurately as possible
- Relevant to interpret observations of circumplanetary disks

---

### Thank you for your attention

Contact: bopp@mpia.de

For reference:

- Klahr & Kley (2006): *Initial radiation hydro model*
- Kuiper, Klahr, Dullemond, Kley, Henning (2010): *Frequency-dependent irradiation*
- Ruge, Wolf, Uribe, Klahr (2014): *Feasibility of detection with ALMA*
- Marleau, Klahr, Kuiper, Mordasini (2017): *Planetary accretion shock*
