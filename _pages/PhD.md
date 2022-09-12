---
layout: page
toc: true
title: My PhD
permalink: /PhD/
categories: [kinetics, statistics, mathematics, physics, science, computer modelling]
description: A overview of my PhD work

---
# Magnesium Chemistry in the Upper Atmosphere of Earth and Mars

This page offers a brief overview of the work undertaken during my PhD - with a focus on modelling and analysis. 

# Introduction  

The frictional ablation of cosmic dust deposits metals into the upper atmospheres of Earth and Mars.  Magnesium is one of the most abundant metals in this cosmic dust and large concentrations have been observed in the Earth’s upper atmosphere.
In the terrestrial atmosphere the peak concentration of Mg⁺ ions lie at higher altitudes (90 - 100 km) than the neutral Mg atoms (~89 km). Other metals (Fe, Ca and Na) have been observed using ground-based LIDAR. However magnesium can not be viewed this way as the wavelengths required (280 and 285 nm for Mg⁺ and Mg, respectively) are absorbed by the ozone layer. Therefore, satellite and rocket measurements were utilised to measure the concentrations, altitudes and global densities of the Mg⁺ and Mg layers. A striking difference between magnesium and other meteoric metals is the large ratio between Mg⁺ and Mg - which is even more striking as Mg⁺ is not depleted relative to other metals in the upper atmosphere. This could not be explained by differential ablation, which affects the Ca⁺/Ca ratio. Thus, a difference in chemistry was the likely explanation for this ratio, and will be discussed later[LINK].   

## Experimental

The aim of the experimental systems was to make gas phase kinetic measurements so that rate coefficients could be obtained - to help facilitate the understanding of the chemistry of magnesium in the upper atmosphere.  I undertook measurements on many of the reactions shown in the scheme below.

![]({{site.baseurl}}/images/reactscheme.png "Magnesium Reaction Scheme")

Two experimental systems were utilised; PLP/LIF (pulsed laser photolysis/ laser induced fluorescence) and a fast flow tube. These will not be discussed in detail here, but I gained a vast amount of experience using lasers, pumps, timing instruments, vacuum systems and a mass spectrometer.  I will not discuss these systems here, however, detailed experimental setups are available in [my publications](https://www.linkedin.com/in/lottes-salter/details/publications/). 

## Analysis

The following reactions were studied in the PLP/LIF system:

Mg⁺ + O₃ → MgO⁺ + O₂  
Mg⁺ + N₂O → Mg⁺.N₂O  
Mg⁺ + X  → Mg⁺.X (where X = O₂, CO₂, H₂O and N₂)  

Mg+ was monitored at an increasing time-delay so that a sufficient decay profile could be built up, as shown below.

[PIC OF DECAY]

The loss of Mg⁺ ions can be described by the pseudo first-order decay coefficient k′ as, during experiments, the concentration of the reactant and bath gases were kept well in excess of Mg⁺. For reactions with O3 :

![]({{site.baseurl}}/images/ko3.png)	

and for the other reactions:

![]({{site.baseurl}}/images/kx.png)

where kX is the rate coefficient for the reaction of Mg+ ions with the selected reactant; kDiffMg+ describes the diffusion of the Mg+ ions out of the volume defined by the intersection of the laser beams within the field of view of the detector; kMgX is the rate coefficient for the reaction between Mg+ and either the organometallic precursor or any degradation/photolysis products. The value of kDiffMg+ + kMgX was determined from a fit of the decay when the concentration of reactant equalled zero. The pseudo first order rate coefficient, k′, was obtained by fitting the experimental decay to a simple single exponential form, A + B-k′t as illustrated by the solid line in the above figure. 

The following reactions were studied using various iterations of the fast flow tube (where X = O₂, CO₂, H₂O and N₂):
Mg⁺.X + X → Mg⁺.X₂ (where X = O₂, CO₂, H₂O and N₂)  
Mg⁺.X + Y → Mg⁺.Y + X (where X = O₂, CO₂, H₂O and N₂)  
  
MgO + O → Mg + O₂  
MgO₂ + O → MgO + O₂  
MgO₃ + O → MgO₂ + O₂  
MgCO₃ + O → MgO₂ + CO₂  
MgO + CO → Mg + CO₂  

Obtaining rate coefficients from the fast flow tube data required the use of a 2-dimensional minimisation model, in which differential equations were solved to find the solution which best fitted the experimental dependence. An example (for Mg⁺.X + Y) of these differential equations is shown below:

![]({{site.baseurl}}/images/diffexample.png "Differential equation for the reaction Mg⁺.X + Y")

where kswitch is the rate coefficient of interest, kx is the second-order rate coefficient for the reaction between Mg⁺ and X, kx2 is the second-order rate coefficient for the reaction between Mg⁺.X and X, kY is the recombination reaction between Mg⁺ and Y and kdiffMg⁺ is the loss of Mg⁺ within the flow tube (i.e. to the walls).



