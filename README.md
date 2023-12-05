# Depth-of-Anaesthesia-design
The design of a novel depth of anaesthesia (DoA) using different supervised machine learning models. In any successful surgery, accurate monitoring of the depth of anaesthesia (DoA) is very important.
This study aims to build DoA index using different supervised machine learning algorithms.

### Data Analysis

10 training data and 5 test data were given. Each of these data contains the same kind of 8 features (x1 to x8) and BIS. The train datasets combined gave the statistical information in Table 1 below while the test datasets combined gave the statistical information in Table 2 below:
Table 1: Statistics information of the combination of the training data
![image](https://github.com/favouritemary/Depth-of-Anaesthesia-design/assets/88316368/7f1bbef7-9bf4-40cb-bad5-5892bb8a46b3)

Table 2: Statistics information of the combination of the test data
![image](https://github.com/favouritemary/Depth-of-Anaesthesia-design/assets/88316368/6ccfffc4-1823-4c89-a70e-3049bc1940f3)

To show the relationship between the features with themselves and with BIS, the correlation was done for each of the train and test data as well as their combination. The correlation for the combination of train data is given below:

![image](https://github.com/favouritemary/Depth-of-Anaesthesia-design/assets/88316368/56d16be8-3481-4d70-bc21-4b0f7a02b3a1)

Correlation for train data

From the diagram above, x2 appears to be the highest correlated feature with BIS while x3 is the lowest correlated feature. Also, while other features are positively correlated, features x4 and x6 are negatively correlated with BIS

### Features Selection

Different feature-selected methods were used on the combination of train data to ascertain that only the best features were selected. The results for each feature selection method are presented in the table below ranking from the most important to the least.

Table 3: Feature selection methods and the selected features based on their importance for training data
![image](https://github.com/favouritemary/Depth-of-Anaesthesia-design/assets/88316368/f99102ca-87a7-454d-9944-65677a32e040)

Across the various feature selection methods, x2 appears to be the most important feature while x4 and x3 appear to be the least important features. Six features in total seem good. However, cross-validation was done to select the right number of features as well as the best subset for the analysis. The selected subsets are x2, x5, x6 and x8 for both models.

### Results

The features selected for the model are x2, x5, x6 and x8 and the hyper-parameters used were kernel=poly, C=40 and epsilon=0.5, giving a train score of 0.81. The model was then tested on each test dataset as well as the combination of the test datasets. 

Table 4: The results for Pearson correlation coefficients (r), R-squared (R2) and Mean square error (MSE)
![image](https://github.com/favouritemary/Depth-of-Anaesthesia-design/assets/88316368/50bf0821-c268-4149-875e-b692073e3171)

The Pearson correlaion coefficient (r) of the SVR index for the test combination is 0.87 with a range from 0.83 (Test 4) to 0.95 (Test 5). However, the performance of Tests 3 and 4 is not good enough with R-square values of 0.74 and 0.73 respectively. The lowest mean squared error (MSE) value is 50.57 (Test 2) while the MSE value for the test combination is 73.2.  

The plots of the new index with BIS for each test data are given below

![image](https://github.com/favouritemary/Depth-of-Anaesthesia-design/assets/88316368/7bb74af4-972b-4ea9-a3c8-0373da23e162)

![image](https://github.com/favouritemary/Depth-of-Anaesthesia-design/assets/88316368/45d24d91-3522-402c-83c0-9700b11f63a0)

![image](https://github.com/favouritemary/Depth-of-Anaesthesia-design/assets/88316368/b2b946f4-2911-4a91-b4c6-ce5ccae0e828)

![image](https://github.com/favouritemary/Depth-of-Anaesthesia-design/assets/88316368/435f6b14-d54f-4473-89af-06354fd0248f)

![image](https://github.com/favouritemary/Depth-of-Anaesthesia-design/assets/88316368/d79b70af-e28c-473a-a335-590320655be3)

![image](https://github.com/favouritemary/Depth-of-Anaesthesia-design/assets/88316368/e781d34b-0eb2-45e4-8e99-75fc49c3ae6c)

For each of the diagram, the trend of the new index shows a close similarity with the BIS values, with few fluctuations.




