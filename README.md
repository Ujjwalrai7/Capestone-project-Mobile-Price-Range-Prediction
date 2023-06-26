# Capestone-project-Mobile-Price-Range-Prediction

# **Project Summary -**

Mobile now a days is one of the most selling and purchasing device. Every day new mobiles with new version and more features are launched. Hundreds and thousands of mobiles are sold and purchased on daily basis.

Therefore, Price estimation and prediction is an important part of consumer strategy as a new product that has to be launched, must have the correct price so that the consumers find it appropriate to buy the product. During the purchase of mobile phones, people fail to make correct decisions due to the non-availability of necessary resources to cross validate the price. To address this issue, we developed different classification models using the data related to different features of a mobile phone. The developed model is then used to predict the price range of the new mobile phones.

The main objective of this work is to find out the relationship between features of a mobile phone and its price range which indicates whether the mobile would be cheap(0), mid-range(1), expensive(2) or very expensive(3). We will be using different classification models to accurately classify the data in correct price ranges.

Based on our dataset, Data prepressing was the first step followed. I have understood the data found that the dataset contains 2000 records of mobile phone information with 21 features which were a mix of categorical and numerical values also the dataset fortunately is not having any null values, got a clear description about the features involved. After that Exploratory Data Analysis and Data Visualization has provided a brief understanding about the relationship present between features and label i.e., the dependent variable also it has given an idea about the features to be selected for the further process.

Heatmap was used to understand the correlation between independent variables, based on which important features were selected. Before fitting the model, Standardization was an important step, it makes the feature values in the data have zero mean and unit variance. While we implement any Machine Learning algorithm it could be a possibility that objective function will not work properly without normalization.

After training and testing was done. I have made the use of Logistic Regression, K Nearest Neighbour, Random Forest, XGBoost, Support Vector Machine techniques.Hyperparameter Tuning was also done over some of the models for better accuracy and to reduce overfitting, made the use of Gridsearch cross validation to achieve the best parameter. These parameters enhanced the predicting capability of our model.

Checked and compared various matrices and came to conclusion that XGBoost model with hyperparameter tuning is giving the best scores. Also, Tree based models (XGBoost and Random Forest in our case) are by far good performing models while dealing with our dataset because of its ability to stay insulated from the effect of worst performing features and at the same time KNN proven to be the worst for this dataset.

# **Problem Statement**


### In the competitive mobile phone market companies want to understand sales data of mobile phones and factors which drive the prices.

### The objective is to find out some relation between features of a mobile phone(e.g:- RAM, Internal Memory etc) and its selling price. **In this problem, we do not have to predict the actual price but a price range indicating how high the price is.**

# Dataset First Look

![image](https://github.com/Ujjwalrai7/Capestone-project-Mobile-Price-Range-Prediction/assets/125723652/dfb53440-d617-4a42-9834-8a0059ad994a)

### Variables Description
#### **Battery_power:** Total energy a battery can store in one time measured in mAh
#### **Blue:** Has bluetooth or not
#### **Clock_speed:** Speed at which microprocessor executes instructions
#### **Dual_sim:** Has dual sim support or not
#### **Fc:** Front camera mega pixels
#### **Four_g:** Has 4G or not
#### **Int_memory:** Internal memory in gigabytes
#### **M_dep:** Mobile depth in cm
#### **Mobile_wt:** Weight of mobile phone
#### **N_cores:** Number of cores of processor
#### **Pc:** Primary camera mega pixels
#### **Px_height:** Pixel resolution height
#### **Px_width:** Pixel resolution width
#### **Ram:** Random Access Memory in Megabytes
#### **Sc_h:** Screen height of mobile in cm
#### **Sc_w:** Screen width of mobile in cm
#### **Talk_time:** Longest time that a single battery charge will last when you are talking over phone
#### **Three_g:** Has 3G or not
#### **Touch_screen:** Has touch screen or not
#### **Wifi:** Has wifi or not
#### **Price_range:** This is the target variable with value of **0(low cost)**, **1(medium cost)**, **2(high cost)** and **3(very high cost)**.

##  Data Vizualization

![image](https://github.com/Ujjwalrai7/Capestone-project-Mobile-Price-Range-Prediction/assets/125723652/227f3a6a-cb2e-43a5-8239-a0409022cd00)

* The insights that can be generated are that they price range is almost evenly distributed in all the categories.

![image](https://github.com/Ujjwalrai7/Capestone-project-Mobile-Price-Range-Prediction/assets/125723652/91cd4d91-2043-4def-be51-39b9e232a677)

* We can visualise that price range is highly dependent on RAM of mobile and increases according to the increase in the RAM of the mobile.

![image](https://github.com/Ujjwalrai7/Capestone-project-Mobile-Price-Range-Prediction/assets/125723652/c256450a-145c-4dcb-a4e2-e9ac2d933a31)

* We can Note that Price Range does not show any significant change with the change in internal Memory.

![image](https://github.com/Ujjwalrai7/Capestone-project-Mobile-Price-Range-Prediction/assets/125723652/af996b47-2cf3-438e-b07e-b884ace8bf36)

* We can observe that for very high cost category we get the maximum RAM across all number of cores available.

* Hence, RAM is a strong predictor of the price range as we can see RAM increases with price for each number of cores available.


## ***7. ML Model Implementation and evaluation matrices ***

![image](https://github.com/Ujjwalrai7/Capestone-project-Mobile-Price-Range-Prediction/assets/125723652/3cee8dc4-1402-4608-931f-601340993a36)

### Feature importance as per XGBClassifier with hyperparameter tunning

![image](https://github.com/Ujjwalrai7/Capestone-project-Mobile-Price-Range-Prediction/assets/125723652/0745544c-37c0-41d3-9e35-35a8a1aed156)

# **Conclusion**


* We have implemented 6 classification models and have achieved a fairly good result for all the algorithms.

  * Logistic Regression
  * Random Forest
  * XGBoosting
  * Decision Tree
  * K Nearest Neighbors
  * Support Vector Machine

* Logistic Regression and XGBoost has performed better than any other model by achieving an accuracy of 92% which is the highest among the 6 models implemented.

* Through the tree based methods we found out that RAM, battery power, px_height and px_width are the most important features for the prediction of price ranges.





