![real-estate-investment-types](https://github.com/anastasiialeskiv/project_2/assets/124845922/4cdb1ede-0f21-42fb-a913-29368f515eef)
# Anastasiia Leskiv Project 2
# Business Understanding
A client reached who is thinking of buying a single family home and doesnt know which area is best. They wanted me to build them a regression to allow them to not overpay for a home and provide analysis on the types of homes they would find in each neighborhood. My objective was to observe properties of King County for various home features and analyze the home prices based on those features. Then build a predictive regression model to predict the price of a home. After refining my model, I built dashboards to visualize and communicate my results. Which I will present to my client with my predictions.

# Data Understanding
Dataset contains thousands of data points. The data files provide all information about real estate market in King County which has 39 cities.In this project I used Data collecting, Data cleaning,Modeling, Exploratory data analysis, and Visualization to make the best prediction and recomendation to my client. I checked which neighborhoods are cheaper which are more expensive.How the footage of the home (sqft_living) affect the price? what features does efect the price and I did my prediction.

# Data Preparation
CSV for reading CSV file

Pandas and Numpy for data manipulation

Matplotlib and Seaborn for visualization

Statsmodel for statistical testing and modeling

SciPy Stats for obtaining probabilistic distributions

LinearRegression to predict the value of a variable based on the value of another variable.

Lasso Regration to remove unnecessary features

A training dataset for creating the linear regression model and a testing dataset was created by taking 80% of the data points for training and 20% for testing.

Feature Variables:

id - Unique ID for each home sold
date - Date of the home sale
price - Price of each home sold
bedrooms - Number of bedrooms
bathrooms - Number of bathrooms, where .5 accounts for a room with a toilet but no shower
sqft_living - Square footage of the apartments interior living space
sqft_lot - Square footage of the land space
floors - Number of floors
waterfront - A dummy variable for whether the apartment was overlooking the waterfront or not
greenbelt - natural, undeveloped, and/or agricultural lands that surround urban areas
nuisance
view - An index from 0 to 4 of how good the view of the property was
condition - An index from 1 to 5 on the condition of the apartment,
grade - An index from 1 to 13, where 1-3 falls short of building construction and design, 7 has an average level of construction and design, and 11-13 have a high quality level of construction and design.
heat_source
sewer_system - A sanitary sewer
sqft_above - The square footage of the interior housing space that is above ground level
sqft_basement - The square footage of the interior housing space that is below ground level
sqft_garage - Square footage of the garage
sqft_patio - Square footage of the patio
yr_built - The year the house was initially built
yr_renovated - The year of the house’s last renovation
address
lat - Lattitude
long - Longitude

# Modeling
During the exploratory analysis I saw a good correlation between square footage and price
![68C84B01-0584-4ED1-B85A-B5A66D7A8361](https://github.com/anastasiialeskiv/project_2/assets/124845922/bb4f59c0-09e2-4d22-8f74-4172b41b5ca6)
The estimated change in price for every sqft and came up with the price of 560 USD 
![A91C618A-1F56-4A49-8BA3-BE07DB291D2A](https://github.com/anastasiialeskiv/project_2/assets/124845922/1890fcb1-b8ab-4019-88e7-686c5a6647d2)
I checked all features to see what affect the price I could see that the most expensive houses have waterfront but there is also cheap houses with waterfront.
![FE6A7255-2494-48B8-B8C7-85B72D85E6F6_1_105_c](https://github.com/anastasiialeskiv/project_2/assets/124845922/882d1266-fd8f-431d-8fa0-917d11a29000)
Greenbelt affect the price a little bit less, but still we can see that price silkily elevated.
![EF9014AC-8F7C-4F0A-963F-5B236976CE0E_1_105_c](https://github.com/anastasiialeskiv/project_2/assets/124845922/f819734d-e9f8-49ef-b96f-2ad1c1a66698)
Here we can see how condition effect the price. Good,Average, and Very good condition have almost the same price range same as fair and poor condition almost on the same level.
![789F2B54-FC5E-47B2-9151-60AFEB754AF0_1_105_c](https://github.com/anastasiialeskiv/project_2/assets/124845922/61740db8-5f9a-47bd-8a7a-0d75bd5184de)
Houses with Gas/Solar heat sources are the most expensive Gas heat sources itself slightly cheaper and all the others are pretty much at the similar price range
![87501345-764F-4867-A7CC-1C0817957EFD_1_105_c](https://github.com/anastasiialeskiv/project_2/assets/124845922/0e1c7b7b-ffd3-424b-9751-2f504351b10d)
# Regression Results

Average is 3 bedrooms 2 bathrooms house. Cheaper option would be Federal Way the house can be as cheap as 204 Thousands USD and up with the square footage of about 1800Sqft but that would be older houses about 1770 year build. Renton city has better option the house was build in 2021 but square footage is about 1310-1290 and the price is 243 thousand USD.
In Seattle we would see mush more expensive houses more then a million USD with ever smaller square footage. 
My model was fairly accurate at making predictions with  a mean scared error of $116,866 and R2 adjusted of 0.46. With more tuning I can get this model to be more accurate.
![46373641-1324-472D-A60B-BD4BFD8D83C1_1_105_c](https://github.com/anastasiialeskiv/project_2/assets/124845922/cbc704ad-fdd1-4580-9cfd-c12353623e1a)
1- Ridge Model - Reduces effect of coliner features

2- R2 Adjusted = .46

3- MAE(mean absolute error) - $116,866

Prediction 
Overall my model was best at predicting homes in Longmont, Osceola and Renton cities
![BBD2B175-A072-4991-8CC9-79BF71595587_1_105_c](https://github.com/anastasiialeskiv/project_2/assets/124845922/7a99d73f-c168-45af-b7c7-c94ddf660f8b)
![DF04E7F8-38D8-4531-A58E-D4C54587C0A2_4_5005_c](https://github.com/anastasiialeskiv/project_2/assets/124845922/fe19a0f4-4181-4601-81b4-de2e132c139a)

# Conclusion
The most expensive houses are in Hunts Point,Mercer Island,Seattle,Medina, Newcastle the price can be up to 235 million USD. The most expensive house in our data set is in Hunts Point 235 million USD the house is with 4 bedrooms 5 bathrooms 4440 Square feet 2 floors with waterfront no basement was build in 1990 and renovated in 2014.
The cheapest houses we can find  in Auburn, Skykomish, Sammamish, Woodinville, and Seattle has very different prices it  can be cheap and it also can be very expensive. The cheapest price for house we can find in Auburn for example  about 40 thousand USD house with 4 bedrooms, 2.5 bathrooms 1670 Square feet 1 floor was build in 1967 and never renovated since. 

  During the exploratory analysis I can see good correlation between square footage and price. I calculated estimated change in price for every sqft and came up with the price of 560 USD 

I checked all features to see what affect the price I could see that the most expensive houses have waterfront but there is also cheap houses with waterfront. Greenbelt affect the price a little bit less, but still we can see that price silkily elevated. Sewer System does not effect price.Nuisance does not effect the price
We can see how condition effect the price. Good,Average, and Very good condition have almost the same price range same as fair and poor condition almost on the same level. Houses with Gas/Solar heat sources are the most expensive Gas heat sources itself slightly cheaper and all the others are pretty much at the similar price range

If my client would want to buy 4 bedrooms 3 bathrooms house looks like the best option would be in Seattle, Kent or Federal Way city those are top 3 cheapest option with the price starts at 207 thousand USD. Kent city there is a lot of newer houses with good square footage.
If we would look in more expensive nice option would  Renton ,Kirkland or Bellevue with almost twice bigger square footage but the price would be more then a million USD.
Average is 3 bedrooms 2 bathrooms house. If we look at something like that cheap option would be Federal Way the house can be as cheap as 204 Thousands USD and up with the square footage of about 1800Sqft but that would be older houses about 1770 year build. Renton city has better option the house was build in 2021 but square footage is about 1310-1290 and the price is 243 thousand USD.
In Seattle we would see mush more expensive houses more then a million USD with ever smaller square footage. 
My model was fairly accurate at making predictions with  a mean scared error of $116,866 and R2 adjusted of 0.46. With more tuning I can get this model to be more accurate.
Overall my model was best at predicting homes in Longmont, Osceola and Renton cities
## Limitation
I wish I had an information about taxes and any information about schools transportation etc.
## Recommendation
I would recomend to my client to buy a house with 3 bedrooms 2 bathrooms in Renton city becouse this city has better option the houses we can find a house wich is new build in 2021 it woul not be big it wold be around 1310-1290 squer feet and the price would be around 243 thousand USD. The more squere footagr the higher price woul be.
## Next Steps
My next step would be to to find oud information about schools in the area.

I also woul like to see property tax for each area, how far the house from public transportation.

I woul like to give a price prediction to the buyer based on his prefer features using the model

Find some ways to reduce kurtosis to make the distribution more normal

## For more information
For any questions, please contact Anastasiia Leskiv at prokopivanastasiia@gmail.com or https://www.linkedin.com/in/anastasiia-leskiv-684b4b250/

## Repository Structure

├── data
├── notebook.ipynb
├── README.md
└── presentation.pdf