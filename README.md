# MeanVarEstimate
Estimate means or SD or variance from limited information (e.g. mimimum/median/maximum).

Estimators for mean are hozo4, hozo5, median, wan1, wan2, wan3 and bland.

Estimators for variance are hozo12, hozo15, range4, range6, wan1, wan2, wan3, bland, hozoc, cochran.

Different estimators require different inputs. 
For mean, these are :

Method	minimum	25th	median	75th	Maximum	N	Preference	Preference
Hozo4	X				X			
Hozo5	X				X			
Wan1	X				X	X	X	
								
Median			X					
								
Wan2	X		X		X			
Wan3		X	X	X		X		
								
Bland	X	X	X	X	X			


Usage:

mean_fnc(min, max, med, q1, q3, n, type = "hozo4")

var_fnc(min, max, med, q1, q3, n, type = "hozoc")


If a mean variable is already present, this can be entered as an additional argument and the missings will be filled.

mean_fnc(min, max, med, q1, q3, n, type = "hozo4", mean)



References:

Wan X, Wang W, Liu J, Tong T (2014) Estimating sample mean and standard deviation from the sample size, median, range and/or interquartile range. BMC Medical Research Methodology 14:135

Hozo SP, Djulbegovic B, Hozo, I (2005) Estimating the mean and variance from the median, range, and the size of a sample. BMC Medical Research Methodology 5:13
