# ezRAD_protocol

ToBo lab EzRAD Protocol-v2.0-gel free
 
 
Introduction
One of the hardest things with the RADseq protocols is knowing how much can you get away with and still get data! This protocol will go through every step to try and help you get genomic data from non-model organisms. Determining from gels what to do/how to salvage your samples and determining how much DNA you really have to have to get it through the Illumina kit and still pass the quality control steps at the end. Our test species were cnidarians, which are notoriously difficult to work with, along with sponges, echinoderms, some mollusks etc. So we hope this protocol is useful to many people who work on a range of organisms. 
 
What’s possible?
Each sequencing system is different, but the library output is the same. For sequencing we currently use the Miseq, which can run 1 flow cell with 2 lanes, one of which is a control lane. On the remaining lane we run 8 libraries to maximize coverage and reduce costs. Primarily we choose to use the Miseq because with the current reagent kits it can sequence 300bp paired-end reads (i.e. 600bp total), which is considerably longer than the Hiseq, which only sequences 100bp paired end reads; however, the Hiseq does have its benefits in that you can load more samples per lane and get considerably more reads per library. 
One of the main differences between ezRAD and other RADseq techniques is that you can end up not only with stacks (vertical coverage), which can be used to call SNPs, but also considerable horizontal coverage. This horizontal coverage means that we can get exceptionally long contigs, resulting often in the resolution of a large percentage, if not all, of the mitochondrial genome amongst other regions (e.g. histones), making ezRAD a very versatile technique.
Also with ezRAD each library can either consist of one individual or a pool of individuals from the same species. The latter requires more work, but the amount of DNA per extraction is less so is easier to reach the goal of 1ug of DNA when entering the Illumina protocol. There is also more than one type of Illumina kit for DNA TruSeq library preparation, primarily ones which are PCR-free and require 1μg of input DNA, and ones which only need 100-200ng (nano kits), so almost anything can be successfully made into a library. You can also purchase both kits in the low-throughput (24 libraries) format or the high throughput format (96 libraries, with dual indexing).
 
Table of Contents
Step 1: Extractions
Step 2:  Are your extractions ok?
Step 3: DNA Quantification
Step 4: Concentrating your DNA
Option 1: SpeedVac (if eluted in water)
Option 2: Bead clean (if eluted in a buffer solution)
Option 3: Spin columns (if eluted in a buffer solution)
Option 4: Precipitation protocol (if eluted in a buffer solution)
Step 5: Digest
Step 6: Ampure XP bead clean up
Quick reference volumes for bead cleans for different steps (DNA:beads):
Step 7: Quantify DNA (optional)
Step 8: Illumina library set-up
Step 8.1: End-repair and size selection
Step 8.2: Adenylate 3’ Ends (A-tailing)
Step 8.3: Ligate Adapters
Step 8.5: Enrich DNA fragments- Nano kit only
Step 9: Validate your library
Appendix 1: Setting up a lab to do ezRAD
Appendix 2: Removed from this protocol, but still in old versions
 
 
 
Step 1: Extractions
The collection and storage of samples is very important in determining how easy it is to get your samples ready to put through the Illumina kit. For most species you should preferentially collect/store samples in DMSO. Ethanol and even dried samples can work but the DNA is often degraded and involves extra clean-up steps and even the use of the Illumina nano kit, which only requires 100ng to make the libraries.
The Qiagen or Omega tissue and genomic DNA extraction kits work well, but any extraction method that yields high quality clean extractions will work.
 
The goal of the extractions is to get at least 1ug of good quality DNA in 25ul in order to run the digest.
Notes: 
1.     For coral in particular to increase the yield, double the amount of tissue and reagents up until the sample is put through the filter. These larger fragments are around 0.5-1cm3 and if necessary the skeleton should be crushed (i.e. with corals). 
2.     Fresh coral samples can yield degraded DNA because of the mucous they produce so an optional step is to put them in DMSO/ETOH at least overnight before extracting. 
3.     If your samples are in ethanol select the piece you wish to extract and leave them on a piece of tissue for 10-15 minutes to allow the ethanol to evaporate.
4.     Do the optional RNase A step in the protocol. The RNase A final concentration is at 20mg/µl and is aliquoted into separate Microcentrifuges and stored in the large freezer on the right on the top shelf. 
5.     Elute the DNA in water not the elution buffer so that you can concentrate the DNA using the SpeedVac instead of having to do a precipitation, which can result in the loss of a lot of your DNA. Also warm this elution water to 70°C as you would for the buffer.
6.     For coral extractions do 3 or 4 elutions (stored in separate tubes):
 
1st elution of 35 µl. This is the most important elution. It often holds a lot of low quality DNA and additional contaminants, which are now eliminated from you subsequent extractions. Alternatively if you’re lucky it can also contain all of your high quality DNA, which is then highly concentrated enough that it can go straight to the digestion step without the need for using the Speed-vac. This elution is specifically 35ul because the digestion requires 25ul and if the sample concentration is high enough the additional 10ul gives you enough volume to run a gel and quantify the sample and still go straight to the digestion. Also if this elution needs to be discarded (because it has all of the low quality DNA) you are not throwing out much of your sample. 
2nd elution of 50 µl. The volume of this elution is also low because it can also have enough good quality DNA to go straight into the digestion without using the Speedvac and may also have the added benefit of having some of the low quality DNA removed in the first elution.
3rd and 4th elutions of 50-100µl each (or 3 x 50 µl elutions, as sometimes the later elutions are the best) and store them together or separately. 
Once you know what works for your species you can reduce the number of elutions if necessary. 
Preferably you will get enough DNA to make a backup, just in case the first library prep you do doesn’t work.
 
 
Step 2:  Are your extractions ok? 
 
First things first there are 2 exceptionally important thing to do throughout the protocol:
1.              Make sure that before any step, where you DNA has been sitting in a fridge or freezer, that you thoroughly mix and spin down the sample. I can’t stress how important this is! It will affect your gels, quantitation, pooling etc. 
2.              Watch your pipetting, literally! This is especially important when using the multiwall pipettes as some tips can loosen. There are often markers on pipette tips, use them. Get to know what 1 or 2ul looks like, it will improve your lab work.
 
Run a gel on your extractions to see the quality of your DNA (here I will assume that most people know how to run a gel, if not someone in the lab will). 
 
From your gel you determine what to do next. Successful libraries were produced from the vast majority of samples in the gel below (Figure 1), including number 1-6, 8-10 and 12, which clearly have variable quantities and qualities. Sample 7 and 11, once digested and cleaned only had ≤ 200ng, so these would be more suitable for the nano kit. So you can see that almost every sample is usable. However, it is still best to aim for high quality extractions as this may affect the quality of data you get from the sequencer.
 
If you have high molecular weight bands (e.g. samples: 2, 9 and 10) that’s perfect and if you have a smear (e.g. samples: 1, 3, 4, 8, 11, 12) then that is workable, you should now quantify your DNA (see below). If you have a bright low band i.e. a large amount of low quality DNA and a smear (e.g. samples: 5 and 6) then the samples can be cleaned with the Ampure beads before quantifying. If you only have a bright low band on the gel (e.g. sample 7 or worse) then if you clean the samples first (and quantify it) then this may work at least with the nano kit, which only needs 100ng DNA, alternatively try re-extracting.
 
 
  
 
Figure 1. 1% agarose gel ran on 12 scleractinian coral extractions using HyperLadder 1 and GelStar nucleic acid stain.
 
Below is a table of the final DNA concentration for each sample put through the Illumina kit. All the samples worked and passed the final quality controls, so again it’s clear that the kit is somewhat flexible to the quantity of input DNA as well as the quality. Essentially with the PCR-free kit it is preferable to start with 1.3 ug but ≥600ng also works.
 
Table 1. The total amount of DNA per sample put into the Illumina protocol after extraction, digest and clean-up. All of these samples made successful libraries passing both quality control (QC) steps (qPCR and bioanalyzer).
 
Sample	Total DNA (ng)
1	500
2	700
3	700
4	600
5	430
6	750
8	800
9	800
10	800
12	1000
 
 
 
 
Step 3: DNA Quantification
For the greatest accuracy we use AccuClear Ultra high sensitivity dsDNA quantitation kit with 1 or 7 DNA standards (plus one blank (0ng/μl) standard making 8 standards in total). 
Note: the 1 standard kit is cheaper but you have to prepare the other 7 standards through serial dilutions (instructions are provided with the kit) but this takes time as “the two lowest concentration DNA dilutions (H, I) should be prepared fresh on the day of assay. The other DNA dilutions (B-G) can be stored at 4o C for at least 6 months with the addition of 2 mM final concentration sodium azide.”-Taken from the AccuClear protocol.
Nanodropping may provide sufficient accuracy when samples have been cleaned, but the microplate AccuClear assay can be used throughout the protocol because the detection of dsDNA is not affected by single stranded RNA or DNA or common contaminants such as proteins, salts and organic solvents. Also this kit is designed to detect DNA concentration accurately from 0.03 to 250ng per assay (well), which should cover most samples.
 How the setup the AccuClear quantitation:
 
 
 
Figure 2. AccuClear can quantify a large number of dsDNA samples in four easy steps. Image taken from the Biotium website, see link here.
 
 
 
 
 
Equipment/required reagents: 
Note: Take all reagents out of the fridge 30 minutes before using!
•	AccuClear dye- because it is stored in DMSO it can form crystals, if so shake it till they’re gone.
•	AccuClear buffer- make sure this is at room temperature before beginning
•	DNA Standards (if there is only 1 need to serially dilute it to make 8, see below)
•	Multiwell pipette 
•	If available a 10ml or 20ml pipette (not essential, but makes it easier)
•	Black 96-well plate
•	Reagent trough/reservoir 
•	Timer
•	Multiplate reader
•	Excel
 
Method for DNA quantitation:
1)    Let the reagents warm up to room temperature for at least 30 minutes! This takes more/less time depending on the volume in the bottle.
2)    Prepare a working solution immediately before use. The mixed solution will be transferred to a 96-well plate using a multiwall pipette so mix the 2 solutions in something like a reagent trough/reservoir. 
3)    For a 96-well plate add 200 µl of dyeto 20ml buffer in the reagent reservoir. Mix well! 
4)    If you have less than 96 samples adjust quantities accordingly. Remember that you have to run 2 rows of standards (16 in total) in addition to your samples!
Note: Once the standards appear consistent for a given kit, you can think about reducing it to 1 row of standards per plate if necessary. 
 
AccuClear calculations: 
For a 96 well plate: 200µl dye and 20ml buffer
Therefore for 1 sample = 2.083 µl dye and 0.208ml buffer
 
An example: 
If you have 52 samples (including 16 wells for standards): 
52 x 2.08 = 108.16 µl dye and 10.82 ml buffer.
 
Note: You don’t need to add any samples to account for pipetting errors, this is already accounted for in the calculations.
 
 
5)    Add 200 µl of the working solution (dye and buffer in the reagent reservoir) to each well of a BLACK 96-well plate using the multiwall pipette. (read point 6 before doing this)
6)    Add 10 µl of DNA template into the remaining wells. Mix well by pipetting up and down. If you have to be conservative with the amount of DNA template you use, you can also mix 1 µl DNA template in 9 µl of H2O and add that to the well. The easiest way to do this is on parafilm, but you have to transfer your sample into the plate fairly fast before it evaporates too much, which will affect your reading. Alternatively add the 9 µl of water and 1 µl of DNA directly into the plate before putting in the working solution.
7)    Add 10 µl of each DNA standard (0, 0.003, 0.01, 0.03, 0.1, 0.3, 1, 3, 10 and 25 ng/µl) to the last row (it is advised to run them in duplicates). The 0ng/µl should be in well A (the top of the plate). Mix for about 1 minute before putting them in the plate by flicking them (be careful that the lid doesn’t pop open) and briefly spinning them down, once in the plate mix by pipetting up and down. 
8)    Incubate the plate at room temperature for 1-5 minutes in the dark (in a drawer is fine).
9)    Whilst the sample is in the drawer turn on the microplate reader (in the Core lab), open the software SoftMax Pro 4.8 and grab a pen drive.
10) After 5 minutes get you’re samples and put them in the open drawer of the microplate reader.
11) Go to Setup and make sure the fluorescence measurements are set to 468 nm excitation and 507 nm emission (these are not the default settings).
12) Set the precision up to the highest possibly number of reads per well (which is 30 for our microplate reader) 
13) If you’re not running a whole plate select the number of columns you’re using.
14) Click OK
15) Press ‘read’.
16) Save the file to a folder in ‘users’ on the desktop. 
17) Also export the fluorescence values from the microplate-reader program as a txt file onto the pen drive.
18) If you want you can open a new file and repeat the read to check the results. Note that it is normal for the fluorescence to drop slightly between reads.
19) Close the drawer of the microplate reader (a button on the machine), switch it off and put the cover back.
20) Copy the txt file fluorescence reads into Excel. Note that the top left number is the temperature. Also once you copy the numbers into excel the first row will be adjusted 2 rows to the left, so correct this before going on. 
21) Use the excel template/protocol if you’re not sure how to do the calculations, but essentially you: 
22) Calculate the average for the standards and minus the blank
23) Make a scatterplot from the average standards (plotting the fluorescence versus the DNA concentration of the DNA standards)
24) Add a trendline with the intercept going through 0 and display the equation on the chart
25) Minus the blank from all of your samples
26) Divide your values by the linear equation given in the scatterplot. This is your DNA concentration. If you used 10 µl of the DNA template then divide this value by 10 to get ng/µl. If you only used 1 µl diluted in 9 µl of water you already have ng/µl!
27) For single sample libraries multiply by the total volume in your sample. 
 
Pooling samples
Although pooling is currently controversial and computationally more difficult to handle it may be your only option when dealing with population questions. Also with pooling you can’t currently pull out the individuals once they are pooled, but we are looking into adding an additional index before pooling to allow us to do this.
 
For the 1µg kit I will always pool 1.3µg to account for any errors in the quantitation and loss of DNA through storage (freeze-thaw cycles or fridge storage) and bead cleans (which I’ll explain later), and for the 100-200ng nano kit I will add 200ng. 
 
If you want to pool samples then you need to know how many samples you want to pool, the ng/µl in each of your samples and their total volumes.
 
For example: if you have 30 samples you want to pool, divide the target total ng of DNA you want (1300ng) by this number of contributing samples (30).
1300ng/30samples=43.3ng/sample
So you will need 43.3ng from each sample to give you an equally pooled library totally 1300ng. 
Once you know this you use the microplate results (ng/µl) to tell you how many μl you need to add from each sample.
 
There are 2 ways to pool your samples, you can either
1)    Calculate the μl needed per sample individually i.e. sample 1a has 4.7ng/µl so you need to add 9.21μl of this sample (43.3ng/4.7=9.21μl) and sample 1b has 18.2ng/µl so you need to add 2.38μl of this sample (43.3ng/18.2=2.38μl). I do this in excel and have each part of the equation in different columns so I can change things easily.
2)    Dilute all of you samples to the same concentration i.e. 4ng/µl and add the same volume from each sample to make your pools (ie 43.3ng/4 = 10.83μl from each sample). This is initially time consuming, but if things don’t work out it’s easy to go back and re-pool. It can also be a little less stressful as adding water to a sample to change its concentration is easier to correct than adding the wrong volume of a sample into the final pool.
 
Deciding on which way to pool can depend on the variability in your sample concentrations, how many samples you need to pool and personal preference. You also have to bear in mind that you’ll need to get this 1.3ng down to 25μl for the digestion, so you’ll have to spin down your samples in the Speed-Vac if you have a high volume pool, which can result in your DNA forming a pellet, so you’ll have to be aware of this fact.
 
Step 4: Concentrating your DNA 
 
Option 1: SpeedVac (if eluted in water)
The SpeedVac is in the Core lab, read the directions on the wall before using it! The machines need to be turned on/off in a particular order, ask Amy Eggers if you have any questions. 
If you eluted your extraction in water you can use a SpeedVac to evaporate off the surplus water. You have to reduce the volume of liquid to 25 µl to proceed to the next step. Depending on the initial volume of liquid it can take a few hours to do this. Only do 30 – 45 min at a time and keep an eye on how fast it evaporates. Avoid completely drying the sample! Do not use heat.
Note: if you’re evaporating your volume down a lot the DNA may form a pellet. To resuspend it just flick the tube several times.
If you eluted your DNA in buffer or if you feel brave do a DNA precipitation but you may lose a lot of your DNA during this step, especially if your yields were low. 
 
Option 2: Bead clean (if eluted in a buffer solution)
You probably only want to do this if you have a small volume or really don’t like the other 2 options below. The magnetic plates used in the rest of the protocol only fit 250 µl tubes (strip tube size) so this is around your maximum total volume (one of the bead cleans in the protocol goes up to 280 µl but this is dangerously near the top). The total volume depends on the ratio of DNA to beads, for a standard clean, I would do a 1:1.8 ratio of DNA:beads. See below for instructions on this protocol. Note also that the Ampure XP beads are expensive (≈ $1000 a bottle), so this may not be an option. 
 
Option 3: Spin columns (if eluted in a buffer solution)
Spin columns are a fast way to concentrate you're samples, but there is a fairly high loss so you need a lot more DNA to start with (at least double). Example products include:
Amicon: http://www.millipore.com/catalogue/module/c84684
Microcon: http://www.millipore.com/catalogue/module/c113861 
 
Option 4: Precipitation protocol (if eluted in a buffer solution)
This protocol has long been used to concentrate DNA, but personally I don’t like how long it takes to do and often the outcome is disappointing, but if you want to do it read on.
 We found Isopropanol (isopropyl alcohol) worked better than ETOH because of the high total volumes, but ethanol (ethyl alcohol) is most commonly used alcohol for DNA precipitation. Smaller fragments and lower concentrations take longer to precipitate out of solution so leaving your samples for longer in the freezer isn’t a bad thing. Also don’t scale up your volumes and do it in larger tubes, stick to the smaller 1.5-2ml Microcentrifuges. If you have more than 2ml reactions, aliquot out your samples to multiple Microcentrifuges. All volumes of the reagents depend on the volume of your sample. 
Reagents required per sample:
•	1.5x Isopropanol or 2-3x Ethanol (stored in freezer)
•	1/10 M 3M Sodium acetate (NaOAc)  pH 5.2
•	2ml 70% Ethanol
•	1 µl Glycogen 20mg/ml
 
Precipitation Method (volumes are an example assuming one 250 µl sample):
1) Add 25 µl NaOAc and 325 µl Isopropanol or 500-750 µl ETOH and 1 µl glycogen.
2) Put in the freezer overnight
3) Spin at max speed at 4°C for 30mins
4) Decant supernatant very carefully. You should see a small milky pellet at the bottom, avoid pouting this out! If you don’t see a pellet don’t panic just be careful when pouring off the supernatant. 
5) Add 1ml 70 ETOH and spin down for 10-15 minutes, and carefully decant the supernatant off.
6) Repeat step 5
7) leave the caps open and air dry the samples for about 30mins or until the alcohol has evaporated off
8) Re-suspend in water or low TE buffer.
9) Flick the samples and put in warm shaker for 1-2 hours (keep below 50°C)  
“Isopropanol is often the better choice when precipitating DNA from large volumes of solution. However, isopropanol also has some disadvantages.
•     Salts are less soluble in solutions consisting of 35 isopropanol than in solutions containing 65 ethanol.
•     The pellets of DNA are translucent and are difficult to see. Isopropanol is less volatile than ethanol and is therefore more difficult to remove.
•     Finally, DNA precipitated by isopropanol does not stick tightly to the wall of the microcentrifuge tube and is easily lost when the isopropanol solution is removed or when the pellet is washed with ethanol (Step 5, below).” Taken from http://www.molecularcloning.com
 
 
Step 5: Digest
This digestion step with this frequent cutter restriction enzyme is the distinguishing feature in ezRAD protocol and is the equivalent of shearing the DNA or using other less frequent cutters. This digest reaction uses the enzymes DpnII, which cleave sequences at GATC cut sites, for more information see Appendix 1. The protocol assumes the digestion of one unit per reaction, which is defined as the amount of enzyme required to digest 1 µg of λ DNA in 1 hour at 37°C in a total reaction volume of 50 µl. 
Note: We normally digest 1.2-1.3 µg per library because the DNA quantification is not 100% reliable and the potential for loss at each step is to be expected so going in with a little more gives a higher chance of the library working.
Note: If the digestion isn’t working too well or you’re concerned it might not work well then do a bead clean before doing the digest.
 
Reagents required:
Table 2. Mastermix for the DpnII restricton enzyme digestion per reaction (50 µl) for approximately 1ug of DNA.
Mastermix reagents 	(µl)
Buffer 3.1	5
HPLC grade H2O	19
DpnII	1
Total	25
 
 
 
 
 
 
Digest Method:
1)    Make a master mix for X amount of samples and add 25 µl of the master mix to your DNA template (25 µl) giving a total of 50 µl per reaction.
2)    Mix gently by pipetting up and down or flick and spin down.
3)    Run the DpnII program in your thermocycler (if you don’t have one make one) incubating the samples for:
3 hours at 37°C
20mins at 65°C
Hold at 15°C
4)    Do a bead clean before entering the Illumina protocol (refer to step 6 below), by adding 90 µl of beads to each of the 50 µl digests.
5)     At the end of the bead clean protocol re-suspend in 62.5 µl and transfer 60 µl to a new tube.
Note: If you’re samples are eluted in water you could also modify the amount of water you put in so you increase or decrease the amount of sample you put in to save time spinning down e.g. if you have 1.3ug of DNA in 30ul put in 12ul of water for that sample instead.
 
 
Step 6: Ampure XP bead clean up
The Aggencourt Ampure XP beads are designed to remove smaller fragments of DNA from your sample as well as remove any other reagents from the previous step. The ratio of sample to beads will determine what size fragments are removed. It does not matter on the concentration of DNA in your samples, but rather the volume.
 
To avoid contamination aliquot a subset of the beads into a separate tube before starting.
 
 
 
Figure 3. How the beads work: 1. DNA template without beads 2. Binding of DNA to magnetic beads 3. Separation of DNA bound to magnetic beads from contaminants 4. Washing of DNA with Ethanol 5. Elution of DNA from the magnetic particles 6. Transfer away from the beads into a new tube. Image taken from the Beckman Coulter website.
 
Reagents/Equipment required:
•	Ampure beads (stored in the fridge) - Let the bottle warm up to room temperature for at least 30 minutes!
•	Resuspension buffer/low TE buffer/HPLC grade water
•	Magnetic plate (see Appendix 1)
•	80% Ethanol
•	Multiwell pipettes (optional)
•	Reagent reservoir/trough (for use with the multiwall pipettes)
•	Waste container
•	Strip tubes
•	Thermocycler
 
Method:
The ratio of DNA template to beads depends on what you want to achieve with the wash. A ratio of 1:1.8 (DNA:beads) will wash out anything below 100bp. A ratio of 1:2 just cleans your sample. You can adjust the ratio as needed but this is not the most precise technique to try and size select due to the variability in beads that you are pipetting (especially when the volumes are low). Keep in mind that the ratio is only volume dependent, the concentration of your sample doesn’t matter. 
Shake the Ampure bead bottle until beads appear well mixed. This is very important. It is suggested to vortex them for 1 minute before starting.
The volumes will vary depending on what step in the protocol you are, see below (Table 3) for a quick reference table. 
1)    Slowly pipette the beads into the sample (see below for volumes) and mix gently by pipetting up and down (use wide bore pipettes if possible). Shake Ampure bottle every time before pipetting into another sample to ensure the beads stay well mixed!
2)    Incubate at room temperature for 5 minutes.
3)    Place samples onto the magnetic stand for 5 minutes or until the liquid appears clear. 
4)    With the samples remaining on the magnetic stand, gently remove the supernatant, leaving 5ul in the tube (this reduces the likelihood of sucking up any beads). If you want to check whether you have accidentally sucked up any beads hold the pipette up to the light or put the supernatant in a separate tube and put it back on the magnetic stand.
5)    With the samples remaining on the magnetic stand, add 200 µl of fresh 80% ethanol without disturbing the beads. You can use a multiwall pipette and a reagent reservoir/trough for this if you want.
6)    Incubate at room temperature for 30 seconds, then remove and discard the supernatant. You can also use the multiwell pipette for this as the DNA sticks to the side of the tube once the ethanol is added. 
7)    Repeat step 6 for a total of 2 washes. 
8)    Use a 20ul pipette (multiwell optional) to remove the remnants of ethanol from the bottom of the tube.
9)    With the samples remaining on the magnetic stand, let the samples air dry at room temperature for 5 minutes. It is important that the beads don’t dry out for longer than 10 minutes.
10) Remove the samples from the magnetic stand and resuspend the dried pellet in the desired volume (if you use less than 10 µl you may not get all DNA back into solution) of HPLC grade water or buffer. Gently pipette the entire volume up and down 10 times to mix the beads back into solution (use wide bore pipettes if possible).
11) Incubate the samples at room temperature for 5mins. 
12) Place the samples back onto the magnetic stand for 5 minutes or until the liquid is clear. 
13) Transfer the supernatant to a new collection tube. 
Optional steps: 
•       If you want to quantify your sample after a bead-clean step just elute your sample in an additional 3ul of resuspension buffer and take-off that additional 3ul (so you’re still leaving 2.5ul on the beads) and nanodrop the sample using 1ul per library. To ensure the most accurate quantification mix the sample well before measuring it on the nanodrop.
•       After the bead clean you can also add 5 µl to the leftover beads and keep them for later just in case, as sometimes not all of the DNA is eluted from the beads the first time.
Note: whatever final volume you want add 2.5 µl so you can cleanly get your DNA back without pipetting up any beads.
 
Quick reference volumes for bead cleans for different steps (DNA:beads):
Note: the volume you want to transfer to a new tube at the end of the bead clean is always 2.5 µl less than the resuspension/elution volume (i.e. if you resuspend the beads in 20 µl you will be transferring 17.5 µl to the new tube).
Table 3. A shortcut table listing all the ratios and volumes required for the bead cleans at each step of the ezRAD protocol. 
 
Step #	Protocol step	Ratio of DNA:beads	Volumes of DNA:beads (µl)	µl removed to leave 5 µl before ETOH clean	Re-suspension volume (µl)
5	Digest	1:1.8	50:90	135	62.5
8.1	End rep. /Size sel. (1)
(diluted beads)	See step 8.1	See step 8.1	n/a	See step 8.1
8.1	End rep. /Size sel. (2)
(undiluted beads)	1:0.8	250:30	138x2	20
8.2	A-Tailing	n/a	n/a	n/a	n/a
8.3	Ligate index adapters (1)	1:1	42.5:42.5	80	52.5
8.3	Ligate index adapters (2)	1:1	50:50	95	27.5
8.4	DNA enrichment 
(Nano kit only)	1:1	50:50	95	27.5
 
Step 7: Quantify DNA (optional)
Use the AccuClear method to quantify your samples again to make sure you didn’t lose too much DNA during the bead clean (refer to step 2). Aliquot 1 µl of your sample into 9 µl of H2O for DNA at this step quantification.
 
Step 8: Illumina library set-up
As described in step 1 there are a couple kits to choose from, a Truseq PCR-free kit (requiring 1ug input DNA) and a Truseq nano kit (requiring 200ng input DNA). The steps below are the same but with the addition of a DNA enrichment (PCR) step for the nano kit, which is not necessary with the PCR-free kit.
 
As you go through the protocol program them into your Thermocycler to make it quicker in the future (use the program names given by Illumina).
 
All the reagents are in the freezer except the Ampure beads and possibly resuspension buffer.
 
Step 8.1: End-repair and size selection
The end repair process blunt ends your DNA in preparation for adding an A-tail. This is also where the size selection occurs. There are 2 options, a 350bp insert (which we use) and the 550bp insert. We size select for the 350bp insert because we want good overlap between the forward and reverse sequences and because you need to start with 2μg if you want to select for the 550bp insert.
 
Reagents/Equipment required:
•	Sample Purification Beads-(SPBs) (provided in the Illumina kit) aka SPRI beads (at room temperature).
•	Resuspension buffer- (at room temperature) 
      aliquot into 1.5 or 5ml tubes. It can be stored in the fridge for the duration of the Illumina protocol.
•	End repair mix 2
•	Magnetic plate
•	80% Ethanol
•	Multiwell pipettes (optional)
•	Reagent reservoir/trough (for use with the multiwall pipettes)
•	Waste container
•	Strip tubes
•	2ml tube if processing ≤ 6 libraries
•	5 or 15ml tube if processing ≥ 6 libraries 
•	Thermocycler
•	60 µl of DNA (digested and clean) 
 
 
 
 
End Repair Method:
1)    Thaw End Repair Mix 2, flick to mix and spin down.
2)    Make sure the SPB’s, Resuspension Buffer are at room temperature, mix well.
3)    Add 40 µl of End Repair Mix to each sample containing 60 µl of DNA template and mix gently by pipetting up and down.
4)    Run the ERP program in you thermocycler:
Preheat the thermocycler lid to 100°C 
Incubate the samples for:
30mins at 30°C
Hold at 4°C
 
5)    Return End Repair Mix 2 to the freezer.
6)    Move straight onto the size selection.
 
Size Selection Method
1)    Vortex SPBs- make sure they are mixed well
2)    In a 2, 5 or 15ml tube (depending on the number of libraries) make a master mix of diluted beads by adding per library:
350bp insert:
•       100.84 µl of SPBs
•       69 µl of HPLC grade water
•       E.g. for 12 libraries mix 1210 µl SPBs and 828 µl water
 
550bp insert:
•       84.9 µl of SPBs
•       84.9 µl HPLC grade water
•       E.g. for 12 libraries mix 1019 µl SPBs and 1019 µl water
 
3)    Vortex the master mix
4)    Slowly aspirate and dispense 160 µl of the diluted beads to each well with your 100 µl of end-repaired sample (mix the beads every 3 samples).
5)    Gently pipette the mixture up and down until well mixed (use wide-bore pipettes if available).
6)    Incubate at room temperature for 5 minutes.
7)    Place samples onto the magnetic stand for 5 minutes or until the liquid appears clear. 
8)    Label a new strip tube
9)    The supernatant is the DNA you want, so transfer 125 µl to the new strip tube. Be careful not to disturb the beads
10) Repeat step 9 so you have 250 µl in total in the new labelled strip tube.
11) Keep the beads just in case.
12) Do a bead clean (see step 6), adding 30 µl of undiluted beads to each sample containing the 250 µl of supernatant.
13)  At the end of the bead clean protocol re-suspend in 20 µl and transfer 17.5 µl to a new tube.
 
Safe Stopping point. If you don’t proceed to the next step immediately you can store the samples in the freezer (-15 to -25) for up to 7 days.
 
 
Step 8.2: Adenylate 3’ Ends (A-tailing)
 
Reagents/Equipment required:
•       Sample Purification Beads (SPBs) or Ampure XP beads (at room temperature)
•       Resuspension buffer (at room temperature)
•       A-tailing mix
•	Magnetic plate
•	80% Ethanol
•	Multiwell pipettes (optional)
•	Reagent reservoir/trough (for use with the multiwall pipettes)
•	Waste container
•	Strip tubes
•	Thermocycler
•       17.5 µl of  DNA (end-repaired)
 
A-tailing Method:
1)  Thaw A-tailing- flick to mix and spin down.
2)  Make sure the SPB’s or Ampure XP beads, Resuspension Buffer are at room temperature, mix well.
3)  Add 12.5 µl of A-Tailing Mix to each sample containing 17.5 µl of sample and mix gently by pipetting up and down.
4)  Run the ATAIL70 program in your thermocycler:
Preheat the thermo cycler lid to 100°C 
Incubate the samples for: 
30 mins at 37°C
5 mins at 70°C
5mins at 4°C
Hold at 4°C
 
5)  Return A-Tailing Mix to the freezer. Keep the Resuspension buffer and SPBs on the bench. 
6)  Immediately remove the samples from the thermocycler and proceed to next step (ligate Adapters).
 
Step 8.3: Ligate Adapters
Reagents required:
•	Sample Purification Beads (SPBs) or Ampure XP beads (at room temperature)
•	Resuspension buffer (at room temperature)
•       DNA adapter indices
    Very important: write down the index adapters you use for each sample and bear in mind you can only have one of each adapter per lane.
•       Ligation mix 2 (leave in the freezer until immediately before use. Keep on ice once removed from the freezer).
•       Ligation stop mix
•	Magnetic plate
•	80% Ethanol
•	Multiwell pipettes (optional)
•	Reagent reservoir/trough (for use with the multiwall pipettes)
•	Waste container
•	Strip tubes
•	Ice/freezable tube rack
•	Thermocycler
•	30 µl of  DNA (A-tailed)
 
Method:
1)    Thaw appropriate DNA Adapter Index tubes and Stop Ligation Buffer. Leave Ligation Mix in the freezer until immediately before use. Keep on ice or in a frozen tube rack once removed from the freezer. 
2)    Flick and spin down all ligation reagents
3)    Add 2.5 µl of Resuspension Buffer to each sample containing 30 µl of sample.
4)    Add 2.5 µl of Ligation Mix 2 and immediately return it to the freezer.
5)    Add 2.5 µl of appropriate DNA Adapter Index and mix gently by flicking or pipetting up and down and spin down.
6)    Run the LIG program in your thermocycler:
Preheat the thermo cycler lid to 100°C
Incubate the samples for: 
10 mins at 30°C
Hold at 4°C
 
7)    Add 5 µl of Stop Ligation Buffer and mix gently by pipetting up and down.
8)    Do 2 bead cleans (refer to step 6) using a ratio of 1:1
9)    Bead clean 1-add 42.5 µl of beads to the 42.5 µl sample.
10) At the end of the clean-up elute the sample in 52.5 µl Resuspension Buffer and transfer 50 µl of the clear supernatant to a new tube.
11) Bead clean 2- add 50 µl of beads to the 50 µl sample.
12) At the end of the clean-up elute the sample in 27.5 µl Resuspension Buffer and transfer 25 µl of the clear supernatant to either a:
•     1.5ml tube with your name, individual sample ID code, and index adapter number written on the side and just the ID on the lid - for PCR-free kit.
•     New strip tube- for nano kit
 
For Truseq PCR-free kit- (1μg input DNA)
1)    Add 10 µl of the resuspension buffer to your beads and mix them.
2)    Store the beads as a backup in the -20°C freezer. The first elution from the beads does not necessarily give you all of your DNA.
3)    Go to step 9 (Validate your library)
 
For Truseq nano kit- (200 ng input DNA):
 
•	Proceed to the next step (Enrich DNA fragments)
 
Safe Stopping point. If you don’t proceed to the next step immediately you can store the samples in the freezer (-15 to -25) for up to 7 days.
 
 
 
 
 
 
 
Step 8.5: Enrich DNA fragments- Nano kit only
Required reagents:
 
•	Sample Purification Beads (SPBs) or Ampure XP beads (at room temperature)
•       Resuspension buffer (at room temperature)
•       Enhanced PCR Master Mix
•       PCR Primer cocktail
•	Magnetic plate
•	80% Ethanol
•	Multiwell pipettes (optional)
•	Reagent reservoir/trough (for use with the multiwall pipettes)
•	Waste container
•	Strip tubes
•	Ice/freezable tube rack
•	Thermocycler
•	25 µl of  DNA (with index adapters ligated)
 
Method:
 
1)    Thaw Enhanced PCR Master Mix and PCR Primer Cocktail - flick to mix and spin down. Once thawed store on ice/in a frozen tube rack.
2)    Make sure the SPB’s or Ampure XP beads, Resuspension Buffer are at room temperature, mix well.
3)    Add 5 µl of PCR Primer Cocktail to each sample containing 20 µl of DNA template.
4)    Add 20 µl of Enhanced PCR Master Mix to each sample and mix gently by pipetting up and down or flick and spin down.
5)    Run the PCRNano program in your thermocycler:
Preheat the thermo cycler lid to 100°C 
Incubate the samples at: 
3 mins at 95°C
Then for 8 cycles: 
20 secs at 98°C
15 secs at 60°C
30 secs at 72°C
Then:
5 mins at 72°C
Hold at 4°C
 
6)    Do a bead clean using the SPBs or Ampure XP beads (refer to step 6) using a ratio of 1:1, adding 50 µl of beads to the 50 µl sample.
7)    At the end of the bead clean-up elute the sample in 27.5 µl Resuspension Buffer.
8)    Transfer 25 µl of the clear supernatant to a new tube 1.5ml tube with your name, individual sample ID code, and index adapter number written on the side and just the ID on the lid.
9)    Add 10 µl of the resuspension buffer to your beads and mix them.
10)    Store the beads as a backup in the freezer. The first elution from the beads does not     necessarily give you all of your DNA.
11)  Go to step 9 (Validate your library)
Step 9: Validate your library
1)    Nanodrop 1 µl of your completed libraries and run a gel using 3 µl to check the results before freezing. Alternatively if you can’t run a gel straight away aliquot out 5 µl to run these tests so you can freeze (at -20°C) your completed libraries straight away.
Note: The nanodrop may not be reliable, so the gel might give you a better idea of how your library looks.
2)    You can then hand your completed libraries (20 µl) to Amy Eggers at the Evolutionary Genetics Core Facility (EGCF) at the Hawaii Institute of Marine (HIMB), Coconut Island for QC/library validation (Bioanalyzer and qPCR) and sequencing on the Miseq. You must fill out a Miseq submission form providing the nanodrop results and gel with the samples. It’s also advisable that you email Amy (aeggers@hawaii.edu) letting her know that you’re going to give her samples. You can also email Amy beforehand for a quote if you need one.
 
Note: Samples are not in the queue at the core lab until they are in their freezer and the paperwork has been submitted.
 
Final Note: All figures are taken from the websites/documents provided by the supplier
 
Appendix 1: Setting up a lab to do ezRAD
Below is a list of the lab equipment, kits and other reagents you’ll need to have in order to do the ezRAD process in house, not including sample collection, gels, quality control checks (bioanalyzer and qPCR) or sequencing. I also assume here that you have a range of standard pipettes and tip sizes. I’ve added in hyperlinks to websites for the more unusual items. 
 
Equipment:
•	Multiwell pipettes (at least an 8 well 1-20μl and 20-200μl)
•	10ml or 20ml pipette (not essential, but makes quantitation easier for larger sample sizes)
•	Vortex
•	Centrifuge-for 1.5ml tubes and strip tubes
•	Incubator/water bath (preferably one that shakes)
•	1.5ml tubes
•	250ul 8 well strip tubes
•	96-well plates and aluminium sealing films (if dealing with large numbers of samples)
•	Speedvac
•	Black 96-well plates-solid bottom (not clear) from either Corning Costar plate (Cat# 3916) or Greiner Bio-One CELLSTAR plate (Cat. # 655079)
•	Microplate reader: Molecular devises- SpectraMax M2 (or other models, the Accuclear assay is designed for use with fluorescence 96-well plate readers equipped with excitation and emission filters for detecting green fluorescence and is especially well-suited for use with instruments with blue LED excitation sources-see the Accuclear litereature).
•	Magnetic plate (for magnetic bead cleans)-DynaMag™-96 Side Magnet-we’ve tried 2 other styles of plates, this is definitely the best (even than the one recommended by Illumina).
•	Reagent trough/reservoir-doesn’t have to be from this site
•	Freezable tube rack
Kits:
•	The Qiagen or Omega tissue and genomic DNA extraction kits.
•	AccuClear Ultra high sensitivity dsDNA quantitation kit
•	Illumina TruSeq DNA preparation kits
      PCR-free kits (1000ng input DNA) 
      Nano kit (100ng input DNA)
•	Both kits come in 2 options either: 
      (LT) low throughput (makes 24 libraries) or 
      (HT) High throughput (makes 96 dual indexed libraries)
Separate reagents (not included in kits): 
•	HPLC or PCR grade water
•	RNase A- We currently use Amresco 0625_500MG, which comes in a powder and has to be made up by adding HPLC grade water to make a final concentration of 20mg/µl. Another option is to buy it pre-made up like this one from Life Technologies.
 
•	Agencourt AMPure XP magnetic beads-see here for the Beckman Colter protocol.
•	DpnII restriction enzyme- If DpnII doesn’t work with your samples there are other isoschizomers of this GATC cut site. We were initially using MboI and Sau3A1 in the same reaction, which worked well for us. We moved over to DpnII because, unlike MboI and Sau3A1, it is not sensitive to CpG methylation, which is found in higher eukaryotes. MboI and Sau3A1 are better at dealing with prokaryotic methylation, so if this is what you are targeting then use these 2 restriction enzymes. Methylation is an issue to consider when digesting DNA with restriction enzymes because they can be blocked or impaired when a particular base in the recognition site is methylated. To read about the different types of methylation see here. For differences between these 3 restriction endonucleases see here.
 
 
 
 
Appendix 2: Removed from this protocol, but still in old versions
Technologies move so fast that a number of steps could be removed from this 2.0 version of the ezRAD protocol, but in the case that you would still like to use them I will list what was removed here:
In ezRAD protocol version 1.5 but not in version 2.0:
•	Accublue high sensitivity kit procedure- the main difference between the Accuclear kit is that it is better suited to accurately measuring 0.2-100ng and the excitation and emission values are different. Note that there is also a Accublue broad range kit, which measures between 2 and 2000ng, which is good when you want to detect high concentrations of DNA, but we often end up on the lower end so use the AcuClear ultra high sensitivity kit. 
•	Serial dilution of standards for quantitation- there are instructions provided with the Accuclear kit if you order the one with 1 standard.
•	Information on previously used digestion enzymes (MboI and Sau3AI)
•	Tips when using the ring magnetic plate
•	Gel excision
•	Flashgel method
 

