# Module 6 Challenge: PlanMyTrip App

## Purpose:

We wanted to create an application to help people determine the best places to visit according to their temperature preferences.
In order to do this, we created a series of three python scripts and broke down the application in three steps.

The Weather_Database script creates the bulk of our data. 
We started by generating 2000 sets of geographic coordinates at random by pairing a random latitude value with a random longitude value. Next, we used the [citipy module](https://github.com/wingchen/citipy) to find the nearest city to these coordinates and eliminate all the coordinates that were in unpopulated areas, bodies of water, etc. After generating the cities, the script then fetches their weather information through the [OpenWeatherMap API](https://openweathermap.org/api) and transfers the dataset to a CSV file.

The Vacation_Search script was used next, and it utilized the CSV database in conjunction with the Google Places API to create  a customer travel destinations map. Its prompts allow the user to choose their ideal temperature range before refining potential destinations to match these criteria before finding the nearest hotel to these locations.

Lastly, the Vacation_Itinerary script generated a list of four prospective towns to visit along with a map for the directions between destinations. It also generated a second map displaying a pop-up marker on each location containing the Hotel Name, the city and country information along with a current weather conditions description and the max temperature.

## Use:

In order to use these scripts, one would have to first run Weather_ Database to generate the potential destinations along with their weather info followed by running the Vacation_Search to refine potential destinations by temperature preference.

In order to do so, the user is prompted to choose a minimum and maximum desired temperature before the script filters out any record that doesn't fit the criteria.

To finish the Road trip planning, the user would have to launch the Vacation_Itinerary script to create maps showing potential routes and showing the ideal vacation spots. This piece of the script may require further work to prompt user to further refine destinations by choosing countries and cities they want to visit rather than finding something suitable only by looking at the potential destinations maps and manually populating each field to add them to the itinerary and pop-up marker maps.
