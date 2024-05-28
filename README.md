# Density-based-cluster resampling

We are resampling high-dimensional imbalanced data based on their density of distribution using clusters determined by DBSCAN. Minority class instances are augmented in border-areas of high density using Nearest Neighbours. This is was inspired by Borderline-SMOTE. 
And majority instances in extremely dense clusters are under-sampled.
We then train base random forest models on the resampled data (oversampled and under-sampled data are different) and original data. We then create an ensemble(weighted majority hard voting) of this to produce a robust model which is sensitive to imbalance without compromising on the original structure of the data.
Although there have been approaches and attempts to effectively combine clustering algorithms(K-Means,DBSCAN) and augmentation techniques like SMOTE, our approach also considers under-sampling of majority instances in highly dense clusters.
We further create an ensemble of models trained on the original as well as the resampled datasets which makes it robust and infers from unseen data with an high accuracy, even with a severe imbalance. 
The strategies employed for dealing with the imbalance of our dataset are:
Density based oversampling:
In this, we are using a method inspired by Borderline-SMOTE using Nearest Neighbours to augment the minority class instances in border areas of high density
Density based under sampling:
Majority class instances belonging to high density clusters are undersampled.
![Screenshot 2024-05-28 154941](https://github.com/Achutha2704/Density-based-clustering/assets/113625925/8c43f1ef-1e94-46b9-a777-1d723f2289c0)

