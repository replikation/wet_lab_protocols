QC Results
===
# Samples

* 5.11.2018
* used the [metagenome]FAST-DNA-BeadBeating.md protocol
* used the "best" DNA approach, and changed bead beating
  * 0.4 ml initial sludge
  * one additional humic acid removal wash step
* used reactor G1 and GR2 in mixture

> GR1 and 2 originate from Uppsala Co-digestion plant and are fed a mixture of household waste and slaughterhouse waste. These reactors operate at mesophilic temperature (37C) and at high nitrogen levels (approx. 8-10 g/L).

# QC Results
## DNA amount

* dsDNA via Qubit

| ID | sludge [ml] | humic wash |  bead beating | dsDNA [ng/µl]
| -| -------- | ---| ---|----|
| 1 | 0.4 | yes | 6m/s 2x 20s |544 |
| 2 | 0.4 | yes | 6m/s 2x 20s | 598|
| 3 |0.4 | yes | 4m/s 2x 20s | 610|
| 4 |0.4 | yes | 4m/s 2x 20s | 446|
| 5 | 0.4| yes | 6m/s 20s | 482|
| 6 | 0.4 | yes | 6m/s 20s | 434|
| 7 | 0.4 | yes | 4m/s 20s | 494|
| 8 | 0.4 | yes | 4m/s 20s | 470||



## DNA gel

* 5 µl sample; 6 µl H2O; 2 µl dye
* 5 µl marker
* 1k marker (from top to down 20kb 10kb 7kb **5kb**)

![image_of_Biorad_2018-11-05](https://raw.githubusercontent.com/replikation/wet_lab_protocols/master/results/img/Biorad_2018-11-05_14hr_26min.jpg)

*Marker, 1 - 8, Marker*

# Conclusion

1. doing 2x 20s instead of 40s increased the total yield of DNA when using 0.4 ml sludge
2. doing 20s in total seems to be sufficient
3. There seems to be an increased in DNA length in comparison to biorad 2018-10-26, in detail:
  * 4 m/s vs 6 m/s; 4m/s more higher bands and DNA in chamber
  * 20s versus 2x 20s; more longer DNA in 20s
  * Summary:
    * reducing strength and time could be to much
    * 6 m/s for 20s looks best gel-wise
4. **6 m/s for 20 s gives good DNA amount and longer DNA** than 4 m/s


Side note: if short/degrated DNAs are mainly sludge remains (e.g. plants, death cells etc.) than I would expect comparable more small DNA, if the strength is to low (less of long and fresh bakterial DNA)). This could be the explanation for the comparable lower DNA lengths in 4 m/s
