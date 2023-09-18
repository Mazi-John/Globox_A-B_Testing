# Globox_A-B_Testing

**DESCRIPTION**

Analyzed A/B Tests to determine if the inclusion of a food &amp; drink banner on the Globox e-commerce website will increase revenue. Implemented statistical hypothesis testing using conversion rates and average amount spent per user as point estimates and provided actionable recommendations.

**SUMMARY**

This is an A/B Test experiment to determine the effect that the inclusion of a ‘food and drinks’ banner on the Globox website will have on revenue. Control and treatment groups were tested for 12 days. The final recommendation is to launch the banner because the experiment showed a statistically significant difference in the proportion of users that converted between the control and treatment groups. Furthermore, this recommendation also considers the fact that the change (setting up a banner on a website) carries minimum financial risk since the cost of designing a banner is a lightweight and does not outweigh the benefit of a possible increase in conversion rate and dollars spent by users on the website.

**CONTEXT**

GloBox is primarily known amongst its customer base for its boutique fashion items and high-end decor products. However, the company wants to beam awareness on its food and drink product category to increase revenue.
The Growth team has chosen to do an A/B test experiment that highlights key products in the food and drink category by setting up a banner at the top of the website. While the control group does not see the banner, the treatment group sees it as shown in the image below.

 

**METHODOLOGY**

The experiment is only being run on the mobile website.
A user visits the GloBox main page and is randomly assigned to either the control or test group. This is the join date for the user.
The page loads the banner if the user is assigned to the test group but does not load the banner if the user is assigned to the control group.
The user subsequently may or may not purchase products from the website. It could be on the same day they join the experiment, or days later. If they do make one or more purchases, this is considered a “conversion”.

 
**ANALYSIS RESULTS**
	
 	Number of users in the control group, A: 24,343
	Number of users in the treatment group, B: 24600
	Total number of distinct users in the experiment: 48943
	Total number users in the Control group, A who converted: 2094.
	Conversion rate for all users: (No. 4 / No. 3) x 100 = 4.28%
	Number of users in the control group who converted: 955.
	Number of users in the treatment group who converted: 1139.
	User conversion rate for control group A: (No.6/No.1) x 100 = 3.92%
	User conversion rate for treatment group B: (No.7/No.2) x 100 = 4.63%
	Average amount spent per user for control group A: $3.375
	Average amount spent per user for treatment group B: $3.391


**Hypothesis test to see whether there is a difference in the conversion rate between the two groups.**

H_0: P ̂_A= P ̂_B 
H_1: P ̂_A≠ P ̂_B

**Type of Test**: Two sample Z-Test with pooled proportion

P ̂_A=convertion rate of control group
P ̂_B=convertion rate of treatment group
P ̂=estimate of proportions
SE=standard error
				n_A=number of users in Control group,A
				n_B=number of users in Treatment group,B

P ̂=(P ̂_A n_A+P ̂_B n_B)/(n_A n_B )

				= 0.0392(24343) + 0.0463(24600)
						24343 + 24600
				P ̂= 0.0428


z^*=((p┴^_A-p┴^_B))/√(p┴^^* (1-p┴^^*)(1/n_1 +1/n_2 )) = (P ̂_A-P ̂_B)/SE

SE=√ 0.0428 (1-0.0428) (1/24343 + 1/24600)
   = 0.00183

Z = (0.0392-0.0463)/0.00183
  = -3.8798         Excel: Norm.s.dist (-3.6798)
  Therefore, P-value = 0.000052271
P-value = 0.0001
Significance level α=0.05
Hence, p-value of 0.0001 < α-value of 0.05

**Conclusion**: We reject the Null hypothesis that the conversion rate of the control group, A is equal to that of the treatment group, B. We have enough evidence to support the Alternative hypothesis which states that the difference in the conversion rates of the control and treatment group is statistically significant.



**95% Confidence interval for the difference in the conversion rate between the treatment and control groups**

Confidence interval = Sample statistic ± Margin of Error
		= Sample Statistic ± Critical Value X  Standard Error 


Sample Statistic, P ̂= P┴^_A-P┴^_B
		= 0.0392-0.0463
		=-0.0071

Critical Value, z_(α∕2)
= 0.05/2
=z_0.025
=-1.96
Standard Error Unpooled = 0.00183

Confidence interval= -0.0071± -1.96 X 0.00183
				= -0.0071 ± -0.0036
Confidence Interval: 0.0035<p<0.0107

**Conclusion**: We are 95% sure that the true conversion rate in the combined population of the control and treatment groups is likely to fall within 0.0035 and $0.0107.


**Hypothesis test to see whether there is a difference in the average amount spent per user between the two groups**.


H_0: x ̅_A=x ̅_B  				x ̅_A=3.375            SE= √((s_1^2)/n_1 +(s_2^2)/n_2 )
H_1: x ̅_A≠x ̅_B				x ̅_B=3.391              
S1=sample standard deviation Control group, A=25.93639
S2=sample standard deviation Treatment group, B=25.41411
N1=sample size of control group, A=24343
N2=sample size of Treatment group, B=24600

**Type of test**: Two Sample T test

 t^*=(¯x_1-¯(x_2 )-0)/√((s_1^2)/n_1 +(s_2^2)/n_2 )

.x ̅_A-x ̅_B=-0.016
SE = 0.2321

Therefore, t = -0.016/0.2321
	       = -0.0689      Excel
P(|t| ≥ 0.0689)
= 0.0527465
= 1- 0.0527465
=0.472535 X 2
=0.94507

P-value = 0.94507 while α=0.05 at 95% confidence level
0.94507 > 0.05

**Conclusion**: the p-value of 0.945 is not statistically significant, therefore we fail to reject the Null Hypothesis that there is no difference in the mean amount spent per user between the control and treatment groups. We, therefore, do not have enough evidence to support the Alternative hypothesis that the mean amount spent per user between the control and treatment groups are different.


**95% confidence interval for the difference in the average amount spent per user between the treatment and control groups**.

Confidence Interval = Test Statistic ± critical value X standard error
		      = -0.016 ± -1.96 X 0.232
		     = -0.016 ± -0.455
		    = 0.439 < µ < -0.471

**Conclusion**: We are 95% sure that the true average amount spent in the combined population of the control and treatment groups is likely to fall within $-0.439 and $0.471.


**RECOMMENDATION**

I recommend launching the banner based on two premises:
	A significant positive difference was observed in the conversion rates between the control and treatment groups. In like manner, there was a positive difference, albeit marginal, in the average amount spent per user between the control and treatment groups.
	Furthermore, hoisting a digital banner on the website constitutes a lightweight expenditure that carries minimal financial risk even if the positive results derived from the experiment are not prolonged. In other words, this risk will have no jeopardizing effect on the business.
