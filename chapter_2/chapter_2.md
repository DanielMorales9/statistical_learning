# Exercises

1. Flexible statistical learning method better of worse than an inflexible method.    
  a. The flexible method will fit the data closer and a larger sample size will be less vulnerable to overfitting    
  b. The flexible method will overfit the small number of observations and the predictor may mislead the model.    
  c. The flexible method will catch the non-linear relationship between the predictors and response variable.    
  d. The flexible method will fit the error term and increase variance.    

2. Explain whether each scenario is a classification or regression problem and indicate whether we are most insterested in inference or prediction. Finally, provide _n_ and _p_.    
  a. Regression, Inference, 500, 3, profit, number of employees, industry    
  b. Classification, Prediction, 20, 13, price charged, marketing budget, comp. price, ten other variables    
  c. Regression, Prediction, number of weeks since 2012, 3, the % change in the US market, % change in the British market, % change in the German market    

3.a We not revisit the bias-variance decomposition.    
- The (squared) bias decreases by increasing the flexibility of the model.    
- The variance increases by increasing the flexibility of the model.    
- The training error decreases by increasing the flexibility of the model.    
- The test error presents a classical U-shape function.    
- The irreducible error or bayes error is represented by a dashed horizontal line which lies below all the other lines except the training error line.    

3.b Explain why each of the five curves has the shape displayed in part (a)         
- The bias represents the error is that is introduced by approximating a real-life problem which may be extremely complicated, by a much simpler model. Thus, the more flexible the model becomes, the lower the squared bias becomes.   
- On the other hand, the variance represents the amount of error the function would introduced if we used different training data. Ideally, a function should not vary to much between estimates on different datasets. Thus, the value of variance starts low on unflexible methods, and the increases severely with more flexible methods.    
- The training error is determined by the error the function has on the training set. Thus more flexible methods will result in overfitting on the training set, fitting even the irreducible error.    
- The irreducible error is the inherent error introduced by either unmesured or unmesurable variables that improve the function estimate and its predictions. This error is constant and does not change no matter what we do.
- Finally, the test error is the error measured at test time and is the combination of bias, variance and irreducible error. Thus, it is higher than the irreducible error and it usually follows the same trend of the bias error on unflexible methods, it touches the irreducible error and then follows the variance trend on more flexible methods.

4. You will now think of some real-life applications for statistical learning.

4.a. Describe three real-life applications in which _classification_ might be useful. Describe the response, as well as the predictors. Is the goal of each application inference or prediction? Explain your answer.
- Spam Filter: the goal is to predict whether an email is a spam and should be delivered to the Junk folder. The response variable is whether the email is spam or not, the predictors are all the possible words in the english dictionary which length is larger than 3. The task is to use the model to infer whether a given email is spam or not.    
- Handwritten Digit Recognizer: the goal is to identify which digit the image represents. The response variable _digit_ is categorical and its value span from 0 to 9. The predictor variables are represented by the image's pixels. We are dealing with a prediction task as we want to predict given an image the represented digit value.     
- Payment Fraud: the goal is to identify whether a certain purchase will be fraud or not. The fraud label is the response variable and its last 5 purchased items and the current purchased item are the predictor variables. It is a prediction task.

4.b. Describe three real-life applications in which _regression_ might be useful. Describe the response, as well as the predictors. Is the goal of each application inference or prediction? Explain your answer.
- Impact of Advertising on Sales: the goal is to understand which relationship contributes the most to the sales of a product given its past advertising expenditure. The response variable is the number of sales or the total sales value, given the different advertising means (predictors): Radio, TV, Web. The task is to infer (inference) which advertising means is contributing the most to it.    
- Salary Analysis: the goal is to understand the relationship between salary values measured in thousands of USD dollars, and education, country, age. The response variable is the salary value, the predictor variables are the education, the state, and the age. The task is an is to infer which predictor contributes the most to the salary.    
- Grade estimate: the goal is to estimate the grade the students will get to exams given the history of exams. The response variable is the grade value, given (the predictors) a student id, course id, professor id, hours studies for the exam.

4.c. Describe three real-life applications in which _cluster analysis_ might be useful.   
- Marketing: finding groups of customers with similar behavior given a large database of customer data containing their properties and past buying records    
- Insurance: identifying groups of motor insurance policy holders with a high average claim cost    
- Earthquake studies: clustering observed earthquake epicenters to identify dangerous zones    

5. Pros and Cons of a very flexible vs less flexible approach for regression or classification? Under what circumstances might a more flexible approach be preferred to a less flexible approach? When might a less flexible approach be preferred?    
- A flexible approach can fit several functions f, which requires to fit many different parameters, on a huge number of predictors and observations. However, it can lead to overfitting the data to quickly, which means that it models also the noise as well.
- On the other hand, a less flexible model is usefull to fit a simple relationship between a small number of predictors, given a little number of observed samples. However, a less flexible model may increase the bias error when fitting more complex relationship on a biggere dataset.
- A simple rule of thumb is to use flexible methods when the relationship between response and predictor variables is complex, when the dataset is big and there are many predicot variables.
- On the other hand the a flexible methods works well on a smaller dataset and with simple relationships to model.

6. Parametric vs Non-parametric approaches.
- A parametric makes an assumption about the functional shape of f, a procedure is then used to make fit or train the model parameters. Thus, parametric approaches reduce the problem of estimating f down to one of estimating a set of parameters. The disadvantage of this is that it may not match the true unknown form of f.
- Non-parametric approaches do not make explicit assumptions about the functional form of f. They can accurately fit a wider range of possible shapes, however, a very large number of observations (far more than is typically needed for a parametric approach).

7. The table below provides a training dataset containing six observations three predictors, and one qualitative response variable.
- Compute distances between variables observations: 3.0, 2.0, 3.16, 2.23, 1.41, 1.73     
- K = 1 prediction is Green, closest is observation number 5
- K = 3 prediction is Red, closest are 5, 6, 2 (Green, Red, Red)
- Small. A small K would be flexible for a non-linear decision boundary, whereas a bigger is not.
