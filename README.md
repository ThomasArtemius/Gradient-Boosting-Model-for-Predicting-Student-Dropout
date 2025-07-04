# Gradient-Boosting-Model-for-Predicting-Student-Dropout
Using SMOTE, Random Undersampling, XGBoost, LightGBM, CatBoost, and Genetic Algorithm in predicting student dropout
# Previous Work
XGBoost is used for predicting student dropout with multiple spliting variations[[1]](#ref1). The data itself is taken from Machine Learning repository[[2]](#ref2). It contains 3 catogory: Dropout, Graduate, and Enrolled. But because it tries to predict the dropout and non-dropout, therefore, Graduate and Enrolled category are combined. The data has 36 features overall and 4424 rows. In this paper, it's not handling imbalance data due to combining of 2 categories.\
This paper doesn't provide any detail on what hyperparameters are used in their XGBoost model. The default parameter from SKLearn doesn't provide an exact result with the paper. I will also provide the result from default parameter from SKLearn for comparison later.
# Models
## SMOTE and Random Undersampling
I try to implement SMOTE and Random Undersampling separately to see what are their impact on model performances.
## Gradient Boosting
In order to comparing "fairly" with the previous paper, I using methods within the domain of gradient boosting. I use XGBoost, LightGBM, and CatBoost. XGBoost will be optimized with genetic algorithm (as well as other 2 other methods). LightGBM is chosen because of its improvement upon XGBoost in its original paper. CatBoost is chosen because of its improvement upon XGBoost and LightGBM in its original paper also.
### XGBoost + Genetic Algorithm
Improvement has been made for classifying Liver Disorder Dataset using Genetic Algorithm for optimizing XGBoost[[3]](#ref3). It increase all metrics like precision, recall, F1-Score, and accuracy.
![](https://github.com/ThomasArtemius/Gradient-Boosting-Model-for-Predicting-Student-Dropout/blob/main/images/XGBoost%20%2B%20GA.png)
Therefore, it is possible that this technique can be used for Student dropout dataset. Because of this achievement, Genetic Algorithm will also be used for optimizing LightGBM and CatBoost
### LightGBM + Genetic Algorithm
LightGBM invention shows has an improvement over XGBoost on several datasets: Allstate, Flight Delay, LETOR, KDD10, KDD12[[4]](#ref4). With AUC metric for comparison, here are the result of LightGBM compare with other methods.
![](https://github.com/ThomasArtemius/Gradient-Boosting-Model-for-Predicting-Student-Dropout/blob/main/images/LightGBM%20Performance.png)
### CatBoost + Genetic Algorithm
CatBoost invention also shows has an improvement over XGBoost and LightGBM on Epsilon dataset[[5]](#ref5). You can see how well CatBoost performance by comparing with XGBoost and LightGBM with Logloss/Zero-One loss metrics.
![](https://github.com/ThomasArtemius/Gradient-Boosting-Model-for-Predicting-Student-Dropout/blob/main/images/CatBoost%20Performance.png)
# Results
## Using SMOTE
### 50:50 (SMOTE)
![](https://github.com/ThomasArtemius/Gradient-Boosting-Model-for-Predicting-Student-Dropout/blob/main/Results/50-50%20SMOTE.png)
### 60:40 (SMOTE)
![](https://github.com/ThomasArtemius/Gradient-Boosting-Model-for-Predicting-Student-Dropout/blob/main/Results/60-40%20SMOTE.png)
### 70:30 (SMOTE)
![](https://github.com/ThomasArtemius/Gradient-Boosting-Model-for-Predicting-Student-Dropout/blob/main/Results/70-30%20SMOTE.png)
### 80:20 (SMOTE)
![](https://github.com/ThomasArtemius/Gradient-Boosting-Model-for-Predicting-Student-Dropout/blob/main/Results/80-20%20SMOTE.png)
### 90:10 (SMOTE)
![](https://github.com/ThomasArtemius/Gradient-Boosting-Model-for-Predicting-Student-Dropout/blob/main/Results/90-10%20SMOTE.png)
## Using Random UnderSampler
### 50:50 (RandomUnderSampler)
![](https://github.com/ThomasArtemius/Gradient-Boosting-Model-for-Predicting-Student-Dropout/blob/main/Results/50-50%20RandomUnderSampler.png)
### 60:40 (RandomUnderSampler)
![](https://github.com/ThomasArtemius/Gradient-Boosting-Model-for-Predicting-Student-Dropout/blob/main/Results/60-40%20RandomUnderSampler.png)
### 70:30 (RandomUnderSampler)
![](https://github.com/ThomasArtemius/Gradient-Boosting-Model-for-Predicting-Student-Dropout/blob/main/Results/70-30%20RandomUnderSampler.png)
### 80:20 (RandomUnderSampler)
![](https://github.com/ThomasArtemius/Gradient-Boosting-Model-for-Predicting-Student-Dropout/blob/main/Results/80-20%20RandomUnderSampler.png)
### 90:10 (RandomUnderSampler)
![](https://github.com/ThomasArtemius/Gradient-Boosting-Model-for-Predicting-Student-Dropout/blob/main/Results/90-10%20RandomUnderSampler.png)

# References
<a id="ref1"/>

[1] [A. Ridwan and A. M. Priyatno, “Predict Students’ Dropout and Academic Success with XGBoost,” Journal of Education and Computer Applications, vol. 1, no. 2, pp. 1–8, Dec. 2024, doi.org/10.69693/jeca.v1i2.13.](https://jeca.aks.or.id/jeca/article/view/13/6)

<a id="ref2"/>

[2] https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success 

<a id="ref3"/>

[3] [J. Chen, F. Zhao, Y. Sun, and Y. Yin, “Improved XGBoost model based on genetic algorithm,” Int. J. Comput. Appl. Technol., vol. 62, no. 3, p. 240, 2020, doi: 10.1504/IJCAT.2020.106571.](https://sci-hub.se/10.1504/ijcat.2020.106571)

<a id="ref4"/>

[4] [G. Ke et al., “LightGBM: A Highly Efficient Gradient Boosting Decision Tree,” Adv. Neural Inf. Process. Syst., vol. 30, 2017.](https://proceedings.neurips.cc/paper_files/paper/2017/file/6449f44a102fde848669bdd9eb6b76fa-Paper.pdf)

<a id="ref5">
  
[5] [L. Prokhorenkova et al., “CatBoost: Unbiased Boosting with Categorical Features,” arXiv preprint, arXiv:1706.09516, 2017.](https://arxiv.org/pdf/1706.09516)
