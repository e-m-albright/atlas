# Machine Learning

Machine Learning / A.I.



Google's AI Course [https://www.reddit.com/r/programming/comments/8k3s6g/google\_provides\_free\_machine\_learning\_course\_for/](https://www.reddit.com/r/programming/comments/8k3s6g/google_provides_free_machine_learning_course_for/)

https://developers.google.com/machine-learning/rules-of-ml/

https://medium.com/@ageitgey/machine-learning-is-fun-part-2-a26a10b68df3

https://ml.berkeley.edu/blog/2017/07/13/tutorial-4/

https://www.reddit.com/r/programming/comments/6kfzmu/pytorch\_tutorial\_facebooks\_deep\_learning\_library/

http://neuralnetworksanddeeplearning.com/index.html

https://towardsdatascience.com/how-to-build-a-real-time-hand-detector-using-neural-networks-ssd-on-tensorflow-d6bac0e4b2ce

https://blog.machinebox.io/processing-video-to-do-face-recognition-with-go-and-python-298275a26095 

https://www.amazon.com/Hands-Machine-Learning-Scikit-Learn-TensorFlow/dp/1491962291/ref=pd\_lpo\_sbs\_14\_t\_0?\_encoding=UTF8&psc=1&refRID=NH8XY2DH82NJAGZSZ5SY

https://www.amazon.com/Python-Machine-Learning-scikit-learn-TensorFlow/dp/1787125939/ref=pd\_sim\_14\_2?\_encoding=UTF8&pd\_rd\_i=1787125939&pd\_rd\_r=GDNZMMCJ3NSB3PAKQGQP&pd\_rd\_w=7uyMe&pd\_rd\_wg=9O6gh&psc=1&refRID=GDNZMMCJ3NSB3PAKQGQP

https://www.amazon.com/Deep-Learning-Adaptive-Computation-Machine/dp/0262035618/ref=pd\_sim\_14\_2?\_encoding=UTF8&pd\_rd\_i=0262035618&pd\_rd\_r=NH8XY2DH82NJAGZSZ5SY&pd\_rd\_w=37gsT&pd\_rd\_wg=MEq6z&psc=1&refRID=NH8XY2DH82NJAGZSZ5SY 

https://ml-cheatsheet.readthedocs.io/en/latest/index.html

https://blog.statsbot.co/deep-learning-achievements-4c563e034257 

http://cachestocaches.com/2017/12/favorite-deep-learning-2017/ 

http://www.inference.vc/sharp-vs-flat-minima-are-still-a-mystery-to-me/







Machine Learning

normalize is zero mean, zero variance?

if data is high dimension, conider using a reducer like PCA, \(principal component analysis\) or random projection



review approximate nearest neighbors



vector p-norm https://planetmath.org/vectorpnorm

Model Explainability

...

Supervised Learning

...

Decision Trees

random forest

gradient boosted \(xgboost\)

still surprisingly SOTA, adaptable, my fav first pick

models non-mathematical boundaries / gradients well

works with imbalanced classes





Unsupervised Learning

Structure learning



KNN Clustering



Hierarchical Clustering



Gaussian Mixture Model:

estimating centers, looking at log probability of point being in class... it's for clustering/outlier detection



Expectation minimization:



Outlier detection

Generalizability

Train, Test, Validate

The whole principle of splitting data is to generalize. Test is sometimes polluted, hence, validation is the final performance measure not to be used more than once.

Regularization

intentionally limit specialization to avoid overfitting and/or create generalizability

\(prevent the model from doing too well on the trainnig data\)

\(Ridge Regression\) L2-Regularization mimization 

spreads out the weights \(big off points add more than many small\)

\(Lasso Regression\) L1-Regularized minimization

big weights/loss same as many small

Elastic net

Dropout

Batch normalization

Stochastic depth, fractional pooling

Normalization

Generalization

Complexity vs generalization

Cross Validation

K-Fold

Cycles through choice of which subset of the training data is the hold-out validation fold. Averge results. 5-Fold is 4 training sets, 1 holdout.



Early Stopping

stop fitting earlier than might be warranted

Hyperparameters

Affects how models train and perform during evaluation

Distances

L1 - manhattan distance, absolute distance

d1\(I1, I2\)=p\|I1p-I2P\|

L2 - euclidean distance, sum of squared



Learning Rate

size of step adjustment



Many more specific to training architecture \(model\)

Bootstrap Frequency of Selection

point estimate vs bootstrap confidence interval

Basis Expansion

related?

Kernels

kernels... distance measures?

kernel ridge regression

feature engineering?

"polynomial kernel"

paired often with SVM's? which makes sense as you need to go to higher dimensions to find clean cuts? RBF's, polynomial degree 2, degree 3, linear

Performance Measures 

Bayes Error Rate - theoretical minimum error rate

Loss

Many means of measuring happiness, loss is semi-arbitrary

Squared errors / losses will emphasize single huge discrepancies.

Multiclass SVM Loss

Loss should have margin for robustness

Loss should be differentiable to know how to update

Exploration vs. Exploitation

Multi-armed bandit problems

- continue looking for new different improvements or work on refining a promising lead



Choosing the best model

you can do some bootstrapping to evaluate the two models to guage their comparative performance. Like accuracy 1 - accuracy 2, 95% confidence interval should not contain 0.



empirical bootstrap distribution

Classification

Logistic regression

\(the classification version of linear\)

F\(x,W\) = Wx

input say 10 x 3072



Hyperplane

separator of classes, geometric concept, with representation in algebra



Bias

...



Regression

linear regression



\(KNN\) Nearest Neighbors / K-Nearest Neighbors

\(SVM\) Support Vector Machine:

The margin is the score between correct & next best class in SVM. Working to maximize this. 

Multiclass SVM Loss - total SVM loss is average loss of classes



basically linear separators, line linear models

max\(0, s\_j - s\_i +1\)

\(for each wrong class\)

score for wrong class vs score for right class. +1 is a margin set, to give loss unless the correct class is at least 1 higher in score.



Kernel:



Gaussian:





Gradients

smoothly defined gradients / solution space can be optiized on

mini-batching, you can estimate gradient pretty well with smaller batches, doing it on the full set is expensive

epoch - a run through the whole training data \(through iterations in mini-batches perhaps\)



backpropagation - finding partial derivatives to adjust weights in huge networks all in a chain of local gradients



sigmoid - a decision bound function of activation threshold?

Stochastic Gradient Descent



Adam Optimizer

## **Machine Learning**

**normalize is zero mean, zero variance?**

**if data is high dimension, conider using a reducer like PCA, \(principal component analysis\) or random projection**  


**review approximate nearest neighbors**  


**vector p-norm** [**https://planetmath.org/vectorpnorm**](https://planetmath.org/vectorpnorm)

#### **Model Explainability**

**...**

#### **Supervised Learning**

**...**

**Decision Trees**

**random forest**

**gradient boosted \(xgboost\)**

**still surprisingly SOTA, adaptable, my fav first pick**

**models non-mathematical boundaries / gradients well**

**works with imbalanced classes**  
  


#### **Unsupervised Learning**

**Structure learning**  


**KNN Clustering**  


**Hierarchical Clustering**  


**Gaussian Mixture Model:**

**estimating centers, looking at log probability of point being in class... it's for clustering/outlier detection**  


**Expectation minimization:**  


**Outlier detection**

### **Generalizability**

#### **Train, Test, Validate**

**The whole principle of splitting data is to generalize. Test is sometimes polluted, hence, validation is the final performance measure not to be used more than once.**

#### **Regularization**

**intentionally limit specialization to avoid overfitting and/or create generalizability**

**\(prevent the model from doing too well on the trainnig data\)**

1. **\(Ridge Regression\) L2-Regularization mimization** 
   1. **spreads out the weights \(big off points add more than many small\)**
2. **\(Lasso Regression\) L1-Regularized minimization**
   1. **big weights/loss same as many small**
3. **Elastic net**

**Dropout**

**Batch normalization**

**Stochastic depth, fractional pooling**

#### **Normalization**

**Generalization**

**Complexity vs generalization**

**Cross Validation**

**K-Fold**

**Cycles through choice of which subset of the training data is the hold-out validation fold. Averge results. 5-Fold is 4 training sets, 1 holdout.**  


**Early Stopping**

**stop fitting earlier than might be warranted**

#### **Hyperparameters**

**Affects how models train and perform during evaluation**

**Distances**

**L1 - manhattan distance, absolute distance**

**d1\(I1, I2\)=p\|I1p-I2P\|**

**L2 - euclidean distance, sum of squared**  


**Learning Rate**

**size of step adjustment**  


**Many more specific to training architecture \(model\)**

#### **Bootstrap Frequency of Selection**

**point estimate vs bootstrap confidence interval**

#### **Basis Expansion**

**related?**

#### **Kernels**

**kernels... distance measures?**

**kernel ridge regression**

**feature engineering?**

**"polynomial kernel"**

**paired often with SVM's? which makes sense as you need to go to higher dimensions to find clean cuts? RBF's, polynomial degree 2, degree 3, linear**

#### **Performance Measures** 

**Bayes Error Rate - theoretical minimum error rate**

**Loss**

**Many means of measuring happiness, loss is semi-arbitrary**

**Squared errors / losses will emphasize single huge discrepancies.**

**Multiclass SVM Loss**

**Loss should have margin for robustness**

**Loss should be differentiable to know how to update**

**Exploration vs. Exploitation**

**Multi-armed bandit problems**

**- continue looking for new different improvements or work on refining a promising lead**  


**Choosing the best model**

**you can do some bootstrapping to evaluate the two models to guage their comparative performance. Like accuracy 1 - accuracy 2, 95% confidence interval should not contain 0.**  


**empirical bootstrap distribution**

#### **Classification**

**Logistic regression**

**\(the classification version of linear\)**

**F\(x,W\) = Wx**

**input say 10 x 3072**  


**Hyperplane**

**separator of classes, geometric concept, with representation in algebra**  


**Bias**

**...**  


#### **Regression**

**linear regression**  


**\(KNN\) Nearest Neighbors / K-Nearest Neighbors**

**\(SVM\) Support Vector Machine:**

**The margin is the score between correct & next best class in SVM. Working to maximize this.** 

**Multiclass SVM Loss - total SVM loss is average loss of classes**  


**basically linear separators, line linear models**

**max\(0, s\_j - s\_i +1\)**

**\(for each wrong class\)**

**score for wrong class vs score for right class. +1 is a margin set, to give loss unless the correct class is at least 1 higher in score.**  


**Kernel:**  


**Gaussian:**  
  


#### **Gradients**

**smoothly defined gradients / solution space can be optiized on**

**mini-batching, you can estimate gradient pretty well with smaller batches, doing it on the full set is expensive**

**epoch - a run through the whole training data \(through iterations in mini-batches perhaps\)**  


**backpropagation - finding partial derivatives to adjust weights in huge networks all in a chain of local gradients**  


**sigmoid - a decision bound function of activation threshold?**

**Stochastic Gradient Descent**

**Adam Optimizer**



