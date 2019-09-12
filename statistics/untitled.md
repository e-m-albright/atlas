# Index

## **Statistics**

[**MIT Cheat Sheet**](http://www.datasciguide.com/content/mit-statistics-cheat-sheet/)

[**SQL for interviews review**](https://towardsdatascience.com/how-to-ace-data-science-interviews-sql-b71de212e433)

**also go to Learn X in Y thing?**  


### **Fundamentals**

**Variable**

**A characteristic which varies over time or in different entities under consideration**

**Experimental Unit**

**The entity on which a variable is measured** 

**Population**

**The set of all measurements of interest to the investigator**

**Sample**

**The subset of measurements selected from the population of interest**

**Qualitative Variables // Categorical Data**

**Measure a quality or characteristic on each experimental unit**

**Quantitative Variables // Numerical Data**

**Measure a numerical quantity or amount on each experimental unit**  


**Discrete: A finite or countable number of values**

**Continuous: Infinitely many values**

**Identifiers**

**Help associate the measurements to the experimental units**

**Don't accidentally try to analyze these**

**Univariate Data**

**A single variable measured on a single experimental unit**

**Bivariate, Multivariate Data**

**Two variables measured on a single experimental unit.**

**Parameter**

**Numerical descriptive measures associated with a population of measurements**

**Statistics**

**Parameters computed from sample measurements**  


**Descriptive**

**Methods for organizing, displaying, and describing data by using tables, graphs, and summary measures**

**Inferential**

**Methods that use sample results to help make decisions or predictions about a population \(inference, inferring general rules about the population from a sample\)**  


**Margin of error - samples usually differ from the true population by some margin**  


**Sampling**

**random sample - avoid bias**

**simple random sampling**  


**random / cluster / stratisfied / systematic sampling**  


**coverage bias \(who can reply\), warning bias \(phrasing in questions\), no response bias \(who answers surveys\)**  


**frequency = real count**

**relative frequencies = response / sample size**

**percentage = relative frequency \* 100**  


**Intervals of uncertainty**  
  


**p-test**

**anova**

**a/b test**

**confidence**

**error bounding**

**bayes theorem**  


**variance**

**standard deviation**  


**regression analysis**

**multivariate statistical methods**

**non-parametric statistics**

**probability theory**  


**power tests**

**how big should my sample size be?**  


**P is probability of event**

**N is total dataset size**

**sample size is n**

**in the sample n-hat events occured**

**probability is then p-hat = n-hat/n \(is an estimation\)**

**find probability of p-hat derivation from p**

**prob\(\|p-hat - p\| &gt; d\(greek letter, error margin\)\) greaterthanequal gamma \(confidence parameter\)**

**prob \(p isinset \[p-d, p+d\]\) lessthanequal 1 - gamma**  


**indicator variable**

**indicator random variable**  


**using n-hat to estimate w/ chernoff bounds**

**chebychev bound**

**markov bound**  


**Jaccard Similarity - I have no idea where to put this**

#### **Distributions**

**Mode**

**Most common value**

**Mean**

**Average value**

**Median**

**Middle of range \(or if tied, average between the two\)**

**Resilient to outliers**

**Skewness**

**- no skew = symmetric, mean = median**

**- right, mean &gt; median \(right tail\)**

**- left mean &lt; median \(left tail\)**

**other shape descriptors**  


**Modality**

**- related to "mode" which is the most frequent value**

**- unimodal \(peaks\)**

**- bimodal**  


**outliers?**

**grouping**

**- qcut \(quantiles, size of population determines bin size, each same population\)**

**- cut \(bins, size of bin determines its population, probably going to be uniform across range\)**

**notation:**

**\[40, 50\) means including 40 to just before 50**  
  
  
  


**normal / gaussian**

**bell curve**  


**binomial?**

**bernoulli?**  


**exponential**

**laplacian - double exponential \(very sharp peak, mirrored exponentials\)**  


**Variability**

**Range**

**The difference between the largest and smallest measurements**

**Deviation** 

**The distance from a point to the mean**

**Variance**

**Average of the squares of the deviations**

**Measures spread, how distinct the points are from the mean**

**compute for samples with n-1 in the denominator, not n**

**Standard Deviation**

**The square root of the variance**

**compute for samples with n-1 in the denominator, not n**

**Tchebysheff's Theorem**

**practical applications of stddev**

**Given a number k greater than or equal to 1 and a set of n measurements, at least \[1-\(1/k^2\)\] of the measurements will lie within k standard deviations of their mean**

**like, k = 3, 3 times the stddev will capture at least 1 - 1/9 or 8/9 of measurements**

**Empirical Rule**

**Given an approximately normal distribution**

**The interval \(μ±\)contains ~68% of the measurements**

**The interval \(μ±2\)contains ~95% of the measurements**

**The interval \(μ±3\)contains ~99.7% of the measurements**

**Z-Score**

**The sample z-score is a measure of relative standing defined by**

**x-xhats**

**in terms of standard deviations away from the mean**

**Percentiles**

**A set of n measurements on the variable x has been arranged in order of magnitude. The pth percentile is the value of x that is greater than p% of the measurements and is less than the remaining \(100-p\)%**

**Quantiles, Quartiles, Deciles**

**Binning the measurements into divisions of the percentile. Quartiles means splitting it into 25%'s, deciles is 10%'s \(hence 4 and 10 groupings\)**

**Interquartile Range**

**The IQR for a set of measurements is the difference between the upper and lower quartiles; that is, IQR = Q3 -Q1**

**\(note it's specific to quartiles, 4 divisions\)**

**Box Plots & The Five Number Summary**

**These measures consist of the smallest number, the lower quartile, the median, the upper quartile, and the largest number. With these you can draw a box-plot.**

**The fences are created using the IQR to separate the outliers from the rest of the dataset, by using the 1.5IQR rule**

**Lower fence: Q1 - 1.5\(IQR\)**

**Upper fence; Q3 + 1.5\(IQR\)**

**The whiskers are connections of the remaining smallest and largest measurements to the box. \(exludes outliers\)**

**Dots remaining typically are considered outlier points.**

**Note the fences are the max range the whiskers can draw to, though the whiskers often don't have a point to connect exactly on the fences, hence they're shorter.**

**Notation**

**n number of measurements in the sample**

**s2 sample variance**

**s standard deviation**

**Confidence**

**Markov P\(xT\)E\[x\]T**

**Chebychev**

**Chernov**

#### **Probability**

**Bayes Theorem**

**P\(A\|B\)=P\(B\|A\)P\(A\)P\(B\)**

**Conditioning**

**P\(A,B\|e\)=P\(A,B,e\)P\(e\)=P\(A\|B,e\)P\(B\|e\)**

**P\(AB\)=P\(A\|B\)P\(B\)**

**Expectation**

**E\[XY\] != E\[X\]E\[Y\] for any two random variables X and Y**  


**Sample Space**

**The set of all possible outcomes of a random experiment**

**Event**

**Union Bound**

**Random Variable**

**Indicator Random Variable**

**Expectation**

**Linearity of Expectation**

**Variance**

**Linearity of Variance**

**Independence**

**Concentration Inequalities**

**Markov Inequality**

**Chebychev's Inequality**

**Chernof Bound**

#### **Experiments**

**Double blind studies**

**null hypothesis**

**statistical significance**

**a/b testing**  


**type 1 error**

**type 2 error**

**false positives / negatives**

#### **Signal Processing**

#### 
