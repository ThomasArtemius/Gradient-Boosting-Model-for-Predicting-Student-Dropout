# Gradient-Boosting-Model-for-Predicting-Student-Dropout
Using SMOTE, XGBoost + Genetic Algorithm, LightGBM, and CatBoost to improve prediction on student dropout
# Previous Work
XGBoost is used for predicting student dropout with multiple spliting variations[1]. The data itself is taken from Machine Learning repository[2]. It contains 3 catogory: Dropout, Graduate, and Enrolled. But because it tries to predict the dropout and non-dropout, therefore, Graduate and Enrolled category are combined. The data has 36 features overall and 4424 rows. In this paper, it's not handling imbalance data due to combining of 2 categories.
# Models
## XGBoost + Genetic Algorithm
Improvement has been made for classifying Liver Disorder Dataset using Genetic Algorithm for optimizing XGBoost[3]. It increase all metrics like precision, recall, F1-Score, and accuracy. Therefore, it is possible that this technique is used for Student dropout dataset
## LightGBM
LightGBM invention shows has an improvement over XGBoost on several datasets: Allstate, Flight Delay, LETOR, KDD10, KDD12[4].
## CatBoost
CatBoost invention also shows has an improvement over XGBoost and LightGBM on Epsilon dataset[5]
## Hybrid Method
If XGBoost, LightGBM, and CatBoost can complement each other, than combining them can probably increase the performance.
# References
[1] A. Ridwan and A. M. Priyatno, “Predict Students’ Dropout and Academic Success with XGBoost,” Journal of Education and Computer Applications, vol. 1, no. 2, pp. 1–8, Dec. 2024, doi: https://doi.org/10.69693/jeca.v1i2.13. \
[2] https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success \
[3] J. Chen, F. Zhao, Y. Sun, and Y. Yin, “Improved XGBoost model based on genetic algorithm,” Int. J. Comput. Appl. Technol., vol. 62, no. 3, p. 240, 2020, doi: 10.1504/IJCAT.2020.106571. \
[4] G. Ke et al., “LightGBM: A Highly Efficient Gradient Boosting Decision Tree,” Adv. Neural Inf. Process. Syst., vol. 30, 2017. \
[5] L. Prokhorenkova et al., “CatBoost: Unbiased Boosting with Categorical Features,” arXiv preprint, arXiv:1706.09516, 2017.
