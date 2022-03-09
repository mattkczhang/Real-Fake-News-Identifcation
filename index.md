## Real / Fake News Identification

### Project Overview

The Real / Fake News Identification project is a in-class group project at Macalester College Statistical Machine Learning course in 2019 fall.

The project intends to classify the news based on their title and text using logistic, KNN, decision tree, and random forest models. The features for modeling are designed and defined our group baased on titles and texts. We finally figure out that the logistic model can generate the highest cross-validated / out-of-bag accuracy, around 82%. The result is robust with different input features and model regularization.

The final logistic model can be applied to the real-world by recognizing fake news based on titles and contents. Given that fake news as a term was added to Oxford Dictionary and widely used among different situations, it is valuable to have such classfication tool for better information processing.

### Project Process

#### 1. Data Cleaning and Variables Creation

- Check the shape, null values of the raw data 
- Define and create variables that could potentially be used to identify fake news through **human thinking**.
- Create simple mean comparison of all features between real and fake news.

#### 2. Modeling Analysis

- Construct Logistic Regression, KNN, Classification Tree, and Random Forest models with different variable selections.
- Optimize the models through visualizations like elbow graph. 
- Compare the error and accuracy, both in-sample and cross-validated, of each optimized model. 
- Find out the variables importance through Random Forest and validate via density plot visualization. 

#### 3. Final Result and Take Home Message

- If we start to further cut the number of variables, our model will have lower both in-sample and CV accuracy.
- Variables provided by the Forest are not necessarily GOOD variables. Based on our examination and visualization, we can see that some important variables given by the Forest actually don’t have good natural cut, or large overlapping area, while some less important variables are the opposite.
- Considering both the ranking provided by Random Forest algorithm and visualizations, we think the most important predictor is `TextNumOfQuotation`(total number of quotation mark in the text), whereas the least important predictor is `TitleNumOfQue`(total number of question mark in the title).
- Logistic models are the fairly good classifications in all senarios and the logistic model using the six most important variables from the Forest is the best model that both balance the computational expense and the CV accuracy.

#### The density plots

#### 1. the 4 most important features

![1](https://user-images.githubusercontent.com/94136772/157403504-5f4b2685-fb9f-45d5-bf88-60b672f1cfcd.png)

![2](https://user-images.githubusercontent.com/94136772/157403614-37181ab6-9a65-40f5-8afa-49ab8a868dfd.png)

![3](https://user-images.githubusercontent.com/94136772/157403654-ad5361ee-a092-4c1b-b373-87217881e9eb.png)

![4](https://user-images.githubusercontent.com/94136772/157403681-718a5042-2ab6-4698-a5c3-1768f896e66c.png)

#### 2. the 4 least important features

![5](https://user-images.githubusercontent.com/94136772/157403754-bde6e5f6-5d4a-4efa-a596-fa3fe84c6eaa.png)

![6](https://user-images.githubusercontent.com/94136772/157403760-2188a990-f3bf-441d-bcc9-723457db50d2.png)

![7](https://user-images.githubusercontent.com/94136772/157403767-e25b7816-74a3-4fc6-bea6-f420b3b04773.png)

![8](https://user-images.githubusercontent.com/94136772/157403771-64e43a2e-aaec-486a-8632-67dd0a7ca6cb.png)

### Software usage

- `R Studio` is used for data cleaning, regression analysis, visualization, and project compliation.

### Authors

Kaichong (Matt) Zhang: Macalester Student

Ling Ma: Macalester Student

Yiming Miao: Macalester Student

##### More details can be seen in Matt's repository [Real-Fake-News-Identifcation](https://github.com/mattkczhang/Real-Fake-News-Identifcation)
