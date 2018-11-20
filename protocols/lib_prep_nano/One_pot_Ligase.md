One-pot ligation protocol for Nanopore libs
===
* original protocol from [here](https://www.protocols.io/view/one-pot-ligation-protocol-for-oxford-nanopore-libr-k9acz2e), by Josh Quick (University of Birmingham)
* this is modified version of Josh Quicks protocol
* for the *one pot barcoding protocol* take a look [here](https://docs.google.com/document/d/1ch2bb-IdGbiu9TCwUrE7FP4xsQiJwHVFUQKJx6q7-v0/edit)

# What you need

* besides the kit...
* [NEBnext ultra II endrepair](https://www.neb.com/products/e7546-nebnext-ultra-ii-end-repair-da-tailing-module#Product%20Information)
* [NEBnext FFPE DNA repair](https://international.neb.com/products/m6630-nebnext-ffpe-dna-repair-mix#Product%20Information)
* [NEBnext ultra II Ligation](https://international.neb.com/products/e7595-nebnext-ultra-ii-ligation-module#Product%20Information)

**All the NEB products have compatible buffers for each enzyme**

# DNA

* need short fragment removal first, e.g. [this](pre_lib_cleaning.md)
* you need 200-400 fmol DNA in 24 μl, that means:
  * 500 - 1000 ng DNA with a median of 5000 bp
  * 1 µg - 2 µg DNA with a median of 10000 bp
  * and so on...

# Protocol

1. Set up the following end-prep reaction:

|reagent|amount|
|-|-|
|DNA (200-400 fmol)|	24 μl
|Ultra II End Prep Reaction Buffer|	1.75 μl
|FFPE DNA Repair Buffer |	1.75 μl
|Ultra II End Prep Enzyme Mix| 	1.5 μl
|FFPE DNA Repair Mix|	1 μl
|**Total**|**30 μl**||

2. Incubate at **20°C** for **10 min**
3. Incubate at **65°C** for **10 min**
4. Place on ice for **30s**
5. Add the following **directly** to the previous reaction:

|name|amount|
|-|-|
|AMX 1D|20 μl
|Ultra II Ligation Master Mix|	40 μl
|Ligation Enhancer|	1 μl
|**Total**|**91 μl**|

6. Incubate at **RT** for **20 min**
7. Add **45.5 μl Ampure XP beads**
8. Incubate at **RT** for **10 min**
9. Spin down briefly and place on a magnetic rack until solution clears
10. Taking care to avoid the pellet remove the supernatant.


11. (wash 1/2) Add **150 μl ABB** and resuspend by gently flicking
12. (wash 1/2) Spin down briefly and place on a magnetic rack until solution clears
13. (wash 1/2) Taking care to avoid the pellet remove the supernatant


14. (wash 2/2) Add **150 μl ABB** and resuspend by flicking
15. (wash 2/2) Spin down briefly and place on a magnetic rack until solution clears
16. (wash 2/2) Taking care to avoid the pellet remove the supernatant


17. Spin down again and remove all residual ABB with a P10 pipette
18. Add **12 μl ELB** and resuspend beads by flicking
19. Incubate at **RT** for **10 min**
20. Spin down briefly and place on a magnetic rack until solution clears (Supernatant = *Library*)
21. In a new tube prepare library dilution for sequencing:

|name|amount|
|-|-|
|RBF| 35 µl
|Nuclease-free water| 2.5 µl
|LLB | 25.5 µl
| *Library* | 12 µl
|**Total**| 75 µl	 ||

22. Mix by gently flicking before removing **1 µl to assess concentration by Qubit** (wait until beads have settled before measuring)

**Expected result**
* Expected recovery is 50-80% of starting material
* lower recovery indicates presence of short fragments
