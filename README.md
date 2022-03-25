# Hyperspectral-classification-of-differernt-cultivars-of-Millet-seeds
From the hyperspectral images, the seeds were segmented as the region of interest.  To segment the region of interest (ROI), two masks were used to separate each seed in the image. The first mask was to remove the background using thresholding, so all the seed boundaries in the image were clearly defined.  Then, a connectivity function was used to segment each individual seed from the others in the first mask.  This function counted the connected regions for each seed and fills in every seed area in the mask to a different intensity value. Next, to look at each seed individually, a second mask is created by segmenting out all values that are not equal to intensity value of the seed of interest. 

Spectra extraction 

The spectra for each seed could then be calculated and analyzed by averaging the spectra for all the pixels in the seed.  This ROI and spectra extraction was repeated for every seed in each repetition for each type of millet.  Using these mean spectra, a dataset was created, using the observations as rows, and the features and labels as columns. The seeds can then be classified, and their proximate qualities determined. 

Building classification models 

The dataset of the 10 cultivars was then built for classification. PCA was used to reduce the dimensionality of the hypercube. The data used a 5-fold cross validation model for supervised machine learning classification.  The predictor values were the PCA of the spectral data, and the dependent variables were the cultivars of millet.  Different machine learning classification algorithms of SVM (Support Vector Machine), RF (Random Forest), kNN (k-Nearest Neighbors), linear discriminant analysis (LDA), and Ensemble were performed and compared for their test classification accuracies. Each algorithm produced five models and the mean is taken of the accuracy for each algorithm.  
