DNA sludge Preparation for MinION Sequencing
====
___
# Protocol FastDNA Spin Kit with pre Preparation steps

+ [This product for FastDNA](https://www.mpbio.com/product.php?pid=116540600&country=223)
+ protocol extends on the [FAST-DNA-BeadBeating Protocol]([metagenome]FAST-DNA-BeadBeating.md)
+ therefore sludge 0.4 ml with a humic removal wash step
+ no bead step clean up
+ 6 m/s 20s bead beating
+ **comparing yield and QC:** [**click here**](../../results/FAST_DNA-prePrep_results_1_QC.md)

## Samples

| ID | sludge [ml] | humic wash |  bead beating | prePrep
| -| -------- | ---| ---|----|
| 1z | 0.4 | yes | 6m/s 20s | rm Supernatant (a) |
| 2z | 0.4 | yes | 6m/s 20s | rm Supernatant (a)|
| 3d |0.4 | yes |6m/s 20s | DNase treatment (b)|
| 4d |0.4 | yes | 6m/s 20s | DNase treatment (b)|
| 5n | 0.4| yes | 6m/s 20s | nothing|
| 6n | 0.4 | yes | 6m/s 20s | nothing|
| 7dz | 0.4 | yes | 6m/s 20s | (a) + (b)|
| 8dz | 0.4 | yes |6m/s 20s |(a) + (b)||

## Protocol
### FastDNA Isolation

* [ ] RNase A ready
* [ ] humic acid wash solution ready


1. add **400 µl** of sludge/cells sample via 1 ml syringe to **Lysing Matrix E tube**

  (a) centrifuge (5 min 14,000g) rm supernatant, replace with same volume of H2O


2. Add **778 µl Sodium Phosphate Buffer** to Lysing Matrix E tube

  (b) add 1 µl DNase and incubate for 5 min


3. Add **122 µL MT Buffer**

  (b) add 1 µl Proteinase K and incubate for 5 min


4. Homogenize the FastPrep for **X s** at **Y m/s**, put on ice (see sample table)
5. Centrifuge at 14,000g for 15 min, 4 °C
6. Transfer supernatant to a **clean 2 ml tube**
7. add 1 µl of RNase A to each sample, incubate for 5 min
8. Add **250 µl PPS (Protein precipitation solution)** and mix carefully but efficiently by inverting at least 10 times
9. 14,000 g for 10 min 4 °C to pellet
10. Transfer supernatant to clean 5 ml tube
11. Resuspend **Binding Matrix suspension** and **add 1 ml** to the 5 ml tube
12. invert by hand for 2 min to allow DNA binding (avoid "matrix pellet" here). Place on a rack for **30-60 min** to allow settling of matrix

> Prepare humic acid wash solution:  
>> 1 ml for each sample, so 13 times:
>> 4.564 ml Sodium Phosphate Buffer
>>
>> 0.568 ml MT Buffer
>>
>> 1.166 ml PPS
>>
> * mix at full speed for 2 min
> * add 6.3 ml 5.5 M Guanidine Thiocyanat and mix

13. Remove and discard 650 µl of supernatant, **do not disturb the binding matrix**
14. Gently resuspend Binding Matrix in the remaining amount of supernatant (resuspend gently "matrix pellet"). Transfer **approx. 600 µl of the Mixture to a Spin Filter** and centrifuge at 14,000g for 1 min. Empty the catch tube and add the remaining mixture to the spin filter and centrifuge as before. Empty the catch tube again
15. add **500 µl of humic acid wash solution** to the sample (gently flick/mix) and spin at **14,000 g for 1 min** and empty catch tube
16. **Washing steps:** add **500 µl SEWS-M** and gently resuspend the pellet using a pipet tip, centrifuge for **1 min at 14,000 g**, empty the catch tube and replace
17. Centrifuge a second time at 14,000 g for 2 min to dry the membrane. Discard the catch tube and add a new clean 1.5 ml tube
18. Air dry the Spin-Filter for 5 min at RT
19. Gently **resuspend Binding Matrix** (above the spin filter) **in 70 µl 55 °C DES** (DNase free water), incubate for at least **5 min**
20. Centrifuge at 14,000 g for 1 min to get the eluate
21. Store at 4 °C
