# Random Forest analysis

## Compilation of input data

571 binding sites, 12656 features.

* 8 transcript features (transcript_features.csv) 
* 120 PWM features evaluated downstream/upstream of binding site and at the extended binding site itself = 360 PWM features (pwm_features.csv)
* 4096 6-mers evaluated downstream/upstream of binding site and at the extended binding site itself = 12288 k-mer features (kmer_features.csv)

In total: 
571 cases (binding sites), 12656 features.  
173 binding sites are down regulated invivo (z-score < —1)  
151 binding sites are unregulated invivo (z-score > 1)  

## Random Forest Processing Details

Computational settings:  

R version 3.3.1  
randomForest 4.6-12  

Parameter setting in random Forest call (randomForest()):

sampsize = c(149,151)  
ntree = 20000  


4985 features are removed because there is no entry in current selection of peaks.  
2003 k-mer features are removed because of correlation issues (features are merged if correlation > 0.85).  
129 PWM features are removed because of correlation issues.  

5539 features are kept for first round of Random Forest (Input_for_first_Random_Forest.csv)  
The top 30% features (1846 features, ranked by decreasing accuracy) are taken for second round of Random Forest.  

Feature importance is output for second round of Random Forest for the 1846 features (Features_ranked_by_MeanDecreaseAccuracy.csv').

