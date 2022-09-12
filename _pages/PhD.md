---
layout: page
toc: true
title: My PhD
permalink: /PhD/
categories: [kinetics, statistics, mathematics, physics, science, computer modelling]
description: A overview of my PhD work

---
# Magnesium Chemistry in the Upper Atmosphere of Earth and Mars

This page offers a brief overview of the work undertaken during my PhD - with a focus on modelling and analysis. If you would like to read about my work in further depth, then my [thesis](https://ethos.bl.uk/OrderDetails.do?did=1&uin=uk.bl.ethos.551263) and [journal publications](https://www.linkedin.com/in/lottes-salter/details/publications/) are available online. 

# Introduction  

The frictional ablation of cosmic dust deposits metals into the upper atmospheres of Earth and Mars.  Magnesium is one of the most abundant metals in this cosmic dust and large concentrations have been observed in the Earth’s upper atmosphere.
In the terrestrial atmosphere the peak concentration of Mg⁺ ions lie at higher altitudes (90 - 100 km) than the neutral Mg atoms (~89 km). Other metals (Fe, Ca and Na) have been observed using ground-based LIDAR. However magnesium can not be viewed this way as the wavelengths required (280 and 285 nm for Mg⁺ and Mg, respectively) are absorbed by the ozone layer. Therefore, satellite and rocket measurements were utilised to measure the concentrations, altitudes and global densities of the Mg⁺ and Mg layers. A striking difference between magnesium and other meteoric metals is the large ratio between Mg⁺ and Mg - which is even more striking as Mg⁺ is not depleted relative to other metals in the upper atmosphere. This could not be explained by differential ablation, which affects the Ca⁺/Ca ratio. Thus, a difference in chemistry was the likely explanation for this ratio, and will be discussed later.   

## Experimental

The aim of the experimental systems was to make gas phase kinetic measurements so that rate coefficients could be obtained - to help facilitate the understanding of the chemistry of magnesium in the upper atmosphere.  I undertook measurements on many of the reactions shown in the scheme below.

![]({{site.baseurl}}/images/reactscheme.png "Magnesium Reaction Scheme")

Two experimental systems were utilised; PLP/LIF (pulsed laser photolysis/ laser induced fluorescence) and a fast flow tube. These will not be discussed in detail here, but I gained a vast amount of experience using lasers, pumps, timing instruments, vacuum systems and a mass spectrometer.  I will not discuss these systems here, however, detailed experimental setups are available in [my publications](https://www.linkedin.com/in/lottes-salter/details/publications/). 

## Analysis
_### PLP/LIF_

The following reactions were studied in the PLP/LIF system:

Mg⁺ + O₃ → MgO⁺ + O₂  
Mg⁺ + N₂O → Mg⁺.N₂O  
Mg⁺ + X  → Mg⁺.X (where X = O₂, CO₂, H₂O and N₂)  

Mg⁺ was monitored at an increasing time-delay so that a sufficient decay profile could be built up, as shown below.

[PIC OF DECAY]

The loss of Mg⁺ ions can be described by the pseudo first-order decay coefficient k′ as, during experiments, the concentration of the reactant and bath gases were kept well in excess of Mg⁺. For reactions with O₃ :

![]({{site.baseurl}}/images/ko3.png)	

and for the other reactions:

![]({{site.baseurl}}/images/kx.png)

where _kₓ_ is the rate coefficient for the reaction of Mg⁺ ions with the selected reactant; _k<sub>DiffMg⁺</sub>_ describes the diffusion of the Mg⁺ ions out of the volume defined by the intersection of the laser beams within the field of view of the detector; _k<sub>MgX</sub>_ is the rate coefficient for the reaction between Mg⁺ and either the organometallic precursor or any degradation/photolysis products. The value of _k<sub>DiffMg⁺</sub>_ + _k<sub>MgX</sub>_ was determined from a fit of the decay when the concentration of reactant equalled zero. The pseudo first order rate coefficient, k′, was obtained by fitting the experimental decay to a simple single exponential form, A + B_<sup>-k′t</sup>_ as illustrated by the solid line in the above figure. 

_### Fast Flow Tube_

Reactions in the flow tube can be complicated as several reactions and processes are occurring at once. Therefore in order to determine rate coefficients for the reactions studied it was essential to use a numerical model. The model takes into account any gas phase chemistry occurring, diffusion and loss to the walls of Mg⁺/Mg-containing species and, if necessary, any reactants. The changes in concentration down the flow tube of the species of interest were calculated by integrating coupled ordinary differential equations using a [fourth-order Runge-Kutta numerical integration scheme](https://assets.cambridge.org/97805218/80688/frontmatter/9780521880688_frontmatter.pdf). The integration was split into several parts, corresponding to each reaction zone, in which a specific amount of reactants were present. For each reaction zone the reaction time was calculated and the integration was performed over that time. In order to obtain the required rate coefficient, kx, for magnesium ion work the experimental data points were compared with calculated data points to generate a fitting parameter, χ²;

![]({{site.baseurl}}/images/chisqu.png)	

The integrated intensities have no errors associated with them, so a weighted fit was obtained by using the measured value as the weight, i.e. the larger the value,
the larger the associated error. If an un-weighted fit was required then the weight was taken to be unity for each point. For magnesium atom χ² was generated using;

![]({{site.baseurl}}/images/weightchisqu.png)	

where _error<sub>i</sub>_ is the standard deviation obtained when calculating the average concentration for each data point. Calculations over a range of _k<sub>x</sub>_ are run, so that a minimum value for χ² could be obtained and therefore an optimal value for _k<sub>x</sub>_ . The model takes into account the initial conventration of Mg⁺ or Mg. However, these were not experimentally measured, and therefore had to be calculated during the modelling process. The main method resulted in the experimental data being normalised so that the relative concentration of Mg⁺, Mg or magnesium ion species of interest was unity when no reactants were present.
  
Then, in order to allow the model results to be directly comparable with the experimental results, a scaling procedure was used to find the value for the initial
Mg⁺ or Mg concentration, which resulted in a final concentration of unity at the mass spectrometer or LIF detection cell. If this method could not be employed then the
initial magnesium concentration had to be included as a second fitting parameter, which required a 2-dimensional minimisation model. 

This model was written in Fortran and I worked on updating, improving and modifying the code in order to analyse all of my experimental data. An example of the differential equations solved by the model (for the reaction Mg<sup>+</sup>.X + Y) are shown below:

![]({{site.baseurl}}/images/diffexample.png)	

The model output a best-fit to the data (solid line), error margins (dashed lines) and the resulting rate coefficient:

![]({{site.baseurl}}/images/modefit.png "An example of data obtained during experiment and model fit.")	

## Results

There were a lot of interesting results obtained from my work and I won't go into all of them here - more, I will touch upon the most interesting points. 

_### Earth's atmosphere_

As mentioned above there is a large Mg+/Mg ratio, that could only be explained by a difference in chemistry, compared to other meteoric metals. 

The large ratio of Mg⁺:Mg can be explained by the fast reaction of MgO<sub>2</sub><sup>+</sup> and MgO<sup>+</sup> with atomic O. The rate at which this proceeds is an order of magnitude larger than the analogous reactions of iron and calcium. 

![]({{site.baseurl}}/images/oreact.png)	

This difference allows rapid recycling of Mg⁺-containing ions back to Mg⁺, hence Mg⁺ ions have longer lifetime in the upper atmosphere compared with the other metallic ions. It was also found that the neutral magnesium reservoir species is relatively stable to reaction with atomic H, which leads to efficient removal of Mg atoms from the underside of the Mg layer, which combined with rapid recycling of Mg⁺ ions creates the observed large ion/neutral ratio.


_### Martian Atmosphere_ 

Like the Earth, other planetary bodies in the solar system are subject to a continuous bombardment of interplanetary dust. Low-lying plasma layers, a few km wide, have been observed in the Martian atmosphere around 90 km. These layers of plasma exist in the aerobreaking region of the Martian atmosphere where meteoroids ablate and it has been proposed that they consist of metallic ions by analogy with the terrestrial atmosphere. These Martian plasma layers resemble sporadic E layers found in the terrestrial atmosphere, which consist mostly of Fe<sup>+</sup> and Mg<sup>+</sup> ions. However, metallic ions in the CO<sub>2</sub>-rich Martian atmosphere would be rapidly neutralised by formation of metal-CO<sub>2</sub> cluster ions, followed by dissociative electron recombination.

blerb about CO2 as third body
used results in model
what found

Final link guffins

