## Data Scientist Role Play: Inferences and Analysis (Part 2)

1. Pick one city and category of your choice and group the businesses in that city or category by their overall star rating. 

I chose the city of Phoenix as some of the other cities (like Mesa) had more limited results. I chose the category of resturants and used the following SQL code to JOIN the business, category and hours tables for my analysis.

![Peer_review_P2_1](https://user-images.githubusercontent.com/102244119/167269912-c890f7fc-c56f-474c-8d41-6189aa549c2a.png)

Compare the businesses with 2-3 stars to the businesses with 4-5 stars and answer the following questions. Include your code.

![Peer_review_P2_2](https://user-images.githubusercontent.com/102244119/167269963-5c18a9f8-b02f-47d2-9467-e0088e0ca541.png)
![Peer_review_P2_3](https://user-images.githubusercontent.com/102244119/167269990-6554848f-e740-49ec-a1d2-3982c8061112.png)

* i. Do the two groups you chose to analyze have a different distribution of hours? Yes
* ii. Do the two groups you chose to analyze have a different number of reviews? Yes
* iii. Are you able to infer anything from the location data provided between these two groups? Explain. No, they all have different addresses and zip codes.

SQL code used for analysis:

![Peer_review_P2_4](https://user-images.githubusercontent.com/102244119/167270075-b37ef0d9-e55c-4c5f-af52-49c0a27944ea.png)

![Peer_review_P2_5](https://user-images.githubusercontent.com/102244119/167270091-86e222a9-23ca-4337-a63b-98402908799c.png)


2. Group business based on the ones that are open and the ones that are closed. What differences can you find between the ones that are still open and the ones that are closed? List at least two differences and the SQL code you used to arrive at your answer.

![Peer_review_P2_6](https://user-images.githubusercontent.com/102244119/167270133-5c1cf527-6ee9-412b-9b2c-c1d9754508f7.png)
* i. Difference 1: The restaurants that are open more hours of the day have higher reviews, with the top highest rating belonging to the locations open the most hours. 
* ii. Difference 2: The restaurants that are open more hours of the day also tend to have a higher number of reviews.

SQL code used for analysis:

![Peer_review_P2_7](https://user-images.githubusercontent.com/102244119/167270167-e4b7d96a-2746-483d-81dd-a8a31cdd54da.png)

3. For this last part of your analysis, you are going to choose the type of analysis you want to conduct on the Yelp dataset and are going to prepare the data for analysis. Ideas for analysis include: Parsing out keywords and business attributes for sentiment analysis, clustering businesses to find commonalities or anomalies between them, predicting the overall star rating for a business, predicting the number of fans a user will have, and so on. These are just a few examples to get you started, so feel free to be creative and come up with your own problem you want to solve. Provide answers, in-line, to all of the following:
* i. Indicate the type of analysis you chose to do: Coffee & Tea businesses and which ones are top rated
Findings: there are 92 results within the Yelp data set for 'Coffee & Tea' with all 92 being distinct business ids. Out of those 92 results, the name, state and stars field is NULL in 89 of the businesses, which leaves only three with names and star ratings. I ran various queries (listed below) to explore multiple table and column information.

![Peer_review_P2_8](https://user-images.githubusercontent.com/102244119/167270529-c1119937-c1d6-43f0-9c49-0e607cc11e2c.png)
![Peer_review_P2_9](https://user-images.githubusercontent.com/102244119/167270533-db8665f9-d064-4a7e-b580-53c432a85fcb.png)
![Peer_review_P2_10](https://user-images.githubusercontent.com/102244119/167270535-6a978958-c0bd-451d-a90b-9be8207b9ccf.png)
![Peer_review_P2_11](https://user-images.githubusercontent.com/102244119/167270539-1847ffd7-345d-45f3-b520-4855e17682c5.png)
![Peer_review_P2_12](https://user-images.githubusercontent.com/102244119/167270516-e6899f0e-01a2-4319-a577-ede01d08820e.png)
![Peer_review_P2_13](https://user-images.githubusercontent.com/102244119/167270574-83f1be3c-526a-4ca5-a65b-abdc4491303e.png)

* ii. Write 1-2 brief paragraphs on the type of data you will need for your analysis and why you chose that data:

Being a coffee lover myself, I thought it would be fun data to dive into. I was surprised at how incomplete the date is. For example the 'Coffee & Tea' businesses have a high amount of NULL fields. I choose to narrow down my data to the 'Coffee & Tea' businesses that had not only a name, but also reviews and stars. Out of these three 'Coffee & Tea' businesses, there was no review keyword or attribute or tip to explain why 'Cabin Fever' rated the highest. However, hours show that this is the only option of the three that is open past 10:30 PM which could explain the high rating over the other two options.

* iii. Output of your finished dataset:

![Peer_review_P2_14](https://user-images.githubusercontent.com/102244119/167270606-fb5fee0e-edb4-4407-ab93-61240a8f769e.png)

* iv. Provide the SQL code you used to create your final dataset:

![Peer_review_P2_15](https://user-images.githubusercontent.com/102244119/167270628-15d13b4d-68f5-4cda-b7bb-77702fe6dc55.png)
