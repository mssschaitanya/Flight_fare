## Flight Price Prediction

* Created a tool that estimates Flight Price to help users look for br best prices when booking flight tickets.

* Engineered features from the Departure Time,Date of Journey,to quantify the data and amke it more understandable.

* Optimized multiple Regression models using GridsearchCV to reach the best model.

* Built a client facing API using flask


## Codes and Resources Used

* Python Version : 3.8.5
* Packages : pandas,numpy,sklearn,matplotlib,seaborn,flask,json,pickle
* Dataset : https://www.kaggle.com/nikhilmittal/flight-fare-prediction-mh


### Created an environment

'''
    conda create -p venv python==3.8
    
    conda activate venv/
    '''

### Install all libraries

'''
    pip install -r requirements.txt
    '''

## Problem Statement 

Flight ticket prices can be something hard to guess,today we might see a price ,check out the price of same flight tomorrow ,it will be a different story.We might have often heard traveles saying that flight ticket prices are so unpredictable. As data scientist we are gonna prove that given the right data anything can be predicted.Here you will be provided with price of flight tickets for various airline between the months of March and June of 2019 and various cities.

* Size of test set : 2671 records

* Features :

* Airline : The name of Airlne.
* Date_of_journey : the date of the journey.
* Source: The source from which the services begins.
* Destination : The destination where the services ends.
* Route : The route taken by flight to reach the destination.
* Dep_Time : The time when the journey starts from the sources.
* Arrival_Time : Time of arrival at the destination.
* Duration : Total duration of the flight.
* Total_stops : Total stops between the sources and destination .
* Additional_Info : Additional information about the flight.
* Price : The price of the ticket.

## Cleaning the Data

I needed to clean it up so that it was usable for our model. I made the following changes and created the following variables:

* Calculated the total flight duration
* Removed the null values
* Removed the outliers

* After that we perform some sort of EDA.

## Model Building

First, I transformed the categorical variables into dummy variables. I also split the data into train and tests sets with a test size of 30%.

I tried forteen different models and evaluated them using Root Mean Squared Error. I chose RMSE because it is relatively easy to interpret and outliers aren’t particularly bad in for this type of model.

Different models I tried:

* LinearRegression : 0.5755
* ElasticNet : 0.5897
* Lasso : 0.5755
* Ridge : 0.5897
* RandomForestRegressor : 0.8282422746342984
* Decision Tree : 0.6913
* K-NeighboursRegressor : 0.5783

## Productionization

In this step,I built a flask API endpoint that was hosted on a local webserver.The API endpoint takes in a request with a list of values from a flight and returns an estimated price.






































































































































































