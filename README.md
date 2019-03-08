# BMI551: kaggle project 

## Team members: Nate Evans, Gareth Harman 

## Team name: 


## Overview 

Your task is to predict whether a breast cancer cell line will respond to treatment with a given drug using the subtype of the tumor and the gene expression data provided.  

Note that we are using this data set for instructional purposes only. It is generally too small to be of use in a real study. This data originally had 70 cell lines and 90 drugs, but in order to avoid issues with missing data we have restricted the challenge to those data seen here. One important aspect of this type of challenge is to ascertain whether the data is sufficient to make meaningful inferences.
  
There are 25 cell lines and 12 drugs in the training set which you will use to train your classification algorithms.

The responses are coded as 0 = cell line doesn't respond to drug, 1 =cell line does respond to drug.

Your submissions can either be binary or contain values between 0 and 1 so that the area under the ROC curve can be computed for different threshold cutoffs between 0 and 1.

Once you have a prediction method you will submit predictions for an additional 14 cell lines when treated with the same 12 drugs.

Your score on 9 of the 14 cell lines will be automatically calculated and displayed on the website. These scores will determine the leader board standings.

Scores on the remaining 5 cell lines (along with the above 9) will be used to determine the final standings when the competition is over.

You are provided with: 1) A tab-delimited text file containing expression values for 18,632 genes in 39 samples, 2) a tab-delimited text file showing the subtype for all 39 samples, 3) a tab-delimited text file showing whether each of the 25 training cell lines are responsive to each of the 12 drugs. 4) a comma-separated (csv) file showing the id mappings for the 168 (14x12) predictions that you will submit to Kaggle. 5) two example submission files with random guesses.

You are free to use any prediction techniques you wish, but you must try at least two different methods. At least one of those methods must also use a meta-algorithm (e.g. boosting or bagging).

All work should be done in R.

All well-commented scripts should be submitted by the due date and we should be able to run your code to produce your final predictions. Note that this means you should document the version of R and any packages that you use.

A write-up of your method and experimental results is also due at the end of the competition. Labeling your submissions with the technique (and maybe some parameters) that you used to generate the predictions (e.g. NN30hidden10epochs) will help you keep track of what you've tried. Kaggle will keep track of the submission time for you.

Response in this context means that the concentration of drug needed to inhibit cell growth by 50% was above the median for all cell lines tested (not just those used above). There is a lot to be said about whether this measure reflects how the drug will work in patients.

Acknowledgements The data used comes from the study below by Dr. Joe Gray, Dr. Laura Heiser and others many of whom are here at OHSU.

Anneleen Daemen et al., "Modeling Precision Treatment of Breast Cancer," Genome Biology 14, no. 10 (2013): R110, doi:10.1186/gb-2013-14-10-r110.


## Data Info 

expression.txt - tab-delimited text file with expression values for 18,632 genes for each of the 39 cell lines.


subtypes.txt - tab-delimited text file of subtypes (basal, luminal, claudin-low and normal-like) for each of 39 cell lines


training_set_answers.txt - tab-delimited text file of the correct classification of 0 (non-responsive) or 1 (responsive) for each combination of 25 cell lines and 12 drugs.


scoring_and_test_set_id_mappings.csv - comma-delimited text file of the id used by Kaggle for each of the cell line/drug combinations in the scoring set and test set. The first 108 values are the scoring set (9 cell lines and 12 drugs) and the last 60 are the final test set (5 cell lines 12 drugs). Scores on the final test set will not be shown until the competition is over.


rand_sub_cont.csv - a sample submission file in the correct format with random predictions between 0 and 1. The calculation of the AUROC value summarizes the performance of these guesses at all thresholds between 0 and 1. 

