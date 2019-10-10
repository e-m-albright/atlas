# Distributions

### Measures of Center

#### Mean

s

#### Median

s

#### Mode

s

### Law of Large Numbers

### Central Limit Theorem

s

### Binomial Experiments

each trial is a success or failure, p = P\(S\), q = P\(F\), p+q = 1

for something to be binomial, need to sample fewer or eq to 0.05% of population?  
Binomial = sum o fbernoulli random variables  
P\(X=x\) = nChoosex \* p^x \* q^n-x  
nChoosex = n! / x!\(n-x\)!  
E\[x\]=np  
Var\[x\]=npq  
X~binomial\(n=10, p=1/4\)  
P\(X=6\)=P\(X leq 6\) - P\(X leq 5\)  


Toothpaste given to 20 kids, at the end 1 has cavity, population rate is 0.1. does the toothpaste half cavities?

n=20, each trial focuses on child has cavities \(S\) doesn't have cavities \(F\), p=P\(S\) = 0.1, constant, q=P\(F\)=1-0.1=0.9, constant under the assumption the new toothpaste is not effective  
independence?, n=20 - sample is very small,  
X - \# of cavitiies, X~Binom\(n=20, p=0.1\)  
E\[X\] = n\*p = 20x0.1 = 2

Observed value of x=1, p-value &gt; if we assume the toothpaste is not effective, what is the propability of ovserving a sample like this one or a more extreme?  
P\(X leq 1\) = 0.392 \(from a p table for n=20\)   
Look for a small p-value, reject the claim \(null hypothesis\) p-value &lt; 0.05 usually.  
We don't have that here, so you can't claim the toothpaste changes the rate of cavities   
And we should take bigger samples.





