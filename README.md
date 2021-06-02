# Data Analytics in R Studio
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
   
   ##### A better analysis could comprise of a larger selection of reviewers. In addition the selection of movies could be higher, to show a more conclusive trend.
  
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
   
   > ####### Cinema:
   > ####### Row 115, Riyadh -$79.49
   #
   
   > ####### Wine:
   > ####### Row 127, Manama - $19.61
   > ####### Row 174, Tehran - $26.15
   #   
   
   > ####### Avg.Rent:
   > ####### Row 37, Hong Kong - $5,052
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
  
  ###### Analysis: I noticed for the underweight category, male and female remain a consistent grouping, with an even distribution across the x (height) axis from 50 to 200. As we look at non-underweight variables, the grouping is centered from 130 to 200 with one outlier at around 60 on the x axis. In addition, there is a clear trend towards the males in the dataset being both taller and heavier than the female set. The non-underweight grouping also remains positioned above the underweight grouping, as one would expect to see.
  
</details>

<details>
  <summary>3. Examining Correlations</summary>
  
  ### 2020 Basketball Rankings Correlation Analysis
  ##### From 2020bb_values.csv
  
  ##### Correlation between all columns: 
  
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/3da61bbe1cc56c08ec024cb1572dc80298c125ee/Images/3/3.corr.1.png)
  
  ##### The Rank column and the AdjEM column are most strongly correlated at -0.98. The Luck column is least correlated across the board.

  ##### Narrowing to teams in PAC12 
  
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/3da61bbe1cc56c08ec024cb1572dc80298c125ee/Images/3/3.corr.2.png)
  
  ##### Again, the Rank and AdjEM columns are most strongly correlated - though this time with an even stronger correlation of -0.99. AdjEM seems to have   the highest correlation across all columns. SoS_OppO is least strongly correlated across the columns. This time, luck surprisingly seems to have a          stronger correlation to other columns. Also the correlation between rank and the other columns is significantly lower on average.
  
  ### Cost of Living Correlation Analysis
  ##### From COL2.csv
  
  ##### Correlation between all columns: 
  
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/3da61bbe1cc56c08ec024cb1572dc80298c125ee/Images/3/3pairs.1.png)
  
  ##### Income seems to be one of the strongest correlating values to the other variables, except in the case of wine and gasoline.Both wine and gasoline   indicate not much of a significantly measurable relationship between the other variables. The strong relationship between cinema and cappuccino seems     like an interesting relationship to note. 
  
  ##### Investigating further with a scatterplot between Cappuccino and Cinema Columns, colored by Income:
  
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/3da61bbe1cc56c08ec024cb1572dc80298c125ee/Images/3/3.plot.1.png)
  
  ##### The relationship seems to hold true - people who spend less on drinks per month are less likely to spend money on going to movies. It should also   be noted, income plays a consistent factor, those who make more are observed to spend more on purchases like these - though the relationship is more       scattered at higher income. 
  
</details>

<details>
  <summary>4. Examining Distributions</summary>
  
  ### Examining distributions in seeded rnorm sequences
  
  > ##### **set.seed(2021)**
  > ##### **nmatrix <- matrix(rnorm(10, 25, 3), ncol=10, nrow=50)**
  
  ##### Distribution:
  
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/d5e7feeb9448af5cf93e54c7726d8f4eab7eb9f9/Images/4/4hist1.png)
  
  ##### Normality:
  
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/d5e7feeb9448af5cf93e54c7726d8f4eab7eb9f9/Images/4/4qq1.png)
  
  ##### Analysis: The points form a linear trend in the center as expected, however the extremities do not follow the same behavior and are distinctly        grouped away. This would suggest the sample set does not follow a normal distribution.
  
  ### Same seed with a much larger sample set, n=1000
  
 > ##### **set.seed(2021)**
 > ##### **nmatrix2 <- matrix(rnorm(1000, 25, 3), ncol=10, nrow=50))**
  
  ##### Distribution:
  
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/d5e7feeb9448af5cf93e54c7726d8f4eab7eb9f9/Images/4/4hist2.png)
  
  ##### Normality:
  
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/d5e7feeb9448af5cf93e54c7726d8f4eab7eb9f9/Images/4/4qq2.png)
  
  ##### Analysis: Both tails veer away from the distribution line, though there is more continuity with a higher sample set than in the previous plot. I     would conclude that there is still a higher number of extremities than one would find in a normal distribution set.
  
  ### Examining distributions in Pullman, WA Air Quality Data in 2020
  ##### From .csv
  
  ##### > Mean: 3.5262
  ##### > Standard Deviation 2.424
  
  ##### Histogram of the PM_Concentration column with am overlay a plot of the normal distribution with mean and standard deviation 
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/d5e7feeb9448af5cf93e54c7726d8f4eab7eb9f9/Images/4/4hist3.png)
  
  ##### Whats interesting to note is the PM Concentration tails to the right past PM6. On further analysis this is most likely due to the significant        wildfire season in 2020, this notion is further evidenced by the dates of the extreme values occurring beyond July.

</details>
  
<details>
  <summary>5. Linear Regression</summary>
  
   ### Linear Regression algorithm to fit Median Household Income with Percentage of BS Holders
   ##### From educationincome.csv
   
   ##### Initial scatterplot:
   ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/327bdedce27bb3967059427cf80b4350c4d937d1/Images/5/5.plot.1.png) 
   
   ##### There appears to be a clear linear trend in the two variable's relationship
   
   ##### Fittting a simple linear model: BS.Perc~Median.HH.Income
   
   ##### Scatterplot:
   
   ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/327bdedce27bb3967059427cf80b4350c4d937d1/Images/5/5.plot.2.png)
  
   ##### The coefficient of determination is: 0.66258
   
   ##### QQ plot of the residuals:
   
   ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/d36d073f3b48af369e85fd1cbe9f7b42244138c6/Images/5/5resid1.png)
   
   ##### Lightly tailed distribution
   
   ##### Residuals vs. Fitted 
   
   ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/6de48303bc64d547ba8d6d3686a46809f7f36dd7/Images/5/5.residfit.1.png)
   
   ##### Analysis: There is a notable bend in the fit on the left side through 27, I would mark that as possibly problematic. The graph marks 3 possible outliers as well. Also, the spread of the residuals is increasing as the graph moves towards the right.

  ## Picking another set: BS Rank vs ADV Percentage
  
  ##### Initial Scatterplot:
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/327bdedce27bb3967059427cf80b4350c4d937d1/Images/5/5.plot.3.png)
  
  
  ##### Fittting a simple linear model: BS.Perc~Median.HH.Income
  ##### Scatterplot:
  
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/327bdedce27bb3967059427cf80b4350c4d937d1/Images/5/5.plot.4.png)
  
  ##### There appears to be a strong negative correlation in the two variables' relationship.
  
  ##### The coefficient of determination is: 0.75593
  
  ##### QQ plot of the residuals:
  
  ![a](https://github.com/ElishaPhillips/R_Data_Analytics_Progress/blob/adfba694ee6c87225732ca44c14d014de263cd5a/Images/5/5resid2.png)
   
  ##### Residuals vs. Fitted 
   
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/6de48303bc64d547ba8d6d3686a46809f7f36dd7/Images/5/5.residfit.2.png)
   
  ##### The tails on this qqplot are much more heavily skewed beyond 1, and the residuals vs fitted plot doesn’t seem to hold as close to the centerline.       There does seems to be a quadratic relationship. Also, the heteroskedacity holds closer and remains more consistent from left to right.
 
</details>

<details>
  <summary>6. Multivariate and Logistic Algorithms</summary>
  
  ### Advertisement Investment Sales Metrics Multivariate Linear Analysis
  ##### From advertisment.csv
  
  ##### Correlation Matrix between all columns: 
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/7b0d5dfffc5201eac9559ba46a8f2d0aabe8900a/Images/6/6.pairs.1.png)
  
  ##### Analysis: Based on this plot, it seems that multiple linear regression would be appropriate to attempt due to the correlation between the media types   and the sales. The TV advertisements seem to hold the strongest correlation, while the radio and newspaper come in second and third. 
  
  ##### Fitting a multiple linear regression model using all three media columns as predictors with the sales column as the dependent variable 
  ##### lm(sales ~ TV + radio + newspaper, advertising)
  
  ##### Residuals:
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/61398539aa86ba724e9cb12abbbe7757235bbcf7/Images/6/6.plot.1.png)

  ##### Coefficient of determination for the fit: r^2 = 0.8972
  
  ### ISLR Student Default Logistic Regression Analysis
  ##### From default_ISLR.csv

  ##### Fitted model:
   $$
    \ln\left(\frac{P}{1-P}\right) = -10.65 + 549.9x_i
   $$
  
  ##### Plotting accuracy: 97.25%
  
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/fef57b9c070cb9b868862c9cee9be4f3bc47507c/Images/6/6.plot.2.png)
  
</details>

<details>
  <summary>7. PCA and K-Clustering</summary>
  
  ##### Iris Set PCA and K-Means Clustering
  ###### Initial Scatterplot of petal width vs. petal length colored by the subspecies:
  
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/8d8855ba3db627c767d221213b7c577b6582c549/Images/7/7.plot.1.png)
  
  ##### Variance explained with the four numerical columns as inputs:
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/c15bce1fee8fdef856fd5021bf43a94f8e3a7f24/Images/7/7.hist.1.png)

  ##### Importance of components:
 > #####                           PC1    PC2     PC3     PC4
 > ##### Standard deviation     1.7061 0.9598 0.38387 0.14355
 > ##### Proportion of Variance 0.7277 0.2303 0.03684 0.00515
 > ##### Cumulative Proportion  0.7277 0.9580 0.99485 1.00000
 
 ##### 95% of the variance is explained by the first 2 principal components
 
 ##### Scatterplot matrix:
 ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/8d8855ba3db627c767d221213b7c577b6582c549/Images/7/7.pairs.1.png)
 
 ##### Scatter plot of the 2 selected principal components colored by subspecies
 ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/8d8855ba3db627c767d221213b7c577b6582c549/Images/7/7.plot.2.png)
 
 ##### Original Loading
> #####                     PC1         PC2        PC3        PC4
> ##### sepal_length  0.5223716 -0.37231836  0.7210168  0.2619956
> ##### sepal_width  -0.2633549 -0.92555649 -0.2420329 -0.1241348
> ##### petal_length  0.5812540 -0.02109478 -0.1408923 -0.8011543
> ##### petal_width   0.5656110 -0.06541577 -0.6338014  0.5235463
 
  ##### Applying K means clustering to the dataset using all 4 PC's as a benchmark 
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/8d8855ba3db627c767d221213b7c577b6582c549/Images/7/7.plot.3.png)

  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/8d8855ba3db627c767d221213b7c577b6582c549/Images/7/7.plot.4.png)
 
  ##### Applying K means clustering to the dataset using the 2 selected PC's
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/8d8855ba3db627c767d221213b7c577b6582c549/Images/7/7.plot.5.png)
  ![a](https://github.com/ElishaPhillips/RDataAnalyticsProgress/blob/8d8855ba3db627c767d221213b7c577b6582c549/Images/7/7.plot.6.png)
  
  ##### Total Withins Sum of Squares:
 
  > ##### Original K-Means Clustering: 78.94
  > ##### With 2 Principal Components: 171.32
  
</details>
