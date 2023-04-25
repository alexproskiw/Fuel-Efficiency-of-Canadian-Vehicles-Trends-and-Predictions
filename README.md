# Fuel Efficiency of Canadian Vehicles: Trends and Predictions
A Python Project which utilizes Visualizations and Modelling to Explore the Fuel Efficiency of Canadian Vehicles

## Introduction
With gasoline prices reaching record highs in 2022 and remaining elevated since, fuel efficiency is a key concern for consumers looking to buy a vehicle. There is lots of generic advice thrown around regarding purchasing a vehicle, such as "new vehicles are so much more fuel efficient" or "SUVs are all just gas guzzlers". But what is the reality of the fuel efficiency of vehicles sold in the Canadian market? The goal of this research project is to explore the fuel efficiency of Canadian vehicles by answering the following questions:
> -----
> <ins>**Key Research Questions**</ins>
>
> 1. Has vehicle fuel efficiency improved from 2000 to 2023?
>
> 2. Which manufacturer produces, on average, the most fuel efficient vehicles?
>
> 3. Can existing fuel efficiency information be used to predict the fuel efficiency of future vehicles?
>
> 4. Can we use a company's R&D spending to predict fuel efficiency improvements?
> -----

The dataset chosen for this project is the [Natural Resources Canada Fuel Consumption Ratings Dataset](https://open.canada.ca/data/en/dataset/98f1a129-f628-4ce4-b24d-6f16bf24dd64?fbclid=IwAR1rVpyNw3KJSeAcT6ryyCAADAnmB7uDtujvwlswFkOzaiLlnjIt29EekiY) published by the Government of Canada. This dataset includes fuel consumption information for vehicles sold in Canada from 2000 to 2023, along with supporting information about each vehicle such as make, model, vehicle type, engine size, and transmission type.

## Example Visualization:
![Fuel Efficiency By Manufacturer](/make_fuel_economy.jpg)

## Approach and Key Findings:
Overall, it's clear that in general, the fuel efficiency of vehicles in Canada has been decreasing over time. There are various factors associated with a vehicle that influence its fuel efficiency, including the make, vehicle type, fuel type, engine size, number of cylinders, transmission type, and number of transmission gears. 

This report also explored how the influence of make, vehicle type, fuel type, and transmission type on fuel efficiency has changed over time. Some key findings include:
- On average, Honda has produced the most efficient vehicles, while GMC has produced the least efficient vehicles.

- Every manufacturer in this study has achieved an improvement in the average fuel efficiency of their vehicles from 2000 to 2023. The manufacturers that achieved the largest percentage improvements (>20%) in fuel efficiency between 2000 and 2023 are Buick, Jeep, Kia, Lexus, Maxda, Nissan, Toyota, and Volvo. 

- Cars have predominantly had the best fuel efficiency, while trucks have had the worst. However, SUVs and vans have experienced much larger percentage improvements in fuel efficiency from 2000 to 2023 compared to cars and trucks.

- Regular gasoline vehicles have had a lower fuel economy than premium gasoline vehicles since 2005 and have improved their efficiency more from 2000 to 2023. Diesel vehicles are generally more efficient than gasoline vehicles.

- Continuously variable transmissions are the most efficient transmission type and have improved their efficiency the most since their adoption. 

After visualizing and exploring the data, various models were fitted, including linear regression models, lasso models, regression trees, and neural networks. Each type of model was first fitted without considering any interaction between the variables, followed by considering the interaction between each variable and the vehicle's model year. Regardless of interaction or not, the neural network was found to be the most accurate predictor (i.e., the lowest mean squared error). The neural network was also able to predict the fuel efficiency of unreleased 2024 vehicle models with moderate success, with 4 of the 7 predictions falling within a 5% error of the actual value.

Finally, Toyota's R&D expenses were imported from their full-year annual reports and utilized alongside the model year of a vehicle to make a regression model to predict the efficiency of future vehicles based on R&D spending.
