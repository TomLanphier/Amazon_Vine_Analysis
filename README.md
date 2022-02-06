# Amazon Vine Analysis
## Overview
In this analysis I examined Amazon reviews of video games, and compared the reviews by members of the paid Amazon Vine program and by non-members. The dataset I used is stored on Amazon S3. Using PySpark I performed the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. I further used PySpark to filter the review dataset to compare the effect of Amazon Vine on the review score.

## Results
The outputs from the PySpark code are shown in Figure 1 and 2 for the Amazon Vine reviews and the non-Amazon Vine reviews respectively.

![VineReviews.PNG](VineReviews.PNG)

Figure 1. Amazon Vine reviews first 20 lines of data, number of 5-star reviews, total number of reviews, and percentage of total that are 5-star reviews.

![NonVineReviews.PNG](NonVineReviews.PNG)

Figure 2. Non=Amazon Vine reviews first 20 lines of data, number of 5-star reviews, total number of reviews, and percentage of total that are 5-star reviews.

- 5-star reviews: 48 Amazon Vine, 15,663 non-Amazon Vine
- Total reviews: 94 Amazon Vine, 40,471 non-Amazon Vine
- Percentage of total reviews 5-star: 51% Amazon Vine, 39% non-Amazon Vine

## Summary
There appears to be a bias for Amazon Vine reviews to be 5-star. This observation is based on the 12% difference of 5-star reviews from the video game reviews data set. Further analysis that might provide more light on the bias of these reviews would be to examine the percentage break down of all other ratings as well. Are the Amazon Vine reviews higher in every category or are 1-star and 5-star ratings more common? 
