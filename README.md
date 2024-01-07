# King County, Washington Housing Market Project
### Arnav Boppudi, Stephanie Fissel, Jacqui Unciano, Ian Yung
#### July 14, 2023

## Questions of Interest
### Linear Regression Question:
Is house size (square footage, bedrooms, bathrooms, floors) a good predictor of selling price for houses in King County, Washington between May 2014 and May 2015?
* Response Variable: price
* Motivation: Determine if house size-related attributes accurately predict selling prices, aiding potential buyers in assessing property values.
### Logistic Regression Question:
Can we predict if the house has a zip code considered one of the “20 Wealthiest Zip Codes” in King County (using size, condition, and size of neighboring houses)?
* Response Variable: wealthy
* Motivation: Identify whether specific measures can predict if a house is in a wealthier neighborhood, aiding potential buyers in making informed decisions.

## Data 
A data set containing information about more than 21,600 different house sales for King County, Washington between May 2014 and May 2015 including: `price`, `bedrooms`, `bathrooms`, `sqft_living`, `sqft_lot`, `floors`, `waterfront`, `view`, `condition`, `grade`, `sqft_above`, `sqft_basement`, `yr_built`, `yr_renovated`, `zip_code`, `sqft_living15`, `sqft_lot15`
### Variables
`price` Price of each home sold.

`bedrooms` Number of bedrooms.

`bathrooms` Number of bathrooms, where 0.5 accounts for a room with a toilet but no shower.

`sqft_living` Square footage of the apartments interior living space.

`sqft_lot` Square footage of the land space.

`floors` Number of floors.

`waterfront` A dummy variable for whether the property was overlooking the waterfront or not.

`view` An index from 0 to 4 of how good the view of the property was.

`condition` An index from 1 to 5 on the condition of the property.

`grade` An index from 1 to 13, where 1-3 falls short of building construction and design, 7 has an average level of construction and design, and 11-13 have a high quality level of construction and design.

We created another variable for grade, factoring the levels, called `grade_group`, which included level groupings: poor (1, 2, 3), moderately poor (4, 5, 6), average (7, 8, 9, 10), high (11, 12, 13).

`sqft_above` The square footage of the interior housing space that is above ground level.

`sqft_basement` The square footage of the interior housing space that is below ground level.

`yr_built` The year the house was initially built.

`yr_renovated` The year of the house’s last renovation.

`zip_code` What zip code area the house is in.

We created another variable for zip_code called `wealthy`, grouping the zip codes based on whether they are considered one of the “20 Wealthiest Zip Codes” in King County or not. The 20 wealthiest zip codes are 98039, 98040, 98004, 98112, 98075, 98033, 98074, 98053, 98121, 98006, 98199, 98105, 98065, 98177, 98005, 98005, 98029, 98119, 98027, 98072.

`sqft_living15` The square footage of interior housing living space for the nearest 15 neighbors.

`sqft_lot15` The square footage of the land lots of the nearest 15 neighbors.

## Summary of Findings
Our team investigated two primary questions related to the housing market in King County, Washington, between May 2014 and May 2015. The first question focused on predicting house selling prices using linear regression, considering factors such as size, bedrooms, bathrooms, and floors. The second question used logistic regression to predict whether a house falls within one of the region's "20 Wealthiest Zip Codes," based on size, condition, and the size of neighboring homes.

### Findings:
#### 1. Linear Regression:
* House size, measured by square footage, bedrooms, and bathrooms, plays a crucial role in predicting selling prices.
* The number of bedrooms showed a non-linear relationship, with up to five bedrooms correlating to higher prices, but beyond five bedrooms, prices tended to decrease.
* The number of floors did not significantly improve price prediction accuracy.
* House grade, indicating construction quality, is a significant determinant of selling price.
#### 2. Logistic Regression
* Condition of the house did not significantly influence whether it falls within a wealthy zip code.
* House and neighboring size were indicative of the wealth level of the zip code.
* The model's predictive ability is acceptable, with an AUC of 0.76, but there is room for improvement.
* Bedrooms, property size, and neighboring property size inversely affected the odds of a house being in a wealthier zip code.

## Conclusion
Our findings provide valuable insights into predicting house prices and identifying wealthier neighborhoods in King County. The results can empower buyers and sellers with data-driven decision-making tools. Further refinement and exploration of additional factors could enhance predictive models for more accurate real-world applications.

##
<em> For detailed code, visualizations, and additional information, please refer to the project's R Markdown script and report. </em>




