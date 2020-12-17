---
title: "Visualization"
output: html_notebook
editor_options: 
  chunk_output_type: inline
---

### Visualization - Parellel Coordinates Plot

Since PCA visualization does not explain much in my case, as an alternative, I plot a parellel coordinates plot which shows how each clusters are posited within or consisted of each variables, or, in this case, questionnaires. The figure below shows how the nine clusters contain information of the questionnaires. There is clearly differences across variables in terms of variance across clusters. For instance, the first few variables that are binary (e.g. gender, urban/rural) have higher variance than questions asking if they are concerned about terrorism (T2, q1072) or religiosity (T1, q609).  

<img src="coord1.png">


The variable that I make a foundational reference is q605a, which is their response on political parties - secular vs. religious politial party. These are clusters of people who either responded they prefer Islamist political parties or secular political parties. 

Since question on the Muslim Brotherhood is not available for comparison in Wave 4, this is the closest comparable measurment I can get from the two datasets. The reason I pick 2 clusters instead of 1 is because I am only selecting clusters from one base variable, I might lose some explanatory power with just one cluster. Fortunately, if I choose two clusters for each 
 
We can see from both graphs that clusters 5 and 6 (T1) and 2 and 6 (T2) are groups of people who prefer Islamist groups - they are mostly from rural Egypt - while clusters 7 and 9 (T1) and 3 and 9 (T2) prefer secular groups, who are from the urban Egypt. It is also evident from T1 that clusters 5 and 6 are the ones who are most supportive of the Muslim Brotherhood (q20112), while their counterparts have the lowest rate of support and trust.  

<img src="coord2.png">
