
Analysis of non-isothermal crystallization kinetics
CLICK HERE to watch the instructions video

Introduction
Exothermic peaks of DSC curves are used to generate a Jeziorny plot of the non-isothermal crystallization (see Polymers 2021, 13, 582. https://doi.org/10.3390/polym13040582 for more info and ref 35 of this paper for the Jeziorny analysis 
 both PDF files are availabble in this repository). Acccording to the Jeziorny analysis, the Avrami parameter (
) and the crystallization rate corrected for the cooling rate (
) can be obtained by plotting 
 as a function of 
 (where the time 
 is given in minutes), whose linear fit gives the following equation:

  

which is representing the well-known linear equation:

  

from where we see that the Avrami parameter is the slope of the line and 
 is the intercept. In the first equation, 
 is the relative crystallization degree (normalized to achieve values between 
, but in practice only data with crystallinity between 20 and 80%, i.e., in the normalized range of [0.2, 0.8] are included in the equation). The time zero is assumed to be the time where the crstallization degree is 0.1%. 
 is the uncorrected crystallization rate constant, however, this script uses the cooling rate-corrected 
, which is named 
. Knowing the intercept of the fitted line, as well as the cooling rate, one can calculate 
 by:

  
 



NOTE: A similar form of the first equation above is commonly used in the literature, where 
 is replaced by 
, leading to the equation

  

which also leads to the following value of 
:

  
 

The last two equations give the same results of 
 and 
 as the first two equations above.

Input:
.txt DSC output with different DSC curves, each with its own heating rate (if experiments are noisy, one can also have all repetitions of an experiment using the same heating rate to manually average the individual Avrami parameters).

NOTE: THis script only works for the "mettler toledo dsc1"! Other equipments still need implementation. You should select the exothermic peaks (exo-down, endo-up) before exporting the DSC curves to a txt file, so that appropriate "Rechte Grenze" and "Linke Grenze" parameters appear for each DSC curve in the txt file.

Output:
Avrami parameter (
) + cooling rate-corrected crystallization rate (
) + corresponding plots & data. The saved data consists in .csv files with all DSC curves + all baseline-corrected DSC curves of the original DSC file. Some plots are optional to be saved. All generated files are send to a subfolder named "Results_date_time", where date and time have the formats YYYYMMDD and HHmmSS, respectively.

Script written by RodrigoAlbuquerque@April2023
Experimental collaborators: Andreas Himmelsbach (main), Malvina Boutigny (update)
