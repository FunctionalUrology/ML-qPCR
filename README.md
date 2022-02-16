# MLcps
Here we present a novel Machine Learning (ML) performance scoring algorithm called “MLcps: ML cumulative performance score” to rank the ML performances. MLcps combines multiple performance metrics and reports a cumulative score enabling researchers to compare the ML models. To test this algorithm, we used RNA sequencing and QPCR data obtained from two types of lower urinary tract dysfunction (LUTD) with overlapping symptoms: non-ulcerative bladder pain syndrome (BPS) and the overactive bladder syndrome caused by bladder outlet obstruction. We compared the performance of 36 different ML algorithms to identify signatures of these disease phenotypes. MLcps provides a comprehensive platform to identify the best-performing ML and corresponding features on any given dataset.

### Machine Learning Pipeline 
We developed a computational framework for binary classification problems that automates several ML steps and evaluates multiple algorithms/methods for almost every step. The proposed pipeline first splits the datasets into k(3) equal size different bins in a stratified manner, where k-1 bins will be used as training datasets and the remaining bin as a test dataset.  Next, it uses the RFECV method for feature selection, three data resampling, and twelve ML algorithms.  Then, it evaluates the model performance on the test dataset using the k-fold and nested CV (k=3) method and calculates seven different performance metrics.  As part of k-fold CV methods, it repeats the last two steps for each unique bin.  It repeats the complete process ten times and takes average performance as a final model performance. In the end, it provides a list of the intersection of selected features from top 10 best performing models (based on F1 score) as a final list of selected features.

### Visualization
visualization.ipynb file contains code to visualize the results from the ML pipeline. 

### MLcps
MLcps.Rmd file contains code to calculate *cumulative performance scoring system (CPS)* based on seven different metrics to identify the best performing ML model.
