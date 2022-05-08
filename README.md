## Data Scientist Role Play: Inferences and Analysis (Part 2)

1. Pick one city and category of your choice and group the businesses in that city or category by their overall star rating. 

I chose the city of Phoenix as some of the other cities (like Mesa) had more limited results. I chose the category of resturants and used the following SQL code to JOIN the business, category and hours tables for my analysis.
![Peer_Review_P2-1](https://user-images.githubusercontent.com/102244119/167318677-91c20be8-2a44-422f-92ca-4628b35b4ae3.png)


Compare the businesses with 2-3 stars to the businesses with 4-5 stars and answer the following questions. Include your code.
* i. Do the two groups you chose to analyze have a different distribution of hours? Yes
* ii. Do the two groups you chose to analyze have a different number of reviews? Yes
* iii. Are you able to infer anything from the location data provided between these two groups? Explain. No, they all have different addresses and zip codes.

SQL code used for analysis:
![Peer_Review_P22-2](https://user-images.githubusercontent.com/102244119/167319093-e9bea24d-a6c5-4e7a-8718-7d3c8315fc86.png)

2. Group business based on the ones that are open and the ones that are closed. What differences can you find between the ones that are still open and the ones that are closed? List at least two differences and the SQL code you used to arrive at your answer.
* i. Difference 1: The restaurants that are open more hours of the day have higher reviews, with the top highest rating belonging to the locations open the most hours. 
* ii. Difference 2: The restaurants that are open more hours of the day also tend to have a higher number of reviews.

SQL code used for analysis:
![Peer_Review_P22-3](https://user-images.githubusercontent.com/102244119/167319162-e8e6541d-446a-4c4b-bebb-743dbd5e52c7.png)

3. For this last part of your analysis, you are going to choose the type of analysis you want to conduct on the Yelp dataset and are going to prepare the data for analysis. Ideas for analysis include: Parsing out keywords and business attributes for sentiment analysis, clustering businesses to find commonalities or anomalies between them, predicting the overall star rating for a business, predicting the number of fans a user will have, and so on. These are just a few examples to get you started, so feel free to be creative and come up with your own problem you want to solve. Provide answers, in-line, to all of the following:
* i. Indicate the type of analysis you chose to do: Coffee & Tea businesses and which ones are top rated, my queries show there are 92 results within the Yelp data set for 'Coffee & Tea' with all 92 being distinct business ids. Out of those 92 results, the name, state and stars field is NULL in 89 of the businesses, which leaves only three with names and star ratings. I ran various queries (listed below) to explore multiple table and column information.
![Peer_review_p22-4](https://user-images.githubusercontent.com/102244119/167319245-7c3e98c3-2de0-4af2-8df8-64d0ddefd51f.png)

* ii. Write 1-2 brief paragraphs on the type of data you will need for your analysis and why you chose that data: Being a coffee lover myself, I thought it would be fun data to dive into. I was surprised at how incomplete the date is. For example the 'Coffee & Tea' businesses have a high amount of NULL fields. I choose to narrow down my data to the 'Coffee & Tea' businesses that had not only a name, but also reviews and stars. Out of these three 'Coffee & Tea' businesses, there was no review keyword or attribute or tip to explain why 'Cabin Fever' rated the highest. However, hours show that this is the only option of the three that is open past 10:30 PM which could explain the high rating over the other two options.

* iii. Output of your finished dataset:
![peer_review_p22-5](https://user-images.githubusercontent.com/102244119/167319311-4dc28ac6-a593-4711-a8af-a78ee9fc4b07.png)

* iv. Provide the SQL code you used to create your final dataset:
![peer_review_p22-6](https://user-images.githubusercontent.com/102244119/167319335-cef53715-07f6-414a-ad7b-cfc8d1ce0bcf.png)

