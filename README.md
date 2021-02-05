# Math-Concepts
## Naive Bayes Classifier

### :question: What is Naive Bayes algorithm?
It is a classification technique based on Bayes’ Theorem with an assumption of independence among predictors. In simple terms, a **Naive Bayes** classifier assumes that the presence of a particular feature in a class is unrelated to the presence of any other feature.
![Posterior probability](https://res.cloudinary.com/dnonuly2u/image/upload/v1590449878/Bayes_rule-300x172-300x172_c5nbpd.webp)

### :bar_chart: How does Naive Bayes work?
- Step 1: Convert the data set into a frequency table

- Step 2: Create Likelihood table by finding the probabilities like Overcast probability = 0.29 and probability of playing is 0.64.

![enter image description here](https://res.cloudinary.com/dnonuly2u/image/upload/v1590450256/Bayes_41-850x310_ypovxw.webp)

- Step 3: Now, use Naive Bayesian equation to calculate the posterior probability for each class. The class with the highest posterior probability is the outcome of prediction.

### :blue_book: About this **notebook**
Inside the Naive-Bayes-Classifier.ipynb I have went through the basics of **probability** all the way up to implementing Naive Bayes Classifier from scratch. 

- Used dataset: Iris Flower Species (iris.csv)
 - A look at the first few rows of the dataset:
```python
4.9,3.0,1.4,0.2,Iris-setosa
4.7,3.2,1.3,0.2,Iris-setosa
4.6,3.1,1.5,0.2,Iris-setosa
5.0,3.6,1.4,0.2,Iris-setosa
...
```

- Used resampling method: *K-folds Cross Validation* with 5 folds.

- Steps in achieving the goal:
	- <h4 style="color: orange;"> Step 1: Separate By Class</h4>
	 	- Separate training data by class.
	- <h4 style="color: orange;"> Step 2: Summarize Dataset</h4>
	 	- The two statistics that are required from a given dataset are the mean and the standard deviation (average deviation from the mean).
	- <h4 style="color: orange;"> Step 3: Summarize Data By Class</h4>
	 	- Above, is created the *separate_by_class()* function to separate a dataset into rows by class. In addition, *summarize_dataset()* function is created to calculate summary statistics for each column.
	-  <h4 style="color: orange;"> Step 4: Gaussian Probability Density Function</h4>
	 	- A Gaussian distribution can be summarized using only two numbers: the mean and the standard deviation. Therefore, with a little math, I can estimate the probability of a given value. This piece of math is called a Gaussian Probability Distribution Function (or Gaussian PDF) and can be calculated as:
	 
	 ![image description](https://res.cloudinary.com/dnonuly2u/image/upload/v1590451963/CodeCogsEqn_wpscjh.svg)

	-  <h4 style="color: orange;"> Step 5: Class Probabilities</h4>
	 	- Probabilities are calculated separately for each class. This means that firstly calculated is the probability that a new piece of data belongs to the first class, then calculate probabilities that it belongs to the second class, and so on for all the classes.

