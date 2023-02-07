## Linear and Logistic Regression - HelloWorld for AIML
### Linear Regression - Predict the price of a home, based on multiple different variables. Use sci-kit’s linear_model.LinearRegression()
Linear Regression is a machine learning algorithm that determines the relationship between one dependent variable (y) and one or more independent variables (x). It models a target prediction value based on the dependent variable, using this determined relationship. 

A linear regression line has the equation **Y=mX + b**

where Y is the dependent variable, m is the slope, X is the dependent variable and b is the y intercept. 

If there is more than one independent variable, the equation will be modified to 

**Y = m<sub>1</sub>X<sub></sub>1</sub> +</sub> m<sub>2</sub>X<sub>2</sub> + m<sub>3</sub>X<sub>3</sub> + … + b**

The regression algorithm is being implemented using Jupyter Notebook using some standard built in Python libraries, which include:
<ol>
  <li><strong>NumPy</strong> supports large multi-dimensional arrays and matrices, along with a large collection of mathematical functions to operate on these.</li>
  <li><strong>Pandas</strong>, a software library written mainly for data manipulation and analysis purposes.</li>
  <li><strong>Scikit-learn</strong> is a popular machine learning library with various classification, regression and clustering algorithms.</li>
  <li><strong>Matplotlib</strong> is a library that works as an extension of NumPy. It provides an API for embedding plots into applications.</li>
</ol>
The code can be split into the following major steps:

<ol>
  <li>Importing all the dependent modules and libraries</li>
  <br><img src = "/pictures/1.1.png"></img>
  <li>Now, we import the housing data and store it in a variable</li>
  <br><img src = "/pictures/1.2.png"></img>
  <br>Note that here, data refers to the x values, target refers to the y values and feature names refer to the column names.
  <li>Now, we put this data into a DataFrame using Pandas. DataFrames are used because they are easy to manipulate. The x and y values are put into two separate DataFrames. The conversion function and code is as shown below</li>
  <br><img src = "/pictures/1.3.png"></img>
  <li>Now, we view the first 5 rows of the newly created DataFrame as well as some of its descriptive statistics using the head() and describe() functions</li>
  <br><img src = "/pictures/1.4.png"></img>
  <li>Printing the shape of x and y values (shape is the number of rows and columns in the DataFrame)</li>
  <br><img src = "/pictures/1.5.png"></img>
  <li>Now, we create an instance of scikit- learn's regression model. We go on to use the train_test_split function to split our data into training and testing data.</li>
  <br><img src = "/pictures/1.6.png"></img>
  <br>Here, 66% of the data falls into the training data while the rest becomes testing data
  <li>Now, we train or ‘fit’ the data with the help of our training data</li>
  <br><img src = "/pictures/1.7.png"></img>
  <li>Now, we use the relationship determined by training the model to predict y values for the testing values of x.</li>
  <br><img src = "/pictures/1.8.png"></img>
  <li>Plotting a graph of the actual data against the predicted data (using matplotlib), we get</li>
  <br><img src = "/pictures/1.9.png"></img>
  <li>We calculate the mean squared error (the average of the squared difference between the predicted and actual values). The lower this is, the more accurate the model is. Along with this, we also calculate the r2 score (ratio of information that the model can explain to the total information). Clearly, the higher r2 is, the better the relationship between the dependent and independent values.</li>
  <br><img src = "/pictures/1.10.png"></img>
  <br>So, the model is 99.2673% accurate.
</ol>

### Logistic Regression - Train a model to distinguish between different species of the Iris flower based on sepal length, sepal width, petal length, and petal width. Use sci-kit’s linear_model.LogisticRegression
Logistic Regression is a classification algorithm. It models the probability of an event taking place by plotting the logarithmic sigmoid (to bring the output between 0 and 1) of a linear combination of independent variables. 

Concepts like maximum likelihood and the decision boundary are used in this model to classify the given data into required categories.

Something to note is that classification requires probability of the class and therefore should be between 0 and 1, in contrast to linear regression which places no bounds on the predicted outcome.

Here, we pick up the iris dataset containing 50 instances each for three species of flowers (Iris Setosa, Iris Versicolor and Iris Virginica) and their four attributes - petal width and length and sepal width and length. 

The modules and libraries used are the same as the ones in linear regression except for one - **Seaborn**, a data visualization library based on matplotlib. It is used mainly for integrating high-level statistical graphics.

The implementation of the model can be split up into the following steps:


