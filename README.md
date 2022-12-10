# ADS500B-rog-ver-sha
Final project for USD ADS500B for Roger Qiu, Verity Pierson, &amp; Shailja Somani.

## Step 1: Data Cleaning
We chose to fill in null values with the following methods: 
* We noticed that sqft_living is always equal to sqft_above + sqft_basement in the dataset (and both of those columns have 0 nulls), so we just added those 2 columns to get an accurate sqft_living.
* For the sqft_lot column, we noticed that the sqft_lot15 column (which has 0 nulls) is often the exact same as the sqft_lot column. It's probably square feet from different years, which causes the discrepancy in some houses, but I think, overall, it will be much more accurate for most houses than just using the whole column's median).
* For bedrooms, we think it's a safe bet to assume that, the greater the sqft_living, the higher the # of bedrooms. We chose to make the sqft_living a categorical variable (split it into below 1000, 1000-1500, 1500-2000, etc), get the median # of bedrooms for each one, then use that to fill in the nulls for bedrooms.
* For bathrooms, we could got the median # of bathrooms for each # of bedrooms in a house, then filled in nulls based on # of bedrooms in the house.

## Step 2: Data Analysis and Visualization
* We started by identifying between discrete and continuous fields from our data frame.
* Next we create box plots and histograms of a few chosen fields: prices, sqft_living and yr_built.
* This allows us get an understanding of the centrality and distribution of each of those fields using visualizations. 
* Next we find the correlation between each of the 3 fields, allowing us to understand how they are related to each other. 
* Finally, we map out these comparisons in scatter plots and a heatmap to visualize the relationship between the fields.  
