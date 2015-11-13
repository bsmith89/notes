Re-normalization of 16S survey data


### Estimating copies / g from individual species

When I collect sequence data this is what I know:

Ni = count OTUi 16S sequences [copies]
Nt = count 16S sequences in entire library [copies]
Ni / Nt = relative abundance, unitless fraction

W  = weight of the entire sample extracted (differences in full and empty weight of the tube) [g]

C  = concentration of 16S sequences in the extracted DNA Measured using qPCR [copies / uL]
G  = concentration of genomes in the extracted DNA measured using qPCR of SCHGs [genomes / uL]
V  = volume of the DNA sample after extraction [uL]
C * V = number of 16S copies extracted from the entire sample [copies]


D  = concentration of DNA extracted from the sample [ng / uL]
    

(C * V) / W = 16S copies per gram of sample [copies / g]
[(C * V) / W] * (Ni / Nt) = 16S copies from species i per gram of sample [copies / g]

### This part is harder to conceptualize

G * V = genomes in the entire sample [genomes]
(G * V) / W = genomes per gram of sample [genomes / g]
[(G * V) / W] * (Ni / Nt) = genomes of species i per gram of sample??? [genomes / g]  How does this interact with copy number variation?




