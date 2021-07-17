# Case_Study3
WPI DS 501 Case study 3 

Open zip file and upload to Rstudio


----Read Me----
About the project 

For this project I wanted to look at the trends between the rating of a wine and the year it was produced.  Older wines are typically more expensive but are they arguable better.  Data was collected from https://www.kaggle.com/budnyak/wine-rating-and-price . The data set included fields for the: wine name, country, wine region, year, price, and rating. From here I used a K-Means filter to look for clusters in the data to see if which wine years produced high quality wines.   The k-means algorithm grouped the wines into clusters. These clusters were further analyzed to calculate the best year for a given country. 

---About the GUI--- 

On the left of the screen are the controls for the application and the right has the results of the anay
 
Vintage (Year): Allows the user to select which years to consider in the analysis
 
Price: Allows the user to select which price range to consider in the analysis 

Number of Ratings: Allows the user to select how many reviews a wine needs to have in order to be considered in the analysis.

Wine Type:  Drop down list of wines that can be included in the analysis. A red wine is the largest data set.  Any wine added to the list is included in the analysis.  At least one wine type needs to be included in the list otherwise the application throws an error. 

Number of Centers: This controls the K-Mean analysis and allows the user to select how many different centers to choose from the data.  To assist the user the SSE number cluster graph is included in one of the tabs on the right hand side. 

Plot: shows the output of the k-means clustering algorithm. 

SSE Num Clusters: Creates a plot that assists with determining how many clusters should be included in the k-means analysis. This graph can be used to determine the input to the number of centers field. 

Table: Shows the raw data that is being considered in the analysis. 

Cluster info: shows the output of the k-means cluster and assigns a cluster number to each data point. 

Best year: Is the end result of the analysis and answers the question for which country what was the best year given the cluster.    This analysis is done by taking an average of the clusters for a given country and displays the cluster with the best average rating. 

--K-Means clustering--- 
I selected the k-means algorithm for this project because I wanted to look at the relationship between year and rating for wine. By clustering the wine into the different groups you can see what wine region and year produced the similar wines.  The inputs to the k-means analysis was the year and rating of a wine.  The k-means clustering groups the wines that are similar by looking at how far they are away from centroids. The centroids are centers of data which the k-means clustering uses to calculate which cluster each group belongs to. These centroid locations are calculated by looking for where the centroid can be placed in the closest to all data points. For example if you only have one centroid it would be placed in the middle of the data. However if you have multiple centroids than the k-means algorithm can be placed near the clusters of data in the scatter plot.  
The user must select the number of centroids to include in the analysis. This decision impacts the results of the analysis. To help determine the number of centroids an elbow analysis can be used to select the optimum number of centroids.  The elbow analysis runs the k-means analysis for a range of centroids than computes the average distance the data is from the centroids. This is than graphed and you get a graph that looks like an elbow. If you use only one centroid than the distance between the centroids and the data would be quite large but as you add centroids this decrease, hence the look of the elbow. 

--Questions--- 
-What data you collected?
For this project I wanted to look at the trends between the rating of a wine and the year it was produced.  Older wines are typically more expensive but are they arguable better.  Data was collected from https://www.kaggle.com/budnyak/wine-rating-and-price .
 
-Why this topic is interesting or important to you? (Motivation)
Who does not love drinking wine because every bottle is a new experience?  However picking which experience you are looking for is difficult.  I chose this project to see if machine learning could be used to narrow down years of wine that has good ratings. 

-How did you analyze the data?
I analyzed the data using a k-means analysis. Then broke the k-means into a series of tables that further refined the data. 

-What did you find in the data? (please include figures or tables in the report)
I found that 2017 was the best year for a reasonably priced bottle of red wine from the California wine region.  To get this conclusion I had to run the analysis again with just United States wine. This was not included in the application because I wanted to allow people to look at all the wine regions. 

 

