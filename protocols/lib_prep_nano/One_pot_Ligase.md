One-pot ligation protocol for Nanopore libs
===
* original protocol from [here](https://www.protocols.io/view/one-pot-ligation-protocol-for-oxford-nanopore-libr-k9acz2e), by Josh Quick (University of Birmingham)
* this is modified version of Josh Quicks protocol
* for the *one pot barcoding protocol* take a look [here](https://docs.google.com/document/d/1ch2bb-IdGbiu9TCwUrE7FP4xsQiJwHVFUQKJx6q7-v0/edit)

# Checklist

* [ ] Update Software && QC the flowcell
* [ ] 65 °C on temp block
* [ ] ice bucket
* [ ] Prepare Qubit for later (e.g. WS = 995 µl Buffer + 5 µl QuantIT)
  * 2x 190 µl WS + 10 µl Standard; 199 µl WS + 1 µl Library
  * best during the 20 min wait
* [ ] [NEBnext ultra II endrepair](https://www.neb.com/products/e7546-nebnext-ultra-ii-end-repair-da-tailing-module#Product%20Information) on ice, buffer at RT
  * buffer precipitates - dissolve !
* [ ] [NEBnext FFPE DNA repair](https://international.neb.com/products/m6630-nebnext-ffpe-dna-repair-mix#Product%20Information) on ice, buffer at RT
    * buffer precipitates - dissolve !
* [ ] [NEBnext ultra II Ligation](https://international.neb.com/products/e7595-nebnext-ultra-ii-ligation-module#Product%20Information) & enhancer both on ice
* [ ] RBF on ice
* [ ] ABB on ice
* [ ] AMX 1D on ice
* [ ] ELB at RT until liquid then ice
* [ ] LBB at RT until liquid then ice
* [ ] Nuclease-free water at RT
* [ ] AMPure beads

# DNA Quality

* good DNA preparation e.g. [this protocol](../DNA_isolation/[metagenome]DNA_isolation_v.1.0.md)
* needs a initial short fragment removal e.g. [this protocol](pre_lib_cleaning.md)
* you need 200 - 400 fmol DNA in 24 μl, that means:
  * 500 - 1000 ng DNA with a median of 5000 bp
  * 1 µg - 2 µg DNA with a median of 10000 bp
  * and so on...
* for metagenomic DNA, isolated via the protocols stated above:
  * **2 µg in 24 µl** is sufficient (DNA stock was 232 ng/µl)
  * also good results with **3.6 µg in 24 µl**  (DNA stock was 450 ng/µl) - but more loss in the end

# Protocol
## Library preparation

1. Set up the following end-prep reaction:

|reagent|amount| notes
|-|-|-|
|DNA (200-400 fmol)|	24 μl | |
|Ultra II End Prep Reaction Buffer|	1.75 μl | |
|FFPE DNA Repair Buffer |	1.75 μl| |
|Ultra II End Prep Enzyme Mix| 	1.5 μl| |
|FFPE DNA Repair Mix|	1 μl| |
|**Total**|**30 μl**| gently flick| |

2. Incubate at RT (**20°C**) for **10 min**
3. Incubate at **65°C** for **12 min**
4. Place on ice for exactly **30 s**
5. Add the following **directly** to the previous reaction:

|reagent|amount|notes
|-|-| -|
|AMX 1D |20 μl| |
|Ultra II Ligation Master Mix|	40 μl | viscous in pipette |
|Ligation Enhancer|	1 μl ||
|**Total**|**91 μl**|gently flick|

6. Incubate at **RT** for **20 min**
  * meanwhile prepare the **Priming Solution**

> |reagent| amount|
> |-|-|
> |RBF| 	480 µl
> |Nuclease-free water|	520 µl
> |**Total** |	1000 µl

7. Add **45.5 μl Ampure XP beads**, shake gently via hand
8. Incubate at **RT** for **10 min**
9. Spin down briefly and place on a magnetic rack until solution clears
10. Taking care to avoid the pellet remove the supernatant.
11. **(wash 1/2)** Add **150 μl ABB** and resuspend by gently shaking via hand
12. **(wash 1/2)** Spin down briefly and place on a magnetic rack until solution clears
13. **(wash 1/2)** Taking care to avoid the pellet remove the supernatant
14. **(wash 2/2)** Add **150 μl ABB** and resuspend by gently shaking via hand
15. **(wash 2/2)** Spin down briefly and place on a magnetic rack until solution clears
16. **(wash 2/2)** Taking care to avoid the pellet remove the supernatant
17. Spin down again and remove all residual ABB with a **10 µl pipette**
18. Add **12 μl ELB** and resuspend beads by flicking
19. Incubate at **RT** for **10 min**
  * meanwhile you can do **Step A** for the flowcell priming
20. Spin down briefly and place on a magnetic rack until solution clears (Supernatant = *Library*)
21. In a new tube prepare library dilution for sequencing:

|reagent|amount|
|-|-|
|RBF| 35 µl
|Nuclease-free water| 2.5 µl
|LLB | 25.5 µl
| *Library* | 12 µl
|**Total**| 75 µl	 ||

22. Mix by gently flicking before removing **1 µl to assess concentration by Qubit** (wait until beads have settled before measuring)

**Expected Qubit results**
* Expected recovery is 50-80% of starting material
* lower recovery indicates presence of short fragments
* I recovered 1.4 µg (18.8 ng/µl in 75 µl) out of the initial 2 µg DNA (70 % recovery)

## Library loading & priming

**Step A:**
- open priming port
- Remove 20-25 µl of yellow storage solution (use yellow pipette)
- Take 800 µl Priming solution using a blue Pipette
- change the Pipette settings to 780 µl (Priming solution still in pipette)
- Load 780 µl to priming port avoiding the introduction of air bubbles
- wait at least 5 min (don’t close port)

> Step B after at least 5 min

**Step B:**
- **open the SpotON sample port** (all ports now open)
- Load **really slowly** 200 µl to the priming port avoiding the introduction of air bubbles
- Mix library gently by flicking
- Add all of Library via the SpotON port in a **dropwise fashion**
    - if it won't "go in" slowly close and reopen the spotON port **a bit** to press the first drop into it
- Ensure each drop flows into the port before adding the next
- close the SpotON sample port
- close the priming port
- check if both ports are closed

**Start the MinION sequencing run**
