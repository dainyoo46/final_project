---
title: "Data & Method"
output: html_notebook
editor_options: 
  chunk_output_type: inline
---


### Data & Methods

I use Arab Barometer survey data (2006-2019) to observe latent clusters within public opinion. Because Egypt adopted anti-terror in 2015, I use Wave 3 (2012-2014) and Wave 4 (2016-2017) to see how polarization exacerbated in Egypt after the enactment. 

Among various questionnaires, I included 20 of them for more variation across clusters. They include binary variables (e.g. urban/rural, male/female, voted/did not vote), categorical ordinal variable (e.g. not at all/once a month/once a week/daily, level of education) and continuous variable (e.g. age). Topics of the selected questionnaires include political participation, religious practices, media exposure and stances on economic and diplomatic issues.

* [Arab Barometer Survey Wave III](https://www.arabbarometer.org/surveys/arab-barometer-wave-iii/)
* [Arab Barometer Survey Wave IV](https://www.arabbarometer.org/surveys/arab-barometer-wave-iv/)

As for the method, I am using unsupervised machine learning and visualize the clusters through parellel coordinates plot. 



### Preprocessing
#### 1. Survey Weight

To preprocess the data before analyzing, I account for the weight of the survey to get an ideal representation of the population. As for the first dataset (2012-2014), the weights range from 0.047 to 6.07 while that of the second dataset (2016-2017) range from 0.67 to 1.90. To keep the number of observations similar, I multiply the weights by 10 and round to a whole number. Then I duplicate the each observation by the rounded weight. 

#### 2. Response Scaling

I normalize the responses to convert them uniformly into a numeric vector that ranges from 0 to 1. For binary variables, I recode them into 0 or 1 and, as for the continuous variable (age), I divide the values by 61 as the oldest respondent in each period is 61 and 58 respectively. I rescale them ordinal categorical variables, I use scaling method, by replacing each ordinal categorical variable with the equation below: $$\frac{i-1/2}{M}$$ 

I reiterate this for Wave 4 as well. One thing to note is that there are questions that appear in Wave 3 but not in Wave 4. One important question is q20112 which asks respondents how much trust they have for the Muslim Brotherhood, which is an ideal indicator to measure public opinion on the organization that is outlawed by the government and is often framed as terrorist organization by the government. In this analysis I include this question for Wave 3 due to its significance, but instead in Wave 4, I add question q1072 (which again does not appear in Wave 3) on how much individuals are worried about terrorism.

