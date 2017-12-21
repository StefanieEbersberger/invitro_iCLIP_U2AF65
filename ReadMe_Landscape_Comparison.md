LandscapeComparisonScript contains 8 files in total.


1. InvivoLandscapeComparison_model_Exp.m:  

   The script for the in vitro/in vivo comparison, this script does:    
      + loads the data and in vitro Kds
      + plots the model landscape (with the in vivo fitted mRNA/protein concentrations)
      + plots the measured in vivo landscape
      + returns the z-scores

2. FitInvivoAll3Replicate.m: function file that does the fitting procedure to in vivo iCLIP signal

3-5. In vivo iCLIP data file: contains measured iCLIP signal on each binding site as well as genomic information of each binding site.  

 + KRS13_vivo_DR_raw_peak_data.csv
 + lujh23a_vivo_DR_raw_peak_data.csv
 + lujh32_vivo_DR_raw_peak_data.csv

6. Kd_SF_fromInvitroFit.csv: contains the Kd (binding affinities) and SF (scaling factors) value estimated from fitting to in vitro iCLIP signal.

7. U_mRNA_level_fromInvivoFit.csv: contains the free U2AF65 protein level and each intron level estimated from fitting to in vivo iCLIP signal, when assuming the same Kd and scaling factors as in vitro. In the script, these value could be provided by users as well, to check the binding landscape from any given protein/mRNA level combination.

8. invivoiCLIP_landscape_model_experiment.fig: The comparison plot from this script.

