One-pot ligation protocol for Nanopore libs LSK-109
===
* original protocol from [here](https://www.protocols.io/view/one-pot-ligation-protocol-for-oxford-nanopore-libr-k9acz2e), by Josh Quick (University of Birmingham)
* this is modified version of Josh Quicks protocol

# Checklist

* [ ] Update Software and Windows
* [ ] QC the flowcell for pore count
* [ ] 65 °C on temp block
* [ ] get ice bucket
* [ ] Prepare Qubit for later (e.g. WS = 995 µl Buffer + 5 µl QuantIT)
  * 2x 190 µl WS + 10 µl Standard; 199 µl WS + 1 µl Library
  * best during the 20 min wait



- [ ] [NEBnext ultra II endrepair](https://www.neb.com/products/e7546-nebnext-ultra-ii-end-repair-da-tailing-module#Product%20Information) on ice, buffer at RT
  - buffer precipitates - dissolve !
- [ ] [NEBnext FFPE DNA repair](https://international.neb.com/products/m6630-nebnext-ffpe-dna-repair-mix#Product%20Information) on ice, buffer at RT
    - buffer precipitates - dissolve !
- [ ] [NEBnext ultra II Ligation](https://international.neb.com/products/e7595-nebnext-ultra-ii-ligation-module#Product%20Information) & enhancer both on ice
- [ ] Nuclease-free water at RT
- [ ] AMPure beads

From the LSK Kit:
* [ ] **SQB** on RT, then on ice (vortex, spin down)
* [ ] one tube **FLB** on RT, then on ice (vortex, spin down)
* [ ] **FLT** on RT, then on ice (**mix by pipetting**, spin down)
* [ ] **LFB** on ice
* [ ] **AMX** on ice
* [ ] **EB** at RT until liquid then ice
* [ ] **LB** at RT until liquid then ice


# DNA Quality

* good DNA preparation e.g. [this protocol](../DNA_isolation/[metagenome]DNA_isolation_v.1.0.md)
* needs a initial short fragment removal e.g. [this protocol](pre_lib_cleaning.md)
* you need 400 fmol DNA in 24 μl, that means:
  * 1 µg ng DNA with a median of 5000 bp
  * 2 µg DNA with a median of 10000 bp
  * and so on...
* for metagenomic DNA of sludge, isolated via the protocols stated above:
  * **1.1 µg in 24 µl** (DNA stock was 280 ng/µl) ~ 7.7 Gb / 2 M / old_fc with less than 800 pores / labscale - frozen
  * **1.5 µg in 24 µl** (DNA stock was 336 ng/µl) - inc 10 min to 15min; less Beads in the end


# Protocol
## Library preparation

1. Set up the following end-prep reaction:

|reagent|amount| notes
|-|-|-|
|DNA (400 fmol)|	24 μl | |
|Ultra II End Prep Reaction Buffer|	1.75 μl | |
|FFPE DNA Repair Buffer |	1.75 μl| |
|Ultra II End Prep Enzyme Mix| 	1.5 μl| |
|FFPE DNA Repair Mix|	1 μl| |
|**Total**|**30 μl**| gently flick| |

2. Incubate at RT (**20°C**) for **15 min**
3. Incubate at **65°C** for **15 min**
4. Place on ice for exactly **30 s**
5. Add the following **directly** to the previous reaction:

|reagent|amount|notes
|-|-| -|
|AMX |5 μl| |
|Ultra II Ligation Master Mix|	33 μl | viscous in pipette |
|Ligation Enhancer|	1 μl ||
|**Total**|**69 μl**|gently flick|

6. Incubate at **RT** for **20 min**
7. Add **30 μl Ampure XP beads**, shake gently via hand
8. Incubate at **RT** for **10 min**
9. Spin down briefly and place on a magnetic rack until solution clears
10. Taking care to avoid the pellet remove the supernatant.
11. **(wash 1/2)** Add **250 μl LFB** and resuspend by gently shaking via hand
12. **(wash 1/2)** Spin down briefly and place on a magnetic rack until solution clears
13. **(wash 1/2)** Taking care to avoid the pellet remove the supernatant slowly
14. **(wash 2/2)** Add **250 μl LFB** and resuspend by gently shaking via hand
15. **(wash 2/2)** Spin down briefly and place on a magnetic rack until solution clears
16. **(wash 2/2)** Taking care to avoid the pellet remove the supernatant slowly
17. Spin down again, put on magnet and remove all residual LFB with a **10 µl pipette**
18. Add **12 μl EB** and resuspend beads by flicking
19. Incubate at **RT** for **10 min**
  > meanwhile do **Step A** (flowcell priming)
20. Spin down briefly and place on a magnetic rack until solution clears (Supernatant = *Library*)
21. In a new tube prepare library dilution for sequencing:

|reagent|amount|notes|
|-|-|-|
|SQB| 37.5 µl| check that its clear! |
|LB | 25.5 µl| homogenoize via pipetting |
| *Library* | 12 µl||
|**Total**| 75 µl	 |||

22. Mix by gently flicking before removing **2 µl to assess concentration by Qubit** (wait until beads have settled before measuring)

**Expected Qubit results**
* Expected recovery is 50-80% of starting material
* lower recovery indicates presence of short fragments
* The recovery rate should be around 5-10 ng/µl
* could be "out of range" for Qubit

## Library loading & priming

**Step A:**
- Add **30 µl FLT** (mix with pipett first) to one full tube of **FLB** (= **FLB-FLT**)
- open priming port
- Remove 20-25 µl of yellow storage solution (use yellow pipette)
- Take 800 µl **FLB-FLT** using a blue Pipette
  - reduce Volume on pipette a bit until drop appears (to avoid bubbles to the cell)
- Load **FLB-FLT** to priming port, avoiding the introduction of air bubbles
- wait at least 5 min (don’t close port)

> Step B after at least 5 min

**Step B:**
- **open the SpotON sample port** (all ports now open)
- Load **really slowly** 200 µl **FLB-FLT** to the priming port avoiding the introduction of air bubbles
- Mix library gently by flicking
- Add all of Library via the SpotON port in a **dropwise fashion**
    - if it won't "go in" slowly close and reopen the spotON port **a bit** to press the first drop into it
- Ensure each drop flows into the port before adding the next
- close the SpotON sample port
- close the priming port
- check if both ports are closed

**Start the MinION sequencing run for 48 h with active channel selection enabled**

## Refueling

* repeat every 22-24 h
* mix 35 µl nucl. free water with 35 µl SQB (make sure that SQB is clear before using it)
* open the priming port and SpotON port
* Add 70 µl of the "Refuel-Mix" via SpotON port in a drop wise fashion (like the prepared DNA sample)
* if the first drop is not going in, do the following steps:
  * SpotON is usually clogged (beads, buffer remains etc.)
  * close both port openings from the waste storage part with your fingers (**not** the SpotON and priming port - the other two openings on the flow cell)
  * slowly push a litte air via a 100-200 µl pipett through the priming port
  * this should free the SpotON (you basically push a bit liquid through the SpotON port)
  * if it was done correctly the previous drop should now go in
* add the remaing "Refuel-Mix" via SpotON port in a drop wise fashion
