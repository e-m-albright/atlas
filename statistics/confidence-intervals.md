# Confidence Intervals

point estimate +/- constant variability  
constant - based on how confident  
variability - SD\(Xbar\) = sigma / sqrt\(n\) but we don't know SD in real world scenarios, so we use  
SE\(Xbar\) = s \(numerical approximation\) / sqrt\(n\)  
  
100\(1-alpha\)% C.I. for mu  
Xbar +/- Z\(alpha/2\) \* sigma/sqrt\(n\)  
for 95% Z\(alpha/2\) = +/- 1.96  
which means on a z-table look up 0.05 / 2 \(0.025\) and get z score, which means on upper and lower side  
AUC in bounds is equal to C.I., so between 1.96 z's we have an area of .95

  
parameter mu  
estimator the best unbiased E\(Xbar\) = mu  
point estimate: Xbar  
  
confidence intervals are the point estimate with bounds on either size, base on confidence desired on a normal distribution \(sampling distribution tends towards normal\)

CI's represent the probability that the true population mean is included in the confidence interval of all possible point estimate confidence intervals  
If I take all possible samples of size n, with confidence intervals, about 95% of them will include the true population mean  
In examining one point estimate, it's either a yes or a no, in an unknown manner whether or not it's included.

example: 50 inidivuals surveyed, CSP  
talking about age  
mean is 35.66, median is 33.00, stdev is 17.84, SE Mean is 2.52  
95% CI for mu  
35.66 +/- 1.96 \* 2.52  
35.66 +/- 4.94  
\(lower = 30.72, upper = 40.60\)  
\(30.72, 40.60\)  
interpretation: I am 95% confident the true population mean is between these two values.  
interpretation of confidence level: if you take all possible samples of size n, and create all possible confidence intervals, 95% will include the true population mean  
what I can say about this particular bounds = shrug, don't know if it's right or not.  
  
  
n=70  
avg = $420  
stdev = $110  
what is 99% CI?

Phat for aprx normal\(muphat = p, sigmaphat = sqrt\(p\*q/n\), SE\(phat\)=sqrt\(phat\*qhat/n\)\)  
phat +/- Zalpha/2\*sqrt\(phat\*qhat/n\)  
  
for a survey  
phat=0.19, n=1823  
0.19 +/- 1.96\*sqrt\(0.19\*\(1-0.19\)/1823\)  
confidence interval  


want to get a 99% confidence interval for mean number of whatever \(hours adults do community service\) such that the estimate is within 1.2hours of population mean? assume standard deviation is 3 hours.  
  
n = \(Zalpha/2 ^ 2 \* sigma ^ 2\) / B ^ 2  
where B is the maximum margin of error  
= \(Zalpha/2 \* sigma / B \) ^ 2  
= \(2.57 \* 3 / 1.2\) ^ 2  
= 41.6 so n is greater than or equal to 42 \(round, can't sample .6\)  
  
in reality use "the T distribution" and/or run a pilot study to get an estimate of the stdev so you don't have to guess it/assume it

Same for proportions?  
Zalpha/2 = take a pilot sample estimate phat, research, OR be conservative, and make sure your sample size is large?  
phat \* qhat - assume max value  
max value is 0.25 for phat = 0.5 which means your sample size will be big \(you're computing size of sample with the worse case scenario\)  
  
n =   
  




