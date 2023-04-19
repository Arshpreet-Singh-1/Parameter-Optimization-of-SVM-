# Parameter-Optimization-of-SVM

# Multi-class SVM on Adult Census IncomeDataset

This project demonstrates the use of multi-class SVM on the `Adult Census Income` dataset from the UCI Machine Learning Repository. The dataset contains a total of `15 columns` and `32561 rows.`

The `Adult Census Income` dataset contains information about individuals, such as their age, education level, marital status, occupation, and whether or not they earn more than $50K per year.



## Preprocessing

Before using the dataset for classification, the following preprocessing steps were applied:

1. The "?" values in the dataset were replaced with the mode of the respective column.
2. The categorical features were one-hot encoded.
3. The numerical features were standardized using the StandardScaler from scikit-learn.


## Training and Testing

The dataset was divided into a 70-30 split for training and testing, respectively. The SVM model was optimized for 1000 iterations with random values of C and gamma between 0 and 1, and with different kernels. The optimization was performed on 10 different samples of the dataset, and the best accuracy and SVM parameters were recorded for each sample.

## Results

The results of the SVM optimization for each sample are summarized in the table below:

| Sample | Best Accuracy | Best C | Best Gamma | Best Kernel |
|--------|---------------|--------|------------|-------------|
| 1      | 0.779814         | 0.621529397317055    | 0.18370585815911455       | rbf         |
| 2      | 0.800287         | 0.7293151589606629   | 0.6811439432806408       | poly         |
| 3      | 0.797728         | 0.7288867203557419   | 0.46100263352088766       | poly        |
| 4      | 0.782168         | 0.05309078943383161  | 0.1680117142843266       | rbf         |
| 5      | 0.802743         | 0.25995296118639877 | 0.20122283502869864| poly|
| 6      | 0.798649         | 0.44410793092714784  | 0.5681517380630898| poly|
| 7      | 0.793428         | 0.36063178294224174  | 0.12582310778330696| poly|
| 8      | 0.794964         | 0.8704578887749851   | 0.9407696885526249| poly|
| 9      | 0.790562         | 0.6741497148676773   | 0.0390595787384963| rbf         |
| 10     | 0.794145         | 0.08561209156557315  | 0.10956788956020369| rbf         |



The sample with the highest accuracy was `sample 5`, with an accuracy of `0.802743`. 

## Conclusion

Multi-class SVM can be a powerful tool for classification tasks, especially when applied to preprocessed datasets. By optimizing the SVM parameters, we can achieve high accuracy on the test set. However, care must be taken to avoid overfitting and to select appropriate values for C, gamma, and the kernel function.
