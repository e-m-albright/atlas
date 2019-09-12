# Index

## **Toolbelt**

### **Python**

* **numpy**
  * **the "confusing" indexing is tensor\[row,column\]**
  * **broadcasting:** 
    * [**https://docs.scipy.org/doc/numpy/reference/routines.math.html**](https://docs.scipy.org/doc/numpy/reference/routines.math.html)
    * [**https://docs.scipy.org/doc/numpy/reference/ufuncs.html\#available-ufuncs**](https://docs.scipy.org/doc/numpy/reference/ufuncs.html#available-ufuncs)
    * [**https://scipy.github.io/old-wiki/pages/EricsBroadcastingDoc**](https://scipy.github.io/old-wiki/pages/EricsBroadcastingDoc)
    * [**https://docs.scipy.org/doc/numpy/user/basics.broadcasting.html**](https://docs.scipy.org/doc/numpy/user/basics.broadcasting.html)
    * 

**\#     print\(np.tile\(a\[0\], reps=3\)\)**

**\#     print\(np.diag\(a\[0\]\)\)**

**\#     \# \(a - b\)\*\*2 = a\*\*2 - \(2 \* a \* b\) + b\*\*2**

**\#     a\_squared = a\*\*2**

**\#     b\_squared = b\*\*2**

   **\# if the goal is 500x5000 then can we get that from an addition of a\*\*2 and b\*\*2?**

   **\# if not... what gives.**

**\#     a\_squared + b\_squared**

**\#     two\_ab = 2 \* a.dot\(b.T\)**

**\#     a\_squared\_sums = np.sum\(a\_squared, axis=1\)**

**\#     b\_squared\_sums = np.sum\(b\_squared, axis=1\)**

**\#     print\(a\_squared\_sums.shape\)**

**\#     print\(b\_squared\_sums.shape\)**

**\#     print\(two\_ab\[0:2,0:2\]\)**

**\#     two\_ab += np.tile\(a\_squared\_sums, reps=two\_ab.shape\[1\]\)**

**\#     print\(two\_ab\[0:2,0:2\]\)**

**\#     dists\[:,:\] = \(a\_squared + b\_squared\)\# - \(2 \* a \* b.T\)**  


**\# observation = array\(\[111.0,188.0\]\)**

**\# &gt;&gt;&gt; codes = array\(\[\[102.0, 203.0\],**

**\# ...                \[132.0, 193.0\],**

**\# ...                \[45.0, 155.0\],**

**\# ...                \[57.0, 173.0\]\]\)**

**\# &gt;&gt;&gt; \# here is the broadcast**

**\# &gt;&gt;&gt; diff = codes - observation**

**\# &gt;&gt;&gt; dist = sqrt\(sum\(diff\*\*2,axis=-1\)\)**  


   **\# ... this is frustrating.**

   **\# Eric's Broadcasting Doc, illustration of euc dist NOT WORKING**

**\#     diff = test\[np.newaxis,:,:\] - train\[:,np.newaxis,:\]**

**\#     dists = np.sqrt\(np.sum\(diff\*\*2, axis=-1\)\)**

   **\# okay... gotta use the equation. What are frobenius norms to me?**

   **\# A^2 - 2AB + B^2**

   **\# how the fuck is this supposed to work with dimensions**

   **\# 5x3 - 2\(5x3\)\(50x3\) + 50x3 = 5x50??**

   **\# summed 5x1 - 2 dot product? + summed 50x1??**

   **import numpy as np**  


**x = np.array\(\[\[1,2\],\[3,4\]\]\)**

**y = np.array\(\[\[5,6\],\[7,8\]\]\)**  


**v = np.array\(\[9,10\]\)**

**w = np.array\(\[11, 12\]\)**  


**\# Inner product of vectors; both produce 219**

**print\(v.dot\(w\)\)**

**print\(np.dot\(v, w\)\)**  


**\# Matrix / vector product; both produce the rank 1 array \[29 67\]**

**print\(x.dot\(v\)\)**

**print\(np.dot\(x, v\)\)**  


**\# Matrix / matrix product; both produce the rank 2 array**

**\# \[\[19 22\]**

**\#  \[43 50\]\]**

**print\(x.dot\(y\)\)**

**print\(np.dot\(x, y\)\)**  
  


**\# We will add the vector v to each row of the matrix x,**

**\# storing the result in the matrix y**

**x = np.array\(\[\[1,2,3\], \[4,5,6\], \[7,8,9\], \[10, 11, 12\]\]\)**

**v = np.array\(\[1, 0, 1\]\)**

**vv = np.tile\(v, \(4, 1\)\)   \# Stack 4 copies of v on top of each other**

**print\(vv\)                 \# Prints "\[\[1 0 1\]**

                         **\#          \[1 0 1\]**

                         **\#          \[1 0 1\]**

                         **\#          \[1 0 1\]\]"**

**y = x + vv  \# Add x and vv elementwise**

**print\(y\)  \# Prints "\[\[ 2  2 4**

         **\#          \[ 5 5 7\]**

         **\#          \[ 8 8 10\]**

         **\#          \[11 11 13\]\]"**

**\# We will add the vector v to each row of the matrix x,**

**\# storing the result in the matrix y**

**x = np.array\(\[\[1,2,3\], \[4,5,6\], \[7,8,9\], \[10, 11, 12\]\]\)**

**v = np.array\(\[1, 0, 1\]\)**

**y = x + v  \# Add v to each row of x using broadcasting**

**print\(y\)  \# Prints "\[\[ 2  2 4\]**

         **\#          \[ 5 5 7\]**

         **\#          \[ 8 8 10\]**

         **\#          \[11 11 13\]\]"**  
  
  
  
  
  


**\# Compute outer product of vectors**

**v = np.array\(\[1,2,3\]\)  \# v has shape \(3,\)**

**w = np.array\(\[4,5\]\)    \# w has shape \(2,\)**

**\# To compute an outer product, we first reshape v to be a column**

**\# vector of shape \(3, 1\); we can then broadcast it against w to yield**

**\# an output of shape \(3, 2\), which is the outer product of v and w:**

**\# \[\[ 4  5\]**

**\#  \[ 8 10\]**

**\#  \[12 15\]\]**

**print\(np.reshape\(v, \(3, 1\)\) \* w\)**  


**\# Add a vector to each row of a matrix**

**x = np.array\(\[\[1,2,3\], \[4,5,6\]\]\)**

**\# x has shape \(2, 3\) and v has shape \(3,\) so they broadcast to \(2, 3\),**

**\# giving the following matrix:**

**\# \[\[2 4 6\]**

**\#  \[5 7 9\]\]**

**print\(x + v\)**  


**\# Add a vector to each column of a matrix**

**\# x has shape \(2, 3\) and w has shape \(2,\).**

**\# If we transpose x then it has shape \(3, 2\) and can be broadcast**

**\# against w to yield a result of shape \(3, 2\); transposing this result**

**\# yields the final result of shape \(2, 3\) which is the matrix x with**

**\# the vector w added to each column. Gives the following matrix:**

**\# \[\[ 5  6 7\]**

**\#  \[ 9 10 11\]\]**

**print\(\(x.T + w\).T\)**

**\# Another solution is to reshape w to be a column vector of shape \(2, 1\);**

**\# we can then broadcast it directly against x to produce the same**

**\# output.**

**print\(x + np.reshape\(w, \(2, 1\)\)\)**  


**\# Multiply a matrix by a constant:**

**\# x has shape \(2, 3\). Numpy treats scalars as arrays of shape \(\);**

**\# these can be broadcast together to shape \(2, 3\), producing the**

**\# following array:**

**\# \[\[ 2  4 6\]**

**\#  \[ 8 10 12\]\]**

**print\(x \* 2\)**  


* **pandas**
* **sklearn**
* **scipy**
* **ray**
* **joblib**
* **multiprocessing**
* **debugging libraries / timing libraries? I forget**
* **plotly**
* **seaborn**
* **matplotlib**
* **bokke**
* **keras**
* **tensorflow**
* **pytorch**
* **spaCy**
* **NLTK**

### **Plotly**

**dash/ plotly, react/js compatible plotting awesomeness and custom dashboarding**

### **Jupyter** 

**Notebooks \(basically python, markdown\)**

**Sagemaker - model training, hyperparameter optimization, deployment \(competitors - databricks, google/microsoft?\)**  


**Learn More:**

[**https://nbviewer.jupyter.org/github/jupyter/notebook/tree/master/docs/source/examples/Notebook/**](https://nbviewer.jupyter.org/github/jupyter/notebook/tree/master/docs/source/examples/Notebook/)

### **Git**

**git reset --soft HEAD~3 &&**

**git commit**  


**git push -d origin eda**  


### **AWS**

**aws s3 mb s3://omada-datasciece-production/evan \(might be wrong, think the first is the bucket, directory might come from sync\)**  


**aws s3 sync ~/Downloads/xenos\_data/ s3://omada-datascience-production/evan**  


### **SQL**

#### **Postgresql**

**psql -h**[ **xenos-db.omadahealth.net**](http://xenos-db.omadahealth.net/) **-U xenos\_app -d xenos\_production**  


**\d &lt;table&gt;**

**\d+**  


**rsync -zvh -e ssh output/cache/application\_weights.feather nfs:~/**  


**ALTER TABLE case\_annotations DROP COLUMN multi\_user\_overlap;**  


**ALTER TABLE labeled\_weights ADD COLUMN created\_at TIMESTAMP DEFAULT now\(\);**

**ALTER TABLE case\_annotations ADD COLUMN created\_at TIMESTAMP DEFAULT now\(\);**  


**DELETE FROM labeled\_weights WHERE labeler = 'banana';**  


**UPDATE labeled\_weights SET labeler = 'new.name' where labeler = 'old.name';**  


#### **NoSQL**

### **XGBoost**

**LINKPAPER HERE**

[**https://arxiv.org/pdf/1603.02754.pdf**](https://arxiv.org/pdf/1603.02754.pdf)

[**https://towardsdatascience.com/https-medium-com-vishalmorde-xgboost-algorithm-long-she-may-rein-edd9f99be63d**](https://towardsdatascience.com/https-medium-com-vishalmorde-xgboost-algorithm-long-she-may-rein-edd9f99be63d)

[**https://machinelearningmastery.com/gentle-introduction-gradient-boosting-algorithm-machine-learning/**](https://machinelearningmastery.com/gentle-introduction-gradient-boosting-algorithm-machine-learning/)

[**https://machinelearningmastery.com/gentle-introduction-xgboost-applied-machine-learning/**](https://machinelearningmastery.com/gentle-introduction-xgboost-applied-machine-learning/)

[**https://www.analyticsvidhya.com/blog/2018/09/an-end-to-end-guide-to-understand-the-math-behind-xgboost/**](https://www.analyticsvidhya.com/blog/2018/09/an-end-to-end-guide-to-understand-the-math-behind-xgboost/)  
****

[**https://github.com/aws/sagemaker-python-sdk/tree/master/src/sagemaker/xgboost**](https://github.com/aws/sagemaker-python-sdk/tree/master/src/sagemaker/xgboost)  
****

**Excellent first pick to pretty much any problem**

**sparsity aware**

**approximate tree learning**

**top tier scalability**

**weighed quantile sketch**

**weak learners**

**ensemble**

**\(see paper\)**

**still SOTA since about 2015/2016 on**

**ads, spam, fraud, anomaly detection,**  


### **MapReduce/ApacheSpark \(link to section\)**

### **Hadoop \(link to section\)**

