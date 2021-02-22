# Predict-Taxi-Fares-with-Random-Forests-in-R

In this project,  analyzed a random sample of 49999 New York journeys made in 2013. Used regression trees and random forests to build a model that can predict the locations and times when the biggest fares can be earned.  Taxi dataset contains 49999 records.  The dataset contains the times and price of a large number of taxi trips. Importantly we also get to know the location, the longitude and latitude, where the trip was started. Cleaned the data  by dropping any journeys with zero fares and zero tips and created the total variable as the log sum of fare and tip.  While the dataset contains taxi trips from all over New York City, the bulk of the trips are to and from Manhattan.  Reduced the data to taxi trips starting in Manhattan.  Manhattan is bounded by the rectangle with 
latitude from 40.70 to 40.83 and longitude from -74.025 to -73.93 .  Visualized the data  where in Manhattan people tend to start their taxi journeys. The map  showed that the journeys are highly concentrated in the business and tourist areas.  Predicted the total fare with lat and long being the predictors by using tree. However the result was frugal because  it included one split . It didn't even include long as tree deemed that it didn't improve the predictions.Taxi drivers will need more information than this.  I tried fitting a new regression tree where we include the new time variables. The regression tree has not changed after including the three time variables. This is likely because latitude is still the most promising first variable to split the data on, and after that split, the other variables are not informative enough to be included. Applied random forest to our model where many different trees are fitted to subsets of the data, may well include the other variables in some of the trees that make it up.  If we would compare "residual mean deviance" , we would see that fitted_forest has a slightly lower error.  Neither predictive model was that good, in statistical terms, they explain only about 3% of the variance. Extracted the prediction from fitted_forest and plotted the predicted mean trip prices from according to the random forest. Looking at the map with the predicted fares we see that fares in downtown Manhattan are predicted to be high, while midtown is lower. 
People would  spend the most on a taxi ride in downtown of Manhattan in NYC as a prediction result in  last model
