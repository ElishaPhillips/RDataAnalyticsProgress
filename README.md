# R Data Analytics 
### DATA115 at WSU 

##### A small journal of the learning progress throughout the semester.

<details>
  <summary>1. Visual Analysis</summary>
  
  ### Analysis of Disney Movie Ratings
  ##### From: MovieRating_disneyMovies.csv
  
  
  <details>
    <summary>2. Graphs</summary>
  
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/54d1843c76448c46112788c1f9bf88813e002b30/Images/1/jitter.1.1.png)
  
  
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/54d1843c76448c46112788c1f9bf88813e002b30/Images/1/scatter.1.1.png)
  </details>
  
  #### Analysis:
  
  ##### I noticed the rating of Disney movies is higher, on average, for females when compared to male reviewers. 
  ##### Potential explanations: One potential explanation is the target market for Disney films trend towards a female demographic. Another point to note is    a study done by the Center for the Study of Women in Television and Film, which found that "female critics tend to give higher ratings to films with women    in leading roles than male critics do."
   *[Source](https://www.nytimes.com/2018/07/17/movies/male-critics-are-harsher-than-women-on-female-led-films-study-says.html)* 
   
   ##### A better analysis could comprise of a larger selection of reviewers. In addition the selection of movies could be higher, to show a more conclusive      trend.
  
</details>

<details>
  <summary>2. EDA</summary>
  
  ### Cost of Living Outlier Analysis
  ##### From COL.csv
  <details>
    <summary> Boxplots</summary>
  
  ##### Boxplots:
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/4e914caf4a85a5b0c1b2b7789bdd8b1c8501fe35/Images/2/2.plotadi.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/4e914caf4a85a5b0c1b2b7789bdd8b1c8501fe35/Images/2/2.plotcap.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/4e914caf4a85a5b0c1b2b7789bdd8b1c8501fe35/Images/2/2.plotcin.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/4e914caf4a85a5b0c1b2b7789bdd8b1c8501fe35/Images/2/2.plotgas.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/4e914caf4a85a5b0c1b2b7789bdd8b1c8501fe35/Images/2/2.plotrent.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/4e914caf4a85a5b0c1b2b7789bdd8b1c8501fe35/Images/2/2.plotwine.png)
  

      
   </details> 
   
   ##### Based on the boxplots above, I selected the Cappuccino, Cinema, Wine, and Avg.Rent to investigate further. 
   ##### Running the columns through a Rosner test:
   # 
 
 ##### $all.stats
 <details>
  <summary> Rosner Test</summary>
 
 > ###### $data.name
 > ###### [1] "COL$Cappuccino"
 > ######   i   Mean.i      SD.i Value Obs.Num    R.i+1 lambda.i+1 Outlier
 > ###### 1 0 1.981481 0.7371312  4.48      10 3.389517   3.628495   FALSE
   #   
   
 > ###### $data.name  
 > ###### [1] "COL$Cinema"  
 > ######   i   Mean.i     SD.i Value Obs.Num     R.i+1 lambda.i+1 Outlier
 > ###### 1 0 6.775602 5.632751 79.49     115 12.909216   3.628495    TRUE
 > ###### 2 1 6.437395 2.655904 14.95     104  3.205163   3.627118   FALSE
   #   
   
 > ###### $data.name  
 > ###### [1] "COL$Wine"  
 > ######   i   Mean.i     SD.i Value Obs.Num    R.i+1 lambda.i+1 Outlier
 > ###### 1 0 7.079722 3.325691 26.15     174 5.734230   3.628495    TRUE
 > ###### 2 1 6.991023 3.066689 19.61     127 4.114854   3.627118    TRUE
 > ##### 3 2 6.932056 2.949177 17.43     115 3.559619   3.625734   FALSE
 > ###### 4 3 6.882770 2.866424 16.83     187 3.470258   3.624342   FALSE
   #  
   
 > ###### $data.name
 > ###### [1] "COL$Avg.Rent"
 > ######   i   Mean.i     SD.i   Value Obs.Num    R.i+1 lambda.i+1 Outlier
 > ###### 1 0 1092.979 664.7785 5052.31      37 5.955865   3.628495    TRUE
 > ###### 2 1 1074.564 608.6058 3268.84      22 3.605414   3.627118   FALSE
 > ###### 3 2 1064.310 591.1256 3164.42     106 3.552730   3.625734   FALSE
 > ###### 4 3 1054.450 574.6094 2788.71      16 3.018154   3.624342   FALSE
 > ###### 5 4 1046.270 563.3998 2607.95       3 2.771886   3.622942   FALSE 
 > ###### 6 5 1038.869 554.3124 2590.76      63 2.799669   3.621535   FALSE  
   #   
  </details> 
  
  
   ###### Identified Outliers:
   #  
   
   > ###### Cinema:
   > ###### Row 115, Riyadh -$79.49
   #
   
   > ###### Wine:
   > ###### Row 127, Manama - $19.61
   > ###### Row 174, Tehran - $26.15
   #   
   
   > ###### Avg.Rent:
   > ###### Row 37, Hong Kong - $5,052
   #  
   
   ###### In this specific case I would either exclude the rows from the dataset, or find an alternative dataset to crossreference. One could also            estimate the appropriate value instead, such as using a simple mean or a more complicated algorithm. 
   #   
   
  ### Height Weight Age Sex Analysis
  ##### From Height_Weight_Age_Sex.csv
  
  ##### Boxplots of the Height and Weight distribution:
  
   <details>
    <summary> Boxplots for height and Weight Columns</summary>
  
   ##### Boxplots:
   
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/4e914caf4a85a5b0c1b2b7789bdd8b1c8501fe35/Images/2/2.boxplot.1.png)  
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/4e914caf4a85a5b0c1b2b7789bdd8b1c8501fe35/Images/2/2.boxplot.2.png)
  
   </details>
   
  #### Analysis:

  ###### For the Height boxplot, the count distribution is asymetrical, with the majority of the data lying in the ~130 to 170 range. There lies some       notable outliers in the 50 through 75 range. The median is around 75% towards the top of the box, featuring a negative skew.
  
  ##### For the Weight boxplot, the count distribution is also asymmetrical, with no outliers shown.The box plot is skewed negatively.

   <details>
    <summary> Histograms</summary>
  
  ##### Histograms:  
  
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/4e914caf4a85a5b0c1b2b7789bdd8b1c8501fe35/Images/2/2.hist.1.png)  
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/4e914caf4a85a5b0c1b2b7789bdd8b1c8501fe35/Images/2/2.hist.2.png)
  
   </details>
   
  ##### Analysis:

  ##### For the Height histogram, the count distribution is asymetrical, with a fairly symmetrical hill from ~130-170, and a dip in count at about 155. This is where the majority of the data lies. We do see a definitive negative skewness. From 50 through 125, there is a much smaller amount of values and a small outlier at the 179 mark. I was not expecting to see the amount of values in the 75-125 range, as compared to the boxplot. The symmetry and skewness analysis did remain consistent.

  ##### For the Weight histogram, the count distribution is asymmetrical and has 2 peaks, one from 0-30 and another from 30-60. There are 3 notable outliers: at 7, and 11-12, and at 47. The graph is skewed negatively here as well.I ws not expecting to see the first hill, in the 0-30 range as compared to the boxplot, nor the outliers. The skewness analysis remained consistent. 

  ###### Separate boxplots for the weight data separated by the Male variable:
  
  <details>
    <summary> Boxplots Weight By Gender</summary>
  
  ##### Boxplots Weight by Gender:
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/4e914caf4a85a5b0c1b2b7789bdd8b1c8501fe35/Images/2/2.boxplot.3.png)  
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/4e914caf4a85a5b0c1b2b7789bdd8b1c8501fe35/Images/2/2.boxplot.4.png)
  
  </details>
  
   ##### Analysis: I noticed that the negative skew remains similar for both male and female weights, though the female weight remains lower on average      and has less of a distribution.

   ##### Adding a BMI column and an underweight column:
  
  <details>
    <summary> Histograms For BMI By Gender</summary>

  ##### Histograms for BMI by Gender:  
  
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/4e914caf4a85a5b0c1b2b7789bdd8b1c8501fe35/Images/2/2.hist.3.png)
  
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/4e914caf4a85a5b0c1b2b7789bdd8b1c8501fe35/Images/2/2.hist.4.png)
  
  </details>
  
  ##### Analysis: I noticed that the male BMI is more symmetrically skewed than the female BMI chart, though both are negatively skewed.The male histogram   also highlights two small outliers to the right.The male BMI also peaks at 1 lower than the female chart.


  ###### Scatterplot of height vs. weight for the full dataset that distinguishes both by gender and whether or not the individual is underweight
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/4e914caf4a85a5b0c1b2b7789bdd8b1c8501fe35/Images/2/2.scatter.png)
  
</details>

<details>
  <summary>3. Examining Correlations</summary>
  
  ## Heading
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/3da61bbe1cc56c08ec024cb1572dc80298c125ee/Images/3/3.corr.1.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/3da61bbe1cc56c08ec024cb1572dc80298c125ee/Images/3/3.corr.2.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/3da61bbe1cc56c08ec024cb1572dc80298c125ee/Images/3/3.plot.1.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/3da61bbe1cc56c08ec024cb1572dc80298c125ee/Images/3/3pairs.1.png)
</details>

<details>
  <summary>4. Examining Distributions</summary>
  
  ## Heading
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/d5e7feeb9448af5cf93e54c7726d8f4eab7eb9f9/Images/4/4hist1.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/d5e7feeb9448af5cf93e54c7726d8f4eab7eb9f9/Images/4/4hist2.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/d5e7feeb9448af5cf93e54c7726d8f4eab7eb9f9/Images/4/4hist3.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/d5e7feeb9448af5cf93e54c7726d8f4eab7eb9f9/Images/4/4qq1.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/d5e7feeb9448af5cf93e54c7726d8f4eab7eb9f9/Images/4/4qq2.png)
</details>

<details>
  <summary>5. Linear Regression</summary>
  
  ## Heading
  1. A numbered
  2. 5
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/327bdedce27bb3967059427cf80b4350c4d937d1/Images/5/5.plot.1.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/327bdedce27bb3967059427cf80b4350c4d937d1/Images/5/5.plot.2.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/327bdedce27bb3967059427cf80b4350c4d937d1/Images/5/5.plot.3.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/327bdedce27bb3967059427cf80b4350c4d937d1/Images/5/5.plot.4.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/fef57b9c070cb9b868862c9cee9be4f3bc47507c/Images/5/5.resid.1.png)
</details>

<details>
  <summary>6. Multivariate and Logistic Algorithms</summary>
  
  ## Heading
  1. A numbered
  6
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/7b0d5dfffc5201eac9559ba46a8f2d0aabe8900a/Images/6/6.pairs.1.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/61398539aa86ba724e9cb12abbbe7757235bbcf7/Images/6/6.plot.1.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/fef57b9c070cb9b868862c9cee9be4f3bc47507c/Images/6/6.plot.2.png)
</details>

<details>
  <summary>7. PCA and K-Clustering</summary>
  
  ## Heading
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/8d8855ba3db627c767d221213b7c577b6582c549/Images/7/7.pairs.1.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/8d8855ba3db627c767d221213b7c577b6582c549/Images/7/7.plot.1.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/8d8855ba3db627c767d221213b7c577b6582c549/Images/7/7.plot.2.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/8d8855ba3db627c767d221213b7c577b6582c549/Images/7/7.plot.3.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/8d8855ba3db627c767d221213b7c577b6582c549/Images/7/7.plot.4.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/8d8855ba3db627c767d221213b7c577b6582c549/Images/7/7.plot.5.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/8d8855ba3db627c767d221213b7c577b6582c549/Images/7/7.plot.6.png)
</details>
