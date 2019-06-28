Barcode and Ligation protocol for Nanopore LSK-109 and EXP-NBD104
===
* modified version of the ONT protocol

# Checklist

* [ ] Update Software and Windows
* [ ] QC the flowcell for pore count
* [ ] 65 °C on temp block
* [ ] get ice bucket
* [ ] Prepare Qubit for later (e.g. WS = 1990 µl Buffer + 10 µl QuantIT)
  * 2x 190 µl WS + 10 µl Standard; 199 µl WS + 1 µl Library
  * best during the 20 min wait



- [ ] [NEBnext ultra II endrepair](https://www.neb.com/products/e7546-nebnext-ultra-ii-end-repair-da-tailing-module#Product%20Information) on ice, buffer at RT
  - buffer precipitates - dissolve !
- [ ] [NEBnext FFPE DNA repair](https://international.neb.com/products/m6630-nebnext-ffpe-dna-repair-mix#Product%20Information) on ice, buffer at RT
    - buffer precipitates - dissolve !
- [ ] [Quick T4 DNA ligase]() on ice, NEBNext Quick Ligation Reaction Buffer (5x) at RT
- [ ] [Blunt/TA Ligase Master Mix] ()
- [ ] Nuclease-free water at RT
- [ ] AMPure beads

From the LSK-109 Kit:
* [ ] **SQB** on RT, then on ice (vortex, spin down)
* [ ] one tube **FLB** on RT, then on ice (vortex, spin down)
* [ ] **FLT** on RT, then on ice (**mix by pipetting**, spin down)
* [ ] **LFB** on ice
* [ ] **EB** at RT until liquid then ice
* [ ] **LB** at RT until liquid then ice

From the EXP-NBD104 Kit:
* [ ] **AMII** on ice
* [ ] **Barcodes** on ice

# DNA Quality

* needs a initial short fragment removal e.g. [this protocol, step 23 till end](https://www.protocols.io/view/long-read-dna-preparation-for-metagenomic-samples-w7afhie)
* you need 1 µg per Sample that you want to barcode
* tested with DNA that yielded a N50 of 38 kbp


# Protocol
## Library preparation
### Repair (for each sample)

1. Set up the following end-prep reaction for **each sample**:

|reagent|amount| notes
|-|-|-|
|DNA (1 µg)|	48 μl | |
|NEBnext DNA Repair Buffer |	3.5 μl| |
|NEBnext DNA Repair Mix|	2 μl| |
|Ultra II End Prep Reaction Buffer|	3.5 μl | |
|Ultra II End Prep Enzyme Mix| 	3 μl| |
|**Total**|**60 μl**| **gently flick**| |

2. Incubate at RT (**20°C**) for **20 min**
   + longer than original protocol, less pore clogging  
3. Incubate at **65°C** for **20 min**
4. Place on ice for exactly **30 s**
5. add **60 µl** AMPure XP beads
6. gently flick and incubate **5 min** at **RT**
7. Spin down briefly and place on a magnetic rack until solution clears


**Do the following steps with max. 4 Tubes at once**


8. Taking care to avoid the pellet remove the supernatant
9. **(wash 1/2)** Add **200 μl 80 % EtOH**
10. **(wash 1/2)** remove the supernatant slowly
11. **(wash 2/2)** Add **200 μl 80 % EtOH**
12. **(wash 2/2)** remove the supernatant slowly
13. **(wash 2/2)** Spin down, put on magnet and remove all residual EtOH with a **10 µl pipette**
14. add **25 µl Nuclease-free water** and incubate for **5 min at RT**

### Barcoding (for each sample)

|reagent|amount| notes
|-|-|-|
|repaired DNA |	25 μl | |
|Native Barcode |	2.5 μl| |
|Blunt/TA Ligase Master Mix|	27,5 μl| viscous in pipette |
|**Total**|**55 μl**| **gently flick**| |

15. incubate for **20 min at RT**
16. add **50 µl** AMPure XP beads
17. gently flick and incubate **5 min** at **RT**
18. Spin down briefly and place on a magnetic rack until solution clears


**Do the following steps with max. 4 Tubes at once**


19. Taking care to avoid the pellet remove the supernatant
20. **(wash 1/2)** Add **200 μl 80 % EtOH**
21. **(wash 1/2)** remove the supernatant slowly
22. **(wash 2/2)** Add **200 μl 80 % EtOH**
23. **(wash 2/2)** remove the supernatant slowly
24. **(wash 2/2)** Spin down, put on magnet and remove all residual EtOH with a **10 µl pipette**
25. add **26 µl Nuclease-free water** and incubate for **5 min at RT**

**now messure all the samples via Qubit**

### Adapter Ligation (pooled)

* for pooling the samples, do as follows:
  + you need 65 µl pooled DNA for the next steps
  + make sure that all samples are roughly the same amount (in ng), while using all the 65 µl
  + e.g. dont use 31 µl DNA and add 34 µl water



26. Prepare the next reaction as follows:

|reagent|amount|notes
|-|-| -|
|pooled DNA | 65 μl| |
|AMII |5 μl| |
|NEBNext Quick Ligation Reaction Buffer (5x)|	20 μl  ||
|Quick T4 DNA ligase |	10 μl ||
|**Total**|**100 μl**| **gently flick**|

27. Incubate at **RT** for **10 min**
28. Add **50 μl Ampure XP beads**, shake gently via hand
29. Incubate at **RT** for **5 min**
30. Spin down briefly and place on a magnetic rack until solution clears
31. Taking care to avoid the pellet remove the supernatant.
32. **(wash 1/2)** Add **250 μl LFB** and resuspend by gently shaking via hand
33. **(wash 1/2)** Spin down briefly and place on a magnetic rack until solution clears
34. **(wash 1/2)** Taking care to avoid the pellet remove the supernatant slowly
35. **(wash 2/2)** Add **250 μl LFB** and resuspend by gently shaking via hand
36. **(wash 2/2)** Spin down briefly and place on a magnetic rack until solution clears
37. **(wash 2/2)** Taking care to avoid the pellet remove the supernatant slowly
38. Spin down again, put on magnet and remove all residual LFB with a **10 µl pipette**
39. Add **15 μl EB** and resuspend beads by flicking
40. Incubate at **RT** for **10 min**
  > meanwhile do **Step A** (flowcell priming)
41. Spin down briefly and place on a magnetic rack until solution clears (Supernatant = *Library*)
42. In a new tube prepare library dilution for sequencing:

|reagent|amount|notes|
|-|-|-|
|SQB| 37.5 µl| check that its clear! |
|LB | 25.5 µl| homogenoize via pipetting |
| *Library* | 14 µl||
|**Total**| 77 µl	 |||


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

* repeat every 18 h (or do at least once after the first 18 h)
* mix 35 µl nucl. free water with 35 µl SQB (make sure that SQB is clear before using it)
* open the priming port and SpotON port
* Add 70 µl of the "Refuel-Mix" via SpotON port in a drop wise fashion (like the prepared DNA sample)
