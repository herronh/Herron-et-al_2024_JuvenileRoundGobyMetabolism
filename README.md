README.md for "Temperature- and ontogeny-dependent metabolism in invasive early juvenile round goby, Neogobius melanostomus"
  Authors: Herron, H. A., Zarini, S., Thompson, W. A., Turko, A. J., & Balshine, S. (submitted 2024). 
  Please direct all questions and inquiries to the corresponding author
    Hunter Herron 
    herronh@mcmaster.ca
    
The text files that appear are the raw data traces. Experiments 6 to 25 were used in our study. Note that experiments 1 to 5 were pilot experiments, and do not appear here nor in the manuscript.

The R file, Herron,et.al.Rmd, was used to generate figures and run statistics. 
  This file should be well-enough annotated to figure out what each chunk of code does. 

The Excel file, 'Juvenile_Round_Goby_Metabolism_Herron-et-al.xlxs', contains the data we exported into R.
  This is an explanation of the columns of data: 
    Date: The date of the experiment, in YYYY-MM-DD
    FISH_ID: A unique fish identifier, made from [Temp][ExNo][Channel], e.x. 150601 is 15 degrees, 6th experiment, channel 1. 
    Age: Takes values from 1 (6-7 weeks old) or 2 (12-14 weeks old)
    Experiment: The chronological experiment number (begins at 6 to 25)
    Temp: The experiment and acclimation temperature (15, 19, 23, 27) in degrees Celcius
    Channel: The respirometer the fish was in. Note: For ExNo6/7 Channel 8 was the control; for all others it was Channel 4.  
    Mass_1: The first mass replicate;
    Mass_2: The second mass replicate;
    Mass_3: The third mass replicate;
    AvgMass: The average of the three mass replicates; this was used as the "Mass of the fish" in our figures, statistics, and calculatons
    total_length_mm: The length of the fish (from tip to tip), as measured in ImageJ
    Fultons_body_condition: An exploratory variable; was not described in the manuscript. 
    msRMR_mgO2_gh: Mass-specific RMR (in milligrams oxygen per gram per hour) 
    absoluteRMR_mgO2_h: Absolute RMR (in milligrams oxygen per hour) 
    msRMR_mgO2_kgh: Mass-specific RMR (in milligrams oxygen per kilogram per hour)
    msMMR_mgO2_gh: Mass-specific MMR (in milligrams oxygen per gram per hour)
    absoluteMMR_mgO2_h: Absolute MMR (in milligrams oxygen per hour)
    msMMR_mgO2_kgh: Mass-specific MMR (in milligrams oxygen per kilogram per hour)
    AS_Analysis: A logical argument; tests if MMR > RMR. If TRUE, we included it in our results. If RMR > MMR, we excluded it (n = 7)
    FAS: Factorial Aerobic Scope; here we calculated it as the ratio of MMR:RMR (typically this is calculated as MMR:SMR [the standard metabolic rate]). 
    abs_AS: Absolute Aerobic Scope; though we recalculated this variable in R. We also changed from 'Aerobic Scope' to 'Scope for Activity' 
    when_did_max_occur: This is the amount of time, in seconds, before the maximum slope in our MMR experiment was reached. This maximum slope was used as the MMR, if its R2 was > 0.80
    Ratio of data thrown: Our calculation of MMR considered 1-minute long slopes, whose R2 was > 0.80. This is a ratio of how many of these regressions had an R2 above 0.8 compared to the total number of slopes.
