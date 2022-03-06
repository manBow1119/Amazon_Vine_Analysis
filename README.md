# Amazon_Vine_Analysis
## Technologies and Languages
* SQL and pgAdmin 4
* AWS- RDS
* PySpark
* Google Colab

## Project Overview
This project utilized aforementioned tools to take in big datasets of reviews from Amazon products- specifically Tools. Using pyspark to connect the cloud supported AWS Relational database to the local postgres server in order to create dataframes/table for various areas of interest, with particular attention to ratings and "vine" membership. Examples of such tables below:
* Customers 
* ![Customers Table](https://github.com/manBow1119/Amazon_Vine_Analysis/blob/main/Customer_table.png)
* Products
* ![Products Table](https://github.com/manBow1119/Amazon_Vine_Analysis/blob/main/Products_table.png)
* Reviews
* ![Review Table](https://github.com/manBow1119/Amazon_Vine_Analysis/blob/main/Review_table.png)
* Vine Program
* ![Vine Table](https://github.com/manBow1119/Amazon_Vine_Analysis/blob/main/Vine_basic.png)

## Results
The vine dataframe was filtered to include reviews that had more than 20 votes, and of those, at least 50% were 'helpful'.
* Filtered Vine Dataframe:
* ![Filtered Vine Table](https://github.com/manBow1119/Amazon_Vine_Analysis/blob/main/Vine_filtered.png)
Theses data frames were further filtered by Vine program membership to examine differences in star-rating reviews for those reviewers who were paid, or not.
The total of non-Vine member reviews was 31,545, while the total for Vine members was 285. There is a notable size difference in these two populations. 
These reviews were filtered and counted to determine the percentage of 5 star reviews for each group. The Vine members provided 5 star reviews 57.2% of the time while non-Vine members did 46.3%. In the following images you can see that I took this analysis one step deeper to see how vine membership compares when 4 and 5 star reviews are included. Here, the percentages diverge more, with Vine member providing a 4 or 5 star review 83.2% of the time:
* ![Vine Yes 4/5](https://github.com/manBow1119/Amazon_Vine_Analysis/blob/main/Vine_yes_four_five_stars.png)

The non-vine members, however, only had 4 or 5 stars 64.1% of the time:
* ![Vine No 4/5](https://github.com/manBow1119/Amazon_Vine_Analysis/blob/main/Vine_no_four_five.png)

## Summary
The results of the calculations performed on these filtered tables suggest there is some bias toward more positive review for Vine members, who are paid for their reviews. The different of roughly ten percent (57.2-yes/46.3-no) between Vine program membership was further supported when the 4 star ratings were also included (83.2-yes/64.1-no). The divergence for these two "positive" rated categories further supports this possible bias. Still, the stark difference in population size is worth taking into context.
