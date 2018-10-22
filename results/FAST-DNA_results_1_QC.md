# Quality control (Results)
**Nanodrop & Qubit - ranges for good DNA**
* OD 260/280 ~ 1.8
* OD 260/230 ~ 2.0-2.2
* dsDNA amount (should be like 100 ng/µl)

**table: Samples of FastDNA KIT** n.m. = not messured, used sludge of the B1 reactor - Krarngarden + Albumin

|#| Sample type | 260/280 | 260/230 |Qubit [ng/µl]| Nanodrop [ng/µl] DNeasy|
|---|- |- | -------- | --|-|
|1| sludge.6.40.V1   | 1.7|1.3|77|27|
|2| sludge.6.40.V2   | 1.66|1.35|97|-
|3|  sludge.5.40.V1   | 1.71|1.38|72| 38|
|4| sludge.5.40.V2   | 1.72|1.3  | 75| -
|5 | sludge.6.30.V1   |1.66 |1.05  | 79| 13|
|6 | sludge.6.30.V2   | 1.68 |1.29  | 99|-
|A | Z3.6.40   | 1.6 |0.67  | 4|-
|B |coCulture.6.40   | n.m. | n.m. | 2|-
|C |Z3.5.40   | n.m. | n.m. | 6|-
|D |coCulture.5.40   |n.m.  | n.m. |to low |-
|E |Z3.6.30   | n.m. |n.m.  | 8|-
|F |coCulture.6.30   |n.m.  |n.m.  |to low |-
> High contaminations at 230 nm
>![](https://i.imgur.com/235Jo57.png)

## Agarose Gel, for Degration control
*main Bands should be at around 30 kb*
* observed DNA degration
* DNA starts under 10kb, degrades till 1kb
* cultures produced single bands are around 10kb
* no observation between different bead beating
> ![](https://i.imgur.com/jasiBR8.jpg)
> Figure: **Marker, Sample 1 to 6 - sludge, Marker, Sample A to F - culture**
> * Used 5 µl of Marker and 1 µl sample of sludge (1-6) and 6 µl sample of culture (A-F)
 ## Possible Solutions
 * high degration visible in the gel except for the cultured DNA (could be a sludge thing)
     * Ampure x 0.4 volume of Beads could be a solution (like i did in my adjusted protokoll)

 * all samples and culture still had high salt/protein concentrations (need additional or another clean up)
     * additional clean up required
     * due to the low band length maybe an DNeasy clean up?

>**Results of the DNeasy clean up:**
>* used sample 1, 3 and 5
>* lost roughly 50 - 60 % of DNA
>* still way to much contaminations inside
>* could be remaining humic acid due to the elevated part between 220 to 260nm
>* DNA to RNA ratio is 1.8 however
>* DNA to Protein is still at 1 to 1.3 (should be 2)
>
 >![](https://i.imgur.com/l4nOZ18.png)

> Bettina's samples
>![](https://i.imgur.com/PGI7P6x.png)



## Other clean up approaches

1. Humic acids are rich in aromatic rings and aliphatic chains so my suggestion is to extract your genomic DNA solution with one volume of phenol:chloroform:isoamylic alcohol (15:14:1 vol.)
 * isoamyl is an optional antifoaming agent

> * pool the 3 samples from the DNeasy clean up (1,3,5)
> * take the sample 2 and 4  (6 remaining)
>>* using PCI from Roche (25:24:1)
>>
>>
> * fill up each sample to 656 µl using TE buffer with EDTA pH8 (500 µl for the pooled)
> * add 4 µl Proteinase K to each sample, inc. 5min
>
>> **Wasching with PC solution, repeat 2 times**
>> * add 700 µl PC to each sample
>> * 1 min at 14000 rpm
>> * retreave upper aquaeous phase into a new tube
>>
> * add 1 ml 96% Ethanol to each sample and put it for 30 min in the fridge
> * centrifuge at 13000 rpm for 10 min remove supernatant
> * wash pelett with 70 % Ethanol (5 min 13000 rpm)
> * dry on air until all of the Ethanol is gone
> * resolve in 40 µl of dd water or TE buffer (without EDTA)
> * solve it at least overnight
>
>**Results**
>![](https://i.imgur.com/Bjh3yRD.png)
>
> * DNA highly reduced, still lots of RNA, but the Protein ratio is good
> * 260/280 = 1.38 (should be 1.8); 260/230 = 1.88 (thats okay)
> * need to improve the selective DNA extraction during PCI - but it could be that the proteins/humic acid are stuck to the DNA and therefore removing my DNA during the PCI (?)
> * seems like i did a RNA selective extraction(?) DNA reduced RNA not...
> * need to check the precipitation protocoll
> * FastDNA & PCI Extraction could get rid of the protein
> * need a better RNase inclusion (**incubation step before PCI for instance**)



2. get rid of humic acid by using a PEG/NaCl precipitation, during extraction, see [this publication](http://link.springer.com/article/10.1007%2Fs10295-012-1217-7)

3. The Mo Bio Powersoil DNA extraction kit is an excellent method of extracting DNA - and states that it 'eliminates 100% of humic substances and other PCR inhibitors'. Here is the [link to information](http://www.mobio.com/soil-dna-isolation/powersoil-dna-isolation-kit.html).

4. As you can see in my review (Wang Y et al. Extraction of bacterial RNA from soil: challenges and solutions. Microbes Environ. 2012;27(2):111-121), all of the above suggestions will work for your samples. However, the most easy and efficient way is to purify your DNA with a MicroSpin S-400 HR column as I described in a paper (J Appl Microbiol. 2009;107(4):1168-1177). Although in  that case, it was designed for RNA extraction, it also works for DNA samples as I confirmed recently (FEMS Microbiol Ecol. 2014; 88(2):407-423).

 ____


# Other stuff
**[DNA Isolation after the Nature Paper](https://www.nature.com/articles/srep24645#methods):**

Pre Sedimentation to remove PCR inhibitors
* After thawing soil samples were pre-sedimented, allowing for processing of a greater sample volume (up to 10 g) while simultaneously removing PCR inhibitors known to be present in soil and feces
* Briefly, 30 ml of buffered peptone water (BPW) was added to 10 g of soil or feces in a 50 ml conical tube and samples were shaken vigorously before allowing to sediment for 10 min
* Supernatants, including limited soil/fecal debris, were transferred to a new 50 ml conical tube and centrifuged for 10 min at 4 300 × g
* The BPW was removed and the resulting sample pellet was rinsed with 5 ml of molecular grade sterile PBS, and centrifuged again at 4 300 × g for 10 min
* The supernatant was removed and the resulting pellet was resuspended in 15 ml of PowerBead solution before being processed with the Mo Bio PowerMax Soil DNA Isolation Kit (Mo Bio Laboratories, Solana Beach, CA, USA) according to manufacturer’s instructions (10 min bei rotation max.)
