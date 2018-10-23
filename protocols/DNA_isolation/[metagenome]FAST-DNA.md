DNA sludge Preparation for MinION Sequencing
====
___
# Protokol FastDNA Spin Kit

* [This product](https://www.mpbio.com/product.php?pid=116540600&country=223)

> best approach for nanopore sequencing is currently this FastDNA Kit with the modified steps (step 0 to 18)

+ **comparing yield and QC:** [**click here**](results\FAST_DNA-AmpBeads_results_1_QC.md)

## Samples

> current sludge sample preparation
> all soil preps are based around a vortexing step via beads

> No differences between the cultures DNA quality wise
>
>| sludge | culture | strength | time |
>| -------- | -------- | -------- |-------- |
>| 2x 0.2 ml sludge|0.2 ml Z3 0.2 ml CoCulture | 6.0 m/s|40 s|
>| 2x 0.2 ml sludge | 0.2 ml Z3 0.2 ml CoCulture | 5.0 m/s|40 s|
>| 2x 0.2 ml sludge | 0.2 ml Z3 0.2 ml CoCulture | 6.0 m/s|30 s|
> * **I sequenced the sludge sample with 6.0 m/s and 30s and got average of 850 bp but pores were intact**
> * **approx. 500.000 reads could be assigned to bacteria**
> * over 2 Mio reads also

## Protocol

0. Take **2 ml sludge**, centrifuge, remove supernatant, resolve in 200 µl water
1. add **200 µl** of sludge/cells sample to **Lysing Matrix E tube**
2. Add **978 µl Sodium Phosphate Buffer** to Lysing Matrix E tube
3. Add **122 µL MT Buffer**
4. Homogenize the FastPrep for **40-30 s** at **6-5 m/s** (see sample table)
> * add 1 µl of RNase A to each sample, incubate for 5 min (RNA messes up nanopore total yield)
5. Centrifuge at 14,000g for 15 min
6. Transfer supernatant to a **clean 2 ml tube**. Add **250 µl PPS (Protein precipitation solution)** and mix carefully but efficiently by inverting at least 10 times (to remove proteins)
7. 14,000 g for 10 min to pellet. Transfer supernatant to clean 5 ml tube
8. **Resuspend Binding Matrix suspension** and **add 1 ml** to the 5 ml tube
9. invert by hand for 2 min to allow DNA binding. Place on a rack for **3 to 30 min** to allow settling of matrix
10. Remove and discard 500 µl of supernatant, **do not disturb the binding matrix**
11. Gently resuspend Binding Matrix in the remaining amount of supernatant. Transfer **approx. 600 µl of the Mixture to a Spin Filter** and centrifuge at 14,000g for 1 min. Empty the catch tube and add the remaining mixture to the spin filter and centrifuge as before. Empty the catch tube again
12. **Humic acid removal, repeat 2 times** .
> Prepare humic acid wash solution:  
>> 1 ml for each sample, so 13 times:
>> 4.564 ml Sodium Phosphate Buffer
>>
>> 0.568 ml MT Buffer
>>
>> 1.166 ml PPS
>>
>
> * mix at full speed for 2 min
> * add 6.3 ml 5.5 M Guanidine Thiocyanat and mix

  >* Add 500 µl of humic acid wash solution to the sample (gently flick/mix)
  >* spin at 14,000 g for 1 min and empty catch tube, repeat

* **Washing, repeat 3 times**
>* Add 500 µl prepared SEWS-M and gently resuspend the pellet using a pipet tip
>* Centrifuge for 1 min at 14,000 g, empty the catch tube and replace

14. Centrifuge a second time at 14,000 g for 2 min to dry the membrane. Discard the catch tube and add a new clean catch tube
15. Air dry the Spin-Filter for 5 - 10 min at RT
16. Gently **resuspend Binding Matrix (above the spin filter) in 70 µl 55 °C DES** (DNase free water), incubate for 5 min
17. Centrifuge at 14,000 g for 1 min to get the eluate
18. Store at 4 °C
